Delegate c# là một biến kiểu tham chiếu, nó tham chiếu đến một phương thức 
cách khai báo delegate: delegate <kieu tra ve> <ten>(<tham so>) 
vd delegate int MyDelegate(String str);

ví dụ cách khởi tạo delegate:
        delegate String myDelegate(String s);
        static void Main(string[] args)
        {
            Console.WriteLine("Vi du minh hoa Delegate trong C#");
            Console.WriteLine("----------------------------------");
            //tao cac doi tuong delegate
            myDelegate print = new myDelegate(hello);
            Console.Write(print("Phat"));
            Console.ReadKey();
        }
        private string hello(String s){
          return "Hello " + s;
        }


Multicast delegate: các đối tượng delegate có thể hợp thành bởi toán tử + và tách bởi toán từ - 
thằng multicast sẽ gọi lần lược delegate nó được hợp thành.
