
# sysmon windows

Este é um arquivo de configuração modelo do Sysmon, da Microsoft Sysinternals, com rastreamento de eventos de alta qualidade por padrão.

Esse arquivo foi expirado no projeto [SwiftOnSecurity](https://github.com/SwiftOnSecurity)


## Como instalar o Sysmon no Windows

Para instalar o Sysmon no Windows, siga os passos abaixo:

1.  Baixe o Sysmon no site oficial da [Microsoft Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon).
2.  Extraia o arquivo baixado para um diretório acessível, como `C:\\Sysmon`.
3.  Abra um prompt de comando (cmd) ou PowerShell com privilégios de administrador.
4.  Baixe o arquivo de configuração de [(https://github.com/carlossilva9867/sysmon_and_audit/blob/main/windows/sysmonconfig-export.xml) no diretorio `C:\\Sysmon`
5.  Navegue até o diretório onde extraiu o Sysmon.
6.  Instale o Sysmon com o seguinte comando:
    
    ```
    sysmon.exe -accepteula -i sysmonconfig-export.xml
    ```
    
7.  Verifique se o Sysmon está rodando corretamente executando:
 
    ```
    sc query sysmon
    ```
    
    O status deve indicar que o serviço está em execução.



### Desinstalar

Execute com privilégios de administrador:

```
sysmon.exe -u
```
