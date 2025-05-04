# 🗄️ Configuração de Instância de Banco de Dados SQL no Microsoft Azure

## 📘 Descrição

Este repositório documenta o processo completo de **criação e configuração de uma instância de banco de dados SQL** no portal do Microsoft Azure, baseado no guia oficial da Microsoft.

Devido à limitação de créditos gratuitos, esta entrega apresenta **uma simulação realista** do provisionamento da instância, com **capturas de tela das etapas configuradas** e uma explicação detalhada do processo.

🔗 Tutorial base:  
[Microsoft Docs - Criar um Banco de Dados SQL](https://learn.microsoft.com/pt-br/azure/azure-sql/database/single-database-create-quickstart-portal)

---

## 🎯 Objetivo do Projeto

Demonstrar a criação de uma instância SQL Database no Azure Portal, abordando:

- Escolha do tipo de banco de dados (único)
- Criação do servidor lógico
- Definição de camada de serviço (uso gratuito, se disponível)
- Opções de autenticação e segurança
- Compreensão do fluxo completo sem custos

---

## ⚙️ Parâmetros Utilizados (Simulação)

| Parâmetro               | Valor                       |
|-------------------------|-----------------------------|
| Nome do banco           | `db-teste-azure`            |
| Tipo de instância       | Banco de dados único        |
| Nome do servidor lógico | `srv-db-teste`              |
| Localização             | `East US`              |
| Autenticação            | SQL (usuário/senha)         |
| Camada de preço         | `Basic` / `Gratuito`        |
| Redundância geográfica  | Desabilitada                |

---

## 📷 Capturas de Tela

As imagens do processo estão organizadas na pasta [`/images`](./images):

- Criação do recurso “Banco de Dados SQL”
- Configuração básica da instância
- Definição do servidor lógico
- Escolha de plano e performance
- Tela final de revisão

Exemplo:

![Configuração da Instância SQL](./images/passo3-configuracao-servidor.png)

---

## 🧠 Aprendizado

- Entendimento da hierarquia de recursos no Azure (grupo de recursos, instância, servidor).
- Diferenças entre camadas de desempenho e modelos de compra (vCore x DTU).
- Importância da configuração de firewall e autenticação segura.
- Fluxo completo de deploy via portal, útil para ambientes de testes e POCs.

---

## 🚫 Observações

> A instância **não foi criada de fato** para evitar consumo de recursos fora do plano gratuito.  
> No entanto, todas as etapas foram seguidas e documentadas fielmente conforme o processo real.

---

## 🙋‍♂️ Autor

**Seu Nome**  
[GitHub](https://github.com/VitorSMarinho) • [LinkedIn](https://www.linkedin.com/in/vitor-marinho/)

