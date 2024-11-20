### Abrir e cerrar
FILE* nombre = fopen (char* nome_arquivo, char* modo);
if (nombre == NULL) {printf("error");}

##### Modo:
- r
- w
- a (append)
- t (texto) (comb)
- b (binario) ((comb))
- r+ (r w en xa existente)
- w+ (r w en non existente)

fclose(FILE ftpr);
#### Para leer
- ```int fscanf (FILE* fp, char* formato, ...);```  scanf pero en archivos, avanza o cursos ata o seguinte dato
- ```char* fgets (char* s, int n, FILE* fp);```     colle todos os caracteres ata ocupar os n bytes e gardaos en s
#### Para escribir
- ```int fprintf(FILE* fp, char* formato, ...);```      printf en archivos

#### Escribir en binario
- ```int fwrite (void* p, int tam, int nelem, FILE* fp);```
  
	p -> os elementos (array normalmente) a escribir

	tam -> tamaño en bytes de cada elemento

	nelem -> numero elementos

	fp -> FILE ao que se vai escribir

#### Leer en binario
- ```int fread (void* p, int tam, int nelem, FILE* fp);```
  
	p -> os elementos (array normalmente) a leer

	tam -> tamaño en bytes de cada elemento

	nelem -> numero elementos

	fp -> FILE ao que se vai leer

