#include<iostream>
#include<cmath>
#include <cstdlib>
#include <time.h>
#include <map>
#include <string>
#include <stdio.h>
#include <conio.h>
#include <stdlib.h>

using namespace std;
class Map{
public:
    char** base = new char*[10] ;
   // char base [10][10];
  int size = 10;
    Map() {
        cout<<"Constructor map() is called"<<endl;
        for(int i =0; i<10;i++){
            base[i]= new char[10];
        }
        for(int k = 0;k<10 ;k++){
        	 for(int j = 0;j<10 ;j++){
        		 base [k][j] = 'n';

        	 }
        }
        int i = 0;
        srand(time(0));
        while (i < 40) {
         int x = (int) (rand() % 10);
          int y = (int) (rand()%10);
          if(base[x ] [y]== 'n'&& (x!=9 && y!=0)){
           base[x] [y] = 'G';
          i++;
          }
        }
    }

    void print_map()    {
        cout<<"print_map() called"<<endl;
        for(int i = 0 ;i<10;i++){
             for(int j = 0 ;j<10;j++){
                if(base[i][j] == 'n')
                	base[i][j] = '.';
              }
        }
        for(int i = 0 ;i<10;i++){
            for(int j = 0 ;j<10;j++){
                cout<<base[i][j]<<"  ";
            }
            cout<<endl;
        }
    }
    void randomize_map()    {
            cout<<"randomize_map() called"<<endl;
                    int i = 0;
                    while (i < 20) {
                        int x = (int) (rand() % 10);
                        int y = (int) (rand() % 10);
                        if (base[x][y] == 'n' && (x!=9 && y!=0)) {
                            base[x][y] = 'x';
                            i++;
                        }
                    }

        }
 //   char  (&getbase())[10][10]{
//    	return this->base;
//    }
~Map() {
    for(int i =0;i<10;i++){
        delete [] base[i];
    }
    delete []base;
	}

};
class Point
{
private:
	int x, y;
    public:

        Point(int x, int y) {
            this-> x =x;
            this->y=y;
            }
             Point()= default;
             int getx(){
            return this->x;
             }
             int gety(){
            	 return this->y;
             }
             void setx(int x){
                this->x=x;
             }
             void sety(int y){
                this->y=y;
             }


};
class Champion{
private:
    Point location;
    int health;
    int gemscore;
    int indexX;
    int indexY;
public:
Champion(Map * map) {

   this-> location =  Point (0,0);
   (map)->base[9][0] = 'C';
     indexX =9;
     indexY =0;
     this-> health = 100;
     this->gemscore = 0;
    cout<<"Constructor champion() is called"<<endl;
}
void print_champ_info() {
	int x =this->location.getx();
	int y=this->location.gety();
    cout<<"champion's location " << x<< ","<<y<<" champion's health "<<this->health << " " <<"gems scored "<<this->gemscore<<" /40" <<endl;
}
int getHealth(){
	return this->health;
}
void setHealth(int health){
   this->health=health;
}
int getIndexX(){
	return this->indexX;
}
void setIndexX(int indexX){
   this->indexX=indexX;
}
int getIndexY(){
	return this->indexY;
}
void setIndexY(int indexY){
   this->indexY=indexY;
}
Point getLocation(){
	return this->location;
}
void setLocation(int x ,int y){
	this->location.setx ( x);
	this->location.sety (y);
}
int getGemScore(){
	return this->gemscore;
}
void setGemScore(int gemscore){
    this->gemscore=gemscore;
}
~Champion() {
    // TODO Auto-generated destructor stub
}

};
class Game{
public:
	Map *map;
	Champion *c;
	Game(){
	    map = new Map();
	     map->randomize_map();
	      c = new Champion(map);
	    map->print_map();
	   c->print_champ_info();
	}

	void move(int n){
        switch(n){
            case 54 :  //RIGHT
                if (c->getIndexY()+1 >=0 && c->getIndexY()+1 <=9){
                        int tempx = c->getIndexX();
                        int tempy = c->getIndexY();
                   action(54,c->getIndexY()+1);
                   gameover();
                   (*map).base[c->getIndexX()][c->getIndexY()+1]='C';
                   (*map).base[tempx][tempy]='n';
                   c->setLocation(c->getLocation().getx(),c->getLocation().gety()+1);
                   c->setIndexY(c->getIndexY()+1);
                    system("CLS");
                   map->print_map();
                   c->print_champ_info();
                 cout<<"press 8 to move up , 5 to move down ,6 for right and 4 for left"<<endl;
                }
                break;

            case 52 : //LEFT
                 if (c->getIndexY()-1 >=0 && c->getIndexY()-1 <=9){
                        int tempx = c->getIndexX();
                        int tempy = c->getIndexY();
                   action(52,c->getIndexY()-1);
                   gameover();
                   (*map).base[c->getIndexX()][c->getIndexY()-1]='C';
                   (*map).base[tempx][tempy]='n';
                   c->setLocation(c->getLocation().getx(),c->getLocation().gety()-1);
                   c->setIndexY(c->getIndexY()-1);
                    system("CLS");
                   map->print_map();
                   c->print_champ_info();
                 cout<<"press 8 to move up , 5 to move down ,6 for right and 4 for left"<<endl;
                }
                break;

            case 56 :  //UP
                  if (c->getIndexX()-1 >=0 && c->getIndexX()-1 <=9){
                        int tempx = c->getIndexX();
                        int tempy = c->getIndexY();
                   action(56,c->getIndexX()-1);
                   gameover();
                   (*map).base[c->getIndexX()-1][c->getIndexY()]='C';
                   (*map).base[tempx][tempy]='n';
                   c->setLocation(c->getLocation().getx()+1,c->getLocation().gety());
                   c->setIndexX(c->getIndexX()-1);
                    system("CLS");
                   map->print_map();
                   c->print_champ_info();
                cout<<"press 8 to move up , 5 to move down ,6 for right and 4 for left"<<endl;
                }
                break;

            case 53:  //DOWN
                if (c->getIndexX()+1 >=0 && c->getIndexX()+1 <=9){
                        int tempx = c->getIndexX();
                        int tempy = c->getIndexY();
                   action(53,c->getIndexX()+1);
                   gameover();
                   (*map).base[c->getIndexX()+1][c->getIndexY()]='C';
                   (*map).base[tempx][tempy]='n';
                   c->setLocation(c->getLocation().getx()-1,c->getLocation().gety());
                   c->setIndexX(c->getIndexX()+1);
                    system("CLS");
                   map->print_map();
                   c->print_champ_info();
                  cout<<"press 8 to move up , 5 to move down ,6 for right and 4 for left"<<endl;
                }
                break;
            }

	}
	void action(int n ,int o){
		switch(n){
		 case 54 :  //RIGHT
             if ((*map).base[c->getIndexX()][o] == 'G')
                 c->setGemScore(c->getGemScore()+1);
             else if ((*map).base[c->getIndexX()][o] == 'x')
                 c->setHealth(c->getHealth()-40);
             break;

         case 52 :  //LEFT
             if ((*map).base[c->getIndexX()][o] == 'G')
                 c->setGemScore(c->getGemScore()+1);
             else if ((*map).base[c->getIndexX()][o] == 'x')
                 c->setHealth(c->getHealth()-40);
             break;

		 case 56 : // UP
             if ((*map).base[o][c->getIndexY()] == 'G')
                 c->setGemScore(c->getGemScore()+1);
             else if ((*map).base[o][c->getIndexY()] == 'x')
                 c->setHealth(c->getHealth()-40);
			 break;


		 case 53 : //DOWN
             if ((*map).base[o][c->getIndexY()] == 'G')
                 c->setGemScore(c->getGemScore()+1);
             else if ((*map).base[o][c->getIndexY()] == 'x')
                 c->setHealth(c->getHealth()-40);
			 break;




	 }
	}
	bool gameover(){
	if(c->getHealth()<=0 ){
        cout<<"You Lost";
          return true;
	}
       else if (c->getGemScore() == 40){
        cout<<"You Won";
        return true;
	}
	else
    return false;

	}
	~Game() {
	    delete(map);
	    delete(c);
	}
};



int main(){
Game *g = new Game();

 while(true){
	   cout<<"Want to generate another random map?"<<endl;
	char x = getch();
	if(x =='y'){
     system("CLS");
     g = new Game();
	}
	else{
            cout<<"press 8 to move up , 5 to move down ,6 for right and 4 for left"<<endl;
        break;
	}

 }
int a;
while(!g->gameover()){
            a = getch();

         switch(a){
            case 56 : //UP
                cout<<8;
                g->move(56);
                break;
            case 53 : //DOWN
                 cout<<5;
                g->move(53);
                break;
            case 54 :  //RIGHT
                 cout<<6;
                g->move(54);
                break;
            case 52 :  //LEFT
                 cout<<4;
                g->move(52);
                break;
        }
	}

	delete(g);
    return 0;
}

