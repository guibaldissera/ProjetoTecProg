# _JACK THE JANITOR_ and _ENGINE_ - WIKI

### INTRODUCTION:

* This work has 2 distints projects, Jack the Janitor and Engine development on "Introduction to Eletronic Games".
* Jack The Janitor and Engine are devolopment in C++.

Jack The Janitor is a puzzle game where the player controls Jack, a school's janitor who must organize the school's warehouse. Jack can push boxes to the left or right and jump boxes.
	
Jack The Janitor -> [link repository original GITHUB](https://github.com/fgagamedev/jtj)  
Engine IJE -> [link repository original GITHUB](https://github.com/fgagamedev/IJE)

<a name="summary2"></a>
<a name="summary3"></a>
<a name="summary4"></a>
<a name="summary5"></a>
<a name="summary6"></a>
## DEFAULT STYLE PROGRAMMING
### SUMARY
* [Indentation and Spacing](#head2)
* [Comments](#head3)
* [Attributes](#head4)
* [Class](#head5)
* [Metods / Functions](#head6)

<a name="head2"></a>
### INDENTATION and SPACING:
###### [Summary](#summary2)

* The indentation will have 4 blank spaces or a "tab" of 4 spaces.  
* Before and after matematic operators ('+', '-', '*', '/', '%'), logics ('&&', '||', '==', '!=', '<=', '>=', '>', '<') and assignments ('=') is obligatory the use of 1 blank space.  
* When are use operators of assignment '++' and '--', not need have blank space between the attribute and the operator.  
* Before '{' and after '}' are obligatory a adiction of 1 space.  
* After openned '(' and before closed ')', not need a blank spaces.  
* After the name of a metod, the '()' are obligatory and not need have a separation between the name and '('.  
* After `if`, `for`, `while` are obligatory the inclusion of 1 blank space.  

**Example:**  
```c++
if (enemy != NULL) {  
	...  
}
```
```c++
if (moveDirection % 2 == 0 && movesLeft > 0) {  
	frame++;  
	if(frame > 3) {  
		frame = 1;  
	}  
}  
```
```c++
void SDLUtil::ApplySurface(int x, int y, SDL_Surface *source, SDL_Surface *destination, SDL_Rect *clip) {  
	...  
}  
```

<a name="head3"></a>
### COMMENTS:
###### [Summary](#summary3)

* All comments, without exception, will have '//' in the beginning of the line and 1 clear space before the text.  
* On metods and functions, need exist a sequence of comments with informacion about function before declaration of that.  

**Example:**  
```c++
// -------------------------------------------------------------  
// 	Struct: playing_s -> playing_t, *playing_p  
//	Description: Structure for a currently playing sound.  
// 	Atributes:  
//		int active;  		if this sound should be played  
//		sound_p sound; 		sound data to play  
//		Uint32 position; 	current position in the sound buffer  
// -------------------------------------------------------------  
typedef struct playingS {  
	int active;  
	sound_p sound;  
	Uint32 position;  
} playingT, *playingP;`  
```
```c++
// -------------------------------------------------------------  
// Function: ClearPlayingSounds  
// Description: Removes all currently playing sounds.  
// Parameters: void  
// Return: void  
// -------------------------------------------------------------  
void ClearPlayingSounds() {  
	for (int i = 0; i < MAX_PLAYING_SOUNDS; i++) {  
		playing[i].active = 0;  
	}  
}
```

<a name="head4"></a>
### ATTRIBUTES:
###### [Summary](#summary4)

* The name of the attributes will be using default camelCase and the first letter is lower  
* The name of constants or "define", will composed with upper case and will be _____ by "_" between words.  
	A nomeação das constantes ou "define", serão compostas por todas as letras maiusculas e separadas por '_' entre as palavras compostas.  
* The simbol '*' use for pointer, is obligatory will be together with the name of attributes and not have any blank spaces.  
	O '*' referente à ponteiros, é obrigatorio estar junto com o nome do atributo sem espaço em branco.  
* If necessary the inicialization of attributs, are ________ the inicialization with creation of attribute.  
	Caso necessário a inicialização da variável, é permitido a inicialização junto a criação da variável.  
* The atribution of attribute by values, will not be done in the criation of the same.  
	Atribuição de valores a variável não poderá ser feita na criação da mesma.  

**Example:**  
```c++
Game game;
```
```c++
SDL_Surface *loadedImage = NULL;
loadedImage = IMG_Load(filename.c_str());
```
```c++
#define SCORESCREEN_H
```
```c++
static const int SCORE_X_OFFSET = 506;
```

<a name="head5"></a>
### CLASS:
###### [Summary](#summary5)

* Have 2 types, headers (.h) e as ... (.cpp)  
Existem 2 tipos, headers (.h) e as ... (.cpp)  
* The files will have the same name of classes to ______ the includes and indentification.  
Os arquivos terão o mesmo nome das classes para facilitar a identificação e os includes.  
* The nomination of the classes will be done by a default CamelCase with the first upper letter.  
A nomeação das classes se dará com o padrão CamelCase com a primeira letra maiúscula.  
* The utilization of ':' will be done with blank space in both sides of ':'.  
A utilização de ':' se dará com espaço em branco em ambos os lados do ':'.  
	
**Example:**  
```c++
class Jack : public GameObject {
	...  
}
```
```c++
class OptionsScreen : public GameObject {
	...
}
```

<a name="head6"></a>
### METODS / FUNCTION:
###### [Summary](#summary6)

* The name of the metods will be using defalut CamelCase and the first letter is upper for constructors and destructors, and default cameCase with first letter lower for others metods and functions.  

**Example:**  
```c++
void DrawSelf(SDL_Surface *surface);
```
```c++
void load(const string &name);
```