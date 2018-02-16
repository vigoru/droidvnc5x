# droidvnc5x
Servidor VNC para android. Projeto Original - https://github.com/oNaiPs/droidVncServer 

Testado em Android 5.0 e 5.1

Projeto estrutudado em Eclipse.

# Como compilar Eclipse:

1) tenha o NDK instalado e, se possível, adicione-o à variável de sistema
2) execute o build.sh com os paâmetros -w e -a informando uma API especifica ou não (build.sh -w -a 22)
3) execute o updateExecsAndLibs.sh
4) compile o projeto no Eclipse utilizando o ADT.
5) A cada alteração feita nos arquivos .c, deve-se recompilar o projeto executando novamente o build.sh e updateExecsAndLibs.sh.
6) item 4 novamente

# Como compilar Android Studio:

Como tive muita dor de cabeça para configurar o NDK internamente no Android Studio, fiz de maneira "manual":

1) execute o build.sh com os paâmetros -w e -a informando uma API especifica ou não (build.sh -w -a 22)
2) execute o updateExecsAndLibs.sh
3) importe o projeto no Android Studio, porém faça-o criar a nova estrutura em outra pasta
4) altere o plugin do gradle para gradle-experimental:0.x.x e adicione as alterações conforme modelo: 
5) compile o projeto no Android Studio.
6) A cada alteração feita nos arquivos .c, deve-se recompilar o projeto executando novamente o build.sh e updateExecsAndLibs.sh.
7) Após a execução, copie os arquivos gerados na pasta [Pasta_do_Projeto]/libs para [Pasta_do_projeto_androidstudio]/app\src\main\jniLibs
8) item 5 novamente.

# Como executar app

No momento, o app está sendo executado através do comando /data/data/org.onaips.vnc/lib/libandroidvncserver.so 
Em alguns dispositivos pode funcionar através, do botão START da MainActivity. Mas houve falhas em outros.
