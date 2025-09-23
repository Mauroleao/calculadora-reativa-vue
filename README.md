# 🧮 Calculadora Reativa Vue

Uma calculadora aritmética moderna e responsiva desenvolvida com Vue.js 3, apresentando uma interface elegante com efeitos glassmorphism e reatividade em tempo real.

![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## ✨ Características

- **🎨 Design Moderno**: Interface elegante com gradientes e efeitos glassmorphism
- **⚡ Reatividade**: Cálculos em tempo real usando Vue 3 Composition API
- **📱 Responsivo**: Layout adaptativo para desktop, tablet e mobile
- **🎯 Operações Básicas**: Soma, subtração, multiplicação e divisão
- **⚠️ Validação**: Tratamento de erros e validação de entrada
- **🔄 Animações**: Transições suaves e micro-interações
- **🎨 UX/UI**: Componentes modulares e código limpo

## 🛠️ Tecnologias Utilizadas

- **Vue.js 3** - Framework progressivo para interfaces de usuário
- **Composition API** - Para lógica reativa e reutilizável
- **Vite** - Build tool rápido e moderno
- **CSS3** - Estilos avançados com gradientes e animações
- **JavaScript ES6+** - Sintaxe moderna

## 🚀 Funcionalidades

### Operações Matemáticas
- ➕ **Adição**: Soma de dois números
- ➖ **Subtração**: Diferença entre dois números  
- ✖️ **Multiplicação**: Produto de dois números
- ➗ **Divisão**: Quociente de dois números (com validação para divisão por zero)

### Interface
- 🎭 **Header animado** com ícone bouncing
- 📊 **Inputs modernos** com efeitos de foco
- 🎨 **Select estilizado** com emojis para operações
- 📋 **Área de resultado** com formatação elegante
- ⚡ **Mensagens de erro** com animação shake

## 📦 Instalação

### Pré-requisitos
- Node.js (>= 20.19.0 ou >= 22.12.0)
- npm ou yarn

### Passos

1. **Clone o repositório**
   ```bash
   git clone https://github.com/Mauroleao/calculadora-reativa-vue.git
   cd calculadora-reativa-vue
   ```

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Execute em modo de desenvolvimento**
   ```bash
   npm run dev
   ```

4. **Acesse no navegador**
   ```
   http://localhost:5173
   ```

## 🔧 Scripts Disponíveis

| Comando | Descrição |
|---------|-----------|
| `npm run dev` | Inicia o servidor de desenvolvimento |
| `npm run build` | Gera build para produção |
| `npm run preview` | Visualiza o build de produção |

## 📁 Estrutura do Projeto

```
calculadora-reativa-vue/
├── public/             # Arquivos estáticos
├── src/
│   ├── assets/         # CSS e recursos
│   │   ├── base.css    # Estilos base e variáveis
│   │   └── main.css    # Estilos principais
│   ├── components/     # Componentes Vue
│   │   ├── Header.vue  # Cabeçalho da aplicação
│   │   ├── Body.vue    # Corpo principal (inputs e resultado)
│   │   └── Footer.vue  # Rodapé
│   ├── App.vue         # Componente raiz
│   └── main.js         # Ponto de entrada
├── index.html          # Template HTML
├── package.json        # Dependências e scripts
├── vite.config.js      # Configuração do Vite
└── README.md          # Documentação
```

## 🎨 Design System

### Cores Principais
- **Gradiente Principal**: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- **Background Card**: `rgba(255, 255, 255, 0.95)`
- **Texto**: `#1f2937`
- **Erro**: `#dc2626`

### Tipografia
- **Fonte**: Inter (Google Fonts)
- **Peso**: 300-700
- **Tamanhos**: Responsivos com clamp()

### Efeitos
- **Glassmorphism**: `backdrop-filter: blur(10px)`
- **Sombras**: Box-shadows multicamadas
- **Transições**: `0.3s ease`

## 📱 Responsividade

- **Desktop**: Layout em grid de 3 colunas
- **Tablet** (≤ 768px): Layout empilhado
- **Mobile** (≤ 480px): Otimizações de espaçamento

## 🤝 Contribuindo

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👨‍💻 Autor

**Lion Dev**
- GitHub: [@Mauroleao](https://github.com/Mauroleao)

## 🙏 Agradecimentos

- Vue.js Team pelo framework incrível
- Vite pela ferramenta de build ultra-rápida
- Google Fonts pela tipografia Inter
- Comunidade open source

---

<div align="center">
  <p>Feito com 💙 por Lion Dev</p>
  <p>Vue.js + Vite</p>
</div>
