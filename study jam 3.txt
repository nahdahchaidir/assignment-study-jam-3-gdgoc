import random

def playgame():
    choices = ["Batu", "Gunting", "Kertas"]
    nyawa_player = 3
    nyawa_bot = 3

    while nyawa_player > 0 and nyawa_bot > 0:
        botChoices = random.choice(choices)
        playerChoices = input("Masukkan pilihan anda : ")

        print("Kamu memilih : ", playerChoices)
        print("Bot memilih : ", botChoices)

        if botChoices == playerChoices: 
            print("Hasilnya seri")
            print(f"sisa nyawa kamu {nyawa_player}")
            print(f"sisa nyawa bot {nyawa_bot}")

        elif (botChoices == "Batu" and playerChoices == "Gunting") or (botChoices == "Gunting" and playerChoices == "Kertas") or (botChoices == "Kertas" and playerChoices == "Batu"): 
            print("kamu kalah!")
            nyawa_player -= 1
            print(f"sisa nyawa kamu {nyawa_player}")
            print(f"sisa nyawa bot {nyawa_bot}")

        else:
            print("Kamu menang!")
            nyawa_bot -= 1
            print(f"sisa nyawa kamu {nyawa_player}")
            print(f"sisa nyawa bot {nyawa_bot}")

    if nyawa_player > 0:
        print("\ncongratulation! kamu memenangkan permainan")
    else:
        print("\nkamu kalah! bot memenangkan permainan")

playgame()