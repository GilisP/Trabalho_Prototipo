# Trabalho_Prototipo
jogo dos nnumeros

import random as Random

acertou = 0
pnts = 200
nump = Random.randint(0,100)
print ("***********************************************************")
print ("O Genio te deu 200 pontos use com sabedoria pois cada desejo são 10 deles")
print ("tente acertar o numero do genio")
print ("***********************************************************")
while(acertou == 0 and pnts > 0):
  try:
    print ("***********************************************************")
    numj = float(input("Qual é o numero do gênio? "))
    pnts = pnts - 10
    print ("***********************************************************")

    if(numj > nump):
      print ("***********************************************************")
      numero = Random.randint(1,3)
      if(numero == 1):
        print("Acho que alguem voou ALTO demais")
      if(numero == 2):
        print("Alto demais boy")
      if(numero == 3):
        print("Chutou alto demais")
      print ("***********************************************************")
      

    if(numj < nump):
      numero = Random.randint(1,3)
      
      print ("***********************************************************")
      if(numero == 1):
        print("Errou pois foi baixo")
      if(numero == 2):
        print("baixo demais boy")
      if(numero == 3):
        print("HO HOU alguem chutou BAIXO")
      print ("***********************************************************")
      
      

    if(numj == nump):
      acertou = 1

  except ValueError:
    print ("O Genio não aceita seu chute")
if (acertou == 1):
  print ("***********************************************************")
  print ("Parabens você ganhou você fez ",pnts," pontos!!!")
  print ("***********************************************************")
if (acertou == 0):
  print ("***********************************************************")
  print ("Seus pontos acabaram sem mais desejos")
  print ("***********************************************************")
