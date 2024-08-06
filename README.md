import java.util.Scanner;
import java.util.ArrayList;
import java.util.List;
import java.util.*;
public class Main{
    public static void main(String[]Args){
        Scanner sc=new Scanner(System.in);
        //getting input
        System.out.print("Enter Boy name:");
        String name1=sc.nextLine();
        System.out.print("Enter Girl name:");
        String name2=sc.nextLine();
        //creating empty list
        List<Character>l1=new ArrayList<>();
        List<Character>l2=new ArrayList<>();
        //convert to array
        for(char c:name1.toCharArray()){
            l1.add(c);
        }for(char c:name2.toCharArray()){
            l2.add(c);
        }System.out.println(l1);
        System.out.println(l2);
        int a= l1.size();
        int b= l2.size();
        //replace same character
        for(int i=0;i<a;i++){
            for(int j=0;j<b;j++){
                if(l1.get(i)==l2.get(j)){
                    l1.set(i,'2');
                    l2.set(j,'2');
                }
            }
        }
        System.out.println(l1);
        System.out.println(l2);
        int count1=0;
        int count2=0;
        for(char c:l1){
            if(c!= '2'){
                count1++;
            }
        }
         for(char c:l2){
            if(c!= '2'){
                count2++;
            }
        }int final_count= count1+count2;
        System.out.println(final_count);
        String relation;
        switch(final_count){
            case 1:
                relation="Friend";
                break;
            case 2:
                relation="Lover";
                break;
            case 3:
                relation="Affection";
                break;
            case 4:
                relation="Marriage";
                break;
            case 5:
                relation="Enemy";
                break;
            case 6:
                relation="Sister";
                break;
            case 7:
                relation="Friend";
                break;
            case 8:
                relation="Lover";
                break;
            case 9:
                relation="Affection";
                break;
            case 10:
                relation="Marriage";
                break;
            case 11:
                relation="Enemy";
                break;
            case 12:
                relation="Sister";
                break;
            default:
                relation="unknown";
        }
        System.out.print("The relation is "+relation);
    }


