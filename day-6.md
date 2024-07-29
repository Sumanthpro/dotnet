```c#

internal partial class CSharpFeatures
    {
        // implicit typed local variable


        public void Demo1()
        {
            // use var keyword if u are not sure about
            // datatype to be used
            // var keyword automatically typedcast to its
            // corresponding datatype based on value passed

            // rules
            // can be used only as local variable
            // cannot be used as method parameter
            // multiple variable not supported(var m, n, o;)
            // you have to assign the value while declaring
            //cannot assign null values


            List<int> list = new List<int>();

            var list1 = new List<int>();

            int a = 10; //integer

            var b = 20;
            var s = "hello world";
            DelegateDemo ob = new DelegateDemo();

            var obj = new DelegateDemo();

        }
        public int? MyProperty { get; set; }
        public void Demo2() {
            // reference type (class, string , interface, object, delegate)


            // value type ((int, float, double, boolen, byte)

            // nullable types
            //---------------

            // using nullable types we can assing null values for int, float datatypes
            // it is achived by using ? symbol


            int? i = null;
            float? f = null;
            // real time
            // database programming
            // id name marks(integer)
            // 10  raj  0

            if (i.HasValue)
            {
                Console.WriteLine(i.Value);
            }
            else
            {
                Console.WriteLine("i is null");
            }

        }

        public void Demo3()
        {// extention method

            string s = "hello world";


            // using extention method we can add new methods
            // to exisiting types

            // rules
            // 1. method and class should be static
            // 2. the method has to take 1 parameter

            int m = 11;
            Console.WriteLine(m.IsEven());


            string st = "10";
            int i = int.Parse(st);

            int j = st.ToInteger();


        }

        public void Demo4()
        {
            // inline warning

            // using inline warning feature we can disable the
            // warning messages
#pragma warning disable
            int s;
            int a;
#pragma warning restore
            int k;


        }

        public void Demo5()
        {/// object initializer
            Product p = new Product() { pid = 100, pname = "cd" };
            // collection initializer
            List<Product> li = new List<Product>()
            {
                new Product() { pid = 100, pname = "cd" },
            new Product() { pid = 200, pname = "books" }
           };

        }



        public void Demo6()
        {
            // what is partial methods
            // partial methods can be used only inside partial classes
            // partial methods = declaration + implementation
            // declaration and implementation happens 2 diff files


            try
            {
                int a = int.Parse(Console.ReadLine());
                int b = int.Parse(Console.ReadLine());
                Console.WriteLine(a/b);
            }
            catch(DivideByZeroException e)
            {
                // logging features(db + files)

                Console.WriteLine(e.Message);
            }


        }


        public void Demo7()
        {
            // anomymous type

            var res = new
            {
               name = "Sumanth",
                marks  = 90
            };

            Console.WriteLine(res.name);
            Console.WriteLine(res.marks);

        }
        // lambda expression
        public void Demo8() => Console.WriteLine(1000);


        public void demo9()
        {
            // dynamic keyword
            // .net 4.5

            var a = 10;// type is check at compile time
          //  a = "helloworld";

            // any type can be assinged / type changes accordinly

            dynamic d = 10;// run time
            Console.WriteLine(d);
            d = "hello world";
            Console.WriteLine(d);
            d = new mymath();
            d.cool();
        }
    }


    static class myext
    {
        public static bool IsEven(this int i)
        {
            return i % 2 == 0;
        }

        public static bool IsUpper(this string s)
        {

            return s.ToUpper() == s;
        }
        public static int ToInteger(this string s)
        {

            return    int.Parse(s);
        }

    }
has context menu
```
