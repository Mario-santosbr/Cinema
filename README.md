#PREÇO DOS PRODUTOS
preco_ingresso = 30.00
preco_refrigerante = 10.00
preco_pipoca = 20.00

#QUANTIDADE DOS PRODUTOS
quantidade_ingressos = int(input("Quantos ingressos você deseja?"))
quantidade_refrigerantes = int(input("Quantos refrigerantes você deseja?"))
quantidade_pipocas = int(input("Quantas pipocas você deseja?"))

#CALCULAR O SUBTOTAL
subtotal_ingressos = preco_ingresso * quantidade_ingressos
subtotal_refrigerantes = preco_refrigerante * quantidade_refrigerantes
subtotal_pipocas = preco_pipoca * quantidade_pipocas
total = subtotal_ingressos + subtotal_refrigerantes + subtotal_pipocas

#MEIA ENTRADA
meias_entradas = int(input("Quantos ingressos são meia-entrada?"))
desconto_meia = meias_entradas * (preco_ingresso / 2)
total = total - desconto_meia
# PROMOÇÃO COMBO
combo = quantidade_pipocas >= 1 and quantidade_refrigerantes >= 1
if combo:
    total = total - 5.00

#TAXA DE SERVIÇO
taxa = total * 0.05
total_com_taxa = total + taxa

#DIVIDIR ENTRE AS PESSOAS
pessoas = int(input("Entre quantas pessoas o valor será dividido?"))
valor_por_pessoa = total_com_taxa / pessoas

#ALERTA DE ORÇAMENTO
passeio_caro = valor_por_pessoa > 40.00

#RECIBO
print("/n============== RECIBO ===============")
print(f"Ingressos: R${subtotal_ingressos:.2f}")
print(f"Refrigerantes: R${subtotal_refrigerantes:.2f}")
print(f"Pipocas: R${subtotal_pipocas:.2f}")
print(f"desconto_meia: R${desconto_meia:.2f}")
print(f"taxa: R${taxa:.2f}")
print(f"total final: R${total_com_taxa:.2f}")
print(f"pessoas: {pessoas}")
print(f"valor por pessoa: R${valor_por_pessoa:.2f}")
print(f"combo ativado? {combo}")
print(f"Passeio  saiu caro: {passeio_caro}")
print("/n============= KKK ================")
