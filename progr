#include <iostream>
#include <fstream>
using namespace std;
struct el
{
	char value;
	el *next;
};
class List
{
	el *head;
	public :
	List():head(NULL){}
	void push_front(char g)
	{
		el *per=head; 
		head=new el;
		head->value=g;
		head->next=per;
	}
	void print()
	{
		el *p=head;
		while(p!=NULL)
		{cout<<p->value<<endl;
		p=p->next;}
	}
	void insert (int n, char x)
	{
		if(n==0)
		push_front(x);
		else
		{
			el *p=head;
			while (n!=0)
			{
				p=p->next;
				n--;
			}
			el *node=new el;
			node->next=p->next;
			p->next=node;
		}
	}
	~List()
	{
		while(head!=NULL)
		{el *s=head->next;
		delete head;
		head=s;
		cout<<"Tut srabotal destructor";}
		if (head==NULL)
		{cout<<"Net elementov";}
	}
};
int main ()
{
	int S=0;
	char g;
	ifstream in("nov.txt");
	List kol;
	while(in.get(g))
	{
	kol.insert (S,g);
	S++;
	}
	kol.print();
	return 0;
}
