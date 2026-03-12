# casa-de-apoio
Sistema de gerenciamento de hóspedes da casas de apoio.

# Pitch da visão do produto
## PARA 
casas de apoio que acomodam pacientes e acompanhantes provenientes de outras cidades para realização de tratamentos médicos, procedimentos hospitalares ou períodos de internação,
## QUE
necessitam administrar de forma organizada e sistêmica o controle de quartos, hospedagens, pacientes, acompanhantes e períodos de permanência, garantindo rastreabilidade das informações, transparência administrativa e acompanhamento completo da rotina institucional,
## O
Sistema de Gestão para Casas de Apoio é um software web que permite registrar, organizar, controlar e emitir relatórios sobre toda a operação da casa de apoio, incluindo gestão de hóspedes, vínculos entre pacientes e acompanhantes, ocupação de quartos e histórico de estadias,
## AO CONTRARIO DE
* sistemas atualmente utilizados pelas casas de apoio, que apresentam limitações operacionais como a impossibilidade de alteração do vínculo de uma pessoa entre paciente e acompanhante após o cadastro, além da ausência de relatórios personalizados capazes de demonstrar a rotina da instituição, históricos de hospedagem, alterações cadastrais e vinculações entre hóspedes, quartos e períodos;  
* sistemas hospitalares tradicionais, voltados à gestão clínica e assistencial, cujo foco está em prontuários médicos, procedimentos e internações, não contemplando a dinâmica de acolhimento, hospedagem social e administração de permanência características das casas de apoio;  
* sistemas de hotelaria e hospedagem convencionais, que tratam os usuários apenas como hóspedes, sem considerar vínculos assistenciais entre paciente e acompanhante, motivos médicos da estadia, períodos relacionados a tratamentos de saúde e necessidades de prestação de contas institucionais e sociais;  
## NOSSO SISTEMA
permite cadastrar qualquer pessoa inicialmente como hóspede e vinculá-la, a qualquer momento, como paciente ou acompanhante, possibilitando alterações dinâmicas conforme a necessidade da instituição, além de oferecer controle completo da ocupação de quartos, histórico de permanência e emissão de relatórios personalizados gerais e individuais sobre períodos de hospedagem, vínculos, cadastros e alterações realizadas no sistema.


# Regras de negócio  

Uma casa de apoio é o local da cidade onde pessoas que estão passando por tratamentos médicos e seus acompanhantes podem se hospedar durante o tempo de internação ou tratamento. A hospedagem para acompanhantes pode acontecer desde que haja um paciente, e o paciente pode estar alocado na casa de apoio ou internado em uma unidade hospitalar.

Tanto paciente quanto o acompanhante são hóspedes do sistema. Um acompanhante só pode ser vinculado a um quarto desde que haja um paciente vinculado também.

Existem 3 tipos de pessoas no sistema:  
*Usuário de sistema: São quem vai ter login ao sistema e poderá agir ou executar funções e permissões do sistema.  
*Solicitantes: É a pessoa que não possui acesso do sistema, mas é cadastrada. O solicitante é quem solicita a vaga para um paciente na casa de apoio. O solicitantes pode ser do tipo Diacono ou Cooperador.  
*Hospede: É o objeto proncipal do sistema. É quem se hospeda na casa de apoio. Uma pessoa é cadastrada como hospede no sistema, e depois de ser um hospede pode ser vinculada a um quarto com paciente, ou pode ser vinculado a um paciente como acompanhante dele. Quando o paciente ou o acompanhante terminam sua estadia na casa de apoio, ambos continuam cadastrados no sistema como hóspede.  

O acompanhante pode dar entrada no quarto a qualquer momento, sem necessidade do paciente estar junto presencialmente, embora o paciente precise ser vinculado no momento da entrada (basta que haja os dados do paciente para que a entrada seja efetivada).

O quarto pode ser reservado previamente, antes da data da entrada, desde que haja solicitação de um solicitante.

O acompanhante pode sair a qualquer momento, e, também, pode haver troca de acompanhantes a qualquer momento no período em que o paciente está vinculado ao quarto, mesmo que o paciente não esteja presencialmente na casa de apoio (casos em que o paciente está internado em algum hospital). Cada paciente tem o direito a ter 1 acompanhante no máximo.

Cada vez que um hospede registra entrada e saida como sendo paciente ou acompanhante, esse registro ficar armazenado para futuramente ser auditado e emitido relatorios.

Um quarto pode comportar 1, 2 ou mais pacientes, conforme o administrador da casa de apoio definir. Pontanto, um quarto está livre quando não há nenhum paciente dentro dele, e está ocupado quando seu limite máximo de pacientes esta preenchido.
