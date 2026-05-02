from colorama import init, Fore, Style

# Inicia o colorama
init(autoreset=True)

# Lista com os níveis do reservatório
niveis = [
    "Muito baixo (crítico)",
    "Baixo",
    "Médio",
    "Alto",
    "Muito alto (alerta)"
]

# Função para definir a cor
def mostrar_nivel(nivel):
    if nivel == 1:
        cor = Fore.RED
    elif nivel == 2:
        cor = Fore.YELLOW
    elif nivel == 3:
        cor = Fore.GREEN
    elif nivel == 4:
        cor = Fore.CYAN
    elif nivel == 5:
        cor = Fore.BLUE
    else:
        print("Nível inválido!")
        return

    print(cor + f"Nível {nivel}: {niveis[nivel - 1]}" + Style.RESET_ALL)

# Simulação dos níveis
for i in range(1, 6):
    mostrar_nivel(i)
