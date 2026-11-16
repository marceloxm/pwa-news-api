# 📰 PWA News API (Portal de Notícias)

## 📖 Sobre o Projeto

O **PWA News API** é uma aplicação web de portal de notícias inspirada em grandes veículos como *Forbes* e *The New York Times*, desenvolvida com **ReactJS** como parte de um desafio prático da **[Digital Innovation One (DIO)](https://dio.me)**.

O objetivo principal do projeto é aplicar o conceito de **Progressive Web App (PWA)**, permitindo que o portal seja acessado diretamente pelo navegador e também instalado em dispositivos móveis ou desktops, proporcionando uma experiência fluida, responsiva e semelhante a um aplicativo nativo (incluindo cache via Service Workers).

---

## ✨ Funcionalidades

- **Portal de Notícias Categorizado:** Exibição de matérias organizadas por editorias/categorias (como *Mundo*, *Economia* e *Tecnologia*).
- **Leitura Detalhada de Artigos:** Página dedicada para visualização completa da notícia selecionada, com opção de compartilhamento rápido (`Web Share API` / cópia de link).
- **Experiência PWA (Progressive Web App):**
  - Possibilidade de instalação na tela inicial do smartphone ou desktop;
  - Uso de **Service Workers** e **Web App Manifest** para cache de arquivos estáticos e navegação offline/resiliente.
- **Arquitetura Full-Stack (Front-end + API):** Comunicação entre o cliente React e o serviço de notícias para consumo dinâmico dos artigos.

---

## 🛠️ Tecnologias Utilizadas

Com base na estrutura do repositório (`pwa-news-dio/`, `src/`, `package.json` e `package-lock.json`), o projeto utiliza:

- **[ReactJS](https://react.dev):** Biblioteca principal para construção da interface de usuário e roteamento SPA.
- **JavaScript (ES6+):** Linguagem base utilizada tanto no front-end quanto na camada de serviço/API.
- **Service Workers & Manifest (`PWA`):** Recursos nativos da web para instalação e suporte offline.
- **[Node.js](https://nodejs.org) & Express:** Servidor leve para disponibilização dos endpoints de notícias (caso a API local esteja contida no projeto).
- **[Ant Design](https://ant.design) / CSS3:** Estilização, grid responsivo e componentes visuais da interface.
- **npm (`package.json` / `package-lock.json`):** Gerenciador de pacotes e scripts de execução.

---

## 📂 Estrutura de Diretórios

```text
pwa-news-api/
├── pwa-news-dio/         # Aplicação Front-end ReactJS (PWA, componentes, containers, public/sw.js)
├── src/                  # Código-fonte da camada de API/serviços de notícias
├── package.json          # Dependências e scripts da raiz do projeto
├── package-lock.json     # Árvore exata das dependências instaladas via npm
└── README.md             # Documentação do projeto
```

*(Nota: Como o repositório possui tanto a pasta `src/` na raiz quanto o subdiretório `pwa-news-dio/`, verifique se o back-end da API roda na raiz e o front-end React roda dentro de `pwa-news-dio/`).*

---

## 🚀 Como Executar o Projeto na Sua Máquina

### Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:
- **[Node.js](https://nodejs.org)** (versão LTS recomendada) e **npm**
- **[Git](https://git-scm.com)**

---

### Passo 1: Clonar o Repositório

```bash
git clone https://github.com
cd pwa-news-api
```

---

### Passo 2: Iniciar o Servidor da API (Raiz do Projeto)

1. Na pasta raiz (`pwa-news-api/`), instale as dependências da API:
   ```bash
   npm install
   ```

2. Inicie o servidor da API:
   ```bash
   npm start
   ```
   *(O servidor back-end ficará aguardando requisições HTTP, geralmente na porta `3000` ou `3001` — verifique a porta exibida no terminal).*

---

### Passo 3: Iniciar a Aplicação Front-end React (`pwa-news-dio`)

1. Abra um **segundo terminal**, acesse a subpasta do front-end React e instale as dependências:
   ```bash
   cd pwa-news-dio
   npm install
   ```

2. **Verifique a URL da API (se necessário):**
   Confira dentro do arquivo de serviço em `pwa-news-dio/src/` se a URL das requisições HTTP aponta para a mesma porta em que a API do Passo 2 está rodando (ex.: `http://localhost:3000/api`).

3. Inicie o servidor de desenvolvimento React:
   ```bash
   npm start
   ```

4. **Acesse no navegador:**
   Abra o endereço exibido no terminal (geralmente `http://localhost:3000/` ou `http://localhost:3001/`).

---

## 📦 Testando os Recursos de PWA (Build de Produção)

Os recursos completos de **PWA** (registro do Service Worker em produção, cache offline e ícone de instalação no navegador) são ativados no build otimizado:

1. Dentro da pasta `pwa-news-dio/`, gere o build de produção:
   ```bash
   npm run build
   ```

2. Sirva a pasta `build` localmente para testar a instalação:
   ```bash
   npx serve -s build
   ```
   Acesse o link local exibido no terminal e clique no ícone de **Instalar aplicativo** na barra de endereços do navegador.

---

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Se você quiser melhorar este projeto:

1. Faça um **Fork** deste repositório.
2. Crie uma **Branch** para sua melhoria (`git checkout -b feature/NovaFuncionalidade`).
3. Faça o **Commit** das suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
4. Faça o **Push** para a branch (`git push origin feature/NovaFuncionalidade`).
5. Abra um **Pull Request**.

---

## 👨‍💻 Autor

Desenvolvido por **[marceloxm](https://github.com/marceloxm)** durante os estudos na **Digital Innovation One (DIO)**.
