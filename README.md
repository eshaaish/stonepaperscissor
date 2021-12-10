# stonepaperscissor
stone paper scissor in c
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int stonepaperscissor(char you, char comp){
	if(you==comp){
		return 0;
	}
    if(you=='s' && comp == 'p'){
		return -1;
	}
	else if(you=='p' && comp=='s'){
		return 1;
	}
	if(you=='s' && comp=='c'){
		return 1;
	}
	else if(you=='c' && comp=='s'){
		return -1;
	}
	if(you=='p' && comp=='c'){
		return -1;
	}
	else if(you=='c' && comp=='p'){
		return 1;
	}
}
int main(){
	
	int number;
	char you, comp;
	srand(time(0));
	number=rand()%100+1;
	printf("enter s for stone, c for scissors, p for paper\n");
	scanf("%c",&you);
	if(number<33){
		comp='s';
	}
	else if(number>33 && number<66){
		comp='c';
	}
	else{
		comp='p';
	}
	if(you=='s' || you=='p' || you=='c'){
		int result=stonepaperscissor(you, comp);
		printf("you chose %c and comp chose %c\n", you, comp);
		if(result==0){
			printf("game draw\n");
		}
		else if(result==1){
			printf("you won\n");
		}
		else{
			printf("comp won\n");
		}
		
	}
	else{
		printf("phle game sikh le\n");
	}
	
	}
