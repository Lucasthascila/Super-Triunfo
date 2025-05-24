super_trunfo.py

import random

class Carta: def init(self, nome, velocidade, peso, potencia): self.nome = nome self.atributos = { 'velocidade': velocidade, 'peso': peso, 'potencia': potencia }

def _str_(self):
    return f"{self.nome} - Velocidade: {self.atributos['velocidade']} | Peso: {self.atributos['peso']} | Potência: {self.atributos['potencia']}"

def comparar(cart1, cart2, atributo): val1 = cart1.atributos[atributo] val2 = cart2.atributos[atributo]

print(f"\nComparando atributo '{atributo}':")
print(f"{cart1.nome}: {val1}")
print(f"{cart2.nome}: {val2}")

if val1 > val2:
    print(f"\n{cart1.nome} vence!")
elif val1 < val2:
    print(f"\n{cart2.nome} vence!")
else:
    print("\nEmpate!")

Exemplo de cartas

cartas = [ Carta("Carro A", 220, 1300, 180), Carta("Carro B", 200, 1400, 170), Carta("Carro C", 240, 1250, 190), Carta("Carro D", 210, 1350, 175) ]

Simula jogo simples entre 2 cartas aleatórias

carta1 = random.choice(cartas) carta2 = random.choice([c for c in cartas if c != carta1])

print("Carta 1:") print(carta1)

print("\nCarta 2:") print(carta2)

Atributo escolhido para comparação

atributo_escolhido = input("\nEscolha o atributo para comparar (velocidade, peso, potencia): ").lower() comparar(carta1, carta2, atributo_escolhido)
