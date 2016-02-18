# Constructors

![jcinsanity](Screenshot 001.PNG)
![jcinsanity](Screenshot 002.PNG)
![jcinsanity](Screenshot 003.PNG)

~~~
package ph.edu.dlsu;

import ph.edu.dlsu.Olive.Olive;
import ph.edu.dlsu.OlivePress.OlivePress;

import java.util.ArrayList;

public class Main {

    public static void main(String[] args) {

        ArrayList<Olive> olives = new ArrayList<Olive>();

        Olive olive;

        olive = new Olive(2);
        System.out.println(olive.name);
        olives.add(olive);

        olive = new Olive(1);
        System.out.println(olive.name);
        olives.add(olive);

        olive = new Olive(2);
        System.out.println(olive.name);
        olives.add(olive);

        OlivePress press = new OlivePress();

    }
}
~~~
package ph.edu.dlsu.OlivePress;

import ph.edu.dlsu.Olive.Olive;

import java.util.ArrayList;

public class OlivePress {

    public OlivePress(){
    }

    public void getOil(ArrayList<Olive> olives) {

        int oil = 0;

        for (Olive olive : olives) {
            oil += olive.crush();
        }

        System.out.println("You got " + oil + " units of oil");
    }
}

~~~
package ph.edu.dlsu.Olive;

public class Olive {

    public String name = "Kalamata";
    public String flavor = "Grassy";
    public long color = 0x000000;
    private int oil = 3;

    public Olive() {
        System.out.print("Constructor of " + this.name);
    }

    public Olive(int oil){
        this.oil = oil;
    }

    public int crush(){
        System.out.println("ouch!");
        return oil;
    }
}


~~~
