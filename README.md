# Diagrama-de-flujon
# Función para simular la solución del problema de ronquidos
def solucionar_ronquidos():
    roncando = True
    intentos = 0
    max_intentos = 3

    while roncando and intentos < max_intentos:
        intentos += 1
        print(f"Intento {intentos}:")

        # Opción 1: Aplicar tapones para oídos
        usar_tapones = input("¿Aplicar tapones para oídos? (s/n): ").lower()
        if usar_tapones == 's':
            funciono = input("¿Funcionó? (s/n): ").lower()
            if funciono == 's':
                roncando = False
                print("Problema solucionado con tapones para oídos.")
                break
        else:
            print("No se aplicaron los tapones para oídos.")

        # Opción 2: Usar marcadores para mostrar una nota
        usar_marcadores = input("¿Escribir una nota con marcadores? (s/n): ").lower()
        if usar_marcadores == 's':
            funciono = input("¿El ronquido se detuvo? (s/n): ").lower()
            if funciono == 's':
                roncando = False
                print("Problema solucionado con la nota.")
                break
        else:
            print("No se utilizó el marcador.")

        # Opción 3: Mover la silla suavemente
        mover_silla = input("¿Mover la silla suavemente? (s/n): ").lower()
        if mover_silla == 's':
            funciono = input("¿El ronquido se detuvo? (s/n): ").lower()
            if funciono == 's':
                roncando = False
                print("Problema solucionado moviendo la silla.")
                break
        else:
            print("No se movió la silla.")

        if roncando:
            print("El ronquido continúa. Intentando otra vez...\n")

    if roncando:
        print("No se pudo solucionar el problema después de varios intentos.")
    else:
        print("Problema de ronquidos resuelto.")

# Ejecutar la función
solucionar_ronquidos()
