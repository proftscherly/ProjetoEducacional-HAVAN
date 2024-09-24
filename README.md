# ProjetoEducacional-HAVAN
//Atividade, criar código em Java, um sistema simples de cadastro e exibição de informações que usa interface, classes abstratas, herança e polimorfismo para organizar dados de clientes, //funcionários e produtos (eletrônicos, móveis, decoração, vestuário, vídeo games, brinquedos e utilitários) e funcionários responsáveis pelas áreas. Esse programa simula varejistas como![image]
//(https://github.com/user-attachments/assets/3aafd33b-3ea7-4d10-bf88-8576d4cb0b83)

´´´java
import java.util.Scanner;


interface Cadastro {
    void cadastrar();
    void exibirDados();
}

// Classe Abstrata Pessoa
abstract class Pessoa implements Cadastro {
    protected String nome;
    protected String cpf;

    public Pessoa(String nome, String cpf) {
        this.nome = nome;
        this.cpf = cpf;
    }

    @Override
    public void exibirDados() {
        System.ot.println("Nome: " + nome);
        System.out.println("CPF: " + cpf);
    }
}


class Cliente extends Pessoa {
    private String endereco;

    public Cliente(String nome, String cpf, String endereco) {
        super(nome, cpf);
        this.endereco = endereco;
    }

    @Override
    public void cadastrar() {

        System.out.println("Erro: Método cadastrar() não implementado corretamente.");
    }

    @Override
    public void exibirDados() {
        super.exibirDdos();
        System.out.println("Endereço: " + endereco);

        System.out.println("Telefone: " + telefone);  // 'telefone' não está definida
    }
}

// Classe Funcionario que herda de Pessoa
class Funcionaio extends Pessoa {
    private String cargo;

    public Funcionario(String nome, String cpf, String cargo) {
        super(nome, cpf);
        this.cargo = cargo;
    }

    @Override
    public void cadastrar() {

        int erro = 10 / 0;
        System.out.println("Erro: Cadastro falhou devido a uma operação incorreta.");
    }

    @Override
    public void exibirDados() {
        super.exibirDados();
        System.out.println("Cargo: " + cargo);
    }
}

// Classe Abstrata Produto
abstract class Produto implements Cadastro {
    protected String nomeProduto;
    protected double preco;

    public Produto(String nomeProduto, double preco) {
        this.nomePrduto = nomeProduto;
        this.preco = preco;
    }

    @Override
    public void exibirDados() {
        System.out.println("Nome do Produto: " + nomeProduto);
        System.out.println("Preço: R$ " + preco);
    }
}

// Subclasse Eletronico de Produto
class Eletronco extends Produto {
    private String marca;

    public Eletronico(String nomeProduto, double preco, String marca) {
        super(nomeProduto, preco);
        this.marca = marca;
    }

    @Override
    public void cadastrar() {

        int[] erroArray = new int[2];
        erroArray[5] = 10;
    }

    @Override
    public void exibirDados() {
        super.exibirDados();
        System.out.println("Marca: " + marca);
    }
}

// Subclasse Movel de Produto
class Movel extends Produto {
    private String material;

    public Movel(String nomeProduto, double preco, String material) {
        super(nomeProduto, preco);
        this.material = material;
    }

    @Override
    public void cadastrar() {

        if (preco <= 0) {
            Systm.out.println("Erro: Preço inválido.");
        }
    }

    @Override
    public void exibirDados() {
        super.exibirDados();
        System.out.println("Material: " + material);
    }
}

// Subclasse Vestuario de Produto
class Vestuario extends Produto {
    private String tamanho;

    public Vestuario(String nomeProduto, double preco, String tamanho) {
        super(nomeProduto, preco);
        this.tamanho = tamanho;
    }

    @Override
    public void cadastrar() {

        int erroConversao = Integer.parseInt("texto");
    }

    @Override
    public void exibirDados() {
        super.exibirDados();
        System.out.println("Tamanho: " + tamanho);
    }
}

// Subclasse Videogame de Produto
class Videogame extends Produto {
    private String plataforma;

    public Videogame(String nomeProduto, double preco, String plataforma) {
        super(nomeProduto, preco);
        this.plataforma = plataforma;
    }

    @Override
    public void cadastrar() {
        // Erro introduzido: loop infinito
        while (true) {
            System.out.println("Erro: Loop infinito detectado.");
        }
    }

    @Override
    public void exibirDados() {
        super.exibirDados()
        System.out.println("Plataforma: " + plataforma);
    }
}

// Subclasse Utilitario de Produto
class Utilitario extend Produto {
    private String tipoUtilitario;

    public Utilitario(String nomeProduto, double preco, String tipoUtilitario) {
        super(nomeProduto, preco);
        this.tipoUtiltario = tipoUtilitario;
    }

    @Override
    public void cadastrar() {

    }

    @Override
    public void exibirDados() {
        super.exibirDados();
        System.out.println("Tipo de Utilitário: " + tipoUtilitario);
    }
}

// Pograma Principal
public class LojaHavan {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        System.out.println("Cadastro de Cliente:");
        System.out.print("Nome: ");
        String nomeCliente = scanner.nextLine();
        System.out.print("CPF: ");
        String cpfCliente = scanner.nextLine();
        System.out.print("Endereço: ");
        String enderecoCliente = scanner.nextLine();
        Cliente cliente = new Cliente(nomeCliente, cpfCliente, enderecoCliente);


        System.out.println("\nCadastro de Funcionário:");
        System.out.print("Nome: ");
        String nomeFuncionario = scanner.nextLine();
        System.out.print("CPF: ");
        String cpfFuncioario = scanner.nextLine();
        System.out.print("Cargo: ");
        String cargoFuncionario = scanner.nextLine();
        Funcionario funcionario = new Funcionario(nomeFuncionario, cpfFuncionario, cargoFuncionario);


        System.out.println("\nCadastro de Produto Eletrônico:");
        System.out.print("Nome do Produto: ");
        String nomeEletronico = scanner.nextLine();
        System.out.print("Preço: ");
        double precoEletronico = scanner.nextDouble();
        scanner.nextLine();
        System.out.print("Marca: ");
        String marcaEletronico = scanner.nextLine();
        Eletronico eletronico = new Eletronico(nomeEletronico, precoEletronico, marcaEletronico);


        System.out.println("\nCadastro de Produto Móvel:");
        System.out.print("Nome do Produto: ");
        String nomeMovel = scanner.nextLine();
        System.out.print("Preço: ");
        double precoMovel = scanner.nextDuble();
        scanner.nextLine(); /
        System.out.print("Material: ");
        String materialMovel = scanner.nextLine();
        Movel movel = new Movel(nomeMovel, precoMovel, materialMovel);


        System.out.println("\nCadastro de Produto Vestuário:");
        System.out.print("Nome do Produto: ");
        String nomeVestuario = scanner.nextLine();
        System.out.print("Preço: ");
        double precoVestuario = scanner.nextDouble();
        scanner.nextLine(); // Consumir a nova linha
        System.out.print("Tamanho: ");
        String tamanhoVestuario = scanner.nextLine();
        Vestuario vestuario = new Vestuario(nomeVestuario, precoVestuario, tamanhoVestuario);


        System.out.println("\nCadastro de Videogame:");
        System.out.print("Nome do Produto: ");
        String nomeVideogame = scanner.nextLine();
        System.out.print("Preço: ");
        double precoVideogame = scanner.nextDouble();
        scanner.nextLine(); // Consumir a nova linha
        System.out.print("Plataforma: ");
        String plataformaVideogame = scanner.nextLine();
        Videogame videogame = new Videogame(nomeVideogame, precoVideogame, plataformaVideogame);


        System.out.println("\nCadastro de Utilitário:");
        System.out.print("Nome do Produto: ");
        String nomeUtilitario = scanner.nextLine();
        System.out.print("Preço: ");
        double precoUtilitario = scanner.nextDouble();
        scanner.nextLine();
        System.out.print("Tipo de Utilitário: ");
        String tipoUtilitario = scanner.nextLine();
        Utilitario utilitario = new Utilitario(nomeUtilitario, precoUtilitario, tipoUtilitario);


        System.out.println("\n--- Dados do Cliente ---");
        cliente.exibirDados();

        System.out.println("\n--- Dados do Funcionário ---");
        funcionario.exibirDados();

        System.out.println("\n--- Dados do Produto Eletrônico ---");
        eletronico.exibirDados();

        System.out.println("\n--- Dados do Produto Móvel ---");
        movel.exibirDados();

        System.out.println("\n--- Dados do Produto Vestuário ---");
        vestuario.exibirDados();

        System.out.println("\n--- Dados do Videogame ---");
        videogame.exibirDados();

        System.out.println("\n--- Dados do Utilitário ---");
        utilitario.exibirDados();

        System.out.println("\n--- Dados do Cliente ---");
        cliente.exibirDados();

        System.out.println("\n--- Dados do Cliente ---");
        cliente.exibirDados();

        scanner.close();
    }
}


´´´
