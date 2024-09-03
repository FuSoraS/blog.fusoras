---
layout: ../../layouts/MarkdownLayout.astro
title: Ejercicios de Visual Basic
Description:
author: FuSoraS
---
## Ejercicio 1
### Requerimientos: Ejercicio 1 - Calculadora de promedio:
Escribe un programa que permita al usuario ingresar tres calificaciones, calcule y muestre su promedio.
### Solucion
```vs
        Dim nota1 As Double
        Dim nota2 As Double
        Dim nota3 As Double
        Dim promedio As Double

        nota1 = InputBox("Ingrese su nota 1: ")
        nota2 = InputBox("Ingrese su nota 2: ")
        nota3 = InputBox("Ingrese su nota 3: ")

        promedio = (nota1 + nota2 + nota3) / 3

        MsgBox("Tu promedio es: " & promedio)
```
## Ejercicio 2
### Ejercicio 2 – Conversor de temperatura:
Desarrolla un programa que convierta una temperatura de grados Celsius a grados Fahrenheit o Kelvin. El usuario debe ingresar la temperatura en Celsius.
### Solucion
```vs
        Dim celsius As Double
        Dim k As Double
        Dim f As Double
        Dim opcion As Integer

        celsius = InputBox("Ingrese los grados Celsius: ")
        f = (celsius * 9 / 5 + 32)
        k = celsius + 273.15
        While opcion < 3
            opcion = InputBox("Menu
        1. Fahrenheit
        2. Kelvin
        3. Salir")
        Select Case opcion
            Case 1
                MsgBox("Fahrenheit: " & f)
            Case 2
                    MsgBox(" Kelvin: " & k)
                Case Else

        End Select
        End While
```
## Ejercicio 3
### Ejercicio 3: Desarrolla un programa que determine si un número es par o impar.

```vs
        Dim numero As Integer
        Dim calcular As Integer

        numero = InputBox("Ingrese su numero: ")

        calcular = numero Mod 2

        If calcular = 0 Then
            MsgBox("Es numero par")
        Else
            MsgBox("Es impar")

        End If
```
## Ejercicio 4
### Ejercicio 4 – Calculadora de descuentos: Desarrolla un programa que pregunte al
usuario el precio de un producto y su tipo de cliente (Regular – Premium - VIP)
- ✓ El cliente Regular tiene un 5% de descuento.
- ✓ El cliente Premium tiene un 15% de descuento.
- ✓ El cliente VIP tiene un 30% de descuento.

El programa debe aplicar el descuento según el tipo de cliente y mostrar elprecio final del producto de la siguiente forma:
- Precio original = $XXY
- Descuento = $XX
- Precio Final = $XYX

El programa solo debe finalizar al presionar SALIR
```vs
        'Calculadora de descuento'
        Dim precioPro As Double
        Dim precioProTxt As String
        Dim tipoCliente As Integer
        Dim tipoClienteTxt As String
        Dim descuentoAplicado As Double
        Dim calculo As Double

        precioProTxt = InputBox("Ingrese el precio del producto")
        'Validar si es un numero'
        If IsNumeric(precioProTxt) Then
            precioPro = Convert.ToInt64(precioProTxt)
            While tipoClienteTxt < 4
                tipoClienteTxt = InputBox("Seleccine el tipo de cliente:
        1. Regular
        2. Miembro
        3. Vip
        4. Salir")

                'Validar si es un numero'
                If IsNumeric(tipoClienteTxt) Then
                    tipoCliente = Convert.ToInt64(tipoClienteTxt)
                    Select Case tipoCliente
                        Case 1
                            calculo = precioPro * 0.05
                            descuentoAplicado = precioPro - calculo

                            MsgBox("Eres cliente Regular:
Precio del producto: " & precioPro & " 
Descuento del 5%: " & calculo & "
Precio final: " & descuentoAplicado)
                        Case 2
                            calculo = precioPro * 0.15
                            descuentoAplicado = precioPro - calculo
                            MsgBox("Eres cliente Premium
Precio del producto: " & precioPro & " 
Descuento del 10%: " & calculo & "
Precio final: " & descuentoAplicado)
                        Case 3
                            calculo = precioPro * 0.3
                            descuentoAplicado = precioPro - calculo
                            MsgBox("Eres cliente vip
Precio del producto: " & precioPro & " 
Descuento del 30%: " & calculo & "
Precio final: " & descuentoAplicado)
                        Case 4
                            MsgBox("Saliendo")
                        Case Else
                            MsgBox("No es valido")
                    End Select
                Else
                    MsgBox("Numero no valido")
                End If
            End While
        Else
            MsgBox("No es un numero valido")
        End If
```
## Ejercicio 5
### Ejercicio 5 – Años Bisiestos: Escribe un programa que solicite al usuario ingresar
un año y determine si es bisiesto o no.
Un año bisiesto es aquel que tiene un día adicional, es decir, 366
días en lugar de 365. Esto se debe a la corrección del calendario para
mantenerlo en sincronía con el ciclo de las estaciones. En el
calendario gregoriano, que es el calendario más utilizado en la
actualidad, los años bisiestos siguen una regla:
- ✓ Si un año es divisible por 4, se considera un año bisiesto.
- ✓ Sin embargo, si el año es divisible por 100, debe ser divisible por 400 para ser
considerado bisiesto.
- ✓ Esto significa que la mayoría de los años son comunes y tienen 365 días, pero
aproximadamente cada 4 años, hay un año bisiesto con 366 días. Un ejemplo
de año bisiesto es el año 2020, mientras que el año 2021 es un año común.

```vs
        Dim calculo1 As Integer
        Dim calculo2 As Integer
        Dim calculo3 As Integer
        Dim añoBifiesto As Integer
        Dim validarString As String

        validarString = InputBox("Ingrese su año: ")
        If IsNumeric(validarString) Then
                añoBifiesto = Convert.ToInt64(validarString)
                calculo1 = añoBifiesto Mod 4
                calculo2 = añoBifiesto Mod 100
                calculo3 = añoBifiesto Mod 400

            If calculo3 = 0 Then
                If calculo2 = 0 Then
                    MsgBox("Es año es bifiesto")
                Else
                    MsgBox("No es un año bifiesto")
                End If
            ElseIf calculo2 = 0 Then
                MsgBox("No es un año bifiesto")
            ElseIf calculo1 = 0 Then
                MsgBox("Es un año bifiesto")
            Else
                MsgBox("No es un año bifiesto")
            End If
            Else
                MsgBox("Numero no valido")
            End If
```
## Ejercicio 6
### Ejercicio 6: Desarrolla un programa que solicite al usuario un número y luego
muestre la secuencia de números desde 0 hasta el número ingresado, pero solo
aquellos que son múltiplos de 3.
```vs
        Dim numIngresado As Integer
        Dim multiplo As Integer

        numIngresado = InputBox("Ingrese un numero")
        multiplo = numIngresado \ 3
        For contador As Integer = 0 To numIngresado Step 2
            MsgBox("Numero: " & contador)
            contador += 1
        Next
```
## Ejercicio 7 (no terminado)
### Ejercicio 7 – Validación de Contraseña:
Desarrolla un programa que permita al usuario ingresar una contraseña y verificar
si cumple con los siguientes criterios de seguridad:
- ✓ La contraseña debe tener una longitud mínima de 8 caracteres.
- ✓ La contraseña debe contener al menos una letra (Mayúscula o minúscula).
- ✓ La contraseña debe contener al menos un número.
```vs
Module Module1

    Sub Main()
        Dim password As String
        Dim cPassword As Integer
        Dim numero As Char
        Dim opcion As Integer = 0

        While opcion < 2

            password = InputBox("Ingrese su contraseña: ")
            cPassword = Len(password)

            If cPassword >= 8 Then
                For Each numero In password
                    Char.IsDigit(numero)
                    Char.IsLetter(numero)
                    If IsNumeric(numero) Then
                        If Char.IsUpper(numero) Then
                            If Char.IsLower(numero) Then
                                MsgBox("Contraseña: " & password)
                                opcion = InputBox("Ingrese 1 volver a ingresar
Ingrese 2 para salir")
                            Else
                                MsgBox("Inserte minimamente una letrea en minuscula")
                            End If
                        Else
                            MsgBox("Inserte minimamente una letra en mayuscula")
                        End If

                    Else
                        MsgBox("Ingrese minimo un numero")
                    End If

                Next
            Else
                MsgBox("La contraseña tiene que tener minimo 8 caracteres")
            End If


        End While
    End Sub

End Module
```
## Ejercicio 8 (no terminado)
### Ejercicio 8 – Reservación de hotel
Desarrolla un sistema de reservaciones de hotel donde los usuarios puedan ingresar sus datos,
seleccionar una habitación y calcular el costo total de su estadía. El sistema debe considerar
descuentos, impuestos y validar todas las entradas.
Detalles del sistema:
1. Ingreso de datos del usuario:
▪ Nombre del cliente.
▪ Número de identificación (validar que sea un número de 8 a 10 dígitos).
2. Selección de la cantidad de noches de estadía:
El usuario debe ingresar la cantidad de noches que planea hospedarse. Validar que la 
cantidad de noches sea un número positivo mayor que 0.
3. Selección del tipo de habitación:
▪ Habitación Económica: $50.000 por noche.
▪ Habitación Estándar: $80.000 por noche.
▪ Habitación Suite: $120.000 por noche.
▪ Validar que la opción seleccionada sea una de las tres disponibles.
4. Descuentos:
Si la cantidad de noches es mayor a 5, se aplicará un descuento del 10% sobre el total 
antes de impuestos.
5. Cálculo de impuestos:
Aplicar un impuesto del 15% al costo total (después de aplicar el descuento, si 
corresponde).
6. Salida: Mostrar un resumen de la reservación, incluyendo:
    - Nombre del cliente.
    - Tipo de habitación seleccionada.
    - Número de noches.
    - Costo total antes de impuestos.
    - Descuento aplicado (si corresponde).
    - Impuesto aplicado.
    - Costo total final.

Validaciones:
- ✓ Validar el nombre (debe contener solo letras).
- ✓ Validar el número de identificación (debe ser un número y tener entre 8 - y 10 dígitos).
- ✓ Validar que la cantidad de noches sea un número mayor a 0.
- ✓ Validar que la selección del tipo de habitación sea válida.

El programa finalizar cuando el usuario lo desee. De lo contrario se podrá continuar reservando
habitaciones
```vs
        Dim nombre As String
        Dim id As String
        Dim cId As Integer
        Dim opcion As Integer
        Dim noche As Integer
        Dim descuento As Integer = 10
        Dim descuentoAplicado As Integer
        Dim calculo As Integer
        Dim habitacion As Integer

        nombre = InputBox("Ingrese su nombre: ")
        id = InputBox("Ingrese su Número de identificación:
(rango de 8 a 10) ")
        cId = Len(id)
        If cId >= 8 And cId <= 10 Then
            noche = InputBox("Ingrese la cantidad de noche: ")
            If noche > 0 Then
                opcion = InputBox("Seleccione su habitacion
1. Habitación Económica: $50.000 por noche.
2. Habitación Estándar: $80.000 por noche.
3. Habitación Suite: $120.000 por noche")
                Select Case opcion
                    Case 1
                        If noche > 5 Then
                            habitacion = 50000
                            calculo = (descuento / habitacion)
                            descuentoAplicado = habitacion - calculo
                        End If
                        MsgBox("Habitación Económica: $50.000 por noche
Nombre del cliente: " & nombre &
"Cantidad de noche: " & noche &
"Descuento del 10%: " & descuentoAplicado)
                    Case 2
                        MsgBox("Habitación Estándar: $80.000 por noche.
Nombre del cliente: " & nombre &
"Cantidad de noche: " & noche)
                    Case 3
                        MsgBox("Habitación Suite: $120.000 por noche
Nombre del cliente: " & nombre &
"Cantidad de noche: " & noche)
                    Case Else

                End Select
            Else
                MsgBox("El numero tiene que ser mayor a 0")
            End If
        Else
            MsgBox("La id tiene que estar entre 8 y 10 numeros")
        End If
```