markdown# 🐍 Aula: Lógica de Programação com Python + Git/GitHub

## 1. O que é Git e GitHub?
Antes de programar, precisamos saber como salvar e organizar nossas versões de código.

*   **Git:** Sistema de controle de versão (local na sua máquina).
*   **GitHub:** Plataforma na nuvem para hospedar seus repositórios Git e colaborar com outros desenvolvedores.

### Comandos Essenciais do Git:
1. `git init`: Inicia um repositório na pasta.
2. `git add .`: Prepara os arquivos para o salvamento.
3. `git commit -m "mensagem"`: Grava as alterações com uma nota explicativa.
4. `git push`: Envia o código para o GitHub.

---

## 2. Lógica com Python: Entrada e Saída de Dados
Toda lógica começa com a interação entre o usuário e o programa.

```python
# Entrada de dados
nome = input("Qual o seu nome? ")
idade = int(input("Qual sua idade? "))

# Processamento e Saída
print(f"Olá {nome}, você tem {idade} anos.")
```

---

## 3. Operadores Lógicos e Comparação
Essenciais para criar "regras" no programa.


| Operador | Descrição | Exemplo |
| :--- | :--- | :--- |
| `==` | Igual a | `x == 5` |
| `!=` | Diferente de | `x != 10` |
| `>` / `<` | Maior / Menor | `idade > 18` |
| `and` | E (ambas verdadeiras) | `logado and admin` |
| `or` | OU (uma verdadeira) | `sol or calor` |

---

## 4. Estruturas Condicionais
Onde o programa "decide" o caminho a seguir.

```python
nota = 8.5

if nota >= 7:
    print("Resultado: Aprovado!")
elif nota >= 5:
    print("Resultado: Recuperação.")
else:
    print("Resultado: Reprovado.")
```

---

## 5. Listas e Laços de Repetição
Como lidar com múltiplos dados de uma vez.

```python
# Lista de tarefas
tarefas = ["Estudar Python", "Fazer Commit", "Subir pro GitHub"]

# Percorrendo a lista com for
for item in tarefas:
    print(f"Tarefa pendente: {item}")
```

---

## 🛠️ Atividade Prática: O Primeiro Repositório
Siga os passos abaixo para entregar o seu exercício:

1. **Crie o arquivo:** Crie um script `calculadora.py` que some dois números.
2. **Inicie o Git:** No terminal, digite `git init`.
3. **Commit:** Adicione o arquivo com `git add .` e faça o `git commit -m "Meu primeiro script em Python"`.
4. **GitHub:** Crie um repositório no seu GitHub e use o comando `git push` para enviar o código.

---
*Dica: Commits frequentes evitam a perda de progresso!*