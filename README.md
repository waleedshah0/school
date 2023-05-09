# school
School Management System in C++
#include<stdio.h>
#include<string.h>

int Registration()
{
    char name[30];
    FILE *fptr;


    int age, Contact_number, Photo;
    char Student_name[100], Birth_Date[10], Fathers_name[100], Mothers_name[100], Permanent_Address[100], Present_Address[100], Gender[10];
    fptr = fopen("Registration.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the Student_name\n");
    scanf("%s", Student_name);

    printf("Enter the age \n");
    scanf("%d", &age);

    printf("Enter the Birth Date\n");
    scanf("%s", Birth_Date);

    printf("Enter the Fathers_name\n");
    scanf("%s", Fathers_name);

    printf("Enter the Mothers_name \n");
    scanf("%s", Mothers_name);
    printf("Enter the Gender\n");
    scanf("%s", &Gender);

    printf("Enter the Permanent_Address\n");
    scanf("%s", Permanent_Address);

    printf("Enter the Present_Address\n");
    scanf("%s", Present_Address);

    printf("Enter the Contact_number\n");
    scanf("%d", &Contact_number);

    printf("Enter the  Photo\n");
    scanf("%d", & Photo);

    fprintf(fptr,"Student_name: %s \t|\t Age: %d \t|\t Birth Date: %s \t|\t Fathers name: %s \t|\t  Mothers name: %s \t|\t  Gender: %s \t|\t  Permanent_Address: %s \t|\t Present_Address: %s \t|\t Contact_number: %d \t|\t Photo: %d\n  ", Student_name, age, Birth_Date, Fathers_name, Mothers_name, Gender, Permanent_Address, Present_Address, Contact_number, Photo);

    fclose(fptr);


    FILE *fp;
    char buff[255];
    fp = fopen("Registration.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}


int registration()
{
    printf(" Registration OF THE PROJECT: \n");
    printf("1. ADD Info \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        Registration();
        break;


    default:
        printf("Wrong Input\n");

    }

}

int students_info()
{
    char name[30];
    FILE *fptr;


    int section, roll, shift;
    char students_name[100];
    fptr = fopen("students_info.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the students_name: ");
    scanf("%s", &students_name);
    printf("Enter the section: ");
    scanf("%d", &section);
    printf("Enter the roll: ");
    scanf("%d", &roll);
    printf("Enter the shift: ");
    scanf("%d", &shift);

    //Save Student information into file.
    fprintf(fptr,"Student Name: %s \t|\t Section: %d \t|\t Roll: %d \t|\t Shift: %d\n", students_name, section, roll, shift);

    fclose(fptr);

    FILE *fp;
    char buff[255];
    fp = fopen("students_info.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}



 int Student_information_system()
{
    printf(" Student information system OF THE PROJECT: \n");
    printf("1. students_info \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        students_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}
//rterughitegr

int teachers_info()
{
    char name[30];
    FILE *fptr;


    int Age, Salary, Contact_number;
    char teachers_name[100],Gender[100], marital_status[100];
    fptr = fopen("teachers_info.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the teachers_name\n");
    scanf("%s", &teachers_name);

    printf("Enter the Age \n");
    scanf("%d", &Age);

    printf("Enter the Gender\n");
    scanf("%s", &Gender);

    printf("Enter the marital_status\n");
    scanf("%s", &marital_status);

    printf("Enter the Salary\n");
    scanf("%d", &Salary);

    printf("Enter the Contact_number\n");
    scanf("%d", &Contact_number);


    fprintf(fptr,"teachers_name: %s \t|\t Age: %d \t|\t Gender: %s \t|\t marital_status: %s \t|\t Salary: %d \t|\t Contact_number: %d\n", teachers_name, Age, Gender, marital_status,Salary, Contact_number);

    fclose(fptr);

    FILE *fp;
    char buff[255];
    fp = fopen("teachers_info.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}



int teacher_information_system()
{
    printf(" Teacher information system OF THE PROJECT: \n");
    printf("1. teachers_info \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        teachers_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}

int stuffs_info()
{
    char name[30];
    FILE *fptr;


    int Age, Salary, Contact_number;


    char stuffs_name[100],marital_status[100],Gender[100];
    fptr = fopen("stuffs_info.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the stuffs name\n");
    scanf("%s", &stuffs_name);

    printf("Enter the Age \n");
    scanf("%d", &Age);

    printf("Enter the Gender\n");
    scanf("%s", &Gender);

    printf("Enter the marital_status\n");
    scanf("%s", &marital_status);

    printf("Enter the Salary\n");
    scanf("%d", &Salary);

    printf("Enter the Contact_number\n");
    scanf("%d", &Contact_number);

    fprintf(fptr,"stuffs_name: %s \t|\t Age: %d \t|\t Gender: %s \t|\t marital_status: %s \t|\t Salary: %d \t|\t Contact_number : %d \t|\t,", stuffs_name, Age, Gender, marital_status, Salary, Contact_number);

    fclose(fptr);

    FILE *fp;
    char buff[255];
    fp = fopen("stuffs_info.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}



 int stuff_information_system()
{
    printf(" Stuff information system OF THE PROJECT: \n");
    printf("1. stuffs_info \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        stuffs_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}



int school_fee_info()
{
    char name[30];
    FILE *fptr;


    int Online_payment , No_late_fees , Unpaid_school_fees;


    fptr = fopen("school_fee_info.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the Online_payment\n");
    scanf("%d", &Online_payment);

    printf("Enter the No_late_fees \n");
    scanf("%d", &No_late_fees);

    printf("Enter the Unpaid_school_fees\n");
    scanf("%d", &Unpaid_school_fees);

    fprintf(fptr,"Online_payment: %d \t|\t No_late_fees: %d \t|\t Unpaid_school_fees: %d\n", Online_payment, No_late_fees, Unpaid_school_fees);

    fclose(fptr);

    FILE *fp;
    char buff[255];
    fp = fopen("school_fee_info.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}

 int school_fee_system()
{
    printf(" School fee system OF THE PROJECT: \n");
    printf("1. school fee info \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        school_fee_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}

int result_info()
{
    char name[30];
    FILE *fptr;


    int Class, Roll, Section;
    float Result_GPA;
    char students_name[100];
    fptr = fopen("result_info.txt", "a");/*  Change File open mode w+ to a for add new information in file */
    if (fptr == NULL)
    {
        printf("File does not exists \n");
        return;
    }
    printf("Enter the students_name\n");
    scanf("%s", &students_name);

    printf("Enter the Class \n");
    scanf("%d", &Class);

    printf("Enter the Roll\n");
    scanf("%d", &Roll);

    printf("Enter the Section\n");
    scanf("%d", &Section);

    printf("Enter the Result_GPA\n");
    scanf("%f", &Result_GPA);



   fprintf(fptr,"students_name: %s \t|\t Class: %d \t|\t Section: %d \t|\t Result_GPA: %.2f\n", students_name, Class, Section, Result_GPA);

    fclose(fptr);

    FILE *fp;
    char buff[255];
    fp = fopen("result_info.txt", "r");

   //Change while loop fscanf() to fputs()
   while(fgets(buff, sizeof(buff), fp) != NULL)
    {
        fputs(buff, stdout);
        fputs("\n\n", stdout);
    }
   fclose(fp);
}


int result_management()
{
    printf(" Result management system OF THE PROJECT: \n");
    printf("1. result_management \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        result_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}



  int facilities()
{
    char name[30];
    FILE *fptr;




    printf("1.Library\n2.Common room\n3.Wash room\n4.Stuff room\n5.Canteen\n6.Playing ground\n7.Bus transport\n8.Lab room");
    fprintf(fptr, "facilities= %f\n", facilities);
    fclose(fptr);

    FILE *fp;
   char buff[255];//creating char array to store data of file
   fp = fopen("facilities.txt", "r");
   while(fscanf(fp, "%s", buff)!=EOF){
   printf("%s ", buff);
   }
   fclose(fp);
}


int Facilities()
{
    printf(" Result management system OF THE PROJECT: \n");
    printf("1. facilities \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        result_info();
        break;


    default:
        printf("Wrong Input\n");

    }

}














int User()
{

    char saved_name[] = "neyamul";
    char saved_pass[] = "1234";
    // FILE *fptr;

    char password[30];
    char username[30];
    printf("WELCOME\nPLEASE ENTER YOUR USERNAME AND PASSWORD\n");
    printf("USERNAME: ");
    scanf("%s", username);
    printf("PASSWORD: ");
    scanf("%s", password);

    if(strcmp(saved_name, username)==0 && strcmp(saved_pass, password)==0)
        printf("LOGIN SUCCESSFUL. PLEASE GO TO THE ADMIN PANEL\n\n\n\n");
    else
        printf("LOGIN FAILED, WRONG USERNAME / PASSWORD\n\n\n\n");

}

int Admin()
{
    printf("ADMIN PANEL OF THE PROJECT: \n");
    printf("1. Registration \n");
    printf("2. Student information system: \n");
    printf("3. Teacher information system: \n");
    printf("4. Staff information system: \n");
    printf("5. ​School fee system : \n");
    printf("6. Result management: \n");
    printf("7. Facilities: \n");

    int ch;
    printf("Enter your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        Registration();
        break;
    case 2:
        Student_information_system();
        break;
    case 3:
        teacher_information_system();
        break;
    case 4:
        stuff_information_system();
        break;
    case 5:
        school_fee_system();
        break;
    case 6:
        result_management();
        break;
    case 7:
        facilities();
        break;

    default:
        printf("Wrong Input\n");

    }
}

int main()
{
    printf("PROJECT NAME : SCHOOL MANAGEMENT SYSTEM\n\n\n\n\n\n");
    printf("\n\n\n\n\n");
    printf("\n\t\t\t**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**");
    printf("\n\t\t\t***       =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=       ***");
    printf("\n\t\t\t**  *     =                 WELCOME                   =     *  **");
    printf("\n\t\t\t**    *   =                   TO                      =   *    **");
    printf("\n\t\t\t**      * =                 SCHOOL                    = *      **");
    printf("\n\t\t\t**    *   =               MANAGEMENT                  =   *    **");
    printf("\n\t\t\t**  *     =                 SYSTEM                    =     *  **");
    printf("\n\t\t\t***       =-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=       ***");
    printf("\n\t\t\t**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**-**");
    printf("\n\n\n\t\t\t Enter any key to continue.....\n");
    getch();
    printf("1. USER LOGIN\n");
    printf("2. ADMIN LOGIN\n");
    int ch;
    printf("Enter Your Choice: ");
    scanf("%d", &ch);
    switch(ch)
    {
    case 1:
        User();
        break;
    case 2:
        Admin();
        break;

    default:
        printf("Wrong Input\n");
    }

    return 0;
}
