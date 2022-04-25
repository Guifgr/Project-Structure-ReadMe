# Padronização > Nome do Projeto
---
- ## Tasks / Issues
    - ### **Título das tasks**
        A conveção para os títulos das tasks é (*Preste atenção aos Case Styles*):
        ```
        Título da task apresentando um problema
        ```
        > #### **adicionar uma label com a stack:** *Frontend*, *Backend*; 
        
        ***Se a task for front e back deve-se criar uma issue para cada stack.***

    - ### **Milestone**
       **Deve-se colocar uma milestone referenciando de qual sprint aquela task faz parte**

    - ### **Labels**
        As Labels utilizadas para classificar as issues no projeto são as seguintes:

        - **Open**: São as tasks em aberto - É o estado default

        - **Fazendo:** São tasks que estão sendo feitas por alguém no momento - Quando aplicar essa label a uma issue, não esqueça de colocar o assignee ao responsável pelo desenvolvimento da mesma

        - **Bug**: São as tasks que necessitam de correção

        - **Review**: São as tasks que estão aguardando qualquer tipo de revisão - Geralmente estão esperando a aprovação e o merge da MR

        - **Done**: São as tasks que estão PRONTAS - São as issues que não precisamos mais desenvolver nada relacionadas a ela

        - **Impedimento**: São as tasks que estão com algum impedimento para serem realizadas

        - **Closed**: São as tasks fechadas, portanto, não devemos mais voltar nelas - Tasks prontas só serão fechadas ao FINAL DA SPRINT

        - **Prioridades**: Para labels de prioridades temos: ALTA, MÉDIA, BAIXA - As labels de prioridades não devem ser sempre utilizadas, somente quando realmente houver necessidade
        
        - **Frontend**: São as task relacionadas ao Frontend
        
        - **Backend**: São as task relacionadas ao Backend
        
        - **Backlog**: São as task relacionadas ao backlog dessa sprint
---
- ## Commits e Merge Requests
   A estrutura acordada para os títulos é:
    ```zsh
    type(scope): mensagem de commit
    ```
   sendo scope a issue/task referente à feature ou bugfix que está sendo feito. <br/>
   ***esta mesma estrutura cabe em merge requests***

   > Reitera-se que não há padronização para a **descrição** das commits/MR, porém, elas **DEVEM** ser preenchidas. A descrição é um detalhamento mais longo do que o título sobre o que a commit possui. <br/>
   Espera-se bom senso do time para manter a descrição clara e de fácil entendimento, contendo todas as informações importantes da commit realizada.

    -   ### commit types
        Os tipos de commits são os seguintes:
        -    **WIP:** Work in progress

        -   **build:** Mudanças que afetam o sistema de build ou dependências internas (example scopes: gulp, broccoli, npm)

        -   **ci:** Mudanças no arquivo de configuração de CI (example scopes: Travis, Circle, BrowserStack, SauceLabs)

        -   **docs:** Somente alteração de documentação

        -   **feat:** Nova feature

        -   **fix:** Correção de bug (fix e hotfix)

        -   **perf:** Alterações com objetivo de melhorar a performance da aplicação

        -   **refactor:** Alterações que alteram um código sem afetar ou adicionar funcionalidades

        -   **style:** Mudanças que não afetam a dinâmica do código (espaço em branco, formtação, vírgulas esquecidas, etc)
---

- ## Branches
    A convenção de branches é a seguinte (kebab-case):
    - Para novas implementações: Derivando da develop
    ```zsh
     feature/nome-da-branch
    ```
    - Para refatorações: Derivando da develop
    ```zsh
     refactor/nome-da-branch
    ```
    - Para bugs fixes: Derivando da develop ou staging¹
    ```zsh
     fix/nome-da-branch
    ```
    - Para bug fix de algo sútil que passou para a produção², main ou develop
    ```
    hotfix/nome-da-branch
    ```

---
- ## Referências / Informações Adicionais
    -   ### **1. Staging**

    Replica perfeita do ambiente de produção, um deploy para testar antes de homologar.

    -   ### **2. Produção**

    Onde a aplicação ganha vida e o usuário pode utilizar.

    [_mais sobre diferentes ambientes_](https://klauslaube.com.br/2011/03/07/diferentes-ambientes.html)

    -   ### **3. Sobre patches, hotfixes, coldfixes e bugfixes**

    Geralmente fazemos bugfixes, ou seja, nossa padronização de commits e MR usam o type **fix**

    [_mais sobre a diferença de fixes_](https://www.bmc.com/blogs/patch-hotfix-coldfix-bugfix/)
