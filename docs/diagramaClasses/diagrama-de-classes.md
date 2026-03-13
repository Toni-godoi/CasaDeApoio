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
    +pontoReferencia:text
    +dataCadastro:date
    +dataAlteracao:date
}

class Usuario {
    +login:string
    +senha:string
    +situacao:boolean
}

class PerfilUsuario {
    +codigo:int
    +nome:string
}

class Hospede {
    +comumCgg:string
}

class Solicitante {
    +tipo:string
    +comumCgg:string
}

class Endereco {
    +codigo:int
    +cep:string
    +estado:string
    +cidade:string
    +distrito:string
    +bairro:string
    +dataCadastro:date
    +dataAlteracao:date
}

class Quarto {
    +codigo:int
    +numero:int
    +bloco:string
    +andar:int
    +descricao:string
    +capacidadePacientes:int
    +reservasTemporarias:int
    +situacao:boolean
    +dataCadastro:date
    +dataAlteracao:date
}

class Hospedagem {
    +codigo:int
    +dataEntrada:date
    +dataSaida:date
}

class Acompanhante {
    +codigo:int
    +dataEntrada:date
    +dataSaida:date
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



