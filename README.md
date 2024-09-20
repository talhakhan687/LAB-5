PROBLEM 1

class Prs {
   private String nm;
   private int ag;
   private String gnd;
   private String addr;

   public Prs(String nm, int ag, String gnd, String addr) {
       this.nm = nm;
       this.ag = ag;
       this.gnd = gnd;
       this.addr = addr;
   }

   public Prs(String nm, int ag) {
       this(nm, ag, "Not specified", "Not specified");
   }

   public Prs(String nm) {
       this(nm, 0, "Not specified", "Not specified");
   }
   public Prs() {
       this("Not specified", 0, "Not specified", "Not specified");
   }
   
   public void showDetails() {
       System.out.println("Name: " + this.nm);
       System.out.println("Age: " + this.ag);
       System.out.println("Gender: " + this.gnd);
       System.out.println("Address: " + this.addr);
   }
   public void changeAddr(String addr) {
       this.addr = addr;
       System.out.println("Address updated.");
   }
   
   public void changeAddr(String addr, String nm) {
       this.addr = addr;
       this.nm = nm;
       System.out.println("Address and name updated.");
   }

   public static void main(String[] args) {
    
       Prs p1 = new Prs("tanha", 25, "Female", "khilgaon ");
       p1.showDetails();
     
       Prs p2 = new Prs("roza", 24);
       p2.showDetails();

       Prs p3 = new Prs("Asad");
       p3.showDetails();

       Prs p4 = new Prs();
       p4.showDetails();

       p1.changeAddr("kanchpur");
       p1.showDetails():

       p2.changeAddr("dhaka", "ahona");
       p2.showDetails();
   }
}



PROBLEM 2


public class Emp {
    
    private String nm;
    private int id;
    private double sal;
    private String desg;

    public Emp(String nm, int id, double sal, String desg) {
        this.nm = nm;
        this.id = id;
        this.sal = sal;
        this.desg = desg;
    }
    public Emp(String nm, int id) {
        this(nm, id, 0.0, "Not Assigned");
    }

    public Emp(String nm) {
        this(nm, 0, 0.0, "Not Assigned");
    }

    public Emp() {
        this("Unknown", 0, 0.0, "Not Assigned");
    }

    public void showDetails() {
        System.out.println("Name: " + this.nm);
        System.out.println("ID: " + this.id);
        System.out.println("Salary: " + this.sal);
        System.out.println("Designation: " + this.desg);
        System.out.println();
    }
 
    public void updateSal(double sal) {
        this.sal = sal;
        System.out.println("Salary has been updated.\n");
    }

    public void updateSal(double sal, double raise) {
        this.sal = sal + raise;
        System.out.println("Salary and raise applied.\n");
    }

    public static void main(String[] args) {
     
        Emp e1 = new Emp("roza", 101, 5000, "Developer");
        Emp e2 = new Emp("mim", 102);
        Emp e3 = new Emp("ayshi");

        e1.showDetails();
        e2.showDetails();
        e2.updateSal(3300);
        e2.showDetails();

        e3.showDetails();
        e3.updateSal(4600, 500);
        e3.showDetails();
 }
}



















