## Simulado Deloitte

Parte 1 - Programação Orientada a Objetos(POO)

1- Programação Orientada a Objetos é um paradigma da programação que visa a criação de códigos em torno de classes, objetos, atributos e métodos visando o benefício de organização do código e a manutenção mais fácil e prática. <br>
2- Encapsulamento protege os dados dentro de uma classe, deixando atributos da classe privados. <br>
3- Está sendo violado o princípio de encapsulamento, deixando os atributos da classe como "public". <br>
4- Porque está aderindo ao uso de encapsulamento. <br>
5- <br>
public class Produto {      
    private Long id; <br>
    private String nome; <br>
    private double preco; <br>
} <br>

Parte 2 - Spring Boot e REST

6- SpringBoot é um framework que ajuda no desenvolvimento mais fácil das aplicações Java. <br>
7- @RestController <br>
8- @ResquestMapping inicia o endereço de funcionamento da API, por exemplo, @RequestMapping("/produtos"), rodando localmente por padrão na porta 8080, "http://localhost:8080/produtos" <br>
9- A parte do "GetMapping("/produtos") está errada, deve ser apenas @GetMapping, e anteriormente no controller @RequestMapping("/produtos") e logo após a criaçao da classe controller. <br>
10- GET- Retorna o que foi pedido POST- Adicionar PUT- Modifica os dados, DELETE- Deletar. <br>

Parte 3 - JPA e Hibernate

11 - JPA é uma maneira para persistências de dados e o hibernate é uma ORM que traduz objetos java para o banco de dados. <br>
12 - @Entity <br>
13 - A anotação @Id informa que a classe tem a chave primária id, @GeneratedValue gera o valor automaticamente, por exemplo @GeneratedValue(strategy = GenerationType.IDENTITY), gera o valor do Id automaticamente, facilitando o código. <br>
14 - findById - Procura por Id, deleteById - deleta através do Id fornecido. <br>
15 - Porque o JPA simplifica a parte do banco de dados, criando tabelas automaticamente.  <br>

Parte 4 - DTO e Service Layer <br>

16- O DTO serve para transferir dados de forma eficiente e impede exposição de dados sensíveis.  <br>
17- Essa abordagem não é recomendada porque traz risco a segurança, implementando a API com a estrutura do banco de dados. <br>
18- Implementar e aplicar regra do negócio. <br>
19- ServiceImpl deve conter a regra do negócio enquanto Service apenas aplica. <br>
20- Garantir o SRP, separando as responsabilidades. <br>

Parte 5 - SOLID

21- Cada classe deve ter apenas uma responsabilidade:<br>
///////////// <br>
public class Mensagem <br>
{<br>
    public int Id ; <br>
    public String Tipo; <br>
    public int Remetente; <br>
} <br>
<br>
public class Conversor <br>
{ <br>
    public String Para(String formato) <br>
    { <br>
        if(formato == "json") <br>
        { <br>
            // Lógica para montar json <br>
            return "{'json':'json'}"; <br>
        }
        else if (formato == "xml") <br>
        { <br>
            // Lógica para montar XML<br>
            return "<xml> </xml>"; <br>
        } <br>
        else{ <br>
            System.out.println("Esse formato não existe"); <br>
        } <br>
        return formato; <br>
    }  <br>
} <br>
///////////// <br>
22- SRP. <br>
23- Implementar regra de negócio que podem ser estendidas sem alterar código existente, "Entidades (classes, modulos, funcoes) devem ser abertas para extensão e fechadas para modificações". <br>
24- Utilizar interfaces de serviço garantindo que qualquer mudança não gere impacto no sistema, uma classe base deve poder usar objetos derivados sem saber. <br>
25- Evitar metódos desnecessários, separando "contratos" em interfaces menores e específicas. <br> 
26- ISP, está misturando interfaces de diferentes contextos, "Clientes não devem depender de interfaces que não usam.” <br>
27- Todas as dependências deverão apontar para abstrações. <br>
28- Não instanciar dependência com new. <br>

Parte 6 - Arquitetura<br>

29- Controller -> Interface Service -> Service Implementation -> Repository -> Banco de Dados<br>
30- DTO + Service + SOLID tornam o sistema mais simples, com menos código e mais fácil de entender através da boas práticas/organização do código, facilitando manutenções e implementações do sistema.<br>
