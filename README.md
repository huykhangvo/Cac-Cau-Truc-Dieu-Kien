# Các cấu trúc điều kiện
Nội dung:
1. if, if else, if lồng nhau 
2. Toán tử 3 ngôi 
3. switch

## if, if else, if lồng nhau Lý thuyết
    if  (<điều kiện> )
    {
       <Công việc 1>;
    }
    else
    {
       <Công việc 2>;
    }

##### Ví dụ

    Ví dụ 1
    if (i % 2 == 0)
    	Console.WriteLine("i la so chan");
    else
    Console.WriteLine("i la so le");
    Ví dụ 2
    if ((y % 4 == 0 &&y%100!=0) || y%400==0)
    	Console.WriteLine("y la năm nhuận");
    else
    Console.WriteLine("y không là năm nhuận");

## Toán tử 3 ngôi Lý thuyết
    Có dạng:
      <Điều kiện> ? <Biểu thức 1> : <Biểu thức 2>
    Nếu <Điều kiện> đúng thì <Biểu thức 1> thực hiện, ngược lại <Biểu thức 2> thực hiện
    Là dạng rút gọn của if…else
    Ví dụ
    string a = (i % 2 == 0) ? “so chan” : “so le”

Dùng toán tử 3 ngôi để xuất xếp loại:
Gọi x là điểm nhập vào từ bàn phím
Nếu [8..10]->Giỏi
[6.5..8)->khá
[5..6.5)->trung bình
[0…5)->yếu

# Cấu trúc switch

    switch (<biến cần kiểm tra>) 
    {
       case <giá trị 1>:
    		<công việc 1>;
    		break;
       case <giá trị 2>:
    		<công việc 2>;
    		break;
    	…
       default:
    		<công việc nếu không thuộc trường hợp nào ở trên>;
    		break;
    }

Ví dụ:
    Ví dụ
    switch (i)
    {
    	case 1:
    		Console.WriteLine("so 1");
    		break;
    	case 2:
    		Console.WriteLine("so 2");
    		break;
    	default:
    		Console.WriteLine("default");
    		break;
    }

Cấu trúc switch
Bài 1: Cho a,b là 2 số nguyên, kt là 1 ký tự nhập từ bàn phím (+,-,*,/). 
Nếu nhập kt là phép toán nào thì tự động tính toán cho a,b.
Bài 2: Nhập vào 1 tháng hỏi tháng đó có bao nhiêu ngày, nếu là tháng 2 thì yêu cầu nhập năm để kiểm tra năm nhuần, năm nhuần tháng 2 có 29 ngày, ko nhuần thì có 28 ngày.

    Console.OutputEncoding = Encoding.UTF8;
                //Ví dụ về switch:
                int a, b;
                char kt;
                Console.WriteLine("Nhập a:");
                a = int.Parse(Console.ReadLine());
                Console.WriteLine("Nhập b:");
                b = int.Parse(Console.ReadLine());
                Console.WriteLine("Nhập phép toán(+,-,*,/):");
                kt = Console.ReadLine()[0];
                switch(kt)
                {
                    case '+':
                        Console.WriteLine("{0}+{1}={2}", a, b, a + b);
                        break;
                    case '-':
                        Console.WriteLine("{0}-{1}={2}", a, b, a - b);
                        break;
                    case '*':
                        Console.WriteLine("{0}*{1}={2}", a, b, a * b);
                        break;
                    case '/':
                        Console.WriteLine("{0}/{1}={2}", a, b, a / b);
                        break;
                }
                Console.ReadLine();
    
                /*Console.OutputEncoding = Encoding.UTF8;
                double diem;
                Console.WriteLine("Mời bạn nhập vào 1 điểm:");
                diem = double.Parse(Console.ReadLine());
                string ketqua = diem >= 5 ? "Đậu" : "Rớt";
    
                Console.WriteLine("Điểm ={0}==>{1}", diem, ketqua);
    
    
                Console.ReadLine();*/
    
                /*Console.OutputEncoding = Encoding.UTF8;
                double diem;
                Console.WriteLine("Mời bạn nhập vào 1 điểm:");
                diem = double.Parse(Console.ReadLine());
                //"5.5"==>5.5
                if(diem>=5)
                {
                    Console.WriteLine("Điểm ={0}==>Đậu",diem);
                }
                else
                {
                    Console.WriteLine("Điểm ={0}==>Rớt", diem);
                }
                Console.ReadLine();*/
