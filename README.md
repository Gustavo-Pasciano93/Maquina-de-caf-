# O código é basicamente uma função que simula uma máquina de café


MENU = {
    "espresso": {
        "ingredients": {
            "water": 50,
            "coffee": 18,
        },
        "cost": 1.5,
    },
    "latte": {
        "ingredients": {
            "water": 200,
            "milk": 150,
            "coffee": 24,
        },
        "cost": 2.5,
    },
    "cappuccino": {
        "ingredients": {
            "water": 250,
            "milk": 100,
            "coffee": 24,
        },
        "cost": 3.0,
    }
}



#1° Passo : Criar uma função com todos os requisitos para a maquina de café funcionar

#2° passo: colocar as medidas de água, leite e café da maquina

#3° passo: usar o dicionario de forma que a função reconheça as medidas e preço de cada produto

#4° passo: Tenha certeza que no if vai deduzir da maquina os componentes

#5° passo: criar o report dos ingredientes

# 6° passo, fazer um loop que vai deduzindo o componentes que acaba quando não tem ingredientes suficientes ou quando o consumidor não quiser mais

# 123, boooraaaaaaa



def Maquina_de_café():
    água = 300
    leite = 200
    café = 100
    Fim_do_pedido = False
    
    while not Fim_do_pedido:
        latte = MENU["latte"]
        água_latte = MENU["latte"]["ingredients"]["water"]
        leite_latte = MENU["latte"]["ingredients"]["milk"]
        café_latte = MENU["latte"]["ingredients"]["coffee"]
        
        espresso = MENU["espresso"]
        água_espresso = MENU["espresso"]["ingredients"]["water"]
        café_espresso = MENU["espresso"]["ingredients"]["coffee"]
        
        capuccinno = MENU["cappuccino"]
        água_capuccinno = MENU["cappuccino"]["ingredients"]["water"]
        leite_capuccinno = MENU["cappuccino"]["ingredients"]["milk"]
        café_capuccinno = MENU["cappuccino"]["ingredients"]["coffee"]
        
        print("*********************************")
        print("Bora um cafézinho meu consagrado :)")
        print("******************************")
        
        resposta = input("Qual será o seu pedido hoje? latte, espresso ou capuccino? ")
        
        if resposta == "latte":
            resposta_latte= input("O latte custa R$10,00, insira seu cartão:sim ou não ")
            if resposta_latte == "sim" and água > água_latte and leite > leite_latte and café > café_latte :
                água = água - água_latte
                leite = leite - leite_latte
                café = café - café_latte
                print("3, 2, 1 ...... Saiu o seu Latte, aproveite!")
            else:
                print("Não será possível concluir o seu pedido, estamos com falta de ingredientes")
                Fim_do_pedido = True
        elif resposta == "espresso":
            resposta_espresso= input("O espresso custa R$7,00, insira seu cartão:sim ou não ")
            if resposta_espresso == "sim" and água > água_espresso  and café > café_espresso :
                água = água - água_espresso
                café = café - café_espresso
                print("3, 2, 1 ...... Saiu o seu Espresso, aproveite!")
            else:
                print("Não será possível concluir o seu pedido, estamos com falta de ingredientes")
                Fim_do_pedido = True
        elif resposta == "capuccinno":
            resposta_capuccinno= input("O capuccinno custa R$15,00, insira seu cartão:sim ou não ")
            if resposta_capuccinno == "sim" and água > água_capuccinno and leite > leite_capuccinno and café > café_capuccinno :
                água = água - água_capuccinno
                leite = leite - leite_capuccinno
                café = café - café_capuccinno
                print("3, 2, 1 ...... Saiu o seu Capuccinno, aproveite!")
            else:
                print("Não será possível concluir o seu pedido, estamos com falta de ingredientes")
                Fim_do_pedido = True
        elif resposta == "status":
            print(f"água: {água} ml")
            print(f"leite: {leite} ml")
            print(f"café:{café} ml")
        else:
            print(" Fim do pedido")
            
