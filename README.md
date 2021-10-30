#include<stdio.h>
#include<conio.h>
#include<graphics.h>
#include<string.h>
void main()
{
char ch='y';
int gd=DETECT,gm,x1,y1,x2,y2,rad,sa,ea,xrad,yrad,i;
initgraph(&gd,&gm,"");
while(ch=='y')
{
cleardevice();
setbkcolor(9);
outtextxy(100,130,"Choose From The Following ");
outtextxy(100,150,"1. Line");
outtextxy(100,170,"2.Circle");
outtextxy(100,190,"3.Box");
outtextxy(100,210,"4.Arc");
outtextxy(100,230,"5.Ellipse");
outtextxy(100,250,"6.Rectangle");
outtextxy(100,270,"7.Exit");
ch=getch(); 

cleardevice();
switch(ch)
{
case '1':
line(100,200,300,400);
break;
case '2':
circle(200,200,100);
break;
case '3':
setfillstyle(5,4);
bar(100,300,200,100);
break;
case '4':
setfillstyle(5,4);
arc(200,200,100,300,100);
break;
case '5':
setfillstyle(5,4);
fillellipse(100,100,50,100);
break;
case '6':
settextstyle(DEFAULT_FONT,0,2);
outtextxy(120,140,"AMS COLLEGE ");
line(100,100,100,300); 

line(300,300,100,300);
line(100,100,300,100);
line(300,100,300,300);
break;
case '7':
closegraph();
return;
}
ch='y';
getch();
}
}
