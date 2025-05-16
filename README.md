# Lista-de-Ferramentas
Exercicio em Python

def lista_ferramentas(ferr):
boole = False
while(boole == False):
print('1-Ver ferramentas \n2-Substituir ferramenta \n3-Adicionar ferramenta \n4-Verificar itens para reposição \n0-Sair')
num = int(input())

if(num == 0):
boole = True
elif(num == 1):
count = 0
for i in ferr:
index = count
ferramenta = i[0]
quantidade = i[1]
print('Index %s || %s || quantidade: %s' % (index,ferramenta,quantidade))
count += 1

elif(num == 2):
print('Qual ferramenta quer substituir?')
sub1 = input()
print('Confirma a troca por esta ferramenta? ' + sub1)
sub2 = input()
print('Qual a quantidade deste produto em estoque?')
quantidade = int(input())
novo_item = [sub2, quantidade]
item_existente = False
i = 0
for x in ferr:
if(x[0] == sub1):
ferr[i] = novo_item
item_existente = True
i += 1
if(item_existente == False):
print('Não há nenhumitem com o nome %s registrado' % sub1)

elif(num == 3):
print('Qual ferramenta quer adicionar?')
add = input()
print('Qual a quantidade deste produto em estoque?')
quantidade = int(input())
novo_item = [add, quantidade]

elif(num == 4):
print('Escolha a quantidade de unidades em baixa:')
num = int(input())
i = 0
for x in ferr:
if(x[1] <= num):
index = i
ferramenta = x[0]
quantidade = x[1]
print('Index %s || %s || quantidade: %s' % (index,ferramenta,quantidade))
i += 1

else:
print('Invalido! Favor tentar outra vez')


ferr = ['bronzina', 'biela', 'pistão', 'camisa', 'cilindro', 'valvula de admissão', 'bucha de biela', 'retentor', 'rolamento', 'platinado','condensador', 'valvula termostatica', 'abraçadeira hellermann', 'correia de polia', 'broca de aço rapido', 'broca conica', 'broca de vidia', 'broca de centro', 'tesoura', 'chave inglesa', 'chave de grifo', 'chave turquesa', 'chave combinada', 'chave fixa', 'chave estrela', 'lima mursa', 'lima bastarda', 'chave de fenda', 'chave de borne', 'alicate universal', 'alicade de bico', 'alicate de corte diagonal', 'alicate de bico curvo', 'alicate de corte', 'alicate de pressão', 'alicate descasca-fio', 'macho', 'tarracha', 'desandador', 'goniometro', 'rebolo', 'junta de cabeçote', 'alargador de furo', 'relogio comparador', 'polia', 'arruela', 'porca', 'cárter do motor', 'aspirador', 'turbo', 'virabrequim', 'aneis de pistão', 'cabeçote', 'bloco do motor', 'vela de ignição', 'comando variavel de valvulas', 'bicos injetores', 'coletor de admissão', 'coletor de escape', 'sistema de injeção de combustivel', 'sistema de ignição', 'bomba de combustivel','planitado', 'condensador', 'filtro de ar', 'filtro de óleo', 'corrente de distribuição', 'radiador', 'bomba d'água', 'sistema de lubrificação', 'catalisador', 'silenciador', 'alternador', 'morsa', 'sargento', 'chicote', 'lixadeira', 'furadeira', 'parafusadeira', 'ferramenta de furo para torno', 'ferramenta de desbaste para torno', 'ferramenta de rosca para torno', 'recartilha', 'ferramenta de raio para torno', 'bucha conica', 'paquimetro universal', 'paquimetro de profundidade', 'micrometro de profundidade', 'paquimetro digital', 'micrometro universal', 'micrometro digital', 'calços com degraus', 'tipo numerico', 'tipo alfabetico', 'bico de injetora', 'disco de corte', 'disco de desbaste', 'fresa helicoidal quatro facas', 'talha', 'esquadro de centro', 'esquadro de luz', 'cabeçote de fresa', 'mancal de fresa', 'eixo arvore', 'abraçadeira comum'.]
print(ferr)
quantidadde_ferramentas = lista_ferramentas(ferr)
