package JSP6;

class Pekerja {
    private String nama;
    private int umur;
    private double gaji;
    
    public Pekerja (String nama, int umur, double gaji){
        this.nama = nama;
        this.umur = umur;
        this.gaji = gaji;
    }
    public void info(){
        System.out.println("Nama :"+ nama);
        System.out.println("Umur :"+ umur+ "tahun");
        System.out.println("Gaji :"+ gaji+ "Jt");
    }
}
class Koki extends Pekerja{
    private String keahlian;
    
    public Koki(String nama, int umur, double gaji, String keahlian){
        super(nama, umur, gaji);
        this.keahlian = keahlian;
    }
    public void info(){
        super.info();
        System.out.println("Posisi: Koki");
        System.out.println("Keahlian :"+keahlian);
    }
    public void masak(String menu){
        System.out.println("Memasak :"+ menu+ "sesuai keahlian");
    }
}

class Pelayan extends Pekerja{
    private String shift;
    
    public Pelayan(String nama, int umur, double gaji, String shift){
        super(nama, umur, gaji);
        this.shift = shift;
    }
    public void info(){
        super.info();
        System.out.println("Shift: "+ shift);
    }
    public void pelayanan(int meja){
        System.out.println("Pelayanan:"+meja+ "no");
    }
}

class Kasir extends Pekerja{
    private String metodePembayaran;
    
    public Kasir(String nama, int umur, double gaji, String metodePembayaran){
        super(nama, umur, gaji);
        this.metodePembayaran = metodePembayaran;
    }
    public void info(){
        super.info();
        System.out.println("Metode Pembayaran:"+metodePembayaran);
    }
    public void jumlah(double harga){
        System.out.println("Total Harga:"+harga+"ribu");
    }
}

public class Profesi {
    public static void main(String[] args){
        Koki res = new Koki("Heru", 45, 4.5, "Masakan Lombok");
        res.info();
        res.masak("Ayam Taliwang");
        
        Pelayan rest = new Pelayan("Heri", 25, 2.5, "Pagi");
        rest.info();
        rest.pelayanan(4);
        
        Kasir resto = new Kasir ("Herman", 30, 2.8, "Debit");
        resto.info();
        resto.jumlah(500);
    }
}
