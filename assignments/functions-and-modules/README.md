# 📘 Atividade: Funções e Módulos

## 🎯 Objetivo

Organizar o código em funções reutilizáveis e módulos separados, aprendendo a importar essas funções em outros arquivos usando apenas a biblioteca padrão do Python.

## 📝 Tarefas

### 🛠️	Criando Funções com Parâmetros e Retorno

#### Descrição
Crie um arquivo `converters.py` com funções que convertem temperaturas entre escalas.

#### Requisitos
O programa concluído deve:

- Definir a função `celsius_to_fahrenheit(celsius)` que retorne `celsius * 9 / 5 + 32`.
- Definir a função `fahrenheit_to_celsius(fahrenheit)` que retorne o valor convertido para Celsius.
- Exemplo de uso:
  ```python
  print(celsius_to_fahrenheit(100))  # 212.0
  ```

### 🛠️	Valores Padrão e Argumentos Nomeados

#### Descrição
Crie uma função que formate uma saudação e aceite parâmetros opcionais.

#### Requisitos
O programa concluído deve:

- Definir `greet(name, greeting="Hello")` que retorne a string `"<greeting>, <name>!"`.
- Chamar a função usando um argumento nomeado, por exemplo `greet("Alice", greeting="Hi")`.
- Exemplo de saída:
  ```
  Hi, Alice!
  ```

### 🛠️	Criando um Módulo Utilitário

#### Descrição
Crie um arquivo `math_utils.py` com funções auxiliares que possam ser reutilizadas em outros programas.

#### Requisitos
O programa concluído deve:

- Definir `average(numbers)` que retorne a média de uma lista de números.
- Definir `is_prime(n)` que retorne `True` se `n` for primo e `False` caso contrário.
- Não executar nenhum código de teste no nível do módulo.

### 🛠️	Importando Módulos

#### Descrição
Crie um arquivo `main.py` que importe as funções dos módulos criados nas tarefas anteriores e use a biblioteca padrão do Python.

#### Requisitos
O programa concluído deve:

- Importar `converters` e `math_utils` usando `import` e `from ... import`.
- Usar a função `random.randint()` da biblioteca padrão para sortear um número entre 1 e 100 e informar se ele é primo.
- Executar o código principal somente dentro de `if __name__ == "__main__":`.
