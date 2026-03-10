```mermaid
classDiagram

%% =========================
%% CLASSES
%% =========================

class Usuario {
    +codigo
    +dataCadastro
    +dataAlteracao
    +usuarioCriador
    +nome
    +situacao
    +login
    +senha
    +dataNascimento
    +idade
    +cpf
    +numeroTelefone
    +email
    +perfil
    +logradouro
    +numeroResidencia
    +complemento
}

class PerfilUsuario {
    +codigo
    +nome
}

class Hospede {
    +codigo
    +dataCadastro
    +dataAlteracao
    +usuarioCriador
    +nome
    +comum
    +dataNascimento
    +idade
    +cpf
    +numeroTelefone
    +email
    +logradouro
    +numeroResidencia
    +complemento
}

class Logradouro {
    +codigo
    +dataCadastro
    +dataAlteracao
    +cep
    +estado
    +cidade
    +bairro
}

class Solicitante {
    +codigo
    +dataCadastro
    +dataAlteracao
    +usuarioCriador
    +nome
    +tipo
    +comum
    +dataNascimento
    +idade
    +cpf
    +numeroTelefone
    +email
    +logradouro
    +numeroResidencia
    +complemento
}

class Quarto {
    +codigo
    +numero
    +bloco
    +andar
    +situacao
    +dataRegistro
    +dataAlteracao
    +usuarioCadastro
}

class ReservaQuarto{
}

class Hospedagem {
}

class Paciente {
    +dataEntrada
    +dataSaida
}

class Acompanhante {
    +dataEntrada
    +dataSaida
    +paciente
}

