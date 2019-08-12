#include<fstream.h>
#include<conio.h>
#include<dos.h>
#include<process.h>
#include<string.h>
#include<stdio.h>
#include<stdlib.h>
class account
{
	char fname[20],lname[20],gender[8],f_name[20],adr[40],email[35],mob[11],dob[20];
	int age;
public:
	double inv;
	void get();
	void show();
	void change(int c);
}s;
void account::get()
{
	clrscr();
	gotoxy(12,1);
	cout<<"\t\t#### ACCOUNT DETAILS #####\n\n";
	gotoxy(6,3);
	cout<<"First Name: ";
	gets(fname);
	gotoxy(6,5);
	cout<<"Last Name: ";
	gets(lname);
	gotoxy(6,7);
	cout<<"Father's Name: ";
	gets(f_name);
	gotoxy(6,9);
	cout<<"Gender: ";
	gets(gender);
	gotoxy(6,11);
	cout<<"Address: ";
	gets(adr);
	gotoxy(6,13);
	cout<<"Age: ";
	cin>>age;
	gotoxy(6,15);
	cout<<"Date of Birth: ";
	gets(dob);
	gotoxy(6,17);
	cout<<"Email: ";
	gets(email);
	gotoxy(6,19);
	cout<<"Mobile No.: ";
	gets(mob);
	gotoxy(6,22);
	cout<<"Initial Investment: ";
	cin>>inv;
	getch();
}
void account::show()
{
	clrscr();
	gotoxy(17,3);
	cout<<"#### ACCOUNT DETAILS #####\n\n\n";
	cout<<"\tFirst Name: "<<fname<<endl
		<<"\n\tLast Name: "<<lname<<endl
		<<"\n\tFather's Name: "<<f_name<<endl
		<<"\n\tGender: "<<gender<<endl
		<<"\n\tAddress: "<<adr<<endl
		<<"\n\tAge: "<<age<<endl
		<<"\n\tDate of Birth: "<<dob<<endl
		<<"\n\tEmail: "<<email<<endl
		<<"\n\tMobile No.:"<<mob<<endl
		<<"\n\tInitial Investment: "<<inv;
	getch();
}
void account::change(int c)
{
	clrscr();
	if(c==1)
	{
		gotoxy(10,10);
		cout<<"Original First Name: "<<fname;
		gotoxy(10,12);
		cout<<"Enter new name: ";
		gets(fname);
	}
	else if(c==2)
	{
		gotoxy(10,10);
		cout<<"Original Last Name: "<<lname;
		gotoxy(10,12);
		cout<<"Enter new name: ";
		gets(lname);
	}
	else if(c==5)
	{
		gotoxy(10,10);
		cout<<"Original Gender: "<<gender;
		gotoxy(10,12);
		cout<<"Enter new gender: ";
		gets(gender);
	}
	else if(c==3)
	{
		gotoxy(10,10);
		cout<<"Original Father's Name: "<<f_name;
		gotoxy(10,12);
		cout<<"Enter new name: ";
		gets(f_name);
	}
	else if(c==4)
	{
		gotoxy(10,10);
		cout<<"Original Address: "<<adr;
		gotoxy(10,12);
		cout<<"Enter new address: ";
		gets(adr);
	}
	else if(c==8)
	{
		gotoxy(10,10);
		cout<<"Original Email: "<<email;
		gotoxy(10,12);
		cout<<"Enter new email: ";
		gets(email);
	}
	else if(c==6)
	{
		gotoxy(10,10);
		cout<<"Original Age: "<<age;
		gotoxy(10,12);
		cout<<"Enter new age: ";
		cin>>age;
	}
	else if(c==7)
	{
		gotoxy(10,10);
		cout<<"Original Date of Birth: "<<dob;
		gotoxy(10,12);
		cout<<"Enter new date of birth: ";
		gets(dob);
	}
	else if(c==9)
	{
		gotoxy(10,10);
		cout<<"Original Mobile No.:  "<<mob;
		gotoxy(10,12);
		cout<<"Enter new mobile no: ";
		gets(mob);
	}
	else if(c==10)
	{
		gotoxy(10,10);
		cout<<"Original investment: "<<inv;
		gotoxy(10,12);
		cout<<"Enter new investment: ";
		cin>>inv;
	}
	else
		cout<<"NOT VALID";
	getch();
}


void main()
{
	clrscr();
	int ch,i,ch1,flag=0,ch2,ch3,ch4;
	fstream f1,f2;
	while(1)
	{
		clrscr();
		gotoxy(13,3);
		cout<<"#### WELCOME TO ####\n"
			<<"\n\t1. Create an account"<<endl
			<<"\n\t2. user login"<<endl
			<<"\n\t3. authorized login"<<endl
			<<"\n\t4. Exit"<<endl
			<<"\n\n enter choice=";
		cin>>ch;
		switch(ch)
		{
			case 1:while(1)
					 {
						clrscr();
						{
							gotoxy(14,2);
							cout<<"\t\t\t#### WELCOME TO ####\t\t\t\n"
								 <<"\n\t1. Input Details"<<endl
								 <<"\n\t2. Check Details"<<endl
								 <<"\n\t3. Change Detail"<<endl
								 <<"\n\t4. Save account"<<endl
								 <<"\n\n enter choice=";
							cin>>ch1;
							switch(ch1)
							{
								case 1:flag=1;
										 s.get();
										 break;
								case 2:if(flag==1)
										 s.show();
										 else
										 {
											clrscr();
											cout<<"\n\n\t...first input information...";
											getch();
										 }
										 break;
								case 3:clrscr();
										 if(flag==1)
										 {
											gotoxy(13,1);
											cout<<"\t\t## CHANGE DETAILS ###\n\n";
											cout<<"\n\t1. Fisrt name"<<endl
												 <<"\n\t2. Last name"<<endl
												 <<"\n\t3. Father's name"<<endl
												 <<"\n\t4. Address"<<endl
												 <<"\n\t5. Gender"<<endl
												 <<"\n\t6. Age"<<endl
												 <<"\n\t7. Date of Birth"<<endl
												 <<"\n\t8. Email"<<endl
												 <<"\n\t9. Mobile No."<<endl
												 <<"\n\t10.Initial Investment"<<endl
												 <<"\nenter choice=";
											int ch2;
											cin>>ch2;
											s.change(ch2);
										 }
										 else
										 {
											clrscr();
											cout<<"\n\n\t...first input information...";
											getch();
										}
										break;
								case 4:if(flag==1)
										 {
											f1.open("acc.dat",ios::binary|ios::out);
											f1.write((char*)&s,sizeof(s));
											f1.close();
											clrscr();
											int n;
											char pass[20];
											gotoxy(5,9);
											randomize();
											n=random(10000);
											f2.open("pass.txt",ios::out);
											cout<<"your id : "<<n<<endl;
											cout<<"\n    enter password : ";
											gets(pass);
											f2<<n;
											f2<<pass<<'\n';
											f2.close();
											delay(150);
											cout<<"\n\n\n\t\t\tEXITING TO MAIN MENU";
											delay(200);
											cout<<" . ";
											delay(200);
											cout<<" . ";
											delay(200);
											cout<<" . ";
											delay(100);
										 }
										 else
										 {
											clrscr();
											cout<<"\n\n\t...first input info...";
											getch();
										 }
										 break;
							}
						}
					 if(ch1==4&&flag==1)
							break;
					 }
					 break;
			case 2:while(1)
					 {
						clrscr();
						gotoxy(13,1);
						cout<<"\t\t\t#### WELCOME TO ####\t\t\t\n"
							 <<"\n\t1. account details"<<endl
							 <<"\n\t2. transactions"<<endl
							 <<"\n\t3. current balance"<<endl
							 <<"\n\t4. change profile"<<endl
							 <<"\n\t5. log out"<<endl
							 <<"\n\n enter choice=";
						cin>>ch2;
						if(ch2==5)
							break;
						else
						{
							switch(ch2)
							{
								case 1:s.show();
										 break;
								case 2:clrscr();
									   cout<<"\t\t\t#### WELCOME TO ####\t\t\t\n"
										   <<"\n\t1. Deposit"<<endl
										   <<"\n\t2. Withdraw"<<endl
										   <<"\n\t3. Transfer"<<endl
										   <<"\n\n enter choice=";
									   cin>>ch3;
									   switch(ch2)
									   {
											case 1:
												break;
											case 2:
												break;
											case 3:
													break;
									   }
									   break;
								case 3:s.inv;
										 break;
								case 4:clrscr();
										 cout<<"\t\t## CHANGE DETAILS ###\n\n";
										 cout<<"\n\t1. First name"<<endl
											  <<"\n\t2. Last name"<<endl
											  <<"\n\t3. Father's name"<<endl
											  <<"\n\t4. Address"<<endl
											  <<"\n\t5. Gender"<<endl
											  <<"\n\t6. Age"<<endl
											  <<"\n\t7. Date of Birth"<<endl
											  <<"\n\t8. Email"<<endl
											  <<"\n\t9. Mobile No."<<endl
											  <<"\n\n enter choice=";
										 cin>>ch4;
										 s.change(ch4);
										 break;
							 }

						 }
					}
					break;
			case 3:
					break;
			case 4: exit(0);
			default:clrscr();
					cout<<"\n\n@@@@ NOT A VALID CHOICE @@@@";
					getch();
		}
	}
	getch();
}

