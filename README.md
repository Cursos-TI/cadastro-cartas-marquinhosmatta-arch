
# Definindo as cartas (cidades) como dicionários
sergipe = {
    "nome": "Aracaju - Sergipe",
    "pib": 30000,          # PIB em milhões (exemplo fictício)
    "area_territorial": 181, # km² (exemplo fictício)
    "ponto_turistico": "Orla de Atalaia"
}

alagoas = {
    "nome": "Maceió - Alagoas",
    "pib": 45000,          # PIB em milhões (exemplo fictício)
    "area_territorial": 510, # km² (exemplo fictício)
    "ponto_turistico": "Praia do Gunga"
}

# Função para comparar atributos
def comparar_atributo(carta1, carta2, atributo):
    print(f"\nComparando {atributo} entre {carta1['nome']} e {carta2['nome']}:")
    print(f"{carta1['nome']}: {carta1[atributo]}")
    print(f"{carta2['nome']}: {carta2[atributo]}")
    
    if carta1[atributo] > carta2[atributo]:
        print(f"Vencedor: {carta1['nome']}")
    elif carta1[atributo] < carta2[atributo]:
        print(f"Vencedor: {carta2['nome']}")
    else:
        print("Empate!")

# Menu simples para o jogador escolher o atributo
print("Jogo Super Trunfo: Desafio entre Sergipe e Alagoas")
print("Escolha o atributo para comparar:")
print("1 - PIB")
print("2 - Área Territorial")
print("3 - Ponto Turístico (não comparável)")

escolha = input("Digite o número do atributo: ")

if escolha == "1":
    comparar_atributo(sergipe, alagoas, "pib")
elif escolha == "2":
    comparar_atributo(sergipe, alagoas, "area_territorial")
elif escolha == "3":
    print(f"\nPontos turísticos:")
    print(f"{sergipe['nome']}: {sergipe['ponto_turistico']}")
    print(f"{alagoas['nome']}: {alagoas['ponto_turistico']}")
    print("Esse atributo não é numérico e não pode ser comparado diretamente.")
else:
    print("Opção inválida.")

