#Solicitar al usuario cuántos datos ingresará
n = int(input("¿Cuántos días de ventas deseas analizar? "))
ventas = []

# Ingresar cada valor de venta
for i in range(n):
    valor = float(input(f"Ingresa las ventas del día {i+1}: "))
    ventas.append(valor)

# Cálculos básicos
if ventas:  # Solo si se ingresaron valores
    total = sum(ventas)
    promedio = total / len(ventas)
    maximo = max(ventas)
    minimo = min(ventas)

    print("\nResumen estadístico:")
    print(f"Total de ventas: {total}")
    print(f"Promedio diario: {promedio:.2f}")
    print(f"Venta máxima: {maximo}")
    print(f"Venta mínima: {minimo}")
else:
    print("No se ingresaron datos.")