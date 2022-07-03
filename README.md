# Padrões de codificação

Este projeto apresentará exemplos do estilo de código do CiLab para python.

Os códigos neste projeto são exemplos de como esperamos que o código seja produzido. Todas as regras aqui mencionadas são rigorosamente aplicadas em todos os arquivos deste projeto para fins de exemplificação.


## Python

Recomendamos tutoriais interativos incríveis do Aprenda Python

[https://www.learnpython.org](https://www.learnpython.org)

## Definições

  - Um módulo Python é simplesmente um arquivo fonte Python, que pode expor classes, funções e variáveis globais.

  - Quando importado de outro arquivo de origem Python, o nome do arquivo é tratado como um namespace.

  - Um pacote Python é simplesmente um diretório de módulo(s) Python.
  
  ## Estilo de código 
  
  ### Comentários obrigatórios

Comentários Docstrings são obrigatórios. Utilizamos o formato Google docstring nos nossos projetos

A documentação Docstrings está disponível em [http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html](http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html)

Os tópicos mais importantes são: * A classe/métodos devem ser comentados com triplo " assim que forem declarados. 
  - Exemplo:
  
```python
def add_binary(a, b):
    """
    Returns the sum of two decimal numbers in binary digits.

            Agrs:
                    a (int): A decimal integer
                    b (int): Another decimal integer

            Returns:
                    binary_sum (str): Binary string of the sum of a and b
    """
    binary_sum = bin(a+b)[2:]
    return binary_sum


print(add_binary.__doc__)
```


## Nomes de Pacotes e Módulos

Os módulos devem ter nomes curtos em letras minúsculas. Os sublinhados podem ser usados no nome do módulo se melhorar a legibilidade.

Os pacotes Python também devem ter nomes curtos em letras minúsculas, embora o uso de sublinhados seja desencorajado.

Quando um módulo de extensão escrito em C ou C++ tem um módulo Python que o acompanha que fornece uma interface de nível superior (por exemplo, mais orientada a objetos), o módulo C/C++ tem um sublinhado principal (por exemplo, _socket).

##Nomes de classe

Os nomes de classe normalmente devem usar a convenção CapWords.

A convenção de nomenclatura para funções pode ser usada em casos em que a interface é documentada e usada principalmente como um callable.

Observe que há uma convenção separada para nomes internos: a maioria dos nomes internos são palavras únicas (ou duas palavras juntas), com a convenção CapWords usada apenas para nomes de exceção e constantes internas.

## Nomes de funções

Os nomes das funções devem estar em minúsculas, com palavras separadas por _ conforme necessário para melhorar a legibilidade.

mixedCase é permitido apenas em contextos em que esse já é o estilo predominante (por exemplo, threading.py), para manter a compatibilidade com versões anteriores.

## Argumentos de função e método

Sempre use self para o primeiro argumento para métodos de instância.

Se o nome de um argumento de função colidir com uma palavra-chave reservada, geralmente é melhor anexar um único sublinhado à direita em vez de usar uma abreviação ou corrupção de ortografia. Assim class_ é melhor que classs. (Talvez seja melhor evitar tais confrontos usando um sinônimo.)

## Constantes

As constantes geralmente são definidas em um nível de módulo e escritas em letras maiúsculas com sublinhados separando as palavras. Os exemplos incluem MAX_OVERFLOW e TOTAL.
