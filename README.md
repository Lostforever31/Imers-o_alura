# -*- coding: utf-8 -*-
"""imersão python.ipynb

Automatically generated by Colab.

Original file is located at
    https://colab.research.google.com/drive/1iqFd-5QJnD3Q32RxCtY5lLG8wBdiQa_P
"""

# importando as bibliotecas para usar no código
import requests
import random

#criando as variaveis de acordo com o que fazem ou são
url = "https://raw.githubusercontent.com/guilhermeonrails/api-imersao-ia/main/words.json"

#faço a requisição e armazeno em uma variavel chamada resposta
resposta = requests.get(url)

#transforma a resposta em JSON
data = resposta.json()

#exibe as informações
print(data)

# vendo como acessar cada informação da variavel "data", sempre começando em 0
data[0]

# criei uma variavel, chamada "valor_secreto" que armazena uma tecnologia aleatoria da lista
valor_secreto = random.choice(data)

# variavel para armazenar apenas a palavra
palavra_secreta = valor_secreto ['palavra']

# variavel para imprimir apenas a dica
dica = valor_secreto['dica']

# mostrou na tela quantas letras a palvra secreta possui e a dica
# o 'f' é capaz de juntar palavras e variaveis
print(f'a palavra secreta tem {len(palavra_secreta)} letras -> {dica}')
# receber o palpite da pessoa
chute = input(f'a palavra secreta tem {len(palavra_secreta)} letras -> {dica}')

# faz a comparação do chute com a palavra
if chute == palavra_secreta:
  print('acertou')
else:
  print('errou')

import requests
import random

url = "https://raw.githubusercontent.com/guilhermeonrails/api-imersao-ia/main/words.json"
resposta = requests.get(url)
data = resposta.json()


data[0]

valor_secreto = random.choice(data)

palavra_secreta = valor_secreto ['palavra']
dica = valor_secreto['dica']
print(f'a palavra secreta tem {len(palavra_secreta)} letras -> {dica}')
chute = input('Qual sua resposta?')
if chute == palavra_secreta:
  print('Acertou, parabéns')
else:
  print(f'Errou, a palavra correta era {palavra_secreta} ')
