# Union-of-sorted-array
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    
	    Scanner op = new Scanner(System.in);
	    System.out.println("Enter the size of first Array:- ");
	    int m = op.nextInt();
	    int A[] = new int[m];
	    System.out.println("Enter the elements of first Array:- ");
	    for(int i=0;i<m;i++)
	    {
	        A[i] = op.nextInt();
	    }
	    System.out.println("");
	    
	    System.out.println("Enter the size of 2nd Array:- ");
	    int n = op.nextInt();
	    int B[] = new int[n];
	    System.out.println("Enter the elements of 2nd Array:- ");
	    
	     for(int i=0;i<n;i++)
	    {
	        B[i] = op.nextInt();
	    }
	    System.out.println("");
	    System.out.println("Elements after union of 1st and 2nd array are:- ");
	    
        int x=0;
        int y=0;
        int count=0;
        
        while(x<m && y<n)
        {
            if(A[x]<B[y])
            {
            System.out.println(A[x]);
            x++;
            count++;
            }
            else if(A[x]>B[y])
            {
                System.out.println(B[y]);
                y++;
                count++;
            }
            else if(A[x]==B[y])
            {
                System.out.println(A[x]);
                x++;
                y++;
                count++;
            }
        }
        
        for(;x<m;x++)
        {
            System.out.println(A[x]);
            count++;
        }
        for(;y<n;y++)
        {
            System.out.println(B[y]);
            count++;
        }
        System.out.println("");
        System.out.println("Number of elements in the Union are:- "+count);
	    
	}
}
