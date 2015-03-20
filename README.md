# Design-de-software
atividades 


#pedra papel (....) spock_ 
#pessoas essenciais para essa atividade foram Gabriel patrocinio e Rodrigo entre outros da sala C eng.


import random
from colorama import Fore
print(Fore.CYAN + "\n Bem vindo ao Pedra/Papel/Tesoura/Lagarto/Spock....\nVocê irá jogar contra mim, mas saiba que não será nada fácil! Neste jogo você não conseguirá advinhar o que irei escolher...")
itens=["pedra","papel","tesoura","lagarto","spock"]
player_pontos=0
computer_pontos=0
while player_pontos < 3 and computer_pontos < 3 :
    print(Fore.MAGENTA + "Escolha a sua arma : Pedra,Papel,Tesoura,Lagarto ou Spock! \n(para deixar o jogo digite sair)" + Fore.RESET)
    escolha=input().lower()
    computer_escolha=random.choice(itens)
    if player_pontos>0 and computer_pontos != 0:
        player_pontos=0
        computer_pontos=0
    if escolha == "sair" or escolha == "Sair" or escolha == "SAIR":
        print(Fore.BLUE + "Você saiu do jogo...")
        print(Fore.RESET)
        break
    if escolha==computer_escolha :
        print(Fore.BLUE + "minha escolha foi:"+computer_escolha)
        print(Fore.RESET)
        print(Fore.GREEN + "Empatamos!")
        print(Fore.RESET)
        player_pontos=0
        computer_pontos=0
        print("Agora o jogo está %d a %d" %(player_pontos,computer_pontos))
    if escolha!="papel" and escolha!="pedra" and escolha!="spock" and escolha!="lagarto" and escolha!="tesoura" and escolha!="Tesoura" and escolha!="Papel" and escolha!="Pedra" and escolha!="Spock" and escolha!="Lagarto" and escolha!="PEDRA" and escolha!="TESOURA"and escolha!="PAPEL"and escolha!="LAGARTO"and escolha!="SPOCK" :
        print(Fore.RED + " Por favor faça uma escolha vâlida")
        print(Fore.RESET)
    elif escolha== "pedra" and computer_escolha=="tesoura" or escolha=="pedra" and computer_escolha=="lagarto" :
        print(Fore.BLUE +"A minha escolha foi:"+computer_escolha)
        print("Você ganhou desta vez!")
        print(Fore.RESET)
        player_pontos=player_pontos+1
        print(Fore.GREEN + "O jogo está %d a %d " %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha=="pedra" and computer_escolha=="spock" or escolha=="Pedra" and computer_escolha=="spock" or escolha=="PEDRA" and computer_escolha=="spock" or escolha=="pedra" and computer_escolha=="papel" or escolha=="PEDRA" and computer_escolha=="papel" or escolha=="Pedra" and computer_escolha=="papel":
        print(Fore.BLUE + "A minha escolha foi:" + computer_escolha)
        print(Fore.RESET)
        print("Eu ganhei desta vez seu bobo!")
        computer_pontos=computer_pontos+1
        print(Fore.GREEN +"O jogo está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha=="papel" and computer_escolha=="pedra" or escolha=="Papel"and computer_escolha=="pedra" or escolha=="PAPEL"and computer_escolha=="pedra" or escolha=="papel"and computer_escolha=="spock" or escolha=="Papel"and computer_escolha=="spock" or escolha=="PAPEL"and computer_escolha=="spock":
        print(Fore.BLUE + "A minha escolha foi:"+ computer_escolha)
        print("Você ganhou.... que saco...")
        print(Fore.RESET)
        player_pontos=player_pontos+1
        print(Fore.GREEN + "O jogo está %d a %d"  %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha == "papel" and computer_escolha=="tesoura" or escolha== "papel" and computer_escolha== "lagarto":
        print(Fore.BLUE + "Eu escolhi:"+ computer_escolha)
        print(Fore.RESET)
        print("GANHEI! Quero ver você ganhar de mim!")
        computer_pontos=computer_pontos+1
        print(Fore.GREEN + "O placar está %d a %d"  %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha == "tesoura" and computer_escolha=="pedra"  or escolha=="tesoura"and computer_escolha=="spock":
        print(Fore.BLUE + "joguei" + computer_escolha)
        print("HAHA!")
        print(Fore.RESET)
        print("Ta muito fácil ganhar...")
        computer_pontos==computer_pontos+1
        print(Fore.GREEN + "O placar está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha=="tesoura" and computer_escolha=="lagarto"  or escolha=="tesoura"and computer_escolha=="papel":
        print(Fore.BLUE + "Escolhi:"+ computer_escolha)
        print("Mandei mal...")
        print(Fore.RESET)
        print("Eu sinto a força em você")
        player_pontos=player_pontos+1
        print(Fore.GREEN + "O placar está %d a %d" %(player_pontos,computer_pontos)) 
        print(Fore.RESET)
    elif escolha=="lagarto" and computer_escolha=="tesoura" or escolha=="lagarto" and computer_escolha=="pedra":
        print(Fore.BLUE + "Estou apenas esquentando... minha escolha foi:"+computer_escolha)
        print(Fore.RESET)
        print("Você não é páreo para mim!")
        computer_pontos=computer_pontos+1
        print(Fore.GREEN + "O jogo está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha== "lagarto" and computer_escolha=="spock" or escolha== "lagarto" and computer_escolha=="papel":
        print(Fore.BLUE + "Opa! Você teve sorte! Eu joguei:"+ computer_escolha)
        print(Fore.RESET)
        print("Mais uma vez!")
        player_pontos=player_pontos+1         
        print(Fore.GREEN + "O placar está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha=="spock" and computer_escolha== "papel" or escolha== "spock" and computer_escolha=="lagarto": 
        print(Fore.BLUE + "Minha escolha foi:"+ computer_escolha)
        print(Fore.RESET)        
        print("Estou indo bem...")
        computer_pontos=computer_pontos+1
        print(Fore.GREEN + "O jogo está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    elif escolha=="spock" and computer_escolha== "pedra" or escolha== "spock" and computer_escolha=="tesoura":
        print(Fore.BLUE + "BOOM! Eu escolhi :"+computer_escolha)
        print(Fore.RESET)
        print("Droga! Você não é tão ruim...")
        player_pontos=player_pontos+1
        print(Fore.GREEN + "O placar está %d a %d" %(player_pontos,computer_pontos))
        print(Fore.RESET)
    again=input("Deseja continuar jogando? Sou persistente...").lower()        
    if player_pontos>=3:
        print(Fore.MAGENTA + "Você ganhou.... A força está com você")
        print(Fore.RESET)
        while again=="sim":
              player_pontos=0
    elif again=="não" or again=="nao":
         break
    if again!="sim" and again!="não" and again!="nao":
        print("Por favor , digite sim ou não.")
        print(again)
    if computer_pontos>=3:
        print(Fore.CYAN +"EU ganhei, você está fraco... melhor praticar...")
        print(Fore.RESET)
        print(again)
        while again=="sim":
            computer_pontos=0
    elif again=="não" or again== "nao":
        break
    if again!="sim" and again!="não" and again!="nao":
        print("Por favor , digite sim ou não.")
        print(again)
