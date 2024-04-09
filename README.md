# STUDENT-GRADE-CALCULATOR-CodeSoft


import java.util.Scanner;
class Main
  {
    public static void main(String args [])
    {
      // Taking input from the user..
      Scanner sc= new Scanner(System.in);
       System.out.print("Enter the Number of Subjects : ");

        int n = sc.nextInt();
      System.out.println("Marks obtained (out of 100) in each subject.");

      int marks;
      int total=0;

      for(int i=1 ; i<=n; i++)
        {
          System.out.print("Enter Subject " + i + " marks :  ");
           marks = sc.nextInt();
           total= total+marks;

        }



     System.out.println("Total Marks : " + total);

      double Marks_Avarage = Avarage(total,n);
      System.out.println("Avarage : " + Marks_Avarage );

      String Grade_Student= Grade(Marks_Avarage);
      System.out.println("Grade :" + Grade_Student);
    }


      // Avarage calculator..
    static double Avarage(int Total,int n)
    {
      double avarage = Total / n ;
      return avarage;
    }

    // Grade calculation
    static String Grade( double Marks_Avarage)
    {
        if(Marks_Avarage <20)
        {
            return "D";
        }
        else if(Marks_Avarage < 40)
        {
            return "C";
        }
        else if(Marks_Avarage < 60)
        {
            return "B";
        }
        else if(Marks_Avarage <=75)
        {
            return "B+";
        }
       else  if(Marks_Avarage <=85)
        {
            return "A";
        }
      else  if(Marks_Avarage <=95)
        {
            return "A+";
        }
       else if(Marks_Avarage <=100)
        {
            return "AA+";
        }

     else
        return null;

    }




  }

  
