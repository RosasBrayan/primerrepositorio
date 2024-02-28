Algoritmo GenerarBoletaPago

    // Definir variables de entrada
    Definir nombre, CI, cargo, haberBasico, mesActual, anosAntiguedad, tipoEmpresa como cadena
    Definir bonoAlimentacion, bonoTransporte, valesConsumo, salarioDominical como real
    Definir totalIngresos, AFP, totalEgresos, liquidoPagable como real

    // Solicitar información de entrada al usuario
    Escribir "Ingrese el nombre:"
    Leer nombre
    Escribir "Ingrese la cédula de identidad:"
    Leer CI
    Escribir "Ingrese el cargo:"
    Leer cargo
    Escribir "Ingrese el haber básico:"
    Leer haberBasico
    Escribir "Ingrese el mes actual:"
    Leer mesActual
    Escribir "Ingrese los años de antigüedad:"
    Leer anosAntiguedad
    Escribir "Ingrese el tipo de empresa:"
    Leer tipoEmpresa

    // Calcular bonos y vales
    bonoAlimentacion <- 60
    bonoTransporte <- 157.5
    valesConsumo <- 88

    // Calcular salario dominical
    Escribir "¿Cuántos domingos trabajó?"
    Leer domingosTrabajados
    Si domingosTrabajados > 0 Entonces
        salarioDominical <- (domingosTrabajados * (haberBasico / 30) * 2)
    Sino
        salarioDominical <- 0
    FinSi

    // Calcular total de ingresos
    totalIngresos <- haberBasico + bonoAlimentacion + bonoTransporte + valesConsumo + salarioDominical

    // Calcular AFP
    AFP <- totalIngresos * 0.1271

    // Calcular total de egresos
    totalEgresos <- AFP

    // Calcular líquido pagable
    liquidoPagable <- totalIngresos - totalEgresos

    // Mostrar boleta de pago
    Escribir "-----------BOLETA DE PAGO -------------"
    Escribir "Nombre:", nombre
    Escribir "CI:", CI
    Escribir "Cargo:", cargo
    Escribir "Tipo de Empresa:", tipoEmpresa
    Escribir "Haber Básico:", haberBasico, "Bs"
    Escribir "Bono de Alimentación:", bonoAlimentacion, "Bs"
    Escribir "Bono de Transporte:", bonoTransporte, "Bs"
    Escribir "Vales de Consumo:", valesConsumo, "Bs"
    Escribir "Salario Dominical:", salarioDominical, "Bs"
    Escribir "Total de Ingresos:", totalIngresos, "Bs"
    Escribir "AFP:", AFP, "Bs"
    Escribir "Total de Egresos:", totalEgresos, "Bs"
    Escribir "Líquido Pagable:", liquidoPagable, "Bs"

FinAlgoritmo
