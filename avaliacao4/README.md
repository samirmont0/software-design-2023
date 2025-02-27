# Problema

Profissionais de saúde necessitam trocar informações entre eles visando a continuidade do cuidado de seus pacientes.
Uma rede deve ser criada visando facilitar e agilizar a interação entre profissionais da saúde. 
Possivelmente com a configuração de horários, por exemplo, na qual a comunicação é permitida, sugerida, assim como notificações e outros.
Deve ser possível realizar buscas por meio da especialidade, endereço de estabelecimento, nome do estabelecimento e outros. 
Também deve ser possível a troca de imagens e de texto por tempo limitado.
A rede deve viabilizar a comunicação sem revelar formas de contato pessoais como telefone, por exemplo.

## Projeto (design)

O software será composto por uma aplicação web integrada com um banco de dados.

### Descrição

A proposta é criar um sistema de chat entre profissionais de saude.
A aplicação terá a função de cadastro e de login para cada médico. Ao realizar o cadastro os dados serão populados no banco e disponibilizados para que outros médicos vizualizem e  entrem em contato.
Após o login o profisional poderá acessar chat ou buscar por um novo médico, escolhendo por especialidade, endereço, nome do estabelecimento ou médico.
Após iniciar um chat com um médico e enviar mensagens de texto ou imagem, o outro médico será notificado por email de que um novo chat foi criado.
Dentro dos chats os médicos podem optar por adicionar arquivos, ou enviar mensagens de texto.
Durante a criação do chat o responsavel pela criação pode determinar por quanto tempo esse chat continuará aberto
Cada mensagem será limitada a 1000 caracteres e envios de arquivos serão restritos a 10 MB

### Interface com o usuário

Ao abrir a aplicação, os usuários irão se deparar com uma tela de login, nessa tela permitirá que eles insiram seus emails e senhas para realizar o login ou optem por criar uma nova conta.
Na tela de criação de conta eles poderam fornecer seus emails, senha, nome, crm, especialidade, local de trabalho, endereço
Após realizar o login haverá uma listagem de chats iniciados, ao final da listagem haverá um botão para criação de novos chats
Durante a criação de novos chats o usuário será apresentado com a seleção de filtros, podendo preencher o filtro de especialidade, endereço, nome do estabelecimento ou nome do médico. 
Após aplicar filtros definidos, será listado todos médicos que se incluem nele. Apartir dessa lista será possivel criar um novo chat com o respectivo médico
Dentro dos chats será listado as mensagens enviadas, mensagens de texto ficarão disponiveis diretamente e arquivos e fotos enviadas serão permitidos o download das mesmas. Também será disponibilizado um campo para preenchimento de texto e um botão para envio, assim como um botão para anexo de arquivos ou imagens

### Descrição da estrutura de banco

Deverão ser criadas 3 tabelas:

Médicos, conterão: senha, nome, email, especialidade, crm, local_de_trabalho, endereço

Chats, conterão: medico_criador, medico_remetente

Mensagens, conterão: chat, tipo, conteudo, nome_arquivo

## Implementação

Consulte o diretório [comunicacao] (./comunicacao), que contém uma implementação
do algoritmo definido acima
