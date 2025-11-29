# practica4POO
Objetio de practica 
implementar una red de sensores fisicos conectados a una ESP32, programada en MicroPhyton implementando 
*clases y onjetos
*clases base a clases especificas 
*atributos protegidos y propiedades 
*lectura de sensores 
*mostrar los resultados en la terminal


Para esta practica utilizamos un sensor de efecto hall, fotoresistor LDR, un sensor de temperatura, un potenciometro de 10K y un sensor de flamas

En este código tenemos una clase base donde tenemos un sensor genérico y las propiedades de encapsulamiento, tenemos otra clase llamada DigitalSensor que viene de herencia de BaseSensor y encapsula la lógica

El encapsulamiento evita modificar valores internos desde fuera 
Controla el acceso a atributos mediante propiedades 

El polimorfismo se ve cuando se usa sensor. read() y sensor.as_text()
// cada sensor tiene su propia version de as_text()

Toda la aplicacion esta contenida en 
  class SensorNetworkApp:
    def_setup_sensors(self):
    def run(self):
con esto se puede agregar mas sensores, quitar sensores, cambiar pines y modificar la logica sin alterar el resto del codigo 

para mostrar en la terinal se usa la funicon principal que imprime los valores " print(sensoras_text()), donde en la terminar se va mostrando un motiroreo en tiempo real 

No hay variables globales, esto quiere, decir que todas que todas las variables estan dentro de clases y nada esta declarado fuera de funciones/clases, excepto main()
