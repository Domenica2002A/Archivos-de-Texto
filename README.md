# Escritura de archivo de texto

# Abrimos (o creamos si no existe) el archivo en modo escritura ('w')
with open("my_notes.txt", "w") as file:
    # Escribimos tres líneas de notas personales
    file.write("Hoy aprendí cómo trabajar con archivos en Python.\n")
    file.write("Usar 'with open' es una buena práctica porque cierra el archivo automáticamente.\n")
    file.write("También estoy subiendo mis tareas a GitHub para llevar un buen registro.\n")

# Lectura de archivo de texto

# Abrimos el archivo en modo lectura ('r')
with open("my_notes.txt", "r") as file:
    # Leemos el archivo línea por línea
    linea = file.readline()
    while linea:
        # Mostramos cada línea leída en la consola
        print(linea.strip())  # .strip() elimina el salto de línea al final
        linea = file.readline()

# No es necesario cerrar manualmente el archivo gracias a 'with',
# ya que se cierra automáticamente al salir del bloque.
