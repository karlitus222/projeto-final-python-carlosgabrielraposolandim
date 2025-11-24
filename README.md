[README.md](https://github.com/user-attachments/files/23700018/README.md)
# Sistema de Tarefas (CRUD) — Python Terminal

Projeto final da disciplina **Programação I - Python**: um **CRUD de Tarefas** que roda no terminal.

## Funcionalidades
- **Cadastrar** tarefa (descrição, prioridade 1–5, prazo opcional `dd/mm/aaaa`)
- **Listar** tarefas (todas, pendentes, concluídas, atrasadas e por prioridade)
- **Atualizar/Editar** tarefa (descrição, prioridade, prazo, status)
- **Remover** tarefa
- **Relatório**: total, concluídas, pendentes, atrasadas, taxa de conclusão e distribuição por prioridade
- **Sair** do sistema

## Estrutura de dados
Os registros são armazenados como **lista de dicionários**, por exemplo:
```python
[
  {"id": 1, "descricao": "Estudar Python", "status": "Pendente", "prioridade": 2, "prazo": "2025-12-01", "criada_em": "2025-11-23T21:00:00"}
]
```
Há **persistência em JSON** no arquivo `tarefas_dados.json` (criado automaticamente na pasta onde o programa for executado).


##  Navegação do menu
```
1. Cadastrar tarefa
2. Listar tarefas (todas)
3. Listar pendentes
4. Listar concluídas
5. Listar atrasadas
6. Listar por prioridade
7. Atualizar/editar tarefa
8. Remover tarefa
9. Relatório
0. Sair
```

##  Validações
- Descrição não pode ser vazia
- Prioridade deve ser entre **1 e 5** (padrão: 3)
- Prazo aceita formato **`dd/mm/aaaa`** (opcional)

##  Dicas (alinhadas ao enunciado)
- IDs são gerados automaticamente e **únicos**
- Teste as funções individualmente antes de integrar
- O menu roda em loop até o usuário escolher sair

##  Critérios atendidos
- CRUD completo via terminal
- **5+ funções** com responsabilidades claras
- **Lista de dicionários** para registros
- **Laços** e **condicionais** para controle de fluxo
- **Entradas/Saídas** com `input()` e `print()`
- **Boas práticas**: indentação, nomes claros, comentários, mensagens amigáveis
- **Extra:** persistência em JSON e filtros de listagem (atrasadas, prioridade)

##  Exemplos de uso
- Cadastrar tarefa: informe descrição, prioridade e prazo (opcional)
- Listar atrasadas: calcula automaticamente considerando a data atual
- Atualizar: é possível **mudar status** (Pendente/Concluída) e limpar o prazo

---

