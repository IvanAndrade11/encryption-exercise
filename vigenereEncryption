def main():
    msj = input("|----BIENVENIDO----|\n \n1.Por favor, escribe el mensaje: ")
    action = input("\nEscriba el número de la opción: \n1. Cifrar \n2. Descifrar\n")
    key = input("\nIngrese la llave: ")

    response = process_message(key, msj, action) if action == '1' or action == '2' else f"\nOpción {action} no válida"
        
    print(f"\nResultado de la operación -->> {response}")

def process_message(key,msj,action):
    MOD27 = ("ABCDEFGHIJKLMNÑOPQRSTUVWXYZ")
    response = []
    index = 0
    key = key.upper()

    for char in msj:
        n = MOD27.find(char.upper())
        if n != -1:
            n = n + MOD27.find(key[index]) if action =='1' else n - MOD27.find(key[index])
            n %= len(MOD27)
            response.append(MOD27[n]) if char.isupper() else response.append(MOD27[n].lower())
            index += 1
            if index==len(key):
                index=0
        else:
            response.append(char)
    return ('').join(response)

if __name__ == '__main__':
    main()
