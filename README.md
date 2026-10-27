# SKALAD

Sistema web de controle de estoque desenvolvido com HTML, CSS, JavaScript, PHP e MySQL/MariaDB.

## Recursos

- Dashboard de estoque e movimentações
- Cadastro e edição de produtos
- Entradas e saídas de estoque
- Alertas de estoque baixo
- Geração e leitura de QR Code
- Movimentação rápida por QR Code
- Histórico e filtros de movimentações
- Exportação de dados em CSV
- Usuários e perfis de acesso
- Layout responsivo com identidade visual verde

## Requisitos

- PHP com PDO MySQL
- MySQL ou MariaDB
- Servidor Apache (XAMPP funciona para desenvolvimento local)
- Navegador moderno

## Instalação local com XAMPP

1. Coloque a pasta do projeto em `C:\xampp\htdocs\skalad`.
2. Copie `config.example.php` e renomeie a cópia para `config.php`.
3. Ajuste os dados do MySQL em `config.php` se necessário.
4. Inicie Apache e MySQL no XAMPP.
5. Acesse `http://localhost/skalad/`.

O `api.php` cria as tabelas básicas automaticamente. O arquivo `skalad.sql` também está disponível caso você prefira importar o banco pelo phpMyAdmin.

## Configuração do banco

O arquivo `config.php` é ignorado pelo Git para evitar publicar credenciais. O repositório contém somente `config.example.php` como modelo.

Exemplo:

```php
<?php
return [
    'db_host' => '127.0.0.1',
    'db_name' => 'skalad_db',
    'db_user' => 'root',
    'db_pass' => '',
];
```

## Login inicial

Em uma instalação nova, o sistema pode criar o administrador inicial `admin@skalad.com`. Altere a senha inicial imediatamente depois do primeiro acesso, principalmente se o sistema estiver publicado na internet.

## QR Code e câmera

A leitura pela câmera funciona em `localhost` ou em um site servido por HTTPS. O navegador também precisa ter permissão para acessar a câmera.

## Colocar no GitHub

Crie um repositório vazio no GitHub e, dentro da pasta do projeto, execute:

```bash
git init
git add .
git commit -m "Versão inicial do SKALAD"
git branch -M main
git remote add origin URL_DO_SEU_REPOSITORIO
git push -u origin main
```

Substitua `URL_DO_SEU_REPOSITORIO` pela URL exibida pelo GitHub.

## Segurança

- Não envie `config.php` para o Git.
- Não coloque senhas reais no código-fonte.
- Troque a senha inicial do administrador.
- Em produção, use HTTPS.
- Faça backup do banco antes de atualizações.

## Estrutura principal

- `index.html` — interface principal
- `style.css` — visual do sistema
- `script.js` — comportamento do frontend
- `api.php` — API/backend PHP
- `skalad.sql` — estrutura SQL
- `config.example.php` — modelo de configuração do banco
- `.gitignore` — arquivos que não devem ir para o Git

## Licença

Projeto educacional. Adicione a licença que preferir antes de distribuir publicamente.
