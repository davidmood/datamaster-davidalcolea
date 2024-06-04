
# Custom LLM DataMaster - David Alcolea





## I - Objetivo do Case

O objetivo desse projeto, é criar uma interface simplificada onde o usuário de dados
da empresa possa informar, em forma de texto natural, a necessidade que ele deseja
suprir com o dado, e assim obter uma resposta do programa com os dados encontrados
que possam servir para atender aquela necessidade, dessa forma, facilitando e
agilizando o descobrimento de dados e metadados da empresa.
## II - Arquitetura de Solução e Arquitetura Técnica

**Criação do script de ingestão da tabela de metadados no Databricks:**

A seguir será mostrado 3 prints como evidência da criação da tabela de metadados no
Databricks. Aqui estou utilizando dados mockados para efeito de demonstração.

![App Screenshot](https://uploaddeimagens.com.br/images/004/792/509/full/imagem_2024-06-04_184959850.png?1717537830)

![App Screenshot](https://uploaddeimagens.com.br/images/004/792/510/full/imagem_2024-06-04_185123833.png?1717537914)

**Versão final do 'ddl_scripts' para criação utilizando o csv de demonstração**

![App Screenshot](https://uploaddeimagens.com.br/images/004/792/541/full/imagem_2024-06-04_193119338.png?1717540316)

**Criação do front-end no Databricks onde o usuário enviará perguntas:**
![App Screenshot](https://uploaddeimagens.com.br/images/004/792/515/full/imagem_2024-06-04_190036724.png?1717538467)

**Testes usando metadados na biblioteca Langchain:**

Abaixo demonstração do desenvolvimento do “back-end” do projeto com a biblioteca
LangChain:
![App Screenshot](https://uploaddeimagens.com.br/images/004/792/516/full/imagem_2024-06-04_190139998.png?1717538530)

**Evidência dos resultados:**

Criação do script de ingestão da tabela de metadados no Databricks:
![App Screenshot](https://uploaddeimagens.com.br/images/004/792/517/full/imagem_2024-06-04_190329704.png?1717538639)

**Criação do front-end no Databricks onde o usuário enviará perguntas:**

A seguir, demonstro a utilização do front-end, onde, após uma pergunta ser
inserida no campo de busca, e a execução da célula “back-end” se obtém uma
resposta da pergunta enviada:
![App Screenshot](https://uploaddeimagens.com.br/images/004/792/519/full/imagem_2024-06-04_190657875.png?1717538848)

**Testes usando metadados na biblioteca Langchain:**
Abaixo, demonstramos a utilização do back-end para fazer perguntas sobre os dados
contidos na tabela de metadados:

![App Screenshot](https://uploaddeimagens.com.br/images/004/792/523/full/imagem_2024-06-04_191330501.png?1717539241)
## III - Explicação sobre o case desenvolvimento

Atualmente, a maioria das empresas busca ser “data-driven”, ou seja, tomar decisões
baseadas em dados.

Porém, para as grandes empresas, que possuem e trabalham com enormes quantidades
de dados, a própria catalogação e descobrimento de dados se torna um desafio, visto
que devido ao tamanho da empresa e dos setores internos dela, acabam sendo gerado
“silos” de dados. Portanto, fica evidente a importância do descobrimento de dados e
metadados. A seguir vamos destacar alguns aspectos que destacam essa importância:

**Tomada de Decisão Baseada em Dados:** Ter um entendimento claro sobre o que os
dados representam permite que as empresas tomem decisões mais informadas,
diminuindo riscos e incertezas.

**Otimização de Recursos:** Saber onde estão os dados e como acessá-los evita
redundâncias e melhora a eficiência, economizando tempo e recursos.

**Inovação:** A análise de dados pode revelar padrões e oportunidades que podem ser o
ponto de partida para novos produtos, serviços ou linhas de negócio.

**Conformidade e Governança:** Com a crescente regulação em torno dos dados, saber
exatamente que dados você possui, onde estão e como são usados é vital para estar
em conformidade com leis e regulamentos.

**Personalização:** Entender os dados dos clientes permite criar experiências mais
personalizadas, o que pode aumentar o engajamento e a fidelidade do cliente.
Além disso, os próprios metadados também são de suma importância:

**Contexto:** Metadados fornecem contexto aos dados, tornando mais fácil entender o
que os dados realmente significam, de onde vêm e como foram alterados ao longo do
tempo.

**Rastreabilidade e Linhagem de Dados:** Os metadados ajudam a entender o fluxo de
dados através de sistemas e processos, o que é essencial para a análise de causa raiz
e para garantir a qualidade e integridade dos dados.

**Segurança e Privacidade:** Metadados podem conter informações sobre os controles de
segurança em vigor, ajudando a garantir que os dados sejam manuseados de acordo
com as políticas de segurança e conformidade.

**Automatização:** O descobrimento de metadados facilita a automação de várias tarefas
de gerenciamento de dados, como categorização, limpeza e enriquecimento de dados.

**Colaboração e Produtividade:** Metadados bem gerenciados tornam mais fácil para
equipes diferentes dentro de uma organização encontrar os dados de que precisam e
entender como utilizá-los corretamente.

Em suma, o descobrimento de dados e metadados não é apenas uma "boa prática" em
um ambiente corporativo moderno; é um imperativo estratégico. A implementação
eficaz de ferramentas e processos para o descobrimento de dados e metadados,
portanto, deve ser uma alta prioridade para qualquer empresa que aspire ser
verdadeiramente orientada por dados.


## Benefícios e Justificativas

A utilização de um modelo de LLM e uma interface baseada em perguntas e respostas
para o descobrimento de dados e metadados, traz diversos benefícios, como
respostas mais rápidas, auxílio no descobrimento dos dados, economia de recursos,
eficiência operacional, e empoderamento do usuário.

Para apresentar as justificativas que motivaram o desenvolvimento do projeto, foram
utilizadas as metodologias Blueprint e o Canva de proposta de valor.


![App Screenshot](https://uploaddeimagens.com.br/images/004/792/503/full/imagem_2024-06-04_184002453.png?1717537234)


## IV - Melhorias e Considerações Finais

Durante a implementação do projeto, alcançamos foi alncançado diversos resultados significativos que contribuíram para a criação de uma interface simplificada, permitindo aos usuários da empresa solicitar dados em linguagem natural. A integração bem-sucedida com a LLM (Large Language Model) do OpenAI por meio de chamadas de API na plataforma
Databricks e o uso eficaz da biblioteca LangChain em Python foram os pilares do
sucesso.

Como pontos positivos, temos a utilização da própria plataforma do Databricks para
fornecer as perguntas e obter as respostas, proporcionando aos usuários uma maneira
fácil de expressar suas necessidades de dados. A integração com a LLM do OpenAI
mostrou-se eficiente, permitindo a obtenção de respostas relevantes. Além disso, a
utilização da biblioteca LangChain em Python facilitou o processamento de linguagem
natural.

Como pontos negativos, a escolha da versão Community do Databricks trouxe
limitações em relação aos recursos disponíveis. Restrições de capacidade e
funcionalidades exclusivas da versão paga foram obstáculos adicionais que afetaram a
escalabilidade e a abrangência do projeto.

Em relação as dificuldades encontradas, a implementação da biblioteca LangChain
apresentou um desafio em termos de familiarização e compreensão de seus recursos.
O aprendizado dessa biblioteca específica contribuiu para atrasos no desenvolvimento,
especialmente durante as fases iniciais do projeto.

O projeto proporcionou um aprimoramento significativo nas habilidades de
manipulação de dados, com destaque para o uso de tecnologias como Spark, Databricks
e PySpark. A integração de diversas tecnologias para criar uma solução abrangente
contribuiu para uma experiência de aprendizado enriquecedora. O aprendizado sobre
LLMs, um tema que está em evidência nos últimos tempos, também foi muito
enriquecedor.

Em conclusão, o projeto resultou em uma ferramenta eficaz para facilitar a descoberta
de dados e metadados na empresa, oferecendo respostas rápidas e relevantes às
solicitações em linguagem natural. Reconhecemos a importância contínua da
otimização e aprimoramento do sistema para garantir sua eficácia e relevância em um
ambiente dinâmico de dados.

## **Próximos passos**

Os próximos passos visam elevar ainda mais a eficácia da solução desenvolvida em
Engenharia de Dados, sendo eles:

**Refinamento do Modelo de Linguagem:**

• Investir em treinamento adicional para melhorar a compreensão do modelo
em relação às nuances nas solicitações dos usuários, utilizando conjuntos de
dados mais diversificados.

**Otimização do Desempenho da Chamada de API:**

• Continuar aprimorando as chamadas de API para garantir respostas rápidas,
explorando estratégias de cache e paralelização.

• Possibilidade de utilização geração aumentada de recuperação (RAG), para assim otimizar a chamada uma vez que o dataframe sendo analisado pode ser muito grande e dificultar o envio via API. 

**Ampliação da Interface e Suporte a Múltiplos Idiomas:**

• Expandir a interface para abranger uma variedade maior de solicitações e
considerar suporte para múltiplos idiomas.

**Implementação de Recursos de Feedback do Usuário:**

• Introduzir mecanismos de feedback do usuário para aprimorar a compreensão
do modelo em relação às necessidades específicas da empresa.

**Avaliação de Alternativas de Plataforma Databricks:**

• Avaliar a migração para uma versão paga do Databricks para aproveitar
recursos adicionais.

**Monitoramento Contínuo e Manutenção do Sistema:**

• Estabelecer procedimentos de monitoramento contínuo e manutenção regular
do sistema para acompanhar evoluções tecnológicas e necessidades da
empresa.

Esses passos irão garantir uma evolução contínua da solução, adaptando-se às
demandas dinâmicas do ambiente de descoberta de dados em linguagem natural.
## Variáveis de Ambiente

Para rodar esse projeto, você vai precisar adicionar as seguintes variáveis de ambiente no seu configs.ipynb

`os.environ["OPENAI_API_KEY"] = ""`

`os.environ["LANGCHAIN_API_KEY"] = ""`


## Instalação

O Databricks Community foi utilizado para o desenvolvimento deste case. Para acessar os dados de teste criados, é necessário importar o arquivo .csv para o seguinte caminho dentro do DBFS.

```bash
/FileStore/shared_uploads/david.alcolea@outlook.com
```
Arquivo CSV:
```bash
tabela_metadados.csv
```
    
## Autores

- [@davidmood](https://www.github.com/davidmood)

