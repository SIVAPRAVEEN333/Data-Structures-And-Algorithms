function calls itself called recursion, it should have condition checking statement
otherwise it's leads to the infinite loop

*Recursion has two Phase:
	1.Calling Phase
	2.Returning Phase

1.Calling Phase:
	printf("\n %d",x);            //processing while calling
        fun1(x-1);
excution process will be done before calling is called calling phase, it will excute in ascending order
before the function ends.

2. Returning Phase:
	fun1(x-1);
	printf("%d",x);
excution processs will not be done during calling, after all the calling will happen
the returning will gets happen that time process will be excuted.




*Recursion in stack memory while executing:
//calling phase
Void fun(int n)
{
	if(n>0)
	{
	printf("%d",n);
	fun(n-1);
	}
}

void main()
{
	int x=3;		
	fun(x);
}

1.first the x=3; this will create a space in the stack,
2.after the fun(x) called the local varibale inside the fun n will create a code activitation record for 
each function executes.
3.it will increase the stack size taken until n>0
4.n=3,n=2,n=1 each time every stack frame will be allocated separatly it called as code activitation record
5. this code activition record from stack will be deleted while the recursion returning from the stack
6. atlast all the record will be delted only x=3 will be remain in the stack. no record will be there for fun(x);



total memory consume is o(n);

total calls is (n+1);//activation record created list in fun();


//returning phase:

it is also same memory allocation in stack like calling phase but... it will be delete the top most acttivation record
until the last function called. 
whenever in the function called itself the stack will be created in activation method this is in ascending phase 
and each calling has a seperate activiation record. atlast every function is returning the activaqtion record also
delets from the stack so there is no more any record of the particular record









