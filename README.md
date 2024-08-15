
#include<iostream>
#include<string.h>
#include<stdlib.h>

using namespace std;

class Library{
    public:
    char student[100];
    int id;
    char name[100];
    char author[100];
    int pages;
    int price;
};

int main(){
    Library lib[20];
    int input=0;
    int count=0;
    
    while(input!=2){
        cout<<"Enter 1 to insert details in register "<<endl;
        cout<<"Enter 2 to display the details "<<endl;
        cout<<"Enter 3 to Exit "<<endl;
        cin>>input;
        
        switch(input){
            case 1:
                start:
                cout<<"Enter Student name "<<endl;
                cin.getline(lib[count].student,100,'$');
                cout<<"Enter book id "<<endl;
                cin>>lib[count].id;
                cout<<"Enter Book name "<<endl;
                cin.getline(lib[count].name,100,'$');
                cout<<"Enter Author's name "<<endl;
                cin.getline(lib[count].author,100,'$');
                cout<<"Enter number of pages in book "<<endl;
                cin>>lib[count].pages;
                cout<<"Enter price of the book "<<endl;
                cin>>lib[count].price;
                count++;
                break;
                
            case 2:
                for(int i=0;i<count;i++){
                    cout<<"\nName of Student :"<<lib[i].student;
                    cout<<"\nBook ID :"<<lib[i].id;
                    cout<<"\nBook Name :"<<lib[i].name;
                    cout<<"\nAuthor's Name :"<<lib[i].author;
                    cout<<"\nNumber of pages :"<<lib[i].pages;
                    cout<<"\nPrice :"<<lib[i].price;
                }
                    break;
                
            case 3:
                exit(0);
                break;
            
            default:
                cout<<"You have entered wrong value ,please try again"<<endl;
                goto start;
    
            }
                
        }
    }
