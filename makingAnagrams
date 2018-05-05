import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
import java.util.Map.Entry;
public class Solution {
  
  
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String a = in.next();
        String b = in.next();
        System.out.println(numberNeeded(a, b));
    }
    
    
    public static int numberNeeded(String first, String second) {
		HashMap<Character, Integer> hm=new HashMap<>();
		int count=0;
		for(int i=0;i<first.length();i++){
			if(!hm.containsKey(first.charAt(i))){
				hm.put(first.charAt(i), 1);
			}else{
				hm.put(first.charAt(i),hm.get(first.charAt(i))+1);
			}
		}
		for(int i=0;i<second.length();i++){
			if(!hm.containsKey(second.charAt(i))){
				count++;
			}else{
				hm.put(second.charAt(i),hm.get(second.charAt(i))-1);
			}
		}
        Set<Entry<Character, Integer>> entrySet = hm.entrySet();
		for(Entry<Character,Integer> entry:hm.entrySet()){
			if(entry.getValue()!=0){
				count+=Math.abs(entry.getValue());
			}
		}
		return count;
	}
}
