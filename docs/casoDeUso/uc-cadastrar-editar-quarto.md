# Informações Gerais

| Campo | Valor |
|---|---|
| **Nome do Caso de Uso** | Cadastrar e editar quartos |
| **Descrição** | O gestor de quartos pode cadastrar um novo quarto |
| **Ator envolvido** | Gestor de quartos |

---

# Interação entre ator e sistema

| Funcionário | Sistema |
|---|---|
| Gestor de quartos seleciona para cadastrar um novo quarto ou editar quarto existente | O sistema exibe uma tela para preenchimento das informações do quarto com os campos descritos no dicionário de dados |
| O usuário preenche os campos solicitados e seleciona cadastrar | O sistema atribui automaticamente valores para alguns campos obrigatórios e cadastra o quarto (RI01, RI02, RN01, RN02) |

---

# Exceções

*Nenhuma exceção definida.*

---

# Alternativas

*Nenhuma alternativa definida.*

---

# Regras de Negócio

- **RN01** - O código do quarto não deve ser dado pelo número do quarto, mas pela ordem sequencial que esse quarto foi cadastrado no sistema.

- **RN02** - O campo **Situação** que aparece para o usuário sempre é dado como **ativo** ao cadastrar um novo quarto. O usuário não conseguirá editá-lo durante o primeiro cadastro. Ele só pode ser inativo a partir da edição do cadastro.
---

# Requisitos de Interface com o Usuário

- **RI01** - O campo código que aparece para o usuário é preenchido automaticamente pelo sistema, com base na ordem de cadastro de quartos.

- **RI02** - O campo **Data** deve ter um botão que ao clicar abre um calendário para o usuário selecionar dia/mês/ano do cadastro.

---

# Dicionário de Dados

| Nome Campo | Descrição | Obrigatoriedade | Unique | Tipo | Tamanho | Máscara | Valor Default | Regex |
|---|---|---|---|---|---|---|---|---|
| Código | Código de cadastro do quarto | Obrigatório | TRUE | INT | 3 | | | `^\d{3}$` |
| Data | Data que o quarto foi cadastrado | Obrigatório | FALSE | Data | | | `current_date` | |
| Número | Número do quarto | Obrigatório | TRUE | INT | 4 | | | `^\d{4}$` |
| Andar | Número do andar | Obrigatório | FALSE | INT | 2 | | | `^\d{2}$` |
| Usuário | Usuário que está cadastrando o quarto | Obrigatório | FALSE | Texto | 120 | | `current_user` | `^[A-Za-zÀ-ÿ\s]{2,120}$` |
| Situação | Situação do quarto que sempre será como "ativo" ao cadastrar um novo quarto | Obrigatório | FALSE | Boolean | 1 | | TRUE | |

# BPD da função
<img width="2626" height="762" alt="uc-cadastroQuarto" src="https://github.com/user-attachments/assets/185c68d4-c3d4-487b-b88d-981dd68a5be8" />

