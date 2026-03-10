```mermaid
classDiagram

%% =========================
%% CLASSES
%% =========================

class Pessoa {
    +codigo
    +nome
    +cpf
    +dataNascimento
    +telefone
    +email
    +numeroResidencia
    +complemento
    +dataCadastro
    +dataAlteracao
    +usuarioCadastro
}

class Usuario {
    +login
    +senha
    +situacao
}

class PerfilUsuario {
    +codigo
    +nome
}

class Hospede {
    +comumCgg
}

class Solicitante {
    +tipo
    +comumCgg
}

class Logradouro {
    +codigo
    +cep
    +estado
    +cidade
    +bairro
    +dataCadastro
    +dataAlteracao
}

class Quarto {
    +codigo
    +numero
    +bloco
    +andar
    +descricao
    +capacidadePacientes
    +reservasTemporarias
    +situacao
    +dataCadastro
    +dataAlteracao
    +usuarioCadastro
}

class Hospedagem {
    +codigo
    +dataEntrada
    +dataSaida
}

class Acompanhante {
    +codigo
    +dataEntrada
    +dataSaida
}

%% =========================
%% HERANÇA
%% =========================
Pessoa <|-- Usuario
Pessoa <|-- Solicitante
Pessoa <|-- Hospede

%% =========================
%% AGREGAÇÃO
%% Pedido usa Produto
%% =========================
Usuario o--> PerfilUsuario
Solicitante o--> Hospedagem
Hospede o--> Hospedagem
Quarto o--> Hospedagem
Hospede o--> Acompanhante
Pessoa o--> Logradouro

%% =========================
%% COMPOSIÇÃO
%% =========================
Acompanhante *--> Hospedagem



