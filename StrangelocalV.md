
for (int i = 0; i < 10; i++)
	{
		int *d;
		{
			int p;
			printf("%p\n", &p);
			d = &p;
			p = i;
		}//at.compare_exchange_strong(p, i);
		printf("%d\n", *d);
	}