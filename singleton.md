�ȴ���򵥵Ŀ�ʼ������ģʽ
����˼�壬ֻ��һ��ʵ����ͨ����ĳ��������
java���е�static������ָĳ����������ֻ��ʼ��һ�Σ��������ʵ��Ҳֻ�ǵ�һ�γ�ʼ���Ķ������Կ�����static����־��������
����
public class Singleton{
	private static Singleton singleton = new Singleton();
	private Singleton(){
			System.out.println(��������һ������");
		}
	public static Singleton getInstance(){
			return singleton;
			}
}

javascript �汾


var getSingle = function (fn) {
        var result;
        return function () {
            return result || ( result = fn.apply(this, arguments) );
        }
    };
    
    
function Singleton(name){
var cc=new Object;
cc.name=name;
return cc

}

var dd=getSingle(Singleton);
var c=dd(123);
var d=dd(456);
console.log(c)
console.log(d)
//{name: 123}
//{name: 123}

	