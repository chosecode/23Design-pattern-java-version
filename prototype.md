#ԭ��ģʽ
###���Դ�Ķ�����ǰ����������ʹ��ʱֱ�Ӹ��ƶ�������������
###java�п����ýӿڵĸ����ȷ����������������ͬʵ����Ϊԭ�ͣ���ע�ᵽ�����Ͻ��в�ͬ�ĵ��ã�

* Product��   �����˳��󷽷�ʹ��use �� ������¡���󷽷� createClone�Ľӿ�
* Manager��  ע�᲻ͬ��ԭ�ͣ�����ԭ�Ϳ�¡����
* MessageBox�� ԭ���࣬ʵ���˽ӿڵķ�������������Ϊ���ַ������뷽����
* UnderLinePen�� ԭ���࣬ʵ���˽ӿڵķ�������������Ϊ���ַ��������»���

###Product
    public interface Product extends Cloneable{
        public abstract void use (String s);   //
        public abstract Product creatClone();
        }
###Manager
    public class Manager{
        private HashMap showcase = new HashMap();
        public void register (String name,Product proto){
            showcase.put(name,proto);
            }
        public product creat(String protoname){
            Product p =(product)showcase.get(protoname);
            return p.createClone();
            }
        }
###MessageBox
    private char decochar;
    public MessageBox(char decochar){
        this.decochar=decochar
        }
    public void use(String s){
        ...
        }
    public Product creatClone(){
        Product p=null;
        try{
            p=(Product)clone();
        }catch(CloneNotSupportedException e){
            e.printStackTrace();
        }
        return p;
        }
    }
####Underkine
������ƣ�ֻ�����Ǳ�ɼ��»���

####��ڴ���
    public static void main (String[] args){
    Manager manager = new Manager();
    UnderlinePen upen = new UnderlinePen('~');
    MessageBox mbox = new MessageBox('*');
    MessageBox sbox = new MessageBox('/');
    manager.register("strong message",upen);
    manager.register("warning box",mbox);
    manager.register("slash box".sbox);
    
    
    Product p1 =manager.create("strong message")
    p1.use("Hello,world");
    Product p2 =manager.create("warning box");
    p2.use("hello,word");
    Product p3 = manager.create("slash box");
    p3.use("Hello,world.");
    }
    
####javascript
�������ԭ�ͱ��ݣ����ƶ���ʱʹ��object.creat������protoָ��ԭ�Ͷ���
