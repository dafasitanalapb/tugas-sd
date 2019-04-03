 package bp2;
class node {
    int data;
    node next;
    public node(int d){
        data = d; next = null;
    }
    int getnode(){ return (data); }
}
class LinkedList2{
    node head;
    node tail;
    int jumlah;
    public LinkedList2(){
        head = null; tail = null; jumlah = 0;
    }
    void tambahbelakang(node baru){
        if(head==null){
            head = baru; tail = baru;
        }
        else {
            tail.next = baru;
            tail = baru;
        }
    }
    //bagaimana dengan tambah depan?
    //bagaimana pula dengan hapus belakang atau
    //hapus berdasar pencarian?
    //silahkan ditambahkan sendiri :)
    void hapusdepan(){
        int data;
        if(head.next != null){
            data = head.getnode();
            head = head.next;
            System.out.println("Data "+data+" berhasil dihapus..");
        }
        //node terakhir belum bisa dihapus.
        //silahkan code-nya ditambahkan sendiri :)
    }
    void tampil(){
        node temp;
        for(temp=head; temp!=null; temp=temp.next){
            System.out.print(temp.getnode()+" ");
        }
    }
}
public class linkedlist {
    public static void main(String k[]){
        node simpul1 = new node(4);
        node simpul2 = new node(3);
        node simpul3 = new node(5);
        
        LinkedList2 LL = new LinkedList2();
        LL.tambahbelakang(simpul1);
        LL.tambahbelakang(simpul2);
        LL.tambahbelakang(simpul3);
        LL.tampil();
        LL.hapusdepan();
        LL.tampil();
        LL.hapusdepan();
        LL.tampil();
        LL.hapusdepan();
        LL.hapusdepan();
    }
}
