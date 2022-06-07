# Java_Notes

# printf
System.out.printf("%-15s %d %2","foo",1,2); 

# vararg
# varrags accept zero or multiple arguments.
static void doStuff(int x, int... doArgs) {
        System.out.println(x);

        for (int d : doArgs) {
            System.out.println(d);
        }

# Lambda
https://github.com/LucasHartman/Cookbook_Java/tree/main/06_lambda
BinaryOperator<Integer> BinaryOperatorName = (i,j) -> i*j;
BinaryOperatorName.apply(2,3)

# Ternary
String status = (numOfPets <4 ) ? "yes" : "no";

# ArrayList
ArrayList<Integer> numbers = new ArrayList<Integer>();
numbers.add(5);
numbers.add(9);
numbers.add(8);
numbers.add(1);

# ForEach
numbers.forEach( n -> System.out.println(n));

# for 
 for (Person person : people) {
     System.out.println(person);
     }

# While
int x = 2;
while( x == 2) {
    System.out.println(x);
    ++x;
    }

# Do While
 do {
    System.out.println("Inside loop");
    } while (false);

# Switch
switch(colorOfRainbow) {        
    case red:
        System.out.print("Away");
        break;
    default:
        System.out.print("Home");
        break;
        }

# Array
https://github.com/LucasHartman/Cookbook_Java/blob/main/05_coreAPI/ArrayEx1.java

# StringBuilder
https://github.com/LucasHartman/Cookbook_Java/blob/main/05_coreAPI/StringBuilderEx1.java
StringBuilder sb = new StringBuilder("abc")
System.out.println("append  "+sb.append(3.132));
System.out.println("length: "+sb.length());
System.out.println("reverse "+sb.reverse());
System.out.println("insert  "+sb.insert(3, "---"));
System.out.println("delete  "+sb.delete(2,4));
System.out.println("toString"+sb.toString());

# String
// https://github.com/LucasHartman/Cookbook_Java/blob/main/05_coreAPI/StringEx1.java

# Time
https://github.com/LucasHartman/Cookbook_Java/blob/main/05_coreAPI/TimeEx1.java

# ExactionHandling
https://github.com/LucasHartman/Cookbook_Java/blob/main/10_exception/TryCatchEx1.java
try {
    // do stuff
} catch ( Exception ex) {
    // do exception handling
    ex.printStackTrace();
} finally {
    // clean up
}


# Order of Execution
# 1 abstract static block
    static { x=7; }
# 2 class static block
    static { x=7; }
# 3 abstract instance block
    { y=8; }
# 4 class instance block
    { y=8; }
# 5 class constructor


# “UMARELSA”
# 1. Unary Operators
    -      !      ++,    --
# 2. Multiplicaiton, divsion, modulus
    *      /      %
# 3. Addition, subtraction                   
    +      -
# 4. Relation operators
    <      >      <=    >=
# 5. Equality operators
    ==     !=
# 6. Logical operators (non-circuit)
    &      |   
# 7. Short-circuit
    &&     ||
# 8. Assignment operators
    =      +=      -=
