# ParadigmaOrientadoAspectos
Desafio de Projeto: Desenvolvendo um Projeto com o Paradigma de Programação Orientado à Aspectos

> Neste projeto temos como proposta a implementação de uma solução envolvendo o Paradigma de Programação Orientado a Aspectos. Para que isso seja possível, é aconselhável trabalhar com um paradigma de programação primário para o projeto principal, como por exemplo, o paradigma Orientado a Objetos.
A proposta envolve criar uma função transversal ao código sendo aplicada em diferentes chamadas, no entanto, todas para o mesmo objetivo. Como exemplo de projeto de base podemos utilizar o seguinte problema:
Problema padrão: Em um sistema bancário, o cliente pode optar por fazer saques em diferentes contas (corrente, salário, poupança, investimento), no entanto, uma mensagem deve ser gerada informando caso o saldo seja insuficiente perante o valor requisitado. Essa mensagem deve ser gerada por meio de um log de erro envolvendo todas as contas, ou seja, todas as contas devem ser verificadas antes de liberar o dinheiro, analisando a disponibilidade do mesmo e, caso não seja possível, uma mensagem de saldo insuficiente deve ser gerada.
O programa principal implementando em Paradigma Orientado a Objetos deve abordar as funções básicas da conta bancária, já a verificação de saldo, por estar presente em todas a contas, deve ser implementado em Paradigma Orientado a Aspectos. Pode ser utilizada a linguagem Java com extensão da linguagem para aspectos “AspectJ”.

 - Diagrama da classe Conta
   ```mermaid
   classDiagram
       class Conta{
        TipoConta
        TipoCliente
        DataAbertura
        Saldo
         sacar()
         depositar()
         carculaValorTarifaManutencao()
       }
   ```
    - Diagrama da classe Conta Poupanca
   ```mermaid
   classDiagram
       class Conta{
         ContaCorrente
         verificaSaldoSuficiente()
         CalculaManutencaoTarifa()
       }
   ```
   - Diagrama da classe Conta Investimento
   ```mermaid
   classDiagram
       class Conta{
         ContaInvestimento
         verificaSaldoSuficiente()
         CalculaManutencaoTarifa()
         tipoInvestimento()
       }
   ```
   - Diagrama da classe Conta Salário
   ```mermaid
   classDiagram
       class Conta{
         ContaSalario
         verificaSaldoSuficiente()
         CalculaManutencaoTarifa()
       }
   ```
   - Diagrama da classe Conta Corrente
   ```mermaid
   classDiagram
       class Conta{
         ContaCorrente
         verificaSaldoSuficiente()
         CalculaManutencaoTarifa()
         tipoICorrente()
       }
   ```
 
    - Fluxograma
   ```mermaid
     graph TD;
         Conta-->contaPoupanca;
         Conta-->contaInvestimento;
         Conta-->contaSalario;
         Conta-->contaCorrete;
   ```
 
