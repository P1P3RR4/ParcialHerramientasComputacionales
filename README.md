# ParcialHerramientasComputacionales

# solucion al problema 1
# Santiago Fernandez Fernandez
# Codigo 8967803
# Juan Felipe Muñoz Torijano
# Codigo 8967146
inventario = [["papitas", 0,2000],["gaseosa",  1,2500], [ "helado",2,2500],  ["buñuelo", 3,1000] , ["pandebono", 4,700], ["empanadas", 4,800], ["sandwich", 5,1500],["jugo",6,1000]]

def tienda():
    precioinicial = 0
    preciofinal = 0
    producto = None
    print("Este es el inventario: papitas : Codigo 0,2000, gaseosa :  Codigo 1,2500, helado :  Codigo 2,2500, buñuelo :\n"
          "Codigo 3,1000 , pandebono:  Codigo 4,700, empanadas:  Codigo 4,800, \n"
          "sandwich:  Codigo 5,1500 ,jugo: Codigo 6,1000")
    rol = input("Cual es su rol?: ").upper()
    cedula = input("Cual es su cedula?: ")
    codigop = int(input("Digite el codigo del producto que desea: "))
    canitdadp = int(input("Cantidad de productos que desea: "))
    for i in range(len(inventario)):
        if inventario[i][1] == codigop:
            precioinicial = inventario[i][2] * canitdadp
            producto = inventario[i][1]
    if rol == "ESTUDIANTE":
        preciofinal = precioinicial * 0.5
    elif rol == "PROFESOR":
        preciofinal = precioinicial * 0.8
    elif rol != "ESTUDIANTE" or "PROFESOR":
        print("Escriba bien su rol para poder realizar el proceso correctamente")
    print(f"El {rol} con cedula {cedula}, debe pagar {preciofinal} por el producto {producto}")
tienda()

# ¿Qué tipos de errores se presentaron o se pueden presentar con su implementación al problema?

# El error más común que se presenció, fue a la hora de escribir el rol del usuario, ya que pueden escribirlo de forma incorrecta a como se pide.

# ¿Qué estrategias podría usar para la solucionar estos errores?

# Para solucionarlo implementamos en el código el .upper esto lo que hace es hacer que lo ingresado se transforme en mayúsculas, razón por la cual, sirve para contrarrestar el error anteriormente mencionado.
