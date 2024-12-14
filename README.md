# hostel-management
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
struct fees{
    int totalfees;
    int paidfees;
    int electricityfees;
    int remainingbalance;
};
struct studentdetails{
    char name[30];
    char fathername[30];
    char address[30];
    unsigned long phoneno;
    unsigned long phoneno1;
    int year;
    struct fees fee;
};
struct studentdetails details[100][3];
int input(char a[30],int room,int bedno);
int detailoutput(int room,int bedno);
int search();
int feesdefaulter();
int alldetails();
int allfeedetails();
int feedetails(int room,int bedno);
int totalpendingfee();
int main()
{
    int i=0,a,b,c,d,j;
    a=0,b=0,c=0,d=0;
    while(i==0)
    {
        printf("WELCOME TO ASUM HOSTEL\n");
        i++;
    }
    char username[30];
    char password[30];
    for(j=0;j<5;j++)
    {
        printf("ENTER USERNAME    :");
        scanf("%s",username);
        printf("ENTER PASSWORD   :");
        scanf("%s",password);
        if(strcmp(username,"naveen")==0)
        {
            if(strcmp(password,"warden123")==0)
            {
                printf("YOU HAVE SUCESSFULLY LOGIN\n");
                break;
            }
            else{
                if(j>=2)
                {
                    printf("HINT The PASSWORD IS YOUR DESIGNATION123\n");
                }
                if(j==3)
                {
                    printf("\n\nWARNING THIS IS YOUR LAST CHANCE TO ACCESS THE SYSTEM OR YOU WILL NOT BE ABLE TO ACCESS THE SYSTEM FOR 10 HOURS\n");
                }
                printf("you have entered  wrong password\n");
                continue;
            }
        }
        else if(strcmp(username,"ajay")==0)
        {
            {
               if(strcmp(password,"owner123")==0)
            {
                printf("YOU HAVE SUCESSFULLY LOGIN\n");
                break;
            }
            else{
                
                if(j>=2)
                {
                    printf("HINT The PASSWORD IS YOUR DESIGNATION123\n");
                }
                if(j==3)
                {
                    printf("\n\nWARNING THIS IS YOUR LAST CHANCE TO ACCESS THE SYSTEM OR YOU WILL NOT BE ABLE TO ACCESS THE SYSTEM FOR 10 HOURS\n");
                }
                printf("you have entered  wrong password\n");
                continue;
            }
            }
        }
        else if(strcmp(username,"jaipal")==0)
        {
            {
               if(strcmp(password,"owner2123")==0)
            {
                printf("YOU HAVE SUCESSFULLY LOGIN\n");
                break;
            }
            else{
                
                if(j>=2)
                {
                    printf("HINT The PASSWORD IS YOUR DESIGNATION123\n");
                }
                if(j==3)
                {
                    printf("\n\nWARNING THIS IS YOUR LAST CHANCE TO ACCESS THE SYSTEM OR YOU WILL NOT BE ABLE TO ACCESS THE SYSTEM FOR 10 HOURS\n");
                }
                printf("you have entered  wrong password\n");
                continue;
            }
            }
        }
        else
        {
            printf("your username dont match\n");
            continue;
        }
    }
    if(j==5)
    {
        printf("\n\nDUE TO MULTIPLE INVALID ENETRIES YOU CANT ACCESS THIS FOR 10 HOURS\n");
        return 0;
    }
    strcpy(details[0][0].name,"yash");
    strcpy(details[0][0].fathername,"yashf");
    strcpy(details[0][0].address,"rohtak");
    details[0][0].phoneno=78980;
    details[0][0].phoneno1=78980;
    details[0][0].year=2024;
    details[0][0].fee.totalfees=100000;
    details[0][0].fee.paidfees=30000;
    details[0][0].fee.electricityfees=123;
    
    strcpy(details[0][1].name,"vedansh");
    strcpy(details[0][1].fathername,"vedanshf");
    strcpy(details[0][1].address,"rohtak");
    details[0][1].phoneno=56876;
    details[0][1].phoneno1=56786;
    details[0][1].year=2024;
    details[0][1].fee.totalfees=100000;
    details[0][1].fee.paidfees=40000;
    details[0][1].fee.electricityfees=123;
    
    strcpy(details[0][2].name,"mayank");
    strcpy(details[0][2].fathername,"mayankf");
    strcpy(details[0][2].address,"bharatpur");
    details[0][2].phoneno=76878;
    details[0][2].phoneno1=76678;
    details[0][2].year=2024;
    details[0][2].fee.totalfees=100000;
    details[0][2].fee.paidfees=60000;
    details[0][2].fee.electricityfees=123;
    
    strcpy(details[1][0].name,"manish");
    strcpy(details[1][0].fathername,"mainshf");
    strcpy(details[1][0].address,"bahdurgarh");
    details[1][0].phoneno=58798;
    details[1][0].phoneno1=58798;
    details[1][0].year=2024;
    details[1][0].fee.totalfees=100000;
    details[1][0].fee.paidfees=62000;
    details[1][0].fee.electricityfees=312;
    
    strcpy(details[1][1].name,"piyush");
    strcpy(details[1][1].fathername,"piyushf");
    strcpy(details[1][1].address,"kolkata");
    details[1][1].phoneno=76879;
    details[1][1].phoneno1=76879;
    details[1][1].year=2024;
    details[1][1].fee.totalfees=100000;
    details[1][1].fee.paidfees=67000;
    details[1][1].fee.electricityfees=312;
    
    strcpy(details[1][2].name,"tejasva");
    strcpy(details[1][2].fathername,"tejasvaf");
    strcpy(details[1][2].address,"sonipat");
    details[1][2].phoneno=67898;
    details[1][2].phoneno1=67898;
    details[1][2].year=2024;
    details[1][2].fee.totalfees=100000;
    details[1][2].fee.paidfees=56000;
    details[1][2].fee.electricityfees=312;
    strcpy(details[2][0].name,"ashwani");
    strcpy(details[2][0].fathername,"ashwanif");
    strcpy(details[2][0].address,"gwalior");
    details[2][0].phoneno=56779;
    details[2][0].phoneno1=56779;
    details[2][0].year=2024;
    details[2][0].fee.totalfees=100000;
    details[2][0].fee.paidfees=54000;
    details[2][0].fee.electricityfees=678;
    
    strcpy(details[2][1].name,"rahul");
    strcpy(details[2][1].fathername,"rahulf");
    strcpy(details[2][1].address,"kota");
    details[2][1].phoneno=86789;
    details[2][1].phoneno1=86789;
    details[2][1].year=2024;
    details[2][1].fee.totalfees=100000;
    details[2][1].fee.paidfees=98000;
    details[2][1].fee.electricityfees=678;
    
    strcpy(details[2][2].name,"aditya");
    strcpy(details[2][2].fathername,"adityaf");
    strcpy(details[2][2].address,"banaras");
    details[2][2].phoneno=55567;
    details[2][2].phoneno1=55567;
    details[2][2].year=2024;
    details[2][2].fee.totalfees=100000;
    details[2][2].fee.paidfees=69000;
    details[2][2].fee.electricityfees=678;
    
    strcpy(details[3][0].name,"nishu");
    strcpy(details[3][0].fathername,"nishuf");
    strcpy(details[3][0].address,"saharanpur");
    details[3][0].phoneno=76897;
    details[3][0].phoneno1=76897;
    details[3][0].year=2024;
    details[3][0].fee.totalfees=100000;
    details[3][0].fee.paidfees=23000;
    details[3][0].fee.electricityfees=873;
    
    strcpy(details[3][1].name,"aryaveer");
    strcpy(details[3][1].fathername,"aryaveerf");
    strcpy(details[3][1].address,"jind");
    details[3][1].phoneno=67889;
    details[3][1].phoneno1=67889;
    details[3][1].year=2024;
    details[3][1].fee.totalfees=100000;
    details[3][1].fee.paidfees=65000;
    details[3][1].fee.electricityfees=873;
    
    strcpy(details[3][2].name,"narender");
    strcpy(details[3][2].fathername,"narenderf");
    strcpy(details[3][2].address,"jaipur");
    details[3][2].phoneno=45435;
    details[3][2].phoneno1=45435;
    details[3][2].year=2024;
    details[3][2].fee.totalfees=100000;
    details[3][2].fee.paidfees=32000;
    details[3][2].fee.electricityfees=873;
    
    strcpy(details[4][0].name,"vedu");
    strcpy(details[4][0].fathername,"veduf");
    strcpy(details[4][0].address,"bhratpur");
    details[4][0].phoneno=56783;
    details[4][0].phoneno1=56783;
    details[4][0].year=2024;
    details[4][0].fee.totalfees=100000;
    details[4][0].fee.paidfees=78000;
    details[4][0].fee.electricityfees=322;
    
    strcpy(details[4][1].name,"priyanshu");
    strcpy(details[4][1].fathername,"priyanshuf");
    strcpy(details[4][1].address,"faridabad");
    details[4][1].phoneno=67878;
    details[4][1].phoneno1=67878;
    details[4][1].year=2024;
    details[4][1].fee.totalfees=100000;
    details[4][1].fee.paidfees=53000;
    details[4][1].fee.electricityfees=322;
    
    strcpy(details[4][2].name,"gaurav");
    strcpy(details[4][2].fathername,"gauravf");
    strcpy(details[4][2].address,"ujjain");
    details[4][2].phoneno=68769;
    details[4][2].phoneno1=68769;
    details[4][2].year=2024;
    details[4][2].fee.totalfees=100000;
    details[4][2].fee.paidfees=78000;
    details[4][2].fee.electricityfees=692;
    while(1)
    {
        char z[30];
        printf("ENTER THE OPERATION YOU WANT TO DO\nINPUT\n DETAILOUPUT\nSEARCH\nFEESDEFAULTER\nALLDETAILS\nALLFEEDETAILS\nTOTALPENDING FEE\n");
        scanf("%s",z);
        if(strcmp(z,"input")==0)
        {
            char z1[30];
            int room;
            int bedno;
            printf("enter name of student\n");
            scanf("%s",z1);
            printf("enter room no");
            scanf("%d",&room);
            printf("enter bed number");
            scanf("%d",&bedno);
            input(z1,room,bedno);
        }
        else if(strcmp(z,"detailoutput")==0)
        {
            int room;
            int bedno;
            printf("enter room no");
            scanf("%d",&room);
            printf("enter bed number");
            scanf("%d",&bedno);
            detailoutput(room,bedno);
        }
        else if(strcmp(z,"search")==0)
        {
            search();
        }
        else if(strcmp(z,"feesdefaulter")==0)
        {
            feesdefaulter();
        }
        else if(strcmp(z,"alldetails")==0)
        {
            alldetails();
        }
        else if(strcmp(z,"allfeedetails")==0)
        {
            int room;
            int bedno;
            printf("ENTER ROOM NUMBER");
            scanf("%d",room);
            printf("ENTER BED NUMBER");
            scanf("%d",&bedno);
            feedetails(room,bedno);
        }
        else if(strcmp(z,"totalpendingfee")==0)
        {
          totalpendingfee();
        }
        else
        {
            printf("INVALID OPERATION");
        }
        char k[30];
        printf("DO YOU WANT TO CONTINUE OPERATIONS\n");
        scanf("%s",&k);
        if(strcmp(k,"yes")==0)
        {
            continue;
        }
        else
        {
            break;
        }

    }
    char x[30];
    printf("\n\nTHANK YOU FOR USING OUR SYSTEM \n");
    scanf("%s",x);
    return 0;
}
int input(char a[30],int room,int bedno)
{
  int length=strlen(a);
    strcpy(details[room][bedno].name,a);
  
  printf("fathername is              ");
  scanf("%s",details[room][bedno].fathername);
  printf("enter phone number2        ");
  scanf("%lu",&details[room][bedno].phoneno1);
  printf("enter year of btech        ");
  scanf("%lu",&details[room][bedno].year);
  printf("enter city                 ");
  scanf("%s",details[room][bedno].address);
  printf("enter fees paid            ");
  scanf("%d",&details[room][bedno].fee.paidfees);
  details[room][bedno].fee.totalfees=100000;
  printf("electricity intial fees paid");
  scanf("%d",&details[room][bedno].fee.electricityfees);
  printf("remaining balance=%d         ",details[room][bedno].fee.totalfees-details[room][bedno].fee.paidfees);
return 0;
}
int detailoutput(int room,int bedno)
{
    strupr(details[room][bedno].name);
    strupr(details[room][bedno].fathername);
    printf("\n\nstudent name =          %s \n",details[room][bedno].name);
    printf("father name =           %s \n",details[room][bedno].fathername);
    printf("phone no :              %lu\n",details[room][bedno].phoneno);
    printf("phone no 2:             %lu\n",details[room][bedno].phoneno1);
    printf("year is                 %d\n",details[room][bedno].year);
    printf("address is              %s\n",details[room][bedno].address);
    printf("paid fees =             %d\n",details[room][bedno].fee.paidfees);
    printf("total fees =            %d\n",details[room][bedno].fee.totalfees);
    printf("reamainning fees =      %d\n",details[room][bedno].fee.totalfees-details[room][bedno].fee.paidfees);
    printf("room no is %d bed number is %d",room,bedno);
    return 0;
}
int search()
{
    char s[30],s1[30];
    printf("from which detail you want to use\n");
    scanf("%s",s);
    if(strcmp(s,"name")==0)
    {
        printf("enter name\n");
        scanf("%s",s1);
        int i,j,var;
        for(int i=0;i<100;i++)
        {
            for(int j=0;j<3;j++)
            {
                var=strcmp(details[i][j].name,s1);
                if(var==0)
                {
                    detailoutput(i,j);
                }
            }
        }
    }
    else if(strcmp(s,"fathername")==0)
    {
        printf("enter father name\n");
        scanf("%s",s1);
        int i,j,var;
        for(int i=0;i<100;i++)
        {
            for(int j=0;j<3;j++)
            {
                var=strcmp(details[i][j].fathername,s1);
                if(var==0)
                {
                    detailoutput(i,j);
                }
            }
        }
    }
    else if(strcmp(s,"phoneno")==0)
    {
        unsigned long int phone;
         printf("enter phoneno\n");
         scanf("%lu",&phone);
         
        int i,j,var;
        for(int i=0;i<100;i++)
        {
            for(int j=0;j<3;j++)
            {
                
                if(details[i][j].phoneno==phone)
                {
                    detailoutput(i,j);
                }
            }
        }
    }
    else if(strcmp(s,"address")==0)
    {
        printf("enter city name\n");
        scanf("%s",s1);
        int i,j,var;
        for(i=0;i<100;i++)
        {
            for(j=0;j<3;j++)
            {
                var=strcmp(details[i][j].address,s1);
                if(var==0)
                {
                    detailoutput(i,j);
                }
            }
        }
    }
    return 0;

}
int feesdefaulter()
{
    int remfees,a;
    a=1;
    for(int i=0;i<100;i++)
    {
        for(int j=0;j<3;j++)
        {
           remfees=details[i][j].fee.totalfees-details[i][j].fee.paidfees;
           if(remfees>50000)
           {
            while(a==1)
            {
                printf("name of defaulters are\n");
                a++;
            }
            printf("%s\n",details[i][j].name);
           }
        }
    }
    char b[30];
    printf("do you want to contact them\n");
    scanf("%s",b);
    int com;
    com=strcmp(b,"yes");
    if(com==0)
    {
        for(int i=0;i<100;i++)
    {
        for(int j=0;j<3;j++)
        {
           remfees=details[i][j].fee.totalfees-details[i][j].fee.paidfees;
           if(remfees>50000)
           {
            while(a==1)
            {
                printf("name of defaulters are\n");
                a++;
            }
            printf("%s\n",details[i][j].name);
            printf("contact number %lu\n\n",details[i][j].phoneno);
           }
        }
    }
    }
    return 0;
}
int alldetails()
{
    for(int i=0;i<100;i++)
    {
        for(int j=0;j<3;j++)
        {
            if(details[i][j].name[0]!='\0')
            {detailoutput(i,j);
            printf("\n\n\n");
            }
        }
    }
    return 0;
}
int allfeedetails()
{
    int i,j;
    for(i=0;i<100;i++)
    {
        for(j=0;j<3;j++)
        {
             if(details[i][j].name[0]!='\0')
             {
            printf("%s remainingfees=%d\n\n",details[i][j].name,details[i][j].fee.totalfees-details[i][j].fee.paidfees);
             }
        }
    }
    return 0;
}
int totalpendingfee()
{
    int n=0,pendingfee=0;
    for(int i=0;i<100;i++)
    {
        for(int j=0;j<3;j++)
        {
            if(details[i][j].name[0]!='\0')
            {
              n++;
              pendingfee=pendingfee+details[i][j].fee.totalfees-details[i][j].fee.paidfees;

            }
        }
    }
    printf("the total pending fee is %d\n",pendingfee);
    char a[30];
    printf("do you want to get the deatils of remaining fee\n");
    scanf("%s",a);
    if(strcmp(a,"yes")==0)
    {
    for(int i=0;i<100;i++)
    {
        for(int j=0;j<3;j++)
        {
            if(details[i][j].name[0]!='\0')
            {
              pendingfee=details[i][j].fee.totalfees-details[i][j].fee.paidfees;
              printf("%s   pending fee = %d\n",details[i][j].name,pendingfee);
            }
        }
    }
    }
    return 0;

}
int feedetails(int room,int bedno)
{
   detailoutput(room,bedno);
   return 0;
}
