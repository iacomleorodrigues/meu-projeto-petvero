# 🐾 PetVero — Aplicativo de Cuidado Bucal para Pets

O **PetVero** é um PWA (Progressive Web App) em polonês voltado para tutores de cães e gatos. O foco do aplicativo é criar uma rotina diária de aplicação de um spray natural para a saúde bucal dos pets (combate a tártaro, placa e mau hálito). 

Inspirado na dinâmica do Duolingo, o app combina rastreamento de hábitos, gamificação, educação e prova visual para maximizar o engajamento e a retenção do tutor ao tratamento físico.

---

## 🎯 Proposta de Valor

Transformar a aplicação diária do produto PetVero em um ritual prazeroso, mensurável e compartilhável. Com isso, aumentamos a aderência ao tratamento, o LTV (Lifetime Value) do cliente e a geração orgânica de marketing espontâneo via redes sociais.

---

## 🚀 Funcionalidades Principais

### 🔐 Autenticação & Onboarding Personalizado
* **Supabase Auth:** Login e cadastro seguro via Lovable Cloud (E-mail/Senha + Google OAuth).
* **Onboarding Inteligente:** Coleta dados essenciais do pet (Nome, espécie, raça, idade, peso e nível de tártaro atual).
* **Cálculos Automáticos:** O app define de forma personalizada:
  * **Dose recomendada:** Quantidade exata de sprays baseada no peso + nível de tártaro (máx. 6).
  * **Duração do plano:** Ciclos focados de 14, 21 ou 30 dias.
  * **Cronograma:** Calendário automático de vacinas e vermifugação.

### 🏠 Dashboard Principal (`Rutyna`)
* **Mascote Vivo & Dinâmico:** Cabeçalho com o nome do pet e um *Pet Mood* emocional (🐾😊🏆😟). O mascote reage diretamente ao *streak* do usuário (feliz com sequências altas, preocupado se a rotina for quebrada).
* **Checklist Diário em 3 Passos:**
  1. Agitar o frasco.
  2. Aplicar a dose personalizada de sprays na boca do pet.
  3. Aguardar 30 minutos sem comer ou beber.
* **Timer Integrado de 30 Minutos:** Aciona um cronômetro e dispara uma notificação push quando o tempo acaba, liberando o pet para comer e estimulando a segunda abertura do app no mesmo dia.
* **Gamificação & Medalhas:** Sistema de *streak* (dias consecutivos) com conquistas desbloqueáveis:
  * 🌱 Primeiro passo (1d) → 🥉 7d → 🥈 14d → 🥇 21d → 🏆 Lenda PetVero (30d).

### 💡 Micro-feedback & Pílulas de Conhecimento
* Exibido logo após o check-in diário.
* **Autoridade de Marca:** Rotação de 15 fatos educativos sobre os ingredientes naturais do produto (ex: dente-de-leão, alcaçuz).
* **Avaliação Rápida (👍 😐 👎):** Monitoramento contínuo sobre a evolução do hálito, redução da placa e aceitação do pet.

### 📸 Aba Progresso — Prova Visual e Viralização
* **Evolução Cronológica:** Upload de fotos dos dentes do pet armazenadas de forma segura em Buckets do Supabase através de URLs assinadas.
* **Slider Antes/Depois:** Componente interativo (*drag-to-reveal*) comparando o Dia 1 com o dia atual.
* **Marketing Orgânico (Canvas):** Geração automática de imagem customizada (1080×1350) com a identidade da marca, dados do pet e footer `petvero.pl`. Integração com a **Web Share API** para compartilhamento nativo nas redes sociais.

### 💉 Aba Vacinas
* Criação automatizada de eventos preventivos com base na idade do pet (Antirrábica, Polivalente DHPPi/FVRCP, Vermifugação em 2 doses e Check-up anual) com opção de edição e conclusão.

---

## 🛠️ Detalhes Técnicos & Arquitetura

* **Concepção:** Desenvolvido inicialmente no Lovable e integrado à Lovable Cloud.
* **Frontend:** React, TypeScript, Vite e Tailwind CSS.
* **Estilização:** Uso de tokens semânticos (`oklch`) centralizados em `src/styles.css` suportando perfeitamente **Modo Claro / Escuro**.
* **Banco de Dados & Segurança:** Persistência de dados via Supabase com políticas rígidas de segurança **RLS (Row Level Security)**.
* **PWA (Progressive Web App):** Manifesto configurado com ícones *maskable*, suporte a *service workers* para modo offline e botão nativo de instalação para rodar em modo *standalone* no celular.
* **Abordagem:** *Mobile-first*, otimizado para navegação rápida de rotina.
* **Idioma:** Totalmente em Polonês (focado no mercado-alvo da Polônia).

### 🎨 Identidade Visual
* **Paleta Premium:** Teal (`#1f5560`), Creme (`#FFF8EC`) e Sky Blue — transmitindo sensação natural, minimalista e veterinária de alto padrão.
* **UX/UI:** Cantos arredondados generosos (`rounded-3xl`), microinterações fluidas no clique (`press`) e animações suaves (`animate-fade-in-up`).

---

## 📦 Como Rodar o Projeto Localmente

Caso queira clonar este repositório e rodar o projeto na sua máquina local, certifique-se de ter o [Node.js](https://nodejs.org/) instalado e siga as instruções abaixo:

1. **Clone o repositório:**
```bash
   git clone [https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git](https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git)
