# first
almostprime
#include <iostream>
#include<math.h>
using namespace std;
int countprime(int num)
{
    int count=0;
    while(num%2==0)
	{
	   count++;
	    num=num/2;
	}
	for(int j=3;j<=sqrt(num);j=j+2)
	{
	    while(num%j==0)
	    {
	        count++;
	        num=num/j;
	    }
	}
	if(num>2)
	{
	    count++;
	}
	return count;
}

int main() {
	int n;
	
	int k;
	int num;
	int i;
	
	cin>>n>>k;
	for(i=0,num=2;i<k;num++)
	{
	    if(countprime(num)==n)
	    {
	        cout<<num<<" ";
	        	    i++;
	    }

	    
	}

	return 0;
}
