# lesson
package Сollection;

import java.util.HashMap;
import java.util.HashSet;

public class Notebook {


    private HashMap <String, HashSet<String>> map;


    public Notebook(){
        this.map = new HashMap<>();
    }
    public void add(String surname,String telephone){
        if (!map.containsKey(surname)){
            map.put(surname,new HashSet<>());
        }
        map.get(surname).add(telephone);
    }

    public HashSet<String> find(String surname) {
if (!map.containsKey(surname)){
    return new  HashSet<>();
}
return map.get(surname);
    }

}
package Сollection;

import java.util.HashMap;
import java.util.HashSet;

public class Sheet {
    public static void main(String[] args) {
        String[] words = {"Дом","Дом","Апильсин","Апильсин","Апильсин","Ручка"
                ,"Мышка","Мышка","Ручка","Ракета","Река",
                "Ракета","Гриб","Зайц","Зайц","Гриб" };

        HashSet<String> set =new HashSet<>();
        for (String e :words){
          set.add(e);
        }
        for (String e: set) {
            int quantity = 0;
            for (int i = 0; i < words.length; i++){
                if (e.equals(words[i])){
                    quantity++;
                }
            }
            System.out.println(e +" " + quantity);
        }

        System.out.println(set);
    }

}
