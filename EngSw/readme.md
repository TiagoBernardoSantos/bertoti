09/08 - Atividade trecho livro: Software Enginering at Google - 

" We see three critical differences between programming and software engineering: time, scale, and the trade-offs at play. 
On a software engineering project, engineers need to be more concerned with the passage of time and the eventual need for change. 
In a software engineering organization, we need to be more concerned about scale and efficiency, both for the software we produce as well as for the organization that is producing it. 
Finally, as software engineers, we are asked to make more complex decisions with higher-stakes outcomes, often based on imprecise estimates of time and growth. "

Comentário: 

Após a leitura do trecho, compreendi as funções de um engenheiro de software, que além de realizar o trabalho de programação, devem prestar cuidados a mais, focando na eficiência do software e também na qualidade da realização da empresa,
sendo destinado a eles tomarem decisões cruciais para que consigam finalizar positivamente o projeto.

----------------------------------------------------------------------------------------------------------------------------------------------------------
12/08 - Exemplos de trade-offs: 

1° Estudo ou Lazer: Você escolhe entre estudar mais ou ter mais tempo livre para lazer.

2° Trabalho ou Descanso: Você escolhe entre trabalhar mais horas ou descansar mais.

3° Espaço ou Mobilidade: Você escolhe entre ter um carro maior e mais espaçoso ou um carro menor e mais fácil de estacionar.

----------------------------------------------------------------------------------------------------------------------------------------------------------
19/08 - Atividade Java

Classe Empresa 

```bash
package engsw;

import java.util.LinkedList;
import java.util.List;


public class Empresa {
	private List<Funcionario> funcionarios = new LinkedList<Funcionario>();
	
	public void cadastrarFuncionario(Funcionario funcionario) {
		funcionarios.add(funcionario);
	}
	
	public List<Funcionario> buscarFuncionarioporCpf(String cpf){
		List<Funcionario> funcionariosEncontrados = new LinkedList<Funcionario>();
		
		for(Funcionario funcionario:this.funcionarios) {
			if(funcionario.getCpf().equals(cpf))
              funcionariosEncontrados.add(funcionario);
		}
			
		
		return funcionariosEncontrados;
	}
	
	
	public List<Funcionario> getFuncionarios(){
		return funcionarios;
	}
}
```
Classe Funcionario 

```bash
package engsw;

public class Funcionario {
   private String nome;
   private String cpf;
   
   public Funcionario(String cpf, String nome) {
   	
   	this.cpf = cpf;
   	this.nome = nome;
   }

   public String getCpf() {
   	return cpf;
   }
   
   public String GetNome() {
   	return nome;
   }
}
```
Classe TesteEmpresa 

```bash
package engsw;
import static org.junit.jupiter.api.Assertions.*;

import java.util.List;

import org.junit.jupiter.api.Test;

public class TesteEmpresa {
	
@Test 
void test() {
	Empresa CeA = new Empresa();
	
	Funcionario Tecnica = new Funcionario("43943509855", "Bia");
	Funcionario Desenvolvedor = new Funcionario("54583098549", "Tiago");
	
	CeA.cadastrarFuncionario(Tecnica);
	CeA.cadastrarFuncionario(Desenvolvedor);
	
	assertEquals(CeA.getFuncionarios().size(), 2);
	
	List<Funcionario> Desenvolvedores = CeA.buscarFuncionarioporCpf("54583098549");
	assertEquals(Desenvolvedores.get(0).getCpf(),Desenvolvedor.getCpf());
		
  }

}
```
----------------------------------------------------------------------------------------------------------------------------------------------------------

01/11 - 4) Atividade diagrama de classes uml 

![Diagrama em branco (1)](https://github.com/user-attachments/assets/092fc77f-6339-43b4-9ad7-808464f714eb)

