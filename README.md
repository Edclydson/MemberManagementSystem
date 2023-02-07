# MemberManagementSystem (Backend)
O escopo deste projeto consiste em ser um sistema de gestão de pessoas voluntárias interno da He4rt.

## Descrição Geral
- Aplicativo web com foco em gerenciamento de pessoas.

### Funções da Aplicação
- Cadastro de Usuário
- Login de Usuário
- CRUD de Perfil
- CRUD de Status

## Requisitos Funcionais
> **Requisito 01** | ***RF001*** - Cadastro de Usuário
>
> Cadastro:
>
> Este requisito deve cumprir a funcionalidade que permita o usuário se
> cadastrar no sistema após preencher um formulário próprio ou se optar por
> selecionar uma autenticação via Discord.
>
> 1. Cadastro via API do Discord (Opção 1)
> 2. Cadastro via Backend próprio (Opção 2)
     >     - Opção A: Autenticação via JWT
>     - Opção B: Autenticação via OAuth
>     - Opção C: Dê uma sugestão
>
> Dados do formulário de Cadastro:
> - Nome completo > [String | Obrigatório]
> - Apelido > [String | Opcional]
> - Email [String | Único | Obrigatório]
> - Senha [String/Hash/Password | Obrigatório]


---

> **Requisito 02** | ***RF002*** - Login de Usuário
>
> Este requisito deve cumprir a função de login do sistema, permitindo o
> usuário se autenticar via dados previamente cadastrados ou via Discord
> mediamente escolha feita pelo usuário
>
> 1. Login via API do Discord (Opção 1)
> 2. Login via Backend próprio (Opção 2)
>
> Dados do formulário de Login:
> - Nome de usuário (String | Obrigatório)
> - Senha (String/Hash/Password | Obrigatório)

---

> **Requisito 03** | ***RF003*** - CRUD de Perfil
>
> Este requisito deve cumprir a função que permita o usuário pertencente a
> conta, alterar sua foto de perfil (Caso não seja uma conta linkada por
> Discord), alterar suas competências técnicas (Linguagens de programação,
> Frameworks, Padrões de Código, Boas Práticas e etc...), e demais competências
> pessoais (soft skills no geral)
>
> 1. Foto de perfil
> 2. Descrição de perfil de desenvolvedor
> 3. Descrição de Competências
> 4. Descrição de Competências Técnicas

---

> **Requisito 04** | ***RF004*** - CRUD de Status
>
> Este requisito deve possibilitar que o usuário adicione, altere e/ou remova um status do seu
>
> 1. Status: Disponível para atuar em projetos
> 2. Status: Indisponível para atuar em projetos

## Regras de Negócio

> **Regra de Negócio 01** | *RN001* | Comportamento de Cadastro
>
> O usuário deverá ser alertado sobre os campos que { não foram preenchidos, estão pendentes ou não seguem a regra implantada (ex: email único, username em uso, etc...)} com uma mensagem de erro explicando resumidamente o que está faltante para que seja concluído o cadastro com sucesso.
>
> **Caso de Sucesso:**
> Deverá ser mostrado ao usuário um modal contendo a mensagem "Cadastro Concluído com Sucesso" e um botão com a mensagem "Ok"

---

> **Regra de Negócio 02** | *RN002* | Comportamento de Login
>
> O usuário deverá ser alertado por uma mensagem em { pop-up e/ou push notification } caso { a senha não esteja correta e/ou o usuário não esteja correto }
> No campo de senha deverá conter um botão que permita o usuário ver qual senha foi escrita por ele por motivos de User Experience (UX)
>
> **Caso de Sucesso:** Ao ser efetuado o login na plataforma o usuário deverá ser redirecionado à página inicial da aplicação que conterá seu perfil.

> **Regra de Negócio 03** | *RN003* | Comportamento de Entrada
>
> O usuário após ser redirecionado à pagina inicial, deverá ser sugerido um caminho para ele seguir dentro da aplicação, para que seja feito as alterações no perfil.
