#include<stdio.h>
#include<stdlib.h>
struct person
{
    char name[35];
    char address[50];
     char father_name[35];
     char mother_name[30];
    long int mble_no;
    char mail[100];
    };
void menu();
void start();
void back();
void addrecord();
void listrecord();
void searchrecord();
int main()
{
    start();
    return 0;
}
void back()
{
    start();
}
void start()
{
    menu();
}
void menu()
{
printf("WELCOME TO PHONEBOOK");
printf(" MENU");
printf("\t1.Add New   \t2.List   \t3.Exit   \t4.Search");

switch(getch())
{
    case '1':addrecord();
    break;
    case '2': listrecord();
    break;
    case '3': exit(0);
    break;
    case '4': searchrecord();
    break;
    default:
                printf("\nEnter 1 to 4 only");
                printf(" Enter any key");
                getch();
menu();
}
}
        void addrecord()
{
        FILE *f;
        struct person p;
        f=fopen("project","ab+");
        printf("\n Enter name: ");
        got(p.name);
        printf("\nEnter the address: ");
        got(p.address);
        printf("\nEnter father name: ");
        got(p.father_name);
        printf("\nEnter mother name: ");
        got(p.mother_name);
        printf("\nEnter phone no.:");
        scanf("%ld",&p.mble_no);
        printf("\nEnter e-mail:");
         got(p.mail);
        fwrite(&p,sizeof(p),1,f);
      fflush(stdin);
        printf("\nrecord saved");

fclose(f);

    printf("\n\nEnter any key");

	 getch();
    menu();
}
void listrecord()
{
    struct person p;
    FILE *f;
f=fopen("project","rb");
if(f==NULL)
{
printf("\nfile opening error in listing :");

exit(1);
}
while(fread(&p,sizeof(p),1,f)==1)
{
     printf(" YOUR RECORD IS ");
        printf("\nName=%s\nAdress=%s\nFather name=%s\nMother name=%s\nMobile no=%ld\nE-mail=%s\n",p.name,p.address,p.father_name,p.mother_name,p.mble_no,p.mail);

	 getch();
}
fclose(f);
 printf("\n Enter any key");
 getch();
menu();
}
void searchrecord()
{
    struct person p;
FILE *f;
char name[100];

f=fopen("project","rb");
if(f==NULL)
{
    printf("\n error in opening\a");
    exit(1);
}
printf("\nEnter name of person to search\n");
got(name);
while(fread(&p,sizeof(p),1,f)==1)
{
    if(strcmp(p.name,name)==0)
    {
        printf("\n\tDetail Information About %s",name);
        printf("\nName:%s\naddress:%s\nFather name:%s\nMother name:%s\nMobile no:%ld\nE-mail:%s\n",p.name,p.address,p.father_name,p.mother_name,p.mble_no,p.mail);
    }
        else
        printf("file not found");

}
 fclose(f);
  printf("\n Enter any key");

	 getch();
menu();
}



