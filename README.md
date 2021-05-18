# Projeto_Hora_a_Hora
Com intenção de melhorar e agilizar o processo de informações, criei este pequeno programa.


programa
{
	inclua biblioteca Calendario
	funcao inicio()
	
	{
		//Todas variáveis para execução.
    inteiro jckpp, jfrp, jrrp, jspp, jccp, jdpp, jckpu, jfru, jrru, jspu, jccu, jdpu
		inteiro fckpp, ffrp, frrp, fspp, fccp, fdpp, fckpu, ffru, frru, fspu, fccu, fdpu, prodjckp, prodjch4
		inteiro qtdjckp, qtdjfr, qtdjrr, qtdjsp, qtdjcc, qtdjdp
		inteiro qtdfckp, qtdffr, qtdfrr, qtdfsp, qtdfcc, qtdfdp
		inteiro ttckpf, ttfrf, ttrrf, ttspf, ttccf, ttdpf
		inteiro data, mes, ano
		cadeia hora
		
		data = Calendario.dia_mes_atual()
		mes = Calendario.mes_atual()
		ano = Calendario.ano_atual()

		//Solicitação de entrada de dados.
    escreva ("Digite a hora especifica. EX.: 00:00","\n")
		leia (hora)
		
    //Solicitação de entrada de dados.
		escreva ("Digite a produção Cockpit Jeep: ")
		leia (prodjckp)
		
    //Solicitação de entrada de dados.
		escreva ("Digite a produção Chassis 4: ","\n")
		leia (prodjch4)
		
    //Solicitação de entrada de dados.
		escreva ("A partir de agora digite as sequencias: ","\n")
		escreva ("\n")
		
    //Solicitação de entrada de dados.
		escreva ("1ª Cockpit Jeep ","\n")
		leia (jckpp)
		
    //Solicitação de entrada de dados.
		escreva ("Ultima Cockpit Jeep ","\n")
		leia (jckpu)
		
    //Solicitação de entrada de dados.
		escreva ("1ª Front Jeep ","\n")
		leia (jfrp)
		
    //Solicitação de entrada de dados.
		escreva ("Ultima Front Jeep ","\n")
		leia (jfru)
		
    //Solicitação de entrada de dados.
		escreva ("Ultima Rear Jeep ","\n")		
		leia (jrru)
		
    //Solicitação de entrada de dados.
		escreva ("Ultima Spoiler Jeep ","\n")
		leia (jspu)
		
    //Solicitação de entrada de dados.
		escreva ("Ultima Console Jeep ","\n")
		leia (jccu)
		
    //Solicitação de entrada de dados.
		escreva ("1ª Door Penel Jeep ","\n")
		leia (jdpp)
    
    //Solicitação de entrada de dados.
		  escreva ("Ultima Door Painel Jeep ","\n")
		  leia (jdpu)
		escreva ("\n")

    //Solicitação de entrada de dados.
    escreva ("Agora sequência Faurecia: ","\n")
		escreva ("\n")

		//Solicitação de entrada de dados.
    escreva ("Ultima Cockpit: ","\n")
		leia (fckpu)

		//Solicitação de entrada de dados.
    escreva ("Ultima Front: ","\n")
		leia (ffru)

		//Solicitação de entrada de dados.
    escreva ("Ultima Rear: ","\n")
		leia (frru)

		//Solicitação de entrada de dados.
    escreva ("Ultima Spoiler: ","\n")
		leia (fspu)

		//Solicitação de entrada de dados.
    escreva ("Ultima Console: ","\n")
		leia (fccu)

		//Solicitação de entrada de dados.
    escreva ("Ultima Door Panel: ","\n")
		leia (fdpu)

				jrrp = (jfrp +4)
				jspp = (jfrp +17)
				jccp = (jfrp +3)

				qtdjckp = (jckpu - jckpp)
				qtdjfr = (jfru - jfrp)
				qtdjrr = (jrru - jrrp +4)
				qtdjsp = (jspu - jspp +17)
				qtdjcc = (jccu - jccp +3)
				qtdjdp = (jdpu - jdpp)

				fckpp = (jckpu + 1)
				ffrp = (jfru + 1)
				frrp = (jrru + 1)
				fspp = (jspu + 1)
				fccp = (jccu + 1)
				fdpp = (jdpu + 1)

				qtdfckp = (fckpu - fckpp)
				qtdffr = (ffru - ffrp)
				qtdfrr = (frru - frrp)
				qtdfsp = (fspu - fspp)
				qtdfcc = (fccu - fccp)
				qtdfdp = (fdpu - fdpp)

				//Reunião de todas informações que serão exibidas.
        escreva ("\n")
				escreva ("Status ",data,".",mes,".",ano,"\n")
				escreva (hora,"\n")
				escreva ("*Prod. CH4:* ",prodjch4,"*","\n")
				escreva ("*Prod. CKP:* ",prodjckp,"*","\n")
				escreva ("*CKP JEEP:* ",qtdjckp," *FPCMA:* ",qtdfckp," *TOTAL: ",(qtdjckp+qtdfckp),"*","\n")
				escreva ("*JEEP:* ",jckpp," *FPCMA:* ",fckpu,"*","\n")
				escreva (" *-----------------------------------* ","\n")
				escreva ("*FR JEEP:* ",qtdjfr," *FPCMA:* ",qtdffr," *TOTAL: ",(qtdjfr+qtdffr),"*","\n")
				escreva ("*JEEP:* ",jfrp," *FPCMA:* ",ffru,"*","\n")
				escreva (" *-----------------------------------* ","\n")
				escreva ("*RR JEEP:* ",qtdjrr," *FPCMA:* ",qtdfrr," *TOTAL: ",(qtdjrr+qtdfrr),"*","\n")
				escreva ("*JEEP:* ",jrrp," *FPCMA:* ",frru,"*","\n")
				escreva (" *-----------------------------------* ","\n")
				escreva ("*SP JEEP:* ",qtdjsp," *FPCMA:* ",qtdfsp," *TOTAL: ",(qtdjsp+qtdfsp),"*","\n")
				escreva ("*JEEP:* ",jspp," *FPCMA:* ",fspu,"*","\n")
				escreva (" *-----------------------------------* ","\n")
				escreva ("*CC JEEP:* ",qtdjcc," *FPCMA:* ",qtdfcc," *TOTAL: ",(qtdjcc+qtdfcc),"*","\n")
				escreva ("*JEEP:* ",jccp," *FPCMA:* ",fccu,"*","\n")
				escreva (" *-----------------------------------* ","\n")
				escreva ("*DP JEEP:* ",qtdjdp," *FPCMA:* ",qtdfdp," *TOTAL: ",(qtdjdp+qtdfdp),"*","\n")
				escreva ("*JEEP:* ",jdpp," *FPCMA:* ",fdpu,"*","\n")
				
		
		}
}
