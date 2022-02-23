/* Rafael de França Bisol - Matrícula: 21035533-5 - Curso de Bacharelado em Engenharia de Software

A única coisa que me parece que pode ter faltado nesse MAPA é a utilização de várias funçoes, mas não vi necessidade de usar várias, por isso não o fiz. É possível saber que eu sei usar diversas funções
no exercício 1 dessa matéria.

*/

#include <stdio.h>
#include <locale.h>

typedef struct Paciente
{
    char nome[50];
    char CPF[11];
    char sexo;
    short int idade;
    int contagemPaciente;

} Paciente;

int contagemSintomas;

int main()
{
    setlocale(LC_ALL, "Portuguese");

    printf("Oi, tudo bem? Estou aqui para fazer a triagem inicial em você de COVID-19. Vamos começar. \n");
    system("pause");

    Paciente pessoa;
    int i;
    char resposta;

    //Perguntando dados do paciente

    printf("Qual é seu nome? \n");
    fflush(stdin);
    scanf("%s", &pessoa.nome);
    fflush(stdin);

    printf("Qual é seu CPF? (apenas números) \n");
    fflush(stdin);
    scanf("%s", &pessoa.CPF);
    fflush(stdin);

    printf("Qual é seu sexo? (M/F) \n");
    fflush(stdin);
    scanf("%c", &pessoa.sexo);
    fflush(stdin);

    fflush(stdin);
    printf("Qual é sua idade? \n");
    fflush(stdin);
    scanf("%d", &pessoa.idade);
    fflush(stdin);

    //Perguntando os sintomas

    fflush(stdin);
    printf("Você está com febre? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 5;
    fflush(stdin);

    printf("Você está com dor de cabeça? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 1;
    fflush(stdin);

    printf("Você tem secreção nasal ou espirros? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 1;
    fflush(stdin);

    printf("Você tem dor/irritação na garganta? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 1;
    fflush(stdin);

    printf("Você tem tosse seca? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 3;
    fflush(stdin);

    printf("Você tem dificuldade respiratória? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 10;
    fflush(stdin);

    printf("Você tem dores no corpo? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 1;
    fflush(stdin);

    printf("Você tem diarreia? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 1;
    fflush(stdin);

    printf("Esteve em contato, nos últimos 14 dias, com um caso diagnosticado com COVID-19? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 10;
    fflush(stdin);

    printf("Esteve em locais com grande aglomeração? (Respostas: S/N) \n");
    scanf("%c", &resposta);

    if (resposta == 'S' || resposta == 's')
        contagemSintomas += 3;
    fflush(stdin);

    pessoa.contagemPaciente = contagemSintomas; //igualar a contagem

    //escrever no arquivo
    FILE *testesCOVID;

    testesCOVID = fopen("testesCOVID.txt", "w+");
    fprintf(testesCOVID, "Nome: %s ", pessoa.nome);
    fprintf(testesCOVID, "Sexo: %c ", pessoa.sexo);
    fprintf(testesCOVID, "CPF: %s ", pessoa.CPF);
    fprintf(testesCOVID, "Idade: %d ", pessoa.idade);
    fprintf(testesCOVID, "Contagem dos sintomas: %d", pessoa.contagemPaciente);
    fclose(testesCOVID);

    printf("Sua contagem é de: %d \n", pessoa.contagemPaciente);

    //Risco baixo
    if(contagemSintomas >= 0 && contagemSintomas <= 9)
        printf("Você provavelmente não está com COVID-19 (risco baixo). :) Respeite as medidas de isolação e tudo ficará bem.");

    //Risco médio
    else if (contagemSintomas >= 10 && contagemSintomas <= 19)
        printf("Você está com um risco médio. Aguarde o seu atendimento e então checaremos o que está acontecendo.");

    //Risco alto. Se a pessoa está com esse risco, melhor aguardar o exame para não desespera-la
    else if (contagemSintomas >= 20)
        printf("Aguarde ser atendido. Seu caso será analisado. :)");
    else
        printf("Aguarde ser atendido. Seu caso será analisado. :)");

    return 0;
}
