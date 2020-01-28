#include<iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int t,c,i=0,r,w,s[2]={0,0},b=0;

int toss(int t)
{
	r = (rand() % t);
	cout<<r<<" ";
	return r;
}

void hit(int t)
{
    if(t<10)
    {
        s[i]+=0;
        cout<<"Runs scored "<<0;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<35)
    {
        s[i]+=1;
        cout<<"Runs scored "<<1;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<65)
    {
        s[i]+=2;
        cout<<"Runs scored "<<2;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<85)
    {
        s[i]+=3;
        cout<<"Runs scored "<<3;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<95)
    {
        s[i]+=4;
        cout<<"Runs scored "<<4;
        cout<<"Total is "<<s[i]<<endl;
    }
    else
    {
        s[i]+=6;
        cout<<"Runs scored "<<6;
        cout<<"Total is "<<s[i]<<endl;
    }
}

void latehit(int t)
{
    if(t<5)
    {
        s[i]+=0;
        cout<<"Runs scored "<<0;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<20)
    {
        s[i]+=1;
        cout<<"Runs scored "<<1;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<50)
    {
        s[i]+=2;
        cout<<"Runs scored "<<2;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<60)
    {
        s[i]+=3;
        cout<<"Runs scored "<<3;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<90)
    {
        s[i]+=4;
        cout<<"Runs scored "<<4;
        cout<<"Total is "<<s[i]<<endl;
    }
    else
    {
        s[i]+=6;
        cout<<"Runs scored "<<6;
        cout<<"Total is "<<s[i]<<endl;
    }
}

void lamehit(int t)
{
    if(t<20)
    {
        s[i]+=0;
        cout<<"Runs scored "<<0;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<40)
    {
        s[i]+=1;
        cout<<"Runs scored "<<1;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<70)
    {
        s[i]+=2;
        cout<<"Runs scored "<<2;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<80)
    {
        s[i]+=3;
        cout<<"Runs scored "<<3;
        cout<<"Total is "<<s[i]<<endl;
    }
    else if(t<90)
    {
        s[i]+=4;
        cout<<"Runs scored "<<4;
        cout<<"Total is "<<s[i]<<endl;
    }
    else
    {
        s[i]+=6;
        cout<<"Runs scored "<<6;
        cout<<"Total is "<<s[i]<<endl;
    }
}

void mishit(int t)
{
    if(t<50)
    {
        w++;
        cout<<endl<<w<<"-"<<s[i]<<endl;
        t=toss(100);
        if(t<65 && w<10)
            hit(toss(100));
        else if(w<10)
            mishit(toss(100));
    }
    else
        hit(toss(100));
}

void bat(int t)
{
    if(t<85)
        hit(toss(100));
    else
        mishit(toss(100));
}

void latebat(int t)
{
    if(t<75)
        latehit(toss(100));
    else
        mishit(toss(100));
}

void lamebat(int t)
{
    if(t<60)
        lamehit(toss(100));
    else
        mishit(toss(100));
}

int main()
{
	srand((int)time(0));
    cout<<"Enter a Choice:";
    cin>>t;
    if(t==0 || t==1)
    {
        if(t==toss(2))
        {
            cout<<"You Won the Toss!\n";
            cout<<"Enter a Choice:";
            cin>>c;
            if(c==0)
                cout<<"You Bat first\n\n";
            else
                cout<<"You Bowl first\n\n";
        }
        else
        {
            cout<<"You Lost the Toss!\n";
            c=toss(2);
            if(c==0)
                cout<<"You Bat first\n\n";
            else
                cout<<"You Bowl first\n\n";
        }
    }

    while(i<2)
    {
        w=0;
        b=0;
        while(w<10 && b<60)
         {
             if(w<6)
             {
                if(b<42)
                    bat(toss(100));
                else
                    latebat(toss(100));
             }
             else
                lamebat(toss(100));
             b++;
             if(i==1 && s[1]>s[0])
                break;
         }
        cout<<"Innings "<<i<<" over at "<<s[i]<<"/"<<w<<" in "<<b<<" balls\n\n\n";
        i++;
    }

    if(c==0)
    {
        cout<<"You scored "<<s[0]<<" and Dragger scored "<<s[1]<<endl;
        if(s[0]>s[1])
            cout<<"You Win!!!";
        else if(s[0]==s[1])
            cout<<"Tie!!!";
        else
            cout<<"You Lose!!!";
    }
    else
    {
        cout<<"Dragger scored "<<s[0]<<" and You scored "<<s[1]<<endl;
        if(s[0]<s[1])
            cout<<"You Win!!!";
        else if(s[0]==s[1])
            cout<<"Tie!!!";
        else
            cout<<"You Lose!!!";
    }
	return 0;
}
