# temperatura
def convertir(valor, origen, destino):
    # Primero pasamos todo a Celsius
    if origen == "F":
        c = (valor - 32) * 5 / 9
    elif origen == "K":
        c = valor - 273.15
    else:
        c = valor

    # Luego de Celsius al destino
    if destino == "F":
        return c * 9 / 5 + 32
    elif destino == "K":
        return c + 273.15
    return c


valor = float(input("Temperatura: "))
origen = input("Unidad de origen (C/F/K): ").upper()
destino = input("Unidad de destino (C/F/K): ").upper()

resultado = convertir(valor, origen, destino)
print(f"{valor}°{origen} = {resultado:.2f}°{destino}")
