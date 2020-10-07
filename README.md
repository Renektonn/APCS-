import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner cin = new Scanner(System.in);
    
    int length=1;
    String str="aBBdaaa";
    int max = 0;

    int i,sum;
    //執行一次 先小寫後大寫 
    i=0;
    sum=0;
    while(true){
      
      for(int j=1 ; j<=length && i < str.length() ; j++ , i++){
        if(65 <= str.charAt(i) && str.charAt(i) <= 90 )
          sum++;
        else break;
      }
        
      for(int j=1 ; j<=length && i < str.length() ; j++ , i++){
        if(97 <= str.charAt(i) && str.charAt(i) <= 122)
          sum++;
        else break;
      }
          
    }
    if(sum > max) max=sum;
    //重複執行一次 先大寫後小寫
    i=0;
    sum=0;
    while(true){
      
      for(int j=1 ; j<=length && i < str.length() ; j++ , i++){
        if(97 <= str.charAt(i) && str.charAt(i) <= 122)
          sum++;
        else break;
      }

      for(int j=1 ; j<=length && i < str.length() ; j++ , i++){
        if(65 <= str.charAt(i) && str.charAt(i) <= 90 )
          sum++;
        else break;
      }
          
    }
    if(sum > max) max=sum;

    System.out.println(max);
  }
}
