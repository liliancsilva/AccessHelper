<<<<<<< HEAD
**AccessHelper**

AccessHelper é um chatbot criado para atender ao challenge do Azure Frontier Girls, que exige a criação de um Agente de IA com pelo menos uma ação funcional.

Para cumprir o desafio, optei por desenvolver uma ferramenta aplicável ao meu cotidiano profissional.

Uma das tarefas que mais consome tempo é responder dúvidas em tempo real sobre status de solicitações, endereços e outras informações complementares.

Com o AccessHelper, o tempo normalmente destinado a atendimentos poderá ser redirecionado para tarefas mais complexas, otimizando processos e garantindo maior agilidade — algo altamente valorizado no ramo de telecomunicações.

**Funcionalidades**

- Consultar endereço de um site (equipamento) específico;
- Verificar tipo de instalação (Greenfield, Rooftop, Indoor);
- Checar status do pedido de acesso e protocolo de chaves;
- Informar número da solicitação e status da detentora;
- Retornar instruções de acesso e observações adicionais.

<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image1.png"
style="width:5.90556in;height:0.90694in"
alt="Uma imagem contendo Texto O conteúdo gerado por IA pode estar incorreto." />

A ideia é simples: o usuário faz uma pergunta, o AccessHelper consulta sua base de conhecimento e retorna a informação solicitada de forma rápida e confiável.

**Tecnologias Utilizadas**

- **Azure Cognitive Search:** utilizado para criar o índice de conhecimento do AccessHelper;
- **Azure OpenAI:** fornece o modelo de linguagem que interpreta as perguntas dos usuários e gera respostas naturais com base nos dados do índice;
- **NDJSON:** formato de arquivo utilizado para armazenar os registros de acesso, facilitando a ingestão dos dados no Azure Cognitive Search;
- **Python:** linguagem usada para manipular os arquivos NDJSON, preparar os dados e interagir com os serviços do Azure.

**Visão Geral e Pontos de Extremidade**

<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image2.png"
style="width:5.90556in;height:3.88958in"
alt="Texto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image3.png"
style="width:5.90556in;height:1.99861in"
alt="Tela de computador com fundo preto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image4.png"
style="width:5.90556in;height:4.28333in"
alt="Tela de computador com texto preto sobre fundo branco O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image5.png"
style="width:5.90556in;height:2.71806in"
alt="Interface gráfica do usuário, Texto, Aplicativo O conteúdo gerado por IA pode estar incorreto." />

**Base de Conhecimento**

O AccessHelper utiliza um índice no Azure Cognitive Search com dados de acesso em formato NDJSON. Cada registro contém:

1. **Identificação e Localização**
    - id;
    - site;
    - endereco;
    - município;

2. **Protocolo de Chaves**
    - protocolo_chaves;
    - data_inicio_protocolo;
    - data_fim_protocolo;

3. **Status do Protocolo e Detalhes da Instalação**
    - status_protocolo;
    - tipo_instalacao;
    - data_solicitacao;
    - data_liberacao;

4. **Período de Detentora e Status de Acesso**
    - data_inicio_detentora;
    - data_fim_detentora;
    - status_detentora;

5. **Informações Operacionais**
    - numero_solicitacao;
    - forma_acesso;
    - observacoes_adicionais.

É importante destacar que <u>os dados inseridos na base de conhecimento são fictícios</u>.

<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image6.png"
style="width:5.90556in;height:4.20486in"
alt="Interface gráfica do usuário, Aplicativo, Tabela O conteúdo gerado por IA pode estar incorreto." />

**Configuração do AccessHelper**

A seguir, imagens demonstram o prompt do sistema e a base de dados vinculada.

<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image7.png"
style="width:5.90556in;height:2.19931in"
alt="Tela de computador com texto preto sobre fundo branco O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image8.png"
style="width:5.90556in;height:2.10139in"
alt="Tela de computador com texto preto sobre fundo branco O conteúdo gerado por IA pode estar incorreto." />

**Demonstração**

A seguir, o AccessHelper responde a cinco perguntas diferentes.

<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image9.png"
style="width:5.90556in;height:4.82778in"
alt="Interface gráfica do usuário, Texto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image10.png"
style="width:5.90556in;height:4.82917in"
alt="Interface gráfica do usuário, Texto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image11.png"
style="width:5.90556in;height:4.78194in"
alt="Texto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image12.png"
style="width:5.90556in;height:4.81597in"
alt="Texto O conteúdo gerado por IA pode estar incorreto." />
<img
src="C:\Users\liali\Downloads\Estudos\Mais Mulheres Tech\Azure\Challenge\AccessHelper\media/media/image13.png"
style="width:5.90556in;height:4.83681in"
alt="Interface gráfica do usuário, Texto O conteúdo gerado por IA pode estar incorreto." />

Inspirado em interações reais, o AccessHelper não apenas responde à pergunta feita, mas também antecipa informações relacionadas. Na prática, conversas tendem a se prolongar, pois nem todas as dúvidas são enviadas de uma vez. Para otimizar o atendimento, o chatbot retorna de forma imediata os principais dados que encontra em sua base.
=======
# AccessHelper
Agente de IA como projeto do challenge Azure Frontier Girls 2025
>>>>>>> 1b5bd86ca39e6b3aa1fa88266749f8c859724510
