##������ģʽ
     

�����д��룬���е���������䣬���ӹ���Ч��

   

javaʵ��
###Banner �࣬�������ɫ


    public class Banner {
    private String string;
    public Banner(String string) {
        this.string = string;
    }
    public void showWithParen() {
        System.out.println("(" + string + ")");
    }
    public void showWithAster() {
        System.out.println("*" + string + "*");
    }
    }



###Print   �࣬���������跽��

    public interface Print {
    public abstract void printWeak();
    public abstract void printStrong();
    }


####PrintBanner  �࣬����������

    public class PrintBanner extends Banner implements Print {
    public PrintBanner(String string) {
        super(string);
    }
    public void printWeak() {
        showWithParen();
    }
    public void printStrong() {
        showWithAster();
    }
    }



####��ڴ���

    public class Main {
    public static void main(String[] args) {
        Print p = new PrintBanner("Hello");
        p.printWeak();
        p.printStrong();
    }
    }
    
    
����ͬ���Ĺ��ܱ�������������


    

