class Libro:
    def __init__(self, titulo, autor, genero, puntuacion):
        self.titulo = titulo
        self.autor = autor
        self.genero = genero
        self.puntuacion = puntuacion

lista_libros = [
    Libro("Cien años de soledad", "Gabriel García Márquez", "Ficción", 4.5),
    Libro("1984", "George Orwell", "Ciencia Ficción", 4.3),
    Libro("El Hobbit", "J.R.R. Tolkien", "Fantasía", 4.7),
    Libro("Orgullo y Prejuicio", "Jane Austen", "Romance", 4.2),
    Libro("Crimen y Castigo", "Fiódor Dostoyevski", "Clásico", 4.4),
    Libro("Los Juegos del Hambre", "Suzanne Collins", "Juvenil", 4.1),
    Libro("Don Quijote de la Mancha", "Miguel de Cervantes", "Clásico", 4.6),
    Libro("Harry Potter y la Piedra Filosofal", "J.K. Rowling", "Fantasía", 4.8),
    Libro("Los Pilares de la Tierra", "Ken Follett", "Histórica", 4.4),
    Libro("Cazadores de Sombras: Ciudad de Hueso", "Cassandra Clare", "Fantasía", 4.0)
]

def agregar_libro():
    titulo = input("Ingrese el título del libro: ")
    autor = input("Ingrese el autor del libro: ")
    genero = input("Ingrese el género del libro: ")
    puntuacion = float(input("Ingrese la puntuación del libro: "))
    libro = Libro(titulo, autor, genero, puntuacion)
    lista_libros.append(libro)
    print("Libro agregado con éxito.")

def buscar_por_genero():
    genero_buscado = input("Ingrese el género que desea buscar: ")
    libros_en_genero = [libro.titulo for libro in lista_libros if libro.genero == genero_buscado]
    if libros_en_genero:
        print(f"Libros en el género '{genero_buscado}':")
        for titulo in libros_en_genero:
            print("- " + titulo)
    else:
        print(f"No se encontraron libros en el género '{genero_buscado}'.")

def recomendar_libro():
    genero_interes = input("Ingrese su género de interés: ")
    mejores_libros = [libro for libro in lista_libros if libro.genero == genero_interes]
    if mejores_libros:
        mejor_libro = max(mejores_libros, key=lambda libro: libro.puntuacion)
        print(f"Le recomendamos el libro '{mejor_libro.titulo}' con una puntuación de {mejor_libro.puntuacion}.")
    else:
        print(f"No se encontraron libros en el género '{genero_interes}'.")

while True:
    print("\n¿Qué acción desea realizar?")
    print("1. Agregar Libro")
    print("2. Buscar Libros por Género")
    print("3. Recomendar Libro")
    print("4. Salir")
    opcion = input("Ingrese el número de la opción: ")

    if opcion == "1":
        agregar_libro()
    elif opcion == "2":
        buscar_por_genero()
    elif opcion == "3":
        recomendar_libro()
    elif opcion == "4":
        print("¡Hasta luego!")
        break
    else:
        print("Opción inválida. Por favor, ingrese un número válido.")
