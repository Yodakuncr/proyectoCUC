# proyectoCUC
prueba personal
Este proyecto lo hice en 2011, cuando lleve Python en el CUC, sin embargo, deje de estudiar durante muchos años, y aunque tenia terminado el proyecto, no lo logro encontrar

#entrada:debe de leer numeros
#salida: debe de imprimir por pantalla un dia de la semana
#comentario: Este programa le indicara al usario que dia de la semana inicia el mes que el usuario elija del a�o que desee
#restricciones: solo puede introducir numeros enteros positivos


def zeller():

    print("El siguiente programa le indicara que dia de la semana inicia el mes del a�o que ustede desee")


#Lectura de datos

    annee =int(input('introduzca el ano: '))#ano a saber
    mois= int(input('introduzca el numero del mes que desea averiguar, ejemplo, si es enero, ponga 1, febrero 2, etc:  '))#numero del mes
    mois2=mois #variable reservada para consideracion de mes de febrero
    annee2 = annee #variable reservada para consideracion de ano bisiesto
    if mois <=2:
        annee = annee-1
        mois =  mois+12
    print    

#asignaciones de datos y variables

    centuria = annee/100
    annee_centuria=annee % 100  #ano de la centuria
    jour=1                      #valor constante en el programa
    valor_1= mois+1             #sumando 1
    valor_2= valor_1 * 26       #sumando 2
    valor_3= valor_2 / 10       #sumando 3
    var_bis= annee_centuria / 4 #sumando 4
    century_four = centuria / 4 #sumando 5
    century5 = 5 * centuria     #sumando 6

#suma de todos los sumandos

    diad = jour + valor_3 + annee_centuria + var_bis + century_four + century5
    diad = diad % 7

    #declaracion de inicio de semana

    if diad == 0:
        print("El mes inicia en sabado")
    else:
        if diad == 1:
            print ("El mes inicia en domingo")
        else:
            if diad == 2:
                print ("El mes inicia en lunes")
            else:
                if diad == 3:
                    print ("El mes inicia en martes")
                else:
                    if diad == 4:
                        print("El mes inicia en miercoles")
                    else:
                        if diad == 5:
                            print ("El mes inicia en jueves")
                        else:
                            print ("El mes inicia en viernes")
    #print 
    print(f"El calendario, para el mes {mois2} del año {annee2} es:")
    encabezado = [["D  L  M  M  J  V  S"],[ 0, 0, 0, 0, 0, 0, 0],[ 0, 0, 0, 0, 0, 0, 0],[ 0, 0, 0, 0, 0, 0, 0],[ 0, 0, 0, 0, 0, 0, 0],[ 0, 0, 0, 0, 0, 0, 0]]
    print
    print (encabezado[0])
    print (encabezado[1])
    print (encabezado[2])
    print (encabezado[3])
    print (encabezado[4])
    print (encabezado[5])

    print
    print
    
    #variantes a considerar

    #cambio en el calendario de juliano a gregoriano

    if annee == 1582 and mois == 10:
        print ("cambio de calendario juliano a gregoriano, se suprimen 10 diaz")
            
            
            #suprimir de la tabla los nunmeros del 5 al 14

    #segunda variante
        
    #ano bisiesto
            
 
    if annee2 % 4 == 0 and annee2 % 100>0 or annee2 % 400==0:
        condicional=1
    else:
        condicional=0
        
    print (condicional) #comprobacion momentanea de si se cumple o no el año bisiesto y su resultado
    print
    
    if condicional == 1:
        print ("el año", annee2, "es bisiesto")
    else:
        print("el a�o", annee2, "no es bisiesto")



    #[["D  L  M  M  J  V  S"],
    # [ 0, 1, 2, 3, 4, 5, 6] posiciones reales en la matriz
    # [ 1, 2, 3, 4, 5, 6, 0] posiciones del algoritmo
    #comando
    #if diad==0:
        #diad=diad+6
    #else:
        #diad=diade-1
    
    

def imprime():
    matriz = [[0]*7]
    for num in range(1,32,1):
        print(num)
