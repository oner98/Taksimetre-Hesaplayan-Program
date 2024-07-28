# Taksimetre-Hesaplayan-Program
Kodluyoruz Eğitimi kapsamında açtığım bir proje
import java.util.Scanner;

public class Taksimetre {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Sabit değerler
        double acilisUcreti = 10.0;
        double kmBasiUcret = 2.20;
        double minUcret = 20.0;

        // Kullanıcıdan gidilen mesafeyi al
        System.out.print("Gidilen mesafeyi KM cinsinden giriniz: ");
        double mesafe = scanner.nextDouble();

        // Taksimetre tutarını hesapla
        double tutar = acilisUcreti + (mesafe * kmBasiUcret);

        // Minimum ücret kontrolü
        if (tutar < minUcret) {
            tutar = minUcret;
        }

        // Sonucu ekrana yazdır
        System.out.println("Toplam Taksimetre Tutarı: " + tutar + " TL");
    }
}
