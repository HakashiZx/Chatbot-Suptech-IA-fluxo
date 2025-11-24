# Chatbot-Suptech-IA-fluxo
fluxograma do chatbot integrado com IA da Suptech

## 🧩 Visão Geral
Este projeto consiste em um chatbot interativo desenvolvido no Typebot, criado para auxiliar usuários em atendimentos simples, automáticos e guiados.
O fluxo foi estruturado para oferecer respostas rápidas, limitar interações e encerrar a conversa de forma amigável quando o usuário confirmar que obteve sucesso.

## ⚙️ Funcionamento do Chatbot
O chatbot segue uma lógica de atendimento dividida em etapas bem definidas, permitindo que o usuário seja guiado de forma clara até a solução desejada.

## 1. Coleta da Mensagem do Usuário
O fluxo inicia sempre pelo bloco “Mensagem do Usuário”, onde o bot recebe a entrada enviada pelo visitante.

Este é o ponto de entrada de todas as interações.

## 2. Verificação de Palavras‑Chave
Após o usuário enviar sua mensagem, o bot realiza uma verificação automática para identificar se o usuário informou:

“deu certo”
“funcionou”
“obrigado”
Se qualquer uma dessas expressões for detectada, o bot reconhece que o problema foi solucionado e exibe imediatamente a mensagem de encerramento:

“Fico feliz ter conseguido ajudá-lo!
Obrigado por usar nosso sistema!
Suptech agradece!”

Essa etapa garante que o atendimento seja finalizado rapidamente quando o próprio usuário confirma a resolução.

## 3. Sistema de Contagem de Interações
Caso o usuário não utilize nenhuma expressão de encerramento, o chatbot ativa um sistema interno de contagem.
A cada nova mensagem, uma variável é incrementada para registrar quantas interações ocorreram.

Exemplo:

interacoes = interacoes + 1
Quando o limite definido é atingido, o chatbot exibe uma mensagem final e encerra automaticamente a conversa, evitando loops ou atendimentos muito longos.

## 4. Envio da Mensagem para a IA
Se nenhuma regra de encerramento for acionada e o limite de interações não for atingido, o bot encaminha a mensagem do usuário para a Integração com a IA.
Essa integração é responsável por produzir respostas inteligentes com base no conteúdo enviado.

O fluxo retorna então ao usuário, reiniciando o ciclo com a próxima interação.

## 5. Encerramento do Atendimento
O chatbot encerra a conversa em duas situações:

Quando o usuário informa que o problema foi resolvido
Quando o limite máximo de interações é alcançado
Em ambos os casos, uma mensagem final clara e cordial é exibida.

## 🛠️ Estrutura Lógica Resumida
Mensagem do Usuário ↓ Verificação de Frases de Encerramento ├── Se positivo → Mensagem Final └── Se negativo → Contador de Interações ↓ Verificação do Limite ├── Se atingido → Mensagem Final └── Se não → Envio para IA
## 📦 Finalidade
Este fluxo foi projetado para:

Garantir uma experiência de atendimento simples e intuitiva
Evitar conversas longas ou repetitivas
Encerrar o atendimento no momento certo
Oferecer respostas automáticas complementadas por IA
