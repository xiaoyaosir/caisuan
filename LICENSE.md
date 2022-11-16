#include<iostream>
#include<set>
using namespace std;
set<int> haha;
int check(int n)
{
	set<int>::iterator it;
	it=haha.find(n);
	if(it==haha.end())
	return 1;
	else
	return 0;
}
int main()
{
	
	for(int a=1;a<=9;a++)
	for(int b=1;b<=9;b++)
	for(int c=1;c<=9;c++)
	for(int d=1;d<=9;d++)
	for(int e=1;e<=9;e++)
	for(int f=1;f<=9;f++)
	{
		int i,j,k;
		if(a!=b&&a!=c&&a!=d&&a!=e&&a!=f&&b!=c&&b!=d&&b!=e&&b!=f&&c!=d&&c!=e&&c!=f&&d!=e&&d!=f&&e!=f)
	   {
	   double p=(double)(a*10+b)*(c*10+d)/(e*10+f);
	   haha.insert(a*10+b);
	   if(check(c*10+d)&&p==(int)p)
	   {
	   	i=(int)p%10;
	   	j=(int)p/10%10;
		k=(int)p/100; 
		if(k!=0&&j!=0&&i!=0&&i!=a&&i!=b&&i!=c&&i!=d&&i!=e&&i!=f&&j!=a&&j!=b&&j!=c&&j!=d&&j!=e&&j!=f&&k!=a&&k!=b&&k!=c&&k!=d&&k!=e&&k!=f&&k!=i&&k!=j&&i!=j)
		cout<<a*10+b<<" x "<<c*10+d<<" = "<<e*10+f<<" x "<<k*100+j*10+i<<endl;
	   }
}
	} 
	
} 
