Algoritmo "Acordando"

Var
    horas_de_sono: inteiro
    alarmes_disparados: inteiro
    acordado: logico
Inicio
    // Inicia as variáveis
    horas_de_sono <- 0
    alarmes_disparados <- 0
    acordado <- falso

    // Verifica quantas horas de sono
    escreva("Quantas horas você dormiu? ")
    leia(horas_de_sono)

    // Verifica se dormiu o suficiente
    se horas_de_sono < 8 entao
        escreva("Você precisa dormir mais! Definindo alarme para 1 hora depois...\n")
        alarmes_disparados <- alarmes_disparados + 1
    senao
        escreva("Bom dia! Você dormiu bem.\n")
    fimse

    // Desperta o jovem
    enquanto acordado = falso faca
        escreva("Alarme tocando! Acorde!\n")
        alarmes_disparados <- alarmes_disparados + 1

        // Pergunta se já acordou
        escreva("Você está acordado? (sim/não): ")
        leia(resposta)
        
        se resposta = "sim" entao
            acordado <- verdadeiro
            escreva("Ótimo! Vamos começar o dia!\n")
        senao
            escreva("Mais 5 minutos...\n")
        fimse
    fimenquanto

    // Exibe quantos alarmes foram disparados
    escreva("Total de alarmes disparados: ", alarmes_disparados, "\n")
FimAlgoritmo
