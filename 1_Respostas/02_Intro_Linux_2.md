Para todas as questões, escreva os comandos correspondentes no terminal.

1. Escreva o texto "Ola mundo cruel!" em um arquivo denominado "Ola_mundo.txt". Apresente o conteúdo deste arquivo no terminal.  
`echo "Ola mundo cruel!" > Ola_mundo.txt`

2. Apresente o nome de todos os arquivos e pastas na pasta 'root'.  
`ls -la root`

3. Apresente o tipo de todos os arquivos e pastas na pasta 'root'.  
`file *`

4. Apresente somente as pastas dentro da pasta 'root'.  
`file * | grep "directory"`

5. Descubra em que dia da semana caiu o seu aniversário nos últimos dez anos.  
```bash
for ano in `seq 1 10`; do
date --date="$ano years ago" | awk '{print $1}'
done
```

Para as questões a seguir, use a pasta no endereço https://github.com/DiogoCaetanoGarcia/Sistemas_Embarcados/raw/master/Questoes/02_Intro_Linux_arqs.zip

6. Liste somente os arquivos com extensão .txt.  
`ls *.txt`  
`
arquivo.txt   cal_1996.txt  cal_2003.txt  cal_2010.txt  cal_2017.txt
cal_1990.txt  cal_1997.txt  cal_2004.txt  cal_2011.txt  cal_2018.txt
cal_1991.txt  cal_1998.txt  cal_2005.txt  cal_2012.txt  cal_2019.txt
cal_1992.txt  cal_1999.txt  cal_2006.txt  cal_2013.txt  cal_2020.txt
cal_1993.txt  cal_2000.txt  cal_2007.txt  cal_2014.txt  cal.txt
cal_1994.txt  cal_2001.txt  cal_2008.txt  cal_2015.txt  cal_types.txt
cal_1995.txt  cal_2002.txt  cal_2009.txt  cal_2016.txt
`

7. Liste somente os arquivos com extensão .png.  
`ls *.png`  
`
BusinessTux.png               linux.png
linux1.png                    Tux-in-a-suit.png
linux2.png                    tux-linux-professional_0-100520358-orig.png
linux3.png                    TUX.png
linux_inside.png              xanderrun-tux-construction-8454.png
linux-penguin-icon-39742.png
`

8. Liste somente os arquivos com extensão .jpg.  
`ls *.jpg`  
`
d36f1a2be6a927ac3e2e1e4eacdedded.jpg  oRva1OGD.jpg
oRva1OGD_400x400.jpg                  zz39112bb5.jpg
`

9. Liste somente os arquivos com extensão .gif.  
`ls *.gif`  
`
1086970.gif
`

10. Liste somente os arquivos que contenham o nome 'cal'.  
`ls . | grep "cal"`  
`
cal_1990.txt
cal_1991.txt
cal_1992.txt
cal_1993.txt
cal_1994.txt
cal_1995.txt
cal_1996.txt
cal_1997.txt
cal_1998.txt
cal_1999.txt
cal_2000.txt
cal_2001.txt
cal_2002.txt
cal_2003.txt
cal_2004.txt
cal_2005.txt
cal_2006.txt
cal_2007.txt
cal_2008.txt
cal_2009.txt
cal_2010.txt
cal_2011.txt
cal_2012.txt
cal_2013.txt
cal_2014.txt
cal_2015.txt
cal_2016.txt
cal_2017.txt
cal_2018.txt
cal_2019.txt
cal_2020.txt
cal.txt
cal_types.txt
`

11. Liste somente os arquivos que contenham o nome 'tux'.  
`ls . | grep "tux"`  
`
tux-linux-professional_0-100520358-orig.png
xanderrun-tux-construction-8454.png
`  
Caso não precise diferenciar maiúsculas e minúsculas (*case insensitive*):  
`ls . | grep -i "tux"`  
`
BusinessTux.png
Tux-in-a-suit.png
tux-linux-professional_0-100520358-orig.png
TUX.png
xanderrun-tux-construction-8454.png
`

12. Liste somente os arquivos que comecem com o nome 'tux'.  
`ls . | grep "^tux"`  
`
tux-linux-professional_0-100520358-orig.png
`  
Caso não precise diferenciar maiúsculas e minúsculas (*case insensitive*):  
`ls . | grep -i "^tux"`  
`
Tux-in-a-suit.png
tux-linux-professional_0-100520358-orig.png
TUX.png
`