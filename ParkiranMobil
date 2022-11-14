import java.util.Random;
import java.util.Scanner;

public class Parkiran {
    int JumlahVaksin = 3; //Pfizer, Sinopharm, Moderna
    static  int totalJumlahKapasitasParkiran = 450;
    public static String[] lantai1 = new String[150];
    public static String[] lantai2 = new String[150];
    public static String[] lantai3 = new String[150];

    public static double[] totalBeratLantai1 = {450.000};
    public static double[] totalBeratLantai2 = {200.000};
    public static double[] totalBeratLantai3 = {150.000};


    public static void PrintInfoParkirMobil(){
        int totalLantai1 = 0;
        int totalSisaKapasitas = 0;
        for (int i=0; i<lantai1.length; i++){
            if (lantai1[i] !=null){
                totalLantai1++;
            }
        }
        int totalLantai2 = 0;
        for (int i=0; i<lantai2.length; i++){
            if (lantai2[i] !=null){
                totalLantai2++;
            }
        }
        int totalLantai3 = 0;
        for (int i=0; i<lantai3.length; i++){
            if (lantai3[i] !=null){
                totalLantai3++;
            }
        }
        totalSisaKapasitas = totalJumlahKapasitasParkiran - totalLantai1 - totalLantai2 - totalLantai3;
        System.out.println("Total Kapasitas Parkiran Lantai 1 :  "+ totalLantai1 +"| Total Kapasitas Parkiran Lantai 2 : "+ totalLantai2
                +"| Total Kapasitas Parkiran Lantai 3 :  "+ totalLantai3);
        System.out.println("Jumlah Seluruh Kapasitas Parkir "+ totalJumlahKapasitasParkiran+ "| Sisa Kapasitas Parkiran "+ totalSisaKapasitas);
        System.out.println();
    }
    public static void CekIndexArray(String[] myArray, String Mobil){
        int indexNow = 0;
        for (int i=0; i<myArray.length; i++){
            if (myArray[i] !=null){
                indexNow = i+1;
            }
        }
        if (indexNow< myArray.length){
            myArray[indexNow] = Mobil;
        }
    }
    public static void lahanParkir(int tempatParkir, String Mobil){
        switch (tempatParkir){
            case 1:
                CekIndexArray(lantai1,Mobil);
                System.out.println("Parkir di Lantai 1");
                PrintInfoParkirMobil();
                break;
            case 2:
                CekIndexArray(lantai2,Mobil);
                System.out.println("Parkir di Lantai 2");
                PrintInfoParkirMobil();
                break;
            case 3:
                CekIndexArray(lantai3,Mobil);
                System.out.println("Parkir di Lantai 3");
                PrintInfoParkirMobil();
                break;
        }
    }
    public static void masukanInfoMobil(){
        Scanner gopal = new Scanner(System.in);
        while (true){
            System.out.println("Masukan Nomer Plat = ");
            String platMobil = gopal.nextLine();
            if (platMobil.isBlank()){
                System.out.println("Plat Nomer Wajib Diisi ");
                masukanInfoMobil();
            }else {
                Random HasilRandom = new Random();
                int JenisRandom = HasilRandom.nextInt(3)+1;
                lahanParkir(JenisRandom,platMobil);
            }
        }
    }

    public static void main(String[] args) {
        masukanInfoMobil();
    }
}
