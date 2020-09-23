<div align="center">

## FunctionsLib\.h


</div>

### Description

This is my functionslib (library) that works with some of my programs - including a math program

(remember its a header file)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Morgan L\.D\.](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/morgan-l-d.md)
**Level**          |Beginner
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/morgan-l-d-functionslib-h__3-5559/archive/master.zip)





### Source Code

```
#include <iostream.h>
#include <stdlib.h>
#include <lvp\conio.h>
#include <lvp\string.h>
/*  Call File - Functions Library
   int FindLow(int Hi,int Lo)
   char Upcase(char ch)
   void FindLoHi(int &High,int &Low)
   void FindLoHi(double &High,double &Low)
   void DrawBar(int Area, char Symbol)
   void Input(int Row, char Symbol)
   double PowerOf(double Base,int Power)
   void FrenchNum(int Num)
   void DrawBox(int Area, char Symbol)
   void Switch(int &x, int &y)
   void TimeBreak(int TSec, int &Hr, int &Min, int &Sec)
   int GetNumber(int Low, int High)
   int GetPerfectNumber(int Low, int High, String Str)
   void DrawLine(int Number)
   void Continue()
   bool PlayAgain(String Str)
*/
/* Function Specification
  If the function must return...          Then...
a) No information                  use a void function
b) One item of informaion              use a return statement
c) More than one item of information        use reference parameters */
int FindLow(int Hi,int Lo)
{
  int Answer ;
  if (Hi > Lo)
    Answer =Lo;
  else
    Answer =Hi;
  return(Answer);
}
char Upcase(char ch)
{ char CChar;
 if (ch >='a'&&ch <='z')
   CChar = char(int(ch)-32);
 else
   CChar = ch;
 return(CChar);
}
void FindLoHi(int &High,int &Low)
{  int Temp;
   if (Low > High)
     { Temp = Low;
      Low = High;
      High = Temp;
     }
   else;
}
void FindLoHi(double &High,double &Low)
{  double Temp;
   if (Low > High)
     { Temp = Low;
      Low = High;
      High = Temp;
     }
   else;
}
void DrawBar(int Area, char Symbol)
{
   for(int x=1; x<=Area; x++)
     cout<<Symbol;
   cout<<endl;
}
void Input(int Row, char Symbol)
{
   cout<<'\n';
   cout<< "Enter number of rows: ";
   cin>>Row;
   cout<< "Enter symbol to use: ";
   Symbol=getche();
   cout<<'\n';
   clrscr();
}
double PowerOf(double Base,int Power)
{
   double Value=1;
   for (int X=1; X<=Power; X++)
     Value*=Base;
   cout<<endl;
   return(Value);
}
void FrenchNum(int Num)
{
   if (Num==1)
     cout<<"1 Un"<<endl;
   else if (Num==2)
     cout<<"2 Deux"<<endl;
   else if (Num==3)
     cout<<"3 Trois"<<endl;
   else if (Num==4)
     cout<<"4 Quatre"<<endl;
   else if (Num==5)
     cout<<"5 Cinq"<<endl;
   else;
}
void DrawBox(int Area, char Symbol)
{
   int Num=1;
   while(Num<=Area)
   {
    for(int X=1; X<=Area; X++)
      cout<<Symbol;
    Num++;
    cout<<endl;
   }
   cout<<endl;
}
void Switch(int &x, int &y)
{
   int Temp;
   Temp=x;
   x=y;
   y=Temp;
}
void TimeBreak(int TSec)
{
   int Hr, Min, Sec;
   Hr=TSec/3600;
   int Left=TSec%3600;
   Min=Left/60;
   Sec=Left%60;
}
int GetNumber(int Low, int High)
{
   int Number;
   while(Number<Low || Number>High)
    {
    cout<<"Value must be between "<<Low<<" and "<<High<<endl;
    cout<<"Please re-enter: ";
    cin>>Number;
    }
   return(Number);
}
int GetPerfectNumber(int Low, int High, String Str)
{
   int Number;
   cout<<Str<<Low<<"-"<<High<<": ";
   cin>>Number;
   while(Number<Low || Number>High)
   {
   cout<<"ERROR!! Enter number between "<<Low<<"-"<<High<<": ";
   cin>>Number;
   }
   return(Number);
}
void DrawLine(int Number)
{
   int Counter=0;
   for(int x=1; x<=Number; x++)
     {cout<<"@ ";
     Counter++;
     }
   cout<<" = "<<Counter<<endl<<endl;
}
void Continue()
{
   cout<<"Press 'B' to Begin ";
   getche();
}
bool PlayAgain(String Str)
{
   bool Play=false;
   cout<<Str;
   char ch=getche();
   ch=Upcase(ch);
   if(ch=='Y')
    Play=true;
   return(Play);
}
```

