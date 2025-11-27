# 📊 RPA Power BI - Service Desk Core IT

## 📌 Documentação do Processo
Este repositório contém a automação responsável por **atualizar o Dashboard do Service Desk da Core IT a cada 5 minutos**.

A solução foi desenvolvida em **UiPath** e consiste em um robô que:
1. Abre o Power BI.
2. Aguarda a inicialização.
3. Clica no dashboard já presente no histórico de visualização.
4. Aguarda carregamento.
5. Clica em **Atualizar**.
6. Aguarda.
7. Clica novamente em **Atualizar** (necessário devido a um bug do Power BI).
8. Aguarda.
9. Fecha o painel.

---

## ⚙️ Orquestração (Agendamento)
A orquestração da automação ocorre por meio de **publicação e sincronização entre o UiPath Orchestrator e a configuração da máquina local**.

- Publicação realizada via **versionamento de pastas**.
- Execução agendada pelo **Orchestrator**.

🔗 Recursos úteis:
- [Publicação de processos UiPath](https://www.youtube.com/watch?v=aOLuAZ3e-co)  
- [Solucionar problemas com Unattended Robot](https://www.youtube.com/watch?v=6zVEZCQk69w)

---

## 🛠️ Escolhas Técnicas e Desafios
- Automação construída integralmente em **UiPath**.  
- Por se tratar de uma requisição simples de desktop, a solução é **mais fácil de compreender e sustentar**.  
- Não foi utilizada a **API oficial do Power BI**, devido às limitações de atualização diária (8–42 vezes) e custos de licença adicionais.

---

## 💻 Requisitos
- Computador **sempre ligado**.  
- UiPath instalado e configurado.  
- Power BI instalado e configurado.  
- O dashboard precisa ser aberto **manualmente uma vez** antes de enviar a automação para produção.  
- Máquina configurada para rodar a atividade:  
  - **Memória RAM:** mínimo 8 GB  
  - **CPU:** conforme necessidade  
- O computador **não pode ser utilizado** enquanto a automação estiver em execução, para evitar falhas.

---

## 📂 Repositório da Aplicação
Este repositório contém:
- Código fonte da automação (`Main.xaml` e workflows auxiliares).  
- Configurações de orquestração e publicação.  
- Documentação de suporte.  

---

## 📝 Observações
- A automação é **dependente do ambiente desktop**.  
- Recomenda-se monitoramento periódico para garantir que o robô esteja rodando conforme esperado.  
- Caso o Power BI seja atualizado ou alterado, os **seletores do UiPath** podem precisar de ajustes.

---
