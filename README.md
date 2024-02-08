# Arreglo


class MatrizCalificaciones:
    def __init__(self, num_alumnos, num_materias):
        self.num_alumnos = num_alumnos
        self.num_materias = num_materias
        self.matriz = []
        self.nombres_materias = []
        self.nombres_alumnos = []

    def asignar_nombres_materias(self):
        for i in range(self.num_materias):
            nombre_materia = input(f"Ingrese el nombre de la materia {i + 1}: ")
            self.nombres_materias.append(nombre_materia)

    def asignar_nombres_alumnos(self):
        for i in range(self.num_alumnos):
            nombre_alumno = input(f"Ingrese el nombre del alumno {i + 1}: ")
            self.nombres_alumnos.append(nombre_alumno)

    def crear_matriz(self):
        for i in range(self.num_alumnos):
            fila = []
            for j in range(self.num_materias):
                calificacion = float(input(f"Ingrese la calificación de {self.nombres_alumnos[i]} en {self.nombres_materias[j]}: "))
                fila.append(calificacion)
            self.matriz.append(fila)

    def mostrar_matriz(self):
       
        print("\nAlumno:", self.nombres_alumnos)

        
        for i, fila in enumerate(self.matriz):
            print(f"Materia {self.nombres_materias[i]}: {fila}")


num_materias = 5
num_alumnos = 5


matriz_calificaciones = MatrizCalificaciones(num_alumnos, num_materias)


matriz_calificaciones.asignar_nombres_materias()
matriz_calificaciones.asignar_nombres_alumnos()

matriz_calificaciones.crear_matriz()
matriz_calificaciones.mostrar_matriz()
