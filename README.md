# JavaProgram
Collectiva
// You are using Java
import java.util.regex.*;
import java.util.*;
class hello
{
    public static void main(String[]args)
    {
        Scanner scan=new Scanner(System.in);
        String a=scan.nextLine();
        String a1=scan.nextLine();
        String b="^\\d{10}$";
        String c="^\\d{2}\\w{3}\\d{4}$";
        String d="^[\\d\\w]*$";
        if(a.length()!=10&&a1.length()!=9)
        {
            System.out.println("Invalid");
        }
        else
        {
        try{
            if(a.length()!=10)
            {
                System.out.println("Invalid");
                throw new IllegalArgumentException("Mobile Number Should contains 10 digits");
            }
            Pattern r=Pattern.compile(b);
            Matcher m=r.matcher(a);
        
        if(m.matches())
        {
            System.out.println("valid");
        }
        else
        {
            System.out.println("Invalid");
            throw new NumberFormatException("Mobile Number should contain only 10 Number");
        }
        try{
            
            if(a1.length()!=9)
            {
                System.out.println("Invalid");
                throw new IllegalArgumentException("Register Number does not contain exactly 9 characters");
            }
            Pattern rr=Pattern.compile(d);
            Matcher mm=rr.matcher(a1);
            if(mm.matches())
            {
                System.out.print("");
            }
          
            else
            {
           System.out.println("Invalid");
            throw new NoSuchElementException("Registration Number cannot contain any character other than digits and alphabets in format specified");
            }
            try{
                if(a1.length()!=9)
                {
                    System.out.println("Invalid");
                    throw new IllegalArgumentException("Register Number does not contain exactly 9 characters");
                }
                Pattern rr1=Pattern.compile(c);
                Matcher mm1=rr1.matcher(a1);
                if(mm1.matches())
                {
                    System.out.println("valid");
                }
                else{
                    System.out.println("Invalid");
                    throw new IllegalArgumentException("Register Number does not contain exactly 9 characters");
                }
                
            }
            catch(Exception e)
            {
                System.out.println(e);
            }
        }
        catch (Exception e)
        {
            System.out.println(e);
        }
        }
            
        
        catch(Exception e)
        {
            System.out.println(e);
        }
        }
       
        
    }
}
