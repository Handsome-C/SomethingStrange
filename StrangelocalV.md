/**
Obviously, var p is local var.
But ,even if p is out the scope,we can still read the value by address;
*/
for (int i = 0; i < 10; i++)
{
	int *d;
	{
		int p;
		printf("%p\n", &p);
		d = &p;
		p = i;
	}
	printf("%d\n", *d);
}

/**
First time,var p is declared,and its value is strange value,
but in the rest times,the p's value will be 0,1,2,...8;
*/
for(int i=0;i<10;i++)
{
	int p;
	p=i;
}
