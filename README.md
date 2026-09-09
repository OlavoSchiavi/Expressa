# Expressa

Plataforma para divulgar artistas da periferia, aproximando seus trabalhos de novos públicos e fortalecendo a cultura local.

## Status

O projeto está em fase de protótipo frontend. As páginas possuem identidade visual, navegação responsiva e dados demonstrativos. As rotas de autenticação, banco de dados e moderação ainda precisam ser conectadas ao backend.

## Estrutura

```text
Expressa/
├── assets/
│   ├── img/                       # Favicon e imagens da interface
│   └── js/                        # Scripts existentes de autenticação
├── pages/
│   ├── index.html                 # Home pública da Expressa
│   ├── admin/dashboard.html       # Painel administrativo
│   ├── auth/login.html            # Login de usuários
│   ├── auth/cadastro.html         # Cadastro de usuários comuns
│   ├── auth/cadastro-artista.html # Cadastro multi-step de artistas
│   └── user/config.html           # Configurações do usuário
├── src/
│   ├── input.css                  # Entrada do Tailwind e componentes compartilhados
│   └── output.css                 # CSS compilado usado pelas páginas
├── server.js                      # Servidor Express inicial
└── package.json                   # Dependências do projeto
```

## Como executar

Instale as dependências:

```bash
npm install
```

Recompile o Tailwind uma vez com:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css
```

Durante o desenvolvimento, mantenha a compilação observando alterações:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

As páginas HTML podem ser abertas diretamente no navegador. O `server.js` ainda é uma base do servidor Express e deverá receber as rotas quando a integração com o backend começar.

## Interface atual

- A home apresenta a proposta da Expressa, artistas em destaque e chamadas para ação.
- Login e cadastro seguem a identidade visual da home.
- O cadastro artístico usa um formulário multi-step com progresso, validação, revisão e confirmação de senha.
- O dashboard administrativo apresenta métricas, atividade, distribuição por linguagem e fila de moderação com dados demonstrativos.

## Próximos passos

1. Conectar os formulários às rotas do Express.
2. Persistir usuários e perfis de artistas no SQLite.
3. Substituir os dados demonstrativos por consultas ao banco.
4. Implementar autenticação, autorização de administradores e sessões.
5. Criar telas de revisão, aprovação e edição de perfis.

## Convenções para contribuição

- Preserve a paleta e os componentes compartilhados definidos em `src/input.css`.
- Prefira classes utilitárias do Tailwind às regras CSS isoladas.
- Mantenha `label`, `id`, `name` e `autocomplete` nos campos dos formulários.
- Atualize este README ao adicionar páginas, comandos ou integrações.