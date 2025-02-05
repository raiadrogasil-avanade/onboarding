# Guia de Uso do Git na RD

## Fluxo de Desenvolvimento

Na RD, seguimos o **Git Flow** para organizar nosso desenvolvimento. A estrutura das branches segue o seguinte formato:

``` bash
<tipo>-<módulo>/NSSAPP-<número-da-task>
```

### Tipos de Branches:
- **feature**: Para novas funcionalidades
- **fix**: Para correções de bugs
- **chore**: Para tarefas que não afetam diretamente a lógica do código (configurações, documentação, etc.)
- Outros tipos podem ser utilizados conforme necessário

### Módulos:
- **bc-hub**
- **bc-cart**
- **bc-core**

#### Exemplo de criação de branch:
```bash
git checkout -b feature-bc-core/NSSAPP-1234
```

### Commits semânticos:

Para manter um histórico limpo e padronizado, seguimos o Commit Semântico.
O formato padrão do commit é:

```bash
<tipo>: <descrição curta em inglês>

<descrição mais detalhada (opcional)>

Refs or Closes NSSAPP-<número-da-task>
```

#### Tipos de commits:

- **feat**: Adição de uma nova funcionalidade
- **fix**: Correção de um bug
- **chore**: Tarefa sem impacto direto no código de produção
- **docs**: Alterações na documentação
- **style**: Ajustes de formatação (espaços, indentação, etc.)
- **refactor**: Refatoração de código sem alteração de funcionalidade
- **test**: Adição ou correção de testes

- **Exemplo de commit:**
```bash
git commit -m "feat: add new CPF validation

Cpf validation that checks all numbers

Refs NSSAPP-1234"
```

### Boas práticas
- ✅Sempre crie branches baseadas no Git Flow
- ✅ Use commits semânticos para manter o histórico organizado
- ✅ Relacione os commits às tarefas no Jira com Refs ou Closes
- ✅ Revise o código antes de abrir um Pull Request
- ✅ Utilização de imperativo quando escrever um commit:
    - Use o modo imperativo na linha de assunto. Exemplo – fix: add fix for dark mode toggle state. O modo imperativo dá o tom de que você está dando uma ordem ou fazendo uma solicitação.
