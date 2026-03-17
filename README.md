# Countries & Capitals Quiz (Laravel)

> Jogo educativo para testar seus conhecimentos sobre capitais do mundo.

---

## 🔍 Sobre

Esse projeto é uma aplicação **Laravel** simples que apresenta um quiz de perguntas sobre **países e suas capitais**.

O quiz funciona assim:
- O jogador escolhe quantas perguntas quer responder (entre 3 e 30).
- Para cada país, a aplicação mostra quatro opções de capitais (1 correta + 3 erradas).
- O sistema guarda o total de acertos e erros e mostra o resultado final ao término.

---

## 🚀 Como rodar (Windows / Laragon)

### Pré-requisitos

- PHP 8.1+ (Laragon)
- Composer
- Node.js + npm (para assets)

### Instalação

`~
cd c:\laragon\www\countries_and_capitals
composer install
npm install
`

### Configurar ambiente

1. Copie o .env.example para .env:

`~
copy .env.example .env
`

2. Gere a chave de aplicação:

`~
php artisan key:generate
`

### Rodar localmente

`~
php artisan serve
`

Acesse: http://127.0.0.1:8000

---

## 🧠 Como o quiz funciona (rápido)

- Os dados de países e capitais estão em app/app_data.php.
- O controller principal é App\Http\Controllers\MainController.
- As rotas principais estão em 
outes/web.php:
  - / (formulário de início)
  - /game (pergunta atual)
  - /answer/{answer} (resposta escolhida)
  - /next_question (seguir para próxima pergunta)
  - /show_results (placar final)

---

## 🧪 Testes

Este projeto não inclui testes automatizados, mas você pode rodar a suíte padrão do Laravel:

`~
vendor\bin\phpunit
`

---

## 📦 Estrutura relevante

- 
esources/views/ → templates Blade do jogo
- app/app_data.php → lista de países e capitais
- app/Http/Controllers/MainController.php → lógica do jogo

---

## ✅ Melhorias sugeridas

- Melhora estilo
- Adicionar persistência de pontuação por usuário (BD + autenticação)
- Incluir modo de treino com explicações sobre cada capital
- Adicionar suporte a múltiplas línguas

---

## 📄 Licença

Projeto disponibilizado sob a licença **MIT**.
