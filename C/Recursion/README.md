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



//Recurrence Relation
Time Complexity of recursion--> for eg: if it takes above eg the time is 

T(n)=[1,T(n-1)+2,n=0,n>0 here n=0-> whenever the if conditions fails it takes time values as 1
the time taken by the function depends by the number of calls



//static and global variables in recursion
why static variable doesnt change during execution? -> bcoz it will created in the main memory not in the stack or heap, and also stacic and global variable have a 
seperate subset of memory under main memory. static variable is created at the loading time of the program so it will not get lost through function call.

so it will remain when returns to the another function even in the local variable named static

*imp: whenever you need to call the same function another time while the passing argumemt/variable is static or global then the value stored in the variable
will be same still the last value bcoz it will not deleted from the memory it will be accesible to all the program


//Types of recursion
1.Tail Recursion -> All the operations will be done by only at the calling phase, nothing will be done during returning phase even during the function return everthing will be done in calling phase
	         -> time is same for both if/loop statement is o(n);
                 -> but in the space constraints looping is more efficient  because in recursion func again calling so it will allocate code activiation record in the stack 
                  so in looping space=o(1) bcoz it is use while and -- so it taking 1 but in recursion using n so space is allocate in stack and returns with o(n)
2.Head Recursion -> 
3.Tree Recursion 
4.Indirect Recursion
5.Nested Recursion










