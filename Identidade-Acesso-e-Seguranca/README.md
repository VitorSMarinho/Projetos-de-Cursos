# 🌐 Identidade, Acesso, Segurança e RBAC na Azure

## 📘 Visão Geral

A segurança moderna na nuvem exige uma abordagem baseada em **identidade**, **controle de acesso inteligente** e **políticas de segurança adaptativas**. Na Microsoft Azure, isso é habilitado principalmente por três pilares:

- **Azure Active Directory (Azure AD)** para identidade e autenticação
- **Acesso Condicional** para aplicar políticas dinâmicas baseadas em risco
- **Controle de Acesso Baseado em Funções (RBAC)** para gerenciamento de permissões granulares em recursos

Este repositório documenta os conceitos essenciais, boas práticas e exemplos práticos para **implementar segurança robusta baseada em identidade na Azure**.

---

## 🎯 Objetivos

- Proteger dados e recursos com autenticação forte e permissões mínimas
- Automatizar decisões de acesso baseadas em contexto
- Aplicar segregação de funções com RBAC
- Apoiar a arquitetura Zero Trust

---

## 🔐 Acesso Condicional

O **Acesso Condicional** permite que você aplique políticas automatizadas baseadas em condições como identidade do usuário, localização, dispositivo e risco.

### ⚙️ Como Funciona

1. **Sinais de entrada**: Usuário, localização, dispositivo, risco.
2. **Avaliação de política**: A Azure verifica se há políticas aplicáveis.
3. **Ação de controle**: Permitir, bloquear ou exigir autenticação multifator (MFA), dispositivo gerenciado, etc.

### 🧪 Exemplos de Políticas

- **Requerer MFA para acesso externo**:
  - Condição: Fora da rede corporativa
  - Ação: Requerer MFA

- **Bloquear acesso de dispositivos não conformes**:
  - Condição: Dispositivo não compatível
  - Ação: Bloquear acesso

- **Permitir apenas apps específicos para administradores**:
  - Condição: Aplicativo de destino
  - Ação: Permitir apenas se for o Azure Portal ou PowerShell

### 🛡️ Boas Práticas

- Utilizar **modo "Somente Relatório"** antes de aplicar
- Criar **contas de break-glass** sem Acesso Condicional
- Monitorar com **logs de entrada** e **Microsoft Sentinel**
- Usar **grupos dinâmicos** para controle de escopo

---

## 🧱 RBAC (Role-Based Access Control)

O **RBAC** é o modelo de controle de permissões para recursos da Azure. Ele permite **delegar acesso com base em funções predefinidas ou personalizadas**, seguindo o princípio do **menor privilégio**.

### 🔧 Como Funciona

RBAC utiliza três componentes principais:

- **Principal de segurança**: Usuário, grupo, ou identidade gerenciada
- **Função (Role)**: Conjunto de permissões (ex: `Reader`, `Contributor`, `Owner`)
- **Escopo**: Nível onde a função é aplicada (ex: assinatura, grupo de recursos, recurso)

### 🌍 Exemplo de Hierarquia de Escopo

Assinatura
└── Grupo de Recursos
└── Recurso (ex: Storage Account, VM)

### 🛠️ Exemplo de Atribuição

```text
Usuário: joao@empresa.com
Função: Contributor
Escopo: Grupo de Recursos "projetos-financeiros"

📌 Funções Comuns
Função	Permissões
Owner	Controle total, incluindo delegação de acesso
Contributor	Gerencia tudo, exceto permissões
Reader	Somente leitura
User Access Admin	Gerencia acesso de outros usuários
Funções personalizadas	Permissões sob medida para seu ambiente

🔐 RBAC vs Acesso Condicional
Característica	Acesso Condicional	RBAC
Foco	Autenticação e contexto	Autorização a recursos
Quando age	No momento do login	Após login, ao tentar acessar um recurso
Tipo de controle	Dinâmico e baseado em sinal	Estático e baseado em atribuições
Exemplo	Bloquear login de fora do país	Impedir que um usuário exclua VMs

## 🙋‍♂️ Autor
Vitor Marinho  
[GitHub](https://github.com/VitorSMarinho) | [LinkedIn](https://www.linkedin.com/in/vitor-marinho/)
# Projetos-de-Cursos

