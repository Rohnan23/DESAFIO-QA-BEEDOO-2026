# DESAFIO-QA-BEEDOO-2026
DESAFIO-QA-BEEDOO-2026
CHECKLIST QA VAGA
1. A aplicação visa cadastrar e listar cursos, nos quais são possíveis determinar certos atributos como nome, dt inicio/ dt final, URL da imagem, duração .

2. Apresenta quatro fluxos simples: Cadastro, lista, excluir e editar de cursos.
     Fluxo 1 - Cadastro de curso: O usuário acessa o formulário de cadastro, preenche os atributos do curso e salva.
     Fluxo 2 - Listagem de cursos: O usuário acessa a tela de listagem e visualiza os cursos cadastrados em formato de cards.
     Fluco 3 - Exclusão de cursos: O usuário tenta remover um curso da listagem. Fluxo com falha crítica identificada.
     Fluxo 4 - Edição de cursos: Fluxo inexistente na aplicação atual. Não há opção para editar um curso após o cadastro.

3. Com base na análise da aplicação, os pontos abaixo representam os maiores riscos e merecem atenção prioritária em qualquer ciclo de testes:
1. 🔴 Integridade dos dados no cadastro
O formulário não possui validações. É possível criar cursos com campos vazios, datas incoerentes e valores numéricos inválidos. Qualquer dado pode entrar no sistema —
isso compromete a confiabilidade de toda a base.
2. 🔴 Operação de exclusão
A exclusão de cursos está quebrada. Trata-se de uma operação CRUD fundamental. Sem ela, o sistema acumula registros que não podem ser removidos, tornando o gerenciamento do catálogo inviável a longo prazo.
3. 🟠 Ausência de funcionalidade de edição
Sem edição, qualquer erro de cadastro exige deletar e recriar — o que não é possível dado o bug de exclusão. Isso torna o sistema essencialmente somente-leitura após o cadastro.
4. 🟠 Consistência entre os dados cadastrados e a listagem
Campos preenchidos no cadastro (imagem, endereço) não aparecem na listagem. Essa inconsistência entre o que é salvo e o que é exibido indica falha no mapeamento de dados entre camadas, e pode esconder outros campos com o mesmo problema.
5. 🟡 Experiência de navegação e feedback ao usuário
A ausência de um fluxo de navegação claro (sem Home, sem mensagens de sucesso/erro) compromete a usabilidade e pode mascarar falhas — o usuário não sabe se uma ação foi concluída com sucesso ou não.

PLANILHA QA: https://docs.google.com/spreadsheets/d/1SxzCZpzTOjnYmt0-S5vkaUHtFb-NcusfBUXftkpBLXU/edit?gid=0#gid=0
