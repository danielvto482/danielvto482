- 👋 Hi, I’m @danielvto482
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
danielvto482/danielvto482 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
while player['health'] > 0:
    current_room = random.choice(rooms)
    print(f"\nVocê entrou em {current_room}.")
    
    if current_room == "Sala de Tesouro":
        treasure = random.choice(treasures)
        print(f"Você encontrou um {treasure}!")
        player['inventory'].append(treasure)
    elif current_room == "Sala do Guardião":
        if not combat("Guardião da Masmorra"):
            print("Você foi derrotado. Fim de jogo!")
            break
    elif current_room == "Poço Sem Fundo":
        print("Você caiu no poço sem fundo. Fim de jogo!")
        break
    else:
        print("O corredor está vazio, mas sombrio...")

    show_status()
    if input("Deseja continuar explorando? (S/N) ").lower() == 'n':
        print("Você decidiu sair da masmorra. Fim de jogo!")
        break
