<script setup>
    const props = defineProps(['calcularResultado', 'estado']);
</script>

<template>
    <div class="calculator-body">
        <div class="inputs-section">
            <div class="input-group">
                <label class="input-label">Primeiro número</label>
                <input 
                    class="modern-input" 
                    type="number" 
                    :value="props.estado.num1" 
                    @input="evento => props.estado.num1 = evento.target.value" 
                    placeholder="Digite o primeiro número"
                >
            </div>

            <div class="input-group operator-group">
                <label class="input-label">Operação</label>
                <select 
                    class="modern-select" 
                    :value="props.estado.operacao" 
                    @change="evento => props.estado.operacao = evento.target.value"
                >
                    <option value="--">Selecione</option>
                    <option value="somar">➕ Somar</option>
                    <option value="diminuir">➖ Subtrair</option>
                    <option value="dividir">➗ Dividir</option>
                    <option value="multiplicar">✖️ Multiplicar</option>
                </select>
            </div>

            <div class="input-group">
                <label class="input-label">Segundo número</label>
                <input 
                    class="modern-input" 
                    type="number" 
                    :value="props.estado.num2" 
                    @input="evento => props.estado.num2 = evento.target.value" 
                    placeholder="Digite o segundo número"
                >
            </div>
        </div>
        
        <div class="result-section">
            <div v-if="props.estado.erro" class="error-message">
                ⚠️ {{ props.estado.erro }}
            </div>
            <div class="result-display">
                <span class="result-label">Resultado:</span>
                <span class="result-value">{{ props.calcularResultado }}</span>
            </div>
        </div>          
    </div>
</template>

<style scoped>
.calculator-body {
    padding: 2rem;
    background: linear-gradient(to bottom, #f8f9fa, #ffffff);
}

.inputs-section {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1rem;
    margin-bottom: 2rem;
    align-items: end;
}

.input-group {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.operator-group {
    padding: 0;
}

.input-label {
    font-weight: 500;
    color: #374151;
    font-size: 0.875rem;
    margin-bottom: 0.25rem;
}

.modern-input {
    padding: 0.875rem 1rem;
    border: 2px solid #e5e7eb;
    border-radius: 12px;
    font-size: 1.1rem;
    font-weight: 500;
    text-align: center;
    transition: all 0.3s ease;
    background: white;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    min-width: 0;
    width: 100%;
}

.modern-input:focus {
    outline: none;
    border-color: #667eea;
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1), 0 1px 3px rgba(0, 0, 0, 0.1);
    transform: translateY(-1px);
}

.modern-select {
    padding: 0.875rem 1rem;
    border: 2px solid #e5e7eb;
    border-radius: 12px;
    font-size: 1rem;
    font-weight: 500;
    text-align: center;
    transition: all 0.3s ease;
    background: white;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    min-width: 0;
    width: 100%;
}

.modern-select:focus {
    outline: none;
    border-color: #667eea;
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.result-section {
    text-align: center;
    padding: 1.5rem;
    background: linear-gradient(135deg, #f3f4f6, #ffffff);
    border-radius: 16px;
    border: 1px solid #e5e7eb;
    box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.05);
}

.error-message {
    background: linear-gradient(135deg, #fee2e2, #fecaca);
    color: #dc2626;
    padding: 1rem;
    border-radius: 12px;
    font-weight: 500;
    margin-bottom: 1rem;
    border: 1px solid #fca5a5;
    animation: shake 0.5s ease-in-out;
}

.result-display {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    align-items: center;
}

.result-label {
    font-size: 1rem;
    color: #6b7280;
    font-weight: 500;
}

.result-value {
    font-size: 2rem;
    font-weight: 700;
    color: #1f2937;
    background: linear-gradient(135deg, #667eea, #764ba2);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    min-height: 2.5rem;
    display: flex;
    align-items: center;
}

@keyframes shake {
    0%, 100% { transform: translateX(0); }
    25% { transform: translateX(-5px); }
    75% { transform: translateX(5px); }
}

@media (max-width: 768px) {
    .calculator-body {
        padding: 1.5rem;
    }
    
    .inputs-section {
        grid-template-columns: 1fr;
        gap: 1rem;
    }
    
    .operator-group {
        padding: 0;
        order: 2;
    }
    
    .result-value {
        font-size: 1.5rem;
    }
}

@media (max-width: 480px) {
    .calculator-body {
        padding: 1rem;
    }
    
    .inputs-section {
        gap: 0.75rem;
    }
    
    .modern-input,
    .modern-select {
        padding: 0.75rem;
        font-size: 1rem;
    }
}
</style>