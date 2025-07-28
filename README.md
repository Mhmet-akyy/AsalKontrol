# AsalKontrol
import java.util.Scanner;

public class AsalKontrol {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Bir sayı giriniz: ");
        int sayi = input.nextInt();
        boolean asalMi = true;

        if (sayi <= 1) {
            asalMi = false; // 1 ve daha küçük sayılar asal değildir
        } else {
            for (int i = 2; i <= sayi / 2; i++) {
                if (sayi % i == 0) {
                    asalMi = false;
                    break; // Bölen bulunduysa döngüyü durdur
                }
            }
        }

        if (asalMi) {
            System.out.println(sayi + " bir asal sayıdır.");
        } else {
            System.out.println(sayi + " asal değildir.");
        }
    }
}
