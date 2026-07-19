import java.util.Scanner;
class Diagonal
{
    static boolean Diagonal(int[][] mat,int size)
    {
        for(int i=0;i<size;i++)
        {
            for(int j=0;j<size;j++)
            {
                if(i!=j&&mat[i][j]!=0)
                {
                    return false;
                }
            }
        }
        return true;
    }
    public static void main(String[]args)
    {
        Scanner sc=new Scanner(System.in);
        int size=sc.nextInt();
        int[][] mat=new int[size][size];
        for(int i=0;i<size;i++)
        {
            for(int j=0;j<size;j++)
            {
                mat[i][j]=sc.nextInt();
            }
        }
        boolean res=Diagonal(mat,size);
        if(res)
        {
            System.out.print("Yes");
        }
        else
        {
            System.out.print("No");
        }
    }


