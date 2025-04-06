import gc

class Objeto:
    def __init__(self, nombre):
        self.nombre = nombre
    def __del__(self):
        print(f"Objeto {self.nombre} eliminado de memoria.")

a = Objeto("A")
b = a
del a
gc.collect()  # Se fuerza la recolección de basura
