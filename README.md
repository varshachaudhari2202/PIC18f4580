# PIC18f4580
Projects, code examples, and notes for PIC18F4580 microcontroller.

///1st LED Blink///
#include<p18f4580.h>
#define led1 PORTBbits.RB1
#define led2 PORTBbits.RB2
#define led3 PORTBbits.RB3

///Provide the Direction
#define dir_LED1 TRISBbits.RB1
#define dir_LED2 TRISBbits.RB2
#define dir_LED3 TRISBbits.RB3

void delay(int a)
{
	int i,j;
	for(i=0; i<a; i++)
	for(j=0; j<100; j++);
}
void main()
{
	dir_LED1=0; ///led as a o/p(0)///direction is provide 0
	dir_LED2=0;
	dir_LED3=0;
	while(1)
	{
		
		led1=led2=led3=1; /// LED ON=1// LED OFF=0
		delay(1000);
		led1=led2=led3=0; ///LED off=0
		delay(1000);
		
	}	
}
