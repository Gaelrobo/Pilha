# Pilha

#include <stdio.h> 

#include <stdlib.h> 

#include <stdbool.h> 

 
 

typedef 

struct nodo { 

int info; 

struct nodo *prox; 

} NODO; 

 
 

typedef 

struct { 

NODO *topo; 

} PILHA; 

 
 

void inic_pilha(PILHA *p) { 

 
 

p->topo = NULL; 

} 

 
 

void push(PILHA *p, int valor) { 

 
 

NODO *aux; 

 
 

if (!(aux = (NODO*)malloc(sizeof(NODO)))) { 

printf("Erro na alocação de novo nodo - push.\n"); 

exit(1); 

} 

aux->info = valor; 

 
 

if (p->topo == NULL) { 

aux->prox = NULL; 

} 

else { 

aux->prox = p->topo; 

} 

p->topo = aux; 

} 

 
 

int pop(PILHA *p) { 

 

Int val; 

 
 

return 0; 

} 

 
 

bool pilha_vazia(PILHA *p) { 

return (p->topo == NULL); 

} 

 
 

int main() { 

 
 

PILHA p1, p2; 

 
 

inic_pilha(&p1); 

inic_pilha(&p2); 

 
 

push(&p1, 5); 

push(&p2, 3); 

push(&p1, 7); 

push(&p1, 9); 

push(&p1, 11); 

 
 

while (!pilha_vazia(&p1)) { 

int val; 

val = pop(&p1); 

printf("%d\n", val); 

} 

 
 

return 0; 

 
 

} 

 
