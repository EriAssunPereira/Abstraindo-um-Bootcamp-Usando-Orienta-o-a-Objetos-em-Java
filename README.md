# Abstraindo-um-Bootcamp-Usando-Orienta-o-a-Objetos-em-Java

Para abstrair um Bootcamp usando a Programação Orientada a Objetos (POO) em Java, você pode começar definindo as entidades principais que compõem um Bootcamp e mapeá-las para classes Java. Aqui está um exemplo de como você pode estruturar seu código:

```java
// Classe abstrata que define uma Entidade do Bootcamp
public abstract class EntidadeBootcamp {
    private String nome;
    private String descricao;

    public EntidadeBootcamp(String nome, String descricao) {
        this.nome = nome;
        this.descricao = descricao;
    }

    // Métodos getters e setters
    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getDescricao() {
        return descricao;
    }

    public void setDescricao(String descricao) {
        this.descricao = descricao;
    }
}

// Classe que representa um Curso dentro do Bootcamp
public class Curso extends EntidadeBootcamp {
    private int cargaHoraria;

    public Curso(String nome, String descricao, int cargaHoraria) {
        super(nome, descricao);
        this.cargaHoraria = cargaHoraria;
    }

    // Método específico de Curso
    public int getCargaHoraria() {
        return cargaHoraria;
    }

    public void setCargaHoraria(int cargaHoraria) {
        this.cargaHoraria = cargaHoraria;
    }
}

// Classe que representa um Mentor no Bootcamp
public class Mentor extends EntidadeBootcamp {
    private String especialidade;

    public Mentor(String nome, String descricao, String especialidade) {
        super(nome, descricao);
        this.especialidade = especialidade;
    }

    // Método específico de Mentor
    public String getEspecialidade() {
        return especialidade;
    }

    public void setEspecialidade(String especialidade) {
        this.especialidade = especialidade;
    }
}

// Classe que representa o Bootcamp
public class Bootcamp {
    private List<Curso> cursos;
    private List<Mentor> mentores;

    public Bootcamp() {
        cursos = new ArrayList<>();
        mentores = new ArrayList<>();
    }

    // Métodos para adicionar cursos e mentores
    public void adicionarCurso(Curso curso) {
        cursos.add(curso);
    }

    public void adicionarMentor(Mentor mentor) {
        mentores.add(mentor);
    }

    // Outros métodos relevantes...
}
```

Neste exemplo, utilizamos a **abstração** para criar uma classe base `EntidadeBootcamp` que contém atributos e métodos comuns a todas as entidades do Bootcamp. O **encapsulamento** é aplicado através do uso de modificadores de acesso `private` e métodos `getters` e `setters` para proteger e controlar o acesso aos atributos das classes. A **herança** é demonstrada pela extensão da classe `EntidadeBootcamp` pelas classes `Curso` e `Mentor`, que herdam seus atributos e métodos. O **polimorfismo** poderia ser implementado através de métodos que se comportam de maneira diferente nas subclasses ou pela implementação de interfaces.

Você pode expandir esse código adicionando mais funcionalidades e entidades conforme necessário para o seu Bootcamp. Lembre-se de que a POO é uma poderosa ferramenta de design que pode ajudar a organizar e estruturar seu código de maneiras que facilitam a manutenção e a expansão futuras.

Para representar os participantes de um Bootcamp em Java, você pode criar uma classe `Participante` que inclua informações como nome, email, nível de habilidade e cursos concluídos. Aqui está um exemplo de como essa classe pode ser estruturada:

```java
public class Participante {
    private String nome;
    private String email;
    private String nivelHabilidade;
    private List<Curso> cursosConcluidos;

    public Participante(String nome, String email, String nivelHabilidade) {
        this.nome = nome;
        this.email = email;
        this.nivelHabilidade = nivelHabilidade;
        this.cursosConcluidos = new ArrayList<>();
    }

    // Métodos getters e setters
    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }

    public String getNivelHabilidade() {
        return nivelHabilidade;
    }

    public void setNivelHabilidade(String nivelHabilidade) {
        this.nivelHabilidade = nivelHabilidade;
    }

    public List<Curso> getCursosConcluidos() {
        return cursosConcluidos;
    }

    // Método para adicionar um curso concluído à lista do participante
    public void adicionarCursoConcluido(Curso curso) {
        cursosConcluidos.add(curso);
    }
}
```

Nesta classe `Participante`, utilizamos **encapsulamento** para proteger os atributos através de modificadores de acesso `private` e fornecemos métodos `getters` e `setters` para acessá-los e modificá-los de forma controlada. A lista `cursosConcluidos` armazena os cursos que o participante completou, e o método `adicionarCursoConcluido` permite adicionar novos cursos a essa lista.

Essa é uma forma básica de representar um participante, mas você pode expandir e personalizar a classe conforme as necessidades específicas do seu Bootcamp, adicionando mais atributos ou métodos que considerar relevantes.

https://github.com/cami-la/desafio-poo-dio
