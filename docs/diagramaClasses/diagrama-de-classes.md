```mermaid
classDiagram

%% =========================
%% CLASSES
%% =========================

class Pessoa {
    +codigo:int
    +nome:string
    +cpf:string
    +dataNascimento:date
    +telefone:string
    +email:string
    +numeroResidencia:string
    +complemento:string
    +pontoReferencia:string
    +dataCadastro:date
    +dataAlteracao:date
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

class Endereco {
    +codigo
    +cep
    +estado
    +cidade
    +distrito
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
Pessoa o--> Endereco

%% =========================
%% COMPOSIÇÃO
%% =========================
Acompanhante *--> Hospedagem



