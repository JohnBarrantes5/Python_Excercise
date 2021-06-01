
#Entradas: 1000000 0 0              -   2355255 2 1
#Salidas: 1000000.0 890000.0        -   2594747.2 2309325.0
# Varialbles = salario_base(171), horas extras, bonificacion, horas_ extras
#plan_obligatorio_salud = 0.05 / caja_compesacion = 0.01 / 

salario_base, horas_extras, bonificacion = input().split()

salario_base = float(salario_base)
horas_extras = int(horas_extras)
bonificacion = int (bonificacion)

valor_hora  = salario_base/171

Valor_tot_hora = (valor_hora*0.017)*horas_extras
bonificacion = (salario_base* bonificacion* 0.088) 

salario_total = salario_base + Valor_tot_hora + bonificacion

plan_obligatorio_salud = salario_total*0.05
caja_compesacion = salario_total*0.01
aporte_pension = salario_base*0.05 

salario_final = ((salario_total)-(plan_obligatorio_salud + aporte_pension + caja_compesacion))

print(round(salario_total,1), round(salario_final,1))
