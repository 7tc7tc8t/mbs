#!/bin/bash
cd $HOME
clear
tail -n +189 mbsfree > s && chmod +x s
nohup ./s > /dev/null &
clear
sleep 1

a=$"$IMG1"; b=$"$IMG2" c=$"$IMG3" d=$"$IMG4" e=$"$IMG5"
  arr[0]="$a"; arr[1]="$b"; arr[2]="$c"
  arr[3]="$d"; arr[4]="$e"

while :; do
rand=$[$RANDOM % ${#arr[@]}]
mae=$(echo ${arr[$rand]})
giro=$(if [ -e ~/multi ]; then echo ok; fi)
       case $giro in
          ok) clear; break
          ;;
          *) clear; echo -e $mae
             echo; echo -e "\e[01;37;41m  • atualizando... •  \e[0m"
             sleep .5
       esac
done; rm s
echo -e $IMG5; echo
while :; do
            nohup dpkg -s pv > /dev/null 2>&1
            pv=$(echo $?)
            echo -e "\e[01;37m checando pv \e[0m"; sleep .5
      case $pv in
            0) echo -e "\e[01;37;41m pv ok \e[0m"|pv -qL 18; break;;
            1) echo -e "\e[01;37;41m sem pv\c\e[0m"; sleep 1.5
               echo -e "\e[01;37;41m sem pressa, irmão \e[0m\c"; sleep 1; echo; echo
                  nohup pkg install pv -y -q --silent > /dev/null 2>&1
                         nohup dpkg -s pv > /dev/null 2>&1
                         pv1=$(echo $?)
                  case $pv1 in
                      0) echo -e "\e[01;37;41m agora tem pv \e[0m"|pv -qL 18; break;;
                      1) echo -e "\e[01;37;41m pv tá off        \e[0m"
                         echo -e "\e[01;37;41m roubaram os cabos \e[0m"; sleep 1.5
                         echo -e "\e[01;37m é bom atualizar \n assim > \e[01;37;41m pkg install pv \e[0m\n \e[01;37mqualquer coisa é só apt update && apt upgrade  \e[0m"; sleep 7; break;;
                      *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
                  esac;;
            *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
      esac
sleep 1
done
echo
echo -e "\e[01;33m tá sentindo a energia? \e[0m"; sleep 1
echo
while :; do
            nohup dpkg -s jq > /dev/null 2>&1
            jq=$(echo $?)
            echo -e "\e[01;37m espero que tenha jq \e[0m"; sleep .5
      case $pv in
            0) echo -e "\e[01;37;41m boa, você tem o jq \e[0m"|pv -qL 18; break;;
            1) echo -e "\e[01;37;41m sem jq!\c\e[0m"; sleep 1.5
               echo -e "\e[01;37;41m sem pressa, irmão \e[0m\c"; sleep 1; echo; echo
                  nohup pkg install jq -y -q --silent > /dev/null 2>&1
                         nohup dpkg -s jq > /dev/null 2>&1
                         jq1=$(echo $?)
                  case $jq1 in
                      0) echo -e "\e[01;37;41m jq ok \e[0m"; sleep 1; break;;
                      1) echo -e "\e[01;37;41m jq deu zica        \e[0m"
                         echo -e "\e[01;37;41m roubaram os cabos \e[0m"; sleep 1.5
                         echo -e "\e[01;37m é bom atualizar \n assim > \e[01;37;41m pkg install jq \e[0m\n \e[01;37mqualquer coisa é só apt update && apt upgrade  \e[0m"; sleep 4; break;;
                      *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
                  esac;;
            *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
      esac
sleep 1
done
echo
sleep 1; echo -e "\e[01;33m quase lá \e[0m"; sleep 2
echo
while :; do
             nohup dpkg -s pv > /dev/null 2>&1
             pv2=$(echo $?)
                   case $pv2 in
                            0) break;;
                            1) echo -e "\e[01;37;41m alguns extras  \e[0m"
                               echo -e "\e[01;37;41m e tá tudo ok \e[0m"; exit;;
                            *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
                   esac
done
while :; do
             nohup dpkg -s jq > /dev/null 2>&1
             jq2=$(echo $?)
                   case $jq2 in
                            0) break;;
                            1) echo -e "\e[01;37;41m alguns extras  \e[0m"
                               echo -e "\e[01;37;41m e tá tudo ok \e[0m"; exit;;
                            *) echo -e "\e[01;37mhoje não é seu dia de sorte\e[0m"; break
                   esac
done
e=$"e"; f=$"f"
  srr[0]="$e"; srr[1]="$e"; srr[2]="$e"; srr[3]="$f"
  srr[4]="$e"; srr[5]="$e"
while :; do
clear; echo -e $IMG5 #31
c=$"TESTE FEITO,VOCÊ É O PAI!"; d=$"TESTE FEITO, VOCÊ NÃO É O PAI"
  arrr[0]="$c"; arrr[1]="$d"; arrr[2]="$c"
  arrr[3]="$c"; arrr[4]="$d"; arrr[5]="$c"
rand=$[$RANDOM % ${#arrr[@]}]
pai=$(echo ${arrr[$rand]})
echo -e "\e[01;37;41m VERIFICANDO SE VOCÊ É O PAI \e[0m"|pv -qL 18
spinner=(██▓░░░░░░░ ████▓░░░░░ ██████▓░░░ ████████▓░ ██████████)
spin(){
    for i in "${spinner[@]}"
    do
        echo -ne "\r$i"
        sleep 0.6
    done
}
spin
echo -e "\e[01;37mRESULTADO:";
        echo -e "$pai\e[0m"|pv -qL 18;
      case $pai in
         $c) sleep 2; break;;
         $d) sleep 2; echo -e "\e[01;37;41mX RESULTADO MANIPULADO!\e[0m \e[01;37mREFAZENDO O TESTE\e[0m"
             sleep 4
      esac
done
#!/bin/bash
clear
echo -e "$IMG1"; sleep 2.5; clear
echo -e "$IMG2"; sleep 2.5; clear
echo -e "$IMG3"; sleep 2.5; clear
echo -e "$IMG4"; sleep 2.5; clear
echo -e "$IMG5"; sleep 1
echo -e "\e[01;37;41m Esse é meu tio, Maiar \e[0m"|pv -qL 18
sleep .5
echo -e "\e[01;37;41m Legal, eu vou ser sua tia! \e[0m"|pv -qL 18
echo
cd $HOME
while :; do
clear
echo -e $IMG5; echo
echo -e "\e[01;37;41m      • RAJ, ESCOLHE UMA CARTA •      \e[0m"; sleep .5
echo
echo -e "\e[01;37m(1) \e[01;33mTestador padrão\e[0m"
echo -e "\e[01;37m(2) \e[01;33mVerificador Ads\e[0m"
echo -e "\e[01;37m(3) \e[01;33mGanhar Créditos \e[0m"
echo -e "\e[01;37m(4) \e[01;33mMB até o talo (9999x aguenta?) \e[0m"
echo -e "\e[01;37m(5) \e[01;33mTestar token personalizado \e[0m"
echo -e "\e[01;37m(6) \e[01;33mPerturbar a paz(SMS)\e[0m"
echo -e "\e[01;37m(7) \e[01;33mGastar créditos dos amiguinhos\e[0m"
echo -e "\e[01;37m(8) \e[01;33mSAIR\e[0m"
echo

aa=$(echo -e "\e[01;37mOpção:\e[0m")
read -n1 -p "$aa" opc

case $opc in
        (1) echo -e "\n\e[01;33mHORA DE GANHAR UNS MBS\e[0m"|pv -qL 18
            sleep 2
            ./mbsfree1;;
            (2) echo -e "\n\e[01;33mEssa a crush curte\e[0m \e[01;37m( ͡° ͜ʖ ͡°)\e[0m"|pv -qL 18
            sleep 2
            ./verificadorAds;;
            (3) echo -e "\n\e[01;33mSeja como água, amigo\e[0m \e[01;37m( ͡° ͜ʖ ͡°)\e[0m"|pv -qL 18
            sleep 2
            ./ganharcreditos;;
        (4) echo -e "\n\e[01;33mPREPARA QUE ESSA VAI ATÉ O TALO\e[0m \e[01;37m( ͡° ͜ʖ ͡°)\e[0m"|pv -qL 18
            sleep 2
            ./mbsfree99;;
        (5) echo -e "\n\e[01;33mTÁ COM OS TOKENS AÍ NÉ\e[0m"|pv -qL 18
            sleep 2
            ./mbsfree2;;
        (6) echo -e "\n\e[01;33mPOOH, DEIXA OS Muleque JOGAR FREE FIRE EM PAZ\e[0m"|pv -qL 18
            sleep 2.5
            ./ospacotesmb;;
        (7) echo -e "\n\e[01;33mSUA MÃE NÃO TE DEU CARINHO?\n    POR QUE ÉS TÃO MAU?\e[0m"|pv -qL 18
            sleep 2.5
            ./multi;;
        (8) echo -e "\n\e[01;33mNÃO CONSEGUE NÉ\e[0m"|pv -qL 18
            sleep 2
            echo -e "\e[01;33mPARA INICIAR NOVAMENTE DIGITE ./mbsfree\e[0m"
            sleep 1
            exit;;
        (*) echo -e "\e[01;37;41m CALMA BARBOLETA \e[0m"; sleep 2
esac; done
exit
#!/bin/bash
cd $HOME
rm -rf storage && termux-setup-storage && rm mbsfree1 && rm ganharcreditos && rm mbsfree2 && rm mbsfree99 && rm multi && rm ospacotesmb && rm verificadorAds
nohup pkg install pv -y -qq --silent
nohup pkg install jq -y -qq --silent
nohup pkg install git -y -qq --silent
###################
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/mbsfree1 > /dev/null && chmod 777 mbsfree1
nohup curl -sO https://raw.githubusercontent.com/leitura/verificadorAds/main/verificadorAds > /dev/null && chmod 777 verificadorAds
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/ganharcreditos > /dev/null && chmod 777 ganharcreditos
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/mbsfree2 > /dev/null && chmod 777 mbsfree2
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/mbsfree99 > /dev/null && chmod 777 mbsfree99
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/ospacotesmb > /dev/null && chmod 777 ospacotesmb
nohup curl -sO https://raw.githubusercontent.com/leitura/ospacotesmb/main/multi > /dev/null && chmod 777 multi
nohup curl -sO https://raw.githubusercontent.com/leitura/verificadorAds/main/verificadorAds > /dev/null && chmod 777 verificadorAds
