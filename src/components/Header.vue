<template>
    <div class="modern-header">
        <h1 class="header-title">
            <span class="calculator-icon">🧮</span>
            Calculadora Aritmética
        </h1>
        <p class="header-subtitle">Rápida • Simples • Eficiente</p>
    </div>
</template>

<style scoped>
.modern-header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 2rem;
    text-align: center;
    color: white;
    position: relative;
    overflow: hidden;
}

.modern-header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="1" fill="%23ffffff" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
    opacity: 0.3;
}

.header-title {
    font-size: 2.2rem;
    font-weight: 700;
    margin: 0;
    position: relative;
    z-index: 1;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    letter-spacing: -0.02em;
}

.calculator-icon {
    font-size: 2.5rem;
    margin-right: 0.5rem;
    display: inline-block;
    animation: bounce 2s infinite;
}

.header-subtitle {
    font-size: 1rem;
    font-weight: 400;
    margin: 0.5rem 0 0 0;
    opacity: 0.9;
    position: relative;
    z-index: 1;
    letter-spacing: 0.05em;
}

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-10px);
    }
    60% {
        transform: translateY(-5px);
    }
}

@media (max-width: 768px) {
    .modern-header {
        padding: 1.5rem;
    }
    
    .header-title {
        font-size: 1.8rem;
    }
    
    .calculator-icon {
        font-size: 2rem;
    }
    
    .header-subtitle {
        font-size: 0.9rem;
    }
}
</style>
