# forma_de_pago

print(" ****** BIENVENIDO AL BURGER KING ********")
print("Ingrese los datos para la factura electrónica")


#la condicion int se coloca antes del input para datos enteros.
nombre_cliente=input("Ingrese su nombre: ")
numero_cedula=int(input("Ingrese su número de cédula: "))
correo=input("Ingrese su correo: ")
num_hamburguesas=int(input("Ingrese el número de hamburguesas a adquirir: "))



print("Escoga el tipo de hamburguesa que desea: ")
print("1) sencilla")
print("2) doble")
print("3) triple")
tipo_hamburguesa=int(input("Ingrese la opción: "))


if tipo_hamburguesa == 1 or tipo_hamburguesa == 2 or tipo_hamburguesa ==3:
    if tipo_hamburguesa == 1:
        precio = num_hamburguesas * 1.50
    elif tipo_hamburguesa == 2:
        precio = num_hamburguesas * 2.50
    elif tipo_hamburguesa == 3:
        precio = num_hamburguesas * 3.25


    print("Ingrese su forma de pago.")
    print("1) Tajeta de crédito.")
    print("2) Efectivo.")
    tipo_pago = int(input("Ingrese la opción: "))
    if tipo_pago == 1:
        recargo = precio * 0.05
        total = precio + recargo
        print(f"Genial, {nombre_cliente} el precio final a es ${round(total,2)}") #f es usada para poner varables en las cadenas de texto sin f no seria posible.
        print(f"La factura se enviará a su correo {correo}")
    elif tipo_pago == 2:
        print(f"Genial, {nombre_cliente} el precio final a es ${round(precio,2)}")
        print(f"La factura se enviará a su correo {correo}")
    else:
        
        print("No existe ese tipo de pago")
        
else:
    
    print("Este tipo de hamburguesa no existe")
    


print("********** MUCHAS GRACIAS POR ELEGIRNOS **********")
print("**************** VUELVA PRONTO *******************")
