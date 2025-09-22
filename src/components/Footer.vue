<template>
    <div class="modern-footer">
        <div class="footer-content">
            <p class="copyright">
                <span class="heart">💙</span>
                © 2025 Todos os direitos reservados
            </p>
            <p class="author">
                Desenvolvido por <strong>Lion Dev</strong>
                <span class="tech-stack">Vue.js + Vite</span>
            </p>
        </div>
    </div>
</template>

<style scoped>
.modern-footer {
    background: linear-gradient(135deg, #f8fafc, #e2e8f0);
    border-top: 1px solid #e5e7eb;
    padding: 1.5rem 2rem;
}

.footer-content {
    text-align: center;
    color: #64748b;
}

.copyright {
    margin: 0 0 0.5rem 0;
    font-size: 0.875rem;
    font-weight: 400;
}

.heart {
    display: inline-block;
    animation: pulse 2s infinite;
    margin-right: 0.25rem;
}

.author {
    margin: 0;
    font-size: 0.875rem;
    font-weight: 400;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    flex-wrap: wrap;
}

.author strong {
    color: #374151;
    font-weight: 600;
}

.tech-stack {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
    padding: 0.25rem 0.5rem;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 500;
    letter-spacing: 0.02em;
}

@keyframes pulse {
    0%, 100% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
}

@media (max-width: 768px) {
    .modern-footer {
        padding: 1rem;
    }
    
    .author {
        flex-direction: column;
        gap: 0.25rem;
    }
}
</style>