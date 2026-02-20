class Nodo:
    def __init__(self, dato):
        self.dato = dato
        self.siguiente = None


class Lista_circular:
    def __init__(self):
        self.primero = None
        self.ultimo = None

    def vacia(self):
        return self.primero is None

    def agregarinicio(self, dato):
        if self.vacia():
            self.primero = self.ultimo = Nodo(dato)
            self.primero.siguiente = self.primero
        else:
            aux = Nodo(dato)
            aux.siguiente = self.primero
            self.primero = aux
            self.ultimo.siguiente = self.primero

    def agregarfinal(self, dato):
        if self.vacia():
            self.primero = self.ultimo = Nodo(dato)
            self.primero.siguiente = self.primero
        else:
            aux = Nodo(dato)
            aux.siguiente = self.primero
            self.ultimo.siguiente = aux
            self.ultimo = aux

    def recorrer(self):
        if self.vacia():
            print("Lista vacía")
            return
        aux = self.primero
        while True:
            print(aux.dato)
            aux = aux.siguiente
            if aux == self.primero:
                break

    def removerinicio(self):
        if self.vacia():
            print("Lista vacía")
        elif self.primero == self.ultimo:
            self.primero = self.ultimo = None
        else:
            self.primero = self.primero.siguiente
            self.ultimo.siguiente = self.primero

    def removerfinal(self):
        if self.vacia():
            print("Lista vacía")
        elif self.primero == self.ultimo:
            self.primero = self.ultimo = None
        else:
            aux = self.primero
            while aux.siguiente != self.ultimo:
                aux = aux.siguiente
            aux.siguiente = self.primero
            self.ultimo = aux


if __name__ == "__main__":
    opcion = 0
    lista = Lista_circular()
    while opcion != 6:
        print("--- Listas Circulares ---\n 1. Agregar último\n 2. Eliminar último\n 3. Agregar inicio\n 4. Eliminar inicio\n 5. Mostrar\n 6. Salir")
        opcion = int(input("Ingrese su opción: "))

        if opcion == 1:
            dato = input("Ingresa un número: ")
            lista.agregarfinal(dato)
        elif opcion == 2:
            lista.removerfinal()
        elif opcion == 3:
            dato = input("Ingresa un número: ")
            lista.agregarinicio(dato)
        elif opcion == 4:
            lista.removerinicio()
        elif opcion == 5:
            lista.recorrer()
        elif opcion == 6:
            print("Adiós")
        else:
            print("Ingresaste una opción errónea, vuelve a intentarlo.")
