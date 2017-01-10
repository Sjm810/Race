# Race
Assign only one runner to each lane
package runningtrack;
import java.util.ArrayList;
/*
 *
 * @author Steve McCormick PRG/421 Java II 
 * Professor: Edward Spear 
 * January 25, 2015
 */
public class Race {
    private static Race race;
    private final ArrayList<String> runners; // creates an array list
   
    private Race(){ // Constructor that makes new ArrayList
        
        //adds runners to list
        runners = new ArrayList<>(); 
        runners.add("John");
        runners.add("Steve");
        runners.add("Chris");
        runners.add("Emily");
        runners.add("Kim");
        runners.add("Veronica"); 
        runners.add("Mike");
        runners.add("Bob");
        runners.add("Ed");
    }
    //Singleton method that only creates an object only if one doesn't exist
    public static Race singleton() {
        if(race==null)
             race = new Race();
        return race;
    
    }
    //A method that adds a runner and removes them from the list
         public String getRunner(){
             if(runners.size()>0)
                 return runners.remove(0);
             return "No Runners";
    }
}
