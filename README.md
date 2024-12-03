# 03/12/2024 - CURSO DE PYTHON FATEC HUAWEI - DAY 1

## Introdução 

## 1.1 A Linguagem Python

Python foi criada no início dos anos 1990 por Guido van Rossum e lançada em 1991. Hoje, é mantida e desenvolvida pela Python Software Foundation, uma organização sem fins lucrativos criada em 2001. Python é uma linguagem simples e intuitiva, mas ao mesmo tempo poderosa e robusta, o que a torna ideal tanto para estudantes quanto para profissionais.

### Principais Características de Python

### Portabilidade
Python e suas bibliotecas padrão estão disponíveis em várias plataformas, como Unix, Linux, Windows e Mac OS. Um programa escrito em Python que utiliza apenas as bibliotecas padrão será executado da mesma maneira em qualquer plataforma.

### Código Livre (Opensource)
Python é escrito em C e é disponibilizado como software livre. Isso permite que programadores desenvolvam e distribuam software sem custos, além de poderem baixar, modificar e utilizar o código, conforme os termos de sua licença.

### Simplicidade com Robustez
A sintaxe de Python é simples, elegante e legível, mas também poderosa. Com um núcleo enxuto e coerente, ela permite o desenvolvimento de grandes projetos, incluindo aplicações orientadas a objetos, sistemas multimídia, e integração com outras linguagens.

### Grande Aplicabilidade
Python pode ser usada em diversas áreas, como:
- Administração de sistemas operacionais
- Big Data e bancos de dados SQL e NoSQL
- Aplicações gráficas e multimídia
- Análise de dados
- Machine Learning e Inteligência Artificial
- Programação web
- Desenvolvimento de software para áreas científicas e específicas, como estatística, engenharia e biologia.

### Versões da Linguagem Python

Python possui duas versões principais: Python 2 e Python 3. Embora compartilhem muitos elementos, Python 3 introduziu mudanças significativas que quebraram a compatibilidade com Python 2. Lançada em 2008, a versão 3 foi inicialmente adotada lentamente devido à grande base de código existente em Python 2. No entanto, após campanhas incentivando a migração, Python 3 tornou-se majoritariamente usada. O suporte a Python 2 foi oficialmente encerrado em 20 de abril de 2020 com o lançamento da última versão, 2.7.18.

Neste material, apenas elementos de Python 3 serão abordados.

## 1.2 Instalação

- https://www.python.org/downloads/

## 1.3 Ambiente de desenvolvimento

![img.png](images/img.png)

![img.png](images/img1.png)

## 1.4 Documentação

- https://docs.python.org/3

## 1.5 Requisitos minimos para rodar python

- Programas escritos em linguagem Python não exigem grandes capacidades computacionais. Um
computador antigo com processador i3 das primeiras gerações com 2 Gbytes de memória consegue rodar
programas Python

## 1.6 Elementos Fundamentais de Python

![img.png](images/img2.png)

## 1.7 Comentários

![img.png](images/img3.png)

## Teste Capitulo 1

# 04/12/2024 - CURSO DE PYTHON FATEC HUAWEI - DAY 2

# Capitulo 2: Classes e Objetos - Parte I

## 2.1 Armazenamento de dados

![img.png](images/img4.png)

## 2.2 Classes e objetos em python

![img.png](images/img5.png)

## 2.3 Objetos de classe simples

![img.png](images/img6.png)

## 2.4 Comandos e atributos

![img.png](images/img7.png)

# Capitulo 2: Classes e Objetos - Parte II

## 2.5 Id dos objetos Python Parte I

- Em Python, o ID de um objeto é um número inteiro único que identifica cada objeto durante sua existência no programa. Esse identificador, ou "ID", pode ser obtido usando a função id(objeto), onde objeto é a variável ou o objeto do qual queremos o ID.

![img.png](images/img8.png)

- objetos com os mesmos valores e mesma classe serão apontados para o mesmo id.
- Objetos com o mesmo valor podem ou não compartilhar o mesmo ID, dependendo do tipo de objeto e da implementação.
- Para tipos imutáveis (como inteiros, strings pequenas e tuplas), Python pode reutilizar o mesmo espaço na memória para otimizar o desempenho e economizar recursos. Por exemplo:

```python

a = 10
b = 10
print(id(a) == id(b))  # True, pois Python reaproveita o mesmo valor imutável.
```

- Para objetos mutáveis (como listas ou dicionários), cada instância terá um ID diferente, mesmo que os valores sejam idênticos.


## 2.6 Id dos objetos Python Parte II

![img.png](images/img9.png)

## 2.7 Modelo de dados de Python

# Modelo de Dados em Python

O modelo de dados de Python define como os dados são representados e manipulados na linguagem. Ele descreve como as operações, a memória e os tipos de dados são tratados internamente. Abaixo estão os principais aspectos do modelo de dados de Python.

## 1. **Objetos e Identidade**
   - Em Python, *tudo é um objeto*, incluindo tipos básicos como inteiros e strings.
   - Cada objeto possui um **ID** único, que identifica sua localização na memória durante sua existência. O ID pode ser obtido com `id(objeto)`.

## 2. **Tipos e Classes**
   - Python possui tipos embutidos como `int`, `float`, `str`, `list`, `dict`, e muitos mais.
   - Classes permitem a criação de tipos personalizados. Cada tipo é uma instância da classe `type`.
   - Os tipos são divididos em **imutáveis** (não podem ser alterados, como `int` e `tuple`) e **mutáveis** (podem ser alterados, como `list` e `dict`).

## 3. **Atributos e Métodos**
   - Objetos possuem **atributos** e **métodos** (funções que operam sobre os objetos).
   - É possível acessar os atributos e métodos com a sintaxe `objeto.atributo`.

## 4. **Protocolo de Sequência e Mapeamento**
   - Python permite a manipulação de coleções como **sequências** (`list`, `tuple`, `str`) e **mapeamentos** (`dict`).
   - Sequências suportam operações como indexação (`obj[i]`), fatiamento (`obj[start:stop]`) e iteração.

## 5. **Protocolo de Iteração**
   - O protocolo de iteração permite percorrer coleções de dados. Todo objeto que implementa o método `__iter__()` é um **iterável**.
   - Iteradores são obtidos com a função `iter(objeto)` e iteram com o método `__next__()`.

## 6. **Sobrecarga de Operadores**
   - Python permite a sobrecarga de operadores como `+`, `-`, `*`, etc., usando métodos especiais (`__add__`, `__sub__`, etc.) definidos nas classes.
   - Isso permite personalizar como objetos interagem com esses operadores.

## 7. **Gerenciamento de Memória e Coleta de Lixo**
   - Python gerencia a memória automaticamente usando **contagem de referências** e um **coletor de lixo** para liberar objetos que não estão mais em uso.

## 8. **Protocolo de Contexto**
   - O protocolo de contexto é usado para gerenciar recursos, como arquivos, de forma segura, usando a sintaxe `with`. A classe deve implementar os métodos `__enter__()` e `__exit__()`.

O modelo de dados em Python é flexível e extensível, permitindo manipulação avançada de objetos e controle detalhado sobre o comportamento dos dados.

- No exemplo acima, uma Pessoa tem um Endereco, formando um relacionamento que organiza os dados de forma estruturada.

![img.png](images/img10.png)

![img.png](images/img11.png)

## 2.8 Operadores aritmeticos

#### Operadores Aritméticos em Python

| Operador        | Símbolo | Exemplo          | Descrição                                     |
|-----------------|---------|------------------|-----------------------------------------------|
| Adição          | `+`     | `a + b`          | Soma os valores de `a` e `b`.                 |
| Subtração       | `-`     | `a - b`          | Subtrai o valor de `b` do valor de `a`.       |
| Multiplicação   | `*`     | `a * b`          | Multiplica `a` por `b`.                       |
| Divisão         | `/`     | `a / b`          | Divide `a` por `b` e retorna um `float`.      |
| Divisão Inteira | `//`    | `a // b`         | Divide `a` por `b` e retorna a parte inteira. |
| Módulo          | `%`     | `a % b`          | Retorna o resto da divisão de `a` por `b`.    |
| Exponenciação   | `**`    | `a ** b`         | Eleva `a` à potência `b`.                     |
| Negação         | `-`     | `-a`             | Inverte o sinal de `a`.                       |

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.3333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
print(-a)      # -10

```









