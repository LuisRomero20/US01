# US01
Feature: US01 - Como usuario, quiero vincular mi tarjeta de crédito a mi perfil para poder pagar de manera rápida y segura.
Scenario: S01 - Transferencias online
TA01
Given que los pagos son de manera online, el apoderado hace uso de una banca móvil
When el usuario se inscribe y paga por un curso debe registrarse
Y el usuario digita sus nombres y apellidos completos en el campo [Nombres y Apellidos]
Y el usuario digita su DNI en el campo [DNI]
Y el usuario vincula su tarjeta de crédito o de débito en el campo [Ingrese su número de tarjeta]
Y el usuario presiona el botón vincular tarjeta
Y la tarjeta de crétido o débito del usuario es anexada a su cuenta de la aplicación
Then el usuario dispone de una cuenta vinculada a la aplicación

Examples:
    | Nombres y Apellidos                | DNI      | Ingrese su número de tarjeta |
    | Carlos Eduardo Manrique Villanueva | 42561168 | 4352640680006482             |
    | Mia Fernanda Caviar Fernandez      | 30257618 | 4889665482762257             |
    | Maria Luisa Díaz Cabrera           | 18152433 | 4505222333423319             |
    | Pedro Enrique Díaz Lopez           | 76441218 | 4167784581281243             |
    | Carlos Eduardo Manrique Villanueva | 48451170 | 4082430092589334             |


Scenario: S02 - Devolución de dinero de una transferencia
TA02
Given que el usuario decide no continuar o comenzar la unidad de estudios
Y el usuario aún no ha realizado una actividad o tomado alguna clase
When el usuario hace retiro del monto invertido, debe presionar la opción: "Realizar retiro"
Y el usuario digita sus nombres y apellidos completos en el campo [Nombres y Apellidos]
Y el usuario digita su DNI en el campo [DNI]
Y el usuario digita su tarjeta de crédito o de débito en el campo [Ingrese su número de tarjeta]
Y el usuario digita la cantidad a retirar en el campo [Monto]
Then el usuario recibe el monto retirado en un intervalo de 24 horas

Examples:
    | Nombres y Apellidos              | DNI      | Monto   | Ingrese su número de tarjeta |
    | Carla Giovana Rojas Dávila       | 11224278 | S/. 120 | 4196875127569862             |
    | Luis Fernando Villanueva Quispe  | 15895533 | S/. 50  | 5149658099716637             |
    | Diana Elisa Guevara Rodriguez    | 76442025 | S/. 100 | 4592744568060353             |
    | José Eduardo Mantilla Fernandez  | 15237869 | S/. 50  | 4188923632014733             |
    | Melanny Denisse Calderón Ramírez | 32405518 | S/. 55  | 5596604644636779             |

