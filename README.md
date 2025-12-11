# Site Institucional CD Consult

## 🚀 Visão Geral

Este é o repositório do site institucional da CD Consult, desenvolvido com React + Vite + TypeScript e hospedado na Vercel.
O projeto inclui uma landing page completa e um formulário de contato integrado a um endpoint serverless para envio de e-mails.

## ✨ Funcionalidades

*   **Design Responsivo:** O layout se adapta perfeitamente a qualquer dispositivo (desktop, tablet e mobile) graças ao uso do **Tailwind CSS**.
*   **Captação de Leads:** Formulário de contato principal, que é a única funcionalidade interativa da página.
*   **Envio de E-mail Serverless:** Os dados do formulário são processados por uma **Função Serverless da Vercel** (`api/send-email.ts`) que utiliza o **Nodemailer** para enviar a mensagem.
*   **Autenticação Segura:** O envio de e-mail é autenticado por uma conta Gmail dedicada, utilizando uma **App Password** para garantir a segurança e a entrega da mensagem.
*   **Deploy Contínuo:** O projeto está configurado para **Deploy Automático via Vercel** a partir do GitHub.

## 🛠️ Tecnologias Utilizadas

O projeto é construído com uma stack moderna e eficiente, garantindo velocidade e manutenibilidade.

| Categoria | Tecnologia | Detalhes |
| :--- | :--- | :--- |
| **Frontend** | **React** com **Vite** | Biblioteca principal para a interface do usuário e ferramenta de build rápida. |
| **Linguagem** | **TypeScript** | Garante maior segurança e escalabilidade ao código. |
| **Estilização** | **Tailwind CSS** | Framework CSS utility-first para um desenvolvimento ágil e responsivo. |
| **Backend (Formulário)** | **Node.js** e **Nodemailer** | Utilizado na Função Serverless da Vercel para processar e enviar e-mails. |
| **Hospedagem** | **Vercel** | Plataforma de hospedagem e deploy contínuo. |
| **Serviço de E-mail** | **Gmail + App Password** | Usado para autenticação e envio seguro dos e-mails do formulário. |

## ⚙️ Instalação e Configuração Local

Siga os passos abaixo para configurar e rodar o projeto em seu ambiente de desenvolvimento local.

### Pré-requisitos

Certifique-se de ter o **Node.js** instalado em sua máquina.

### Passos

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/cdconsult-labs/cdconsult-site.git
    cd cdconsult-site
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Configuração das Variáveis de Ambiente (Apenas para Teste Local do Formulário)**
    Para testar o envio de e-mail localmente, você precisará configurar as variáveis de ambiente. **Atenção:** Em produção (Vercel), estas variáveis são configuradas diretamente na plataforma.

    *   Crie um arquivo `.env` na raiz do projeto.
    *   Adicione as seguintes variáveis:
        ```
        # Credenciais do Gmail (com App Password) para autenticação do Nodemailer
        EMAIL_USER="[Seu Email Gmail para Envio]"
        EMAIL_PASS="[Sua App Password do Gmail]"
        
        # Email de destino (para onde as mensagens do formulário serão enviadas)
        EMAIL_TO="[O e-mail de destino]"
        ```

4.  **Execute o projeto em modo de desenvolvimento:**
    ```bash
    npm run dev
    ```

### Comandos Úteis

| Comando | Descrição |
| :--- | :--- |
| `npm run dev` | Inicia o servidor de desenvolvimento local. |
| `npm run build` | Gera a build de produção na pasta `dist`. |
| `npm install` | Instala todas as dependências do projeto. |

## 🌐 Deploy e Hospedagem

O projeto está hospedado na **Vercel** e utiliza o recurso de **Deploy Contínuo**.

*   **URL do Site:** `https://cdconsult.net`
*   **Fluxo de Deploy:** Qualquer `push` para a branch principal do repositório no GitHub aciona automaticamente um novo build e deploy na Vercel.

## 🔑 Configuração de Produção (Vercel )

As variáveis de ambiente (`EMAIL_USER`, `EMAIL_PASS`, `EMAIL_TO`) são essenciais para o funcionamento do formulário em produção e devem ser configuradas nas **Environment Variables** do projeto na Vercel.

*   **EMAIL_USER:** O endereço de e-mail Gmail configurado para envio.
*   **EMAIL_PASS:** A App Password gerada para esta conta Gmail.
*   **EMAIL_TO:** O e-mail de destino.

## 📝 Como Contribuir

1.  Faça um fork do projeto.
2.  Crie uma branch para sua feature (`git checkout -b feature/nome-da-feature`).
3.  Faça commit das suas alterações (`git commit -m 'feat: Adiciona nova feature'`).
4.  Faça push para a branch (`git push origin feature/nome-da-feature`).
5.  Abra um Pull Request.

## 🔒 Propriedade e Direitos Autorais

Este código-fonte é de propriedade exclusiva da **CD Consult**. Todos os direitos são reservados.

O acesso e uso deste repositório são restritos aos membros da equipe e colaboradores autorizados, conforme os acordos internos da empresa.

