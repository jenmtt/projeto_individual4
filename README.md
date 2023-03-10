<h1 id="topo" align="center"> 4° Projeto Individual - Resilia / Senac </h1>

<h2 id="sobre">Sobre 🔎</h2>

<h4> Contexo da situação: </h4>
A Resilia está pensando em lançar um novo sistema de
acompanhamento e para isso precisa de ajuda para modelar um
banco de dados que vai armazenar seus cursos, turmas e alunos.


<h4 id="aqui"> O que é para ser feito? </h4>
<p>Para apoiar nesse sistema recebemos a tarefa de realizar essa modelagem
e responder algumas perguntas com nosso modelo:<br>
⇨ Existem outras entidades além dessas três?<br>
⇨ Quais são os principais campos e tipos?<br>
⇨ Como essas entidades estão relacionadas?<br>
</p>

<h2 id="projeto">Projeto 📈</h2>

- Print da Modelagem no site Miro.com:<br><br>

<div align="center">
  <img width="80%" src="https://user-images.githubusercontent.com/97655280/214456406-0b22a509-c47d-4c29-9a0c-eaf74bd6c68c.jpg" />
</div>


<h3>⇨ Explicação para cada atributo de cada entidade.</h3>

**Três entidades a mais (Unidades,Professor e Endereços), com essas entidades a mais podemos ter uma noção melhor, como?**<br>

- Unidades: A entidade Unidades abrange todo o "universo" de todas as entidades, pois ela é mais importante, ela diz onde a instituição fica alocada mostrando com as colunas id (para pegar toda a linha), nome, bairro, estado cnpj e o tipo, a coluna tipo é para dizer se é a empresa Matriz ou Filial. <br><br>
- Cursos: A entidade Cursos abrange todos os cursos de todas as Unidades, ela recebe duas chaves estrageiras para saber em qual nome da unidade e o Estado da Unidade que fica alocada. <br><br>
- Alunos: A entidade Alunos é a base para o cadastro básico do aluno com as colunas nome, nascimento, cpf e recebendo duas chaves estrangeira "nome_cursos" para saber de qual curso o aluno pertence e "nome_unidades" para saber em qual unidade o aluno X pertence, essa chave estrangeira de Unidades é ideal para responder uma pergunta "Quantos alunos tem na Unidade X?". <br><br>
- Professor: A entidade Professor é basicamente a mesma de Alunos, sendo que acrescentei a especialidade do professor, a formação dele se é Frontend, Backend ou Full-Stack. <br><br>
- Endereços: Uma unidade muito importante é a endereço, pois ela pega todo o endereço de Alunos e Professores recebendo as colunas id, nome_professor, nome_aluno, rua, bairro, cidade, estado e cep. Repare que coloquei nome_professor e nome_aluno, quando utilizarmos o comando SELECT, utilizamos um ou outro, pois não seria possível utilizar as duas chaves e dando conflito, chamando a entidade nome_professor iria buscar pelo nome dele e aparecer todos os dados do mesmo. <br><br>
- Turmas: E por último a entidade Turmas, essa entidade é responsável por gerenciar as colunas id, nome, turno, alunosQuant, nome-cursos, modalidade_cursos e diasDasAulas_cursos, com essa entidade é possível saber a quantidade de alunos na turma X, e recebe três chaves estrangeira para saber qual curso é a turma X, quais são os dias de aulas e a modalidade do curso se é Presencial ou Ensino a Distância (EAD). <br><br>

**Por que algumas entidades estão relacionadas uma com as outras (FK, chave estrangeira)?**<br>
- Para o nosso banco de dados é fundamental ter elas, pois o relacionamento conseguimos responder algumas perguntas básicas, por exemplo: <br>
> Quantos cursos X tem na unidade Y? <br>
Quais são os cursos que tem na unidade Y? <br>
Quantos alunos matriculados tem na unidade Y? <br>
Quantos alunos tem em sala de aula do curso X? <br>

Essas são algumas perguntas que poderiamos responder fácil com o banco de dados, pois elas estão relacionadas. Caso não conseguíssemos resolver alguma outra pergunta futuramente, poderíamos acrescentar uma FK em uma entidade para solucionar o problema ou dependendo da situação, acrescentar um atributo nas entidades.

<br>

<h3>Respostas das perguntas mencionadas  <a href="#aqui">aqui</a> </h3>

> **⇨ Existem outras entidades além dessas três?**<br>
Sim, existem mais duas entidades, "Unidades" e "Professor". <br>
Precisei colocar essas entidades para ter um parâmetro, aonde a entidade "Curso" fica vinculado a entidade "Unidades" e a entidade "Professor" fica vinculado a "Turmas", portanto, todas conectadas para um gerenciamento melhor no banco de dados. <br> <br>

> **⇨ Quais são os principais campos e tipos?**<br>
Os principais campos são o nome, cpf, nascimento e sem dúvida o ID referenciando toda a entrada na Entidade.<br>
Os dois tipos mais importante são a Chave Primária e a Chave estrangeira.   <br><br>

> **⇨ Como essas entidades estão relacionadas?**<br>
As entidades estão relacionadas com as chaves estrageiras (FK), como podemos ver na imagem feita no <a href="#projeto"> Miro </a>, em algumas entidades tem um atributo com "id_nomeDaEntidade", fazendo com que elas fiquem relacionadas. <br>

<h2 id="ferramentas">Ferramentas utilizadas nesse projeto 📚</h2>

  - [x] Miro.com
<br>

<div align="center">
  &#11165;&nbsp;<a href="#topo"><strong>Voltar ao topo</strong></a>&nbsp;&#11165;
</div>
