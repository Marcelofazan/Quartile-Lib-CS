### DLL-CSharp-Estatistica-Calculo-Quartil
Exemplo de criação de componente de calculo de Estatísticas e Cálculo do Quadro de Quartil DLL em CSharp para ser utilizado como componente em outras linguaguens de programação 32 bits (Delphi, Visual Basic, FoxPro) como componente (**COM/ActiveX**), 

### O que você vai encontrar neste projeto
- **DLL** - Criação de DLL em Csharp
- **FoxPro** - Utilização do uso como componente DLL e consumindo dados retornados em formato Json.
- **Json** - Serialização e desserialização utilizado nas linguaguens   
- **COM** - Criação de Componente Objetos COM/ActiveX em .NET onde para ser usadas por outras linguaguens (rundll32), devem ter e serem criadas como ComVisible(true) e serem registradas para interoperação com registro (regasm.exe). 

#### Execução da aplicação em outras linguaguens
A DLL deve ser registrada com o seguinte .BAT, necessário ajustar o diretório do arquivo BAT.
```bash
@ECHO OFF
echo %cd%
C:\Windows\Microsoft.NET\Framework\v4.0.30319\RegAsm.exe D:\DLLTeste3\DLLTeste3\Foxpro\DLLTeste3.dll /codebase /tlb
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\RegAsm.exe D:\DLLTeste3\DLLTeste3\Foxpro\DLLTeste3.dll /codebase /tlb
timeout /t 20
EXIT
```

#### Cálculo do Quartil
Os quartis são medidas estatísticas que dividem um conjunto de dados ordenados (do menor para o maior) em quatro partes iguais, cada uma contendo 25% dos dados. Eles são fundamentais para entender a distribuição e a dispersão dos dados, indo além do que uma simples média pode mostrar.
