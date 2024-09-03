---
layout: ../../layouts/MarkdownLayout.astro
title: Ejercicios de Visual Basic
Description:
author: FuSoraS
---
## Ejercicio 1
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
```vs
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
                Next

                If IsNumeric(numero) Then
                    MsgBox("Contraseña: " & password)
                    opcion = InputBox("Ingrese 1 volver a ingresar
Ingrese 2 para salir")
                Else
                    MsgBox("Ingrese minimo un numero")
                End If
            Else
                MsgBox("La contraseña tiene que tener minimo 8 caracteres")
            End If
        End While
```
## Ejercicio 8 (no terminado)
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