## Código de média ponderada de 10 alunos  (com funções) em C

------

```
#include <stdio.h>
#include <math.h>

float mediapond(float nota1, float nota2) 
{
	return ((nota1 * 4) + (nota2 * 6))/10;
}

char conceito(float mediapond) 
{
	if (mediapond >= 0.0 && mediapond <= 4.9) 
	{
		return 'D';
	}

	if (mediapond >= 5.0 && mediapond <= 6.9) 
	{
		return 'C';
	}

	if (mediapond >= 7.0 && mediapond <= 8.9) 
	{
		return 'B';
	}

  	if (mediapond >= 9.0 && mediapond <= 10.0) 
  	{
		return 'A';
	}
}

int main()
{
	int i;
	float nota1, nota2, media;
	char conc;
	
	for (i = 0; i < 10; i++) 
	{
		printf("Digite a primeira nota do aluno %d: ", (i+1));
		scanf("%f", &nota1);
		printf("Digite a segunda nota do aluno %d: ", (i+1));
		scanf("%f", &nota2);
		
		media = mediapond(nota1, nota2);
		
  		conc = conceito(media);

  		printf("A media do aluno %d é: %.1f, dentro do conceito: %c\n", (i+1), media, conc);
	}  

return 0;
}
```

