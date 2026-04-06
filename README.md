# Fundamentos-Algoritmicos-TallerFinal
resultado <- 5 + 3 * 2 ^ 2 - (10 MOD 3)
	resultado <- 5 + 3 * 2 ^ 2 - 1
	resultado <- 5 + 3 * 4 - 1
	resultado <- 5 + 12- 1
	resultado <- 16

  <img width="1366" height="768" alt="ejercicio1" src="https://github.com/user-attachments/assets/be19d336-c7f4-4c83-867b-281e3a2754bc" />
---
resultado_logico <- No(var_A O var_B) Y (var_C Y No(var_B))
	resultado_logico <- No Verdadero Y (var_C Y verdadero)
	resultado_logico <- Falso Y Verdadero
	resultado_logico <- Falso 

	<img width="1366" height="768" alt="ejercicio2" src="https://github.com/user-attachments/assets/4e40b2f5-a7de-4b66-8b41-a9485bc2d634" />

---
Algoritmo SelectorCandidatos
	definir estatura_ingresada como real 
	definir peso_ingresado como real 
	
	Escribir "ingrese su estatura"
    Leer estatura_ingresada
	Escribir "ingrese su peso"
	Leer peso_ingresado
    
	Si estatura_ingresada > 1.70 O peso_ingresado < 80 Entonces
        Escribir "Validación del perfil: Correcta."
         Sino
        Escribir "Validación del perfil: Fallida." 
	finsi
	
FinAlgoritmo<img width="1366" height="768" alt="ejercicio3" src="https://github.com/user-attachments/assets/1e8dfdfc-d3e5-405f-9fb9-d085755e50b6" />

---
Algoritmo LiquidacionNominaTechSolutions
    
    Definir nombre_operador Como Caracter
    Definir horas_ejecutadas, horas_normales, horas_extras Como Real
    Definir tarifa_normal, tarifa_extra, subtotal_a Como Real
    Definir salud, pension, fondo_solidario, total_deducciones Como Real
    Definir salario_neto Como Real
    
   
    tarifa_normal <- 35000  
    limite_horas <- 160
    
    Escribir "SISTEMA DE LIQUIDACIÓN DE NÓMINA TECHSOLUTIONS CORE"
    Escribir "Ingrese el nombre del operador:"
    Leer nombre_operador
    Escribir "Ingrese las horas ejecutadas en el mes:"
    Leer horas_ejecutadas
    
   
    Si horas_ejecutadas <= limite_horas Entonces
        horas_normales <- horas_ejecutadas
        horas_extras <- 0
    Sino
        horas_normales <- limite_horas
        horas_extras <- horas_ejecutadas - limite_horas
    FinSi
    
  
    subtotal_a <- (horas_normales * tarifa_normal) + (horas_extras * tarifa_normal * 1.35)
    
    
    Si subtotal_a < 1500000 Entonces
        salud <- subtotal_a * 0.04
        pension <- 0
        fondo_solidario <- 0
    Sino
        Si subtotal_a >= 1500000 Y subtotal_a < 3000000 Entonces
            salud <- subtotal_a * 0.06
            pension <- subtotal_a * 0.02
            fondo_solidario <- 0
        Sino
            Si subtotal_a >= 3000000 Entonces
                salud <- subtotal_a * 0.08
                pension <- subtotal_a * 0.04
                fondo_solidario <- subtotal_a * 0.01
            FinSi
        FinSi
    FinSi
    

    total_deducciones <- salud + pension + fondo_solidario
    salario_neto <- subtotal_a - total_deducciones
    
 
    
    
   
    
    Escribir "DESPRENDIBLE DE PAGO - TECHSOLUTIONS"
    
    Escribir "Operador: ", nombre_operador
   
    Escribir "DETALLE DE HORAS:"
    Escribir "  Horas normales (hasta 160): ", horas_normales, " horas"
    Escribir "  Horas extras (35% recargo): ", horas_extras, " horas"
   
    Escribir "CÁLCULO DE INGRESOS:"
    Escribir "  Tarifa normal: $", tarifa_normal, " COP/hora"
    Escribir "  Valor horas normales: $", horas_normales * tarifa_normal
    Escribir "  Valor horas extras: $", horas_extras * tarifa_normal * 1.35
  
    Escribir "SUBTOTAL A (Salario Bruto): $", subtotal_a
    
    Escribir "DEDUCCIONES LEGALES:"
    Escribir "  Salud (según tramo): $", salud
    Escribir "  Pensión (según tramo): $", pension
    Escribir "  Fondo Solidario (1% si aplica): $", fondo_solidario
  
    Escribir "TOTAL DE RETENCIONES TRIBUTARIAS: $", total_deducciones
 
    Escribir "SALARIO NETO VALIDADO: $", salario_neto
  
    Escribir " Documento válido como soporte de pago "
    

	FinAlgoritmo
<img width="1366" height="768" alt="ejercicio4" src="https://github.com/user-attachments/assets/5979ab66-42fc-49e9-8dbd-5079644b9159" />


---
Algoritmo CajeroCripto
    
    Definir saldo_disponible Como Real
    Definir opcion, monto_retiro, monto_btc Como Real
    Definir btc_adquirido Como Real
    Definir valor_btc_referencia Como Real
    
   
    saldo_disponible <- 5000.00  
    valor_btc_referencia <- 60000.00  
    
    Repetir
       
        Limpiar Pantalla
        
        Escribir " TERMINAL DE CONEXIÓN CRIPTO "
        Escribir "[1] Consultar estado de cuenta corriente"
        Escribir "[2] Retiro estricto de fondos USD"
        Escribir "[3] Ejecutar Orden de Compra de Bitcoin (BTC)"
        Escribir "[4] Finalizar sesión"
       Escribir Sin Saltar "Seleccione una opción (1-4): "
        Leer opcion
        
        
        Segun opcion Hacer
            Caso 1:
                Escribir ">> ESTADO DE CUENTA CORRIENTE <<"
                Escribir "Saldo disponible actual: $", saldo_disponible, " USD"
                Esperar 20 Segundos
                
            Caso 2:
              Escribir ribir "RETIRO DE FONDOS USD"
                Escribir Sin Saltar "Ingrese el monto a retirar (USD): "
                Leer monto_retiro
                
                Si monto_retiro <= 0 Entonces
                    Escribir "ERROR: El monto debe ser mayor a cero"
                Sino
                    Si monto_retiro > saldo_disponible Entonces
                        Escribir "EXCEPCIÓN: Flujo de fondos insuficientes en la bóveda actual"
                        Escribir "Saldo disponible: $", saldo_disponible, " USD | Solicitado: $", monto_retiro, " USD"
                    Sino
                        saldo_disponible <- saldo_disponible - monto_retiro
                        Escribir ">> TRANSACCIÓN EXITOSA <<"
                        Escribir "Retiro realizado: $", monto_retiro, " USD"
                        Escribir "Nuevo saldo disponible: $", saldo_disponible, " USD"
                    FinSi
                FinSi
               
                Esperar 20 Segundos
                
            Caso 3:
                
                Escribir " ORDEN DE COMPRA DE BITCOIN (BTC) "
                Escribir "Precio de referencia BTC: $", valor_btc_referencia, " USD/BTC"
                Escribir "Saldo disponible: $", saldo_disponible, " USD"
                Escribir Sin Saltar "Ingrese monto en USD a invertir en BTC: "
                Leer monto_btc
                
                Si monto_btc <= 0 Entonces
                    Escribir "ERROR: El monto debe ser mayor a cero"
                Sino
                    Si monto_btc > saldo_disponible Entonces
                        Escribir "EXCEPCIÓN: Fondos insuficientes para la orden de compra"
                        Escribir "Saldo disponible: $", saldo_disponible, " USD | Solicitado: $", monto_btc, " USD"
                    Sino
                        
                        btc_adquirido <- monto_btc / valor_btc_referencia
                        saldo_disponible <- saldo_disponible - monto_btc
                        
                        Escribir " ORDEN EJECUTADA EXITOSAMENTE "
                        Escribir "Inversión: $", monto_btc, " USD"
                        Escribir "BTC adquiridos: ", btc_adquirido, " BTC"
                        Escribir "Nuevo saldo en USD: $", saldo_disponible, " USD"
                    FinSi
                FinSi
                
                Esperar 20 Segundos
                
            Caso 4:
               
                Escribir " PROTOCOLO DE CIERRE ACTIVADO "
                Escribir "Gracias por usar la Terminal de Conexión Cripto"
                Escribir "Sesión finalizada exitosamente"
                
                Esperar 20 Segundos
                
            De Otro Modo:
                
                Escribir "ERROR: Protocolo Inexistente"
                Escribir "La opción ", opcion, " no está disponible en el menú"
                Escribir "Seleccione una opción válida (1-4)"
                
                Esperar 20 Segundos
        FinSegun
        
    Hasta Que opcion = 4
    

FinAlgoritmo

<img width="1366" height="768" alt="ejercicio5" src="https://github.com/user-attachments/assets/73910e95-a9f4-430e-a485-0330b30e04e2" />
