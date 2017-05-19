# A N00b's Guide to Kotlin
# V.1

// You are always require to make at least one entry point into your program and this is main() a
// and always created like this



fun main(args: Array<String>) {
    /*
    A Multiline comment
    like you can see
    there are 3 lines
     */

    /*
    Block tags in kotlin are:
        @param <name>
        @return
        @constructor
        @property <name>
        throws <class>, @exception <class>
        @sample <identifier>
            /*
            Embeds the body of the function with the specified qualified
            name into the documentation for the current element, in order
            to show an example of how the element could be used.
             */
        @see <identifier>
            /*
            Adds a link to the specified class or method to the See Also
            block of the documentation.
             */
        @author
        @since
        @suppress
     */

    //Printing
    println("Hello world! I am Kotlin")

    //Appending
    println("This is how i calculate sum of 3 and 5 :"+sum(3,5))

    //Appending 2
    println("This is how i calculate sum of 3 and 5 like this too ${sum(3,5)}")

    //Method Calling and this is how you create a comment
    printSum(23,67)

    //Local variables

    //val is Assign-Once that is read only
    val a: Int = 1 //Instant/Immediate Assignment
    val b = 2 //Automatic type inference
    val c : Int //Type is required if you are not assigning it to the val
    c = 23
    println("Value of a,b,c is $a, $b, $c")

    //Like Swift and Python we don't require to end the statement with semicolon ";" same is the case for Kotlin

    //Mutable Variable
    //var is mutable but val is not
    var x = 21 //Int is automatically inferred
    x+=12 //we can do this with var

    /*
    c+=21
    we cannot do this as val is not mutable
     */

    //There are no primitive data type is in Kotlin like
    //int
    //boolean
    //float
    //double

    //All it have is classes
    //Int
    //Boolean
    //Float
    //Double
    //Etc..

    //Lets see who is bigger
    var temp1 = 23
    var temp2 = 32
    println("The number which is bigger is : ${whoIsBigger(temp1, temp2)}")
    //Lets use for loop to print from 1-100
    //This for loop is more like the for loop of swift ;)
    for (i in 1..100)//it explicitly tells i to start moving from 1 to 100 (inclusive of both)
    {
        println(i)
    }
    //Lets make a listOf  countries
    var countries = listOf<String>("India", "UK", "USA", "CHINA", "JAPAN", "SOUTH AFRICA")
    //lets traverse it
    for( country in countries)
    {
        println(country)
    }

    //lets print the countries again using while loop
    var index = 0
    while (index<countries.size)
    {
        println("Country at index $index is ${countries[index]}")
        index++ //this is how you increment the value of var by 1
    }
    //In Kotlin we don't have switch case, like we have it in C, C++ and many languages that are influenced by C or C++
    //In Kotlin we have when, lets see it in action
    var i = 1
    when(i)
    {
        1 -> println("i is 1")
        2 -> println("i is 2")
            else -> {
                println("i is neither") //Notice this, it is written in block
            }
    }

    //Kotlin does have a feature of checking a var in certain range, whether that variable is in the specified range or not
    //Lets see it in action
    var t = 23
    if(t in 1..30)
    {
        println("$t fits in range")
    }
    else{
        println("$t doesn't fit in range")
    }
}
//Method creation with return type
fun sum(a: Int, b: Int) : Int{
    return a+b
}
//Method creation without return type
fun printSum(a:Int, b: Int)
{
    println("Sum of $a and $b is ${a+b}")
}

//Method for checking who is bigger
fun whoIsBigger(a:Int, b:Int):Int
{
    //if is conditional statement that check for truthness of the expression provided in
    //(  ) parenthesis
    //You can use Boolean checks only in it, that means your expression should always
    //return into true or false
    //you can use all logical operators in if statement
    if(a>b /* <,>,!=,==,&&,|| and many more */)
    {
        return  a
    }
    return  b
}
