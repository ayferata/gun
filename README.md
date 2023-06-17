# gun
public final class Gun {

    public static final Gun PAZARTESI = new Gun(1);
    public static final Gun SALI = new Gun(2);
    public static final Gun CARSAMBA = new Gun(3);
    public static final Gun PERSEMBE = new Gun(4);
    public static final Gun CUMA = new Gun(5);
    public static final Gun CUMARTESI = new Gun(6);
    public static final Gun PAZAR = new Gun(7);

    private final int day;

    private Gun(int f) {
        this.day = f;
    }

    public int getDay() {
        return day;
    }

}



İlgili örnekteki sadece sabitlerden oluşan sınıflar için Java'da ENUM sınıflar kullanılır ve kullanımı daha kolaydır.



public enum Day {
    PAZARTESI(1),
    SALI(2),
    CARSAMBA(3),
    PERSEMBE(4),
    CUMA(5),
    CUMARTESI(6),
    PAZAR(7);

    private int day;

    private Day(int day) {
        this.day = day;
    }

    public int getDay() {
        return day;
    }
}


public class PatikaDev {
    public static void main(String[] args) {

        Day gunPzt = Day.PAZARTESI;
        System.out.println(gunPzt.ordinal()); // Dizideki indeksini verir.
        System.out.println(gunPzt.name()); // Sabit'in adını döndürür.

        Day[] values = Day.values(); // Tüm sabitlerini döndürür.

        Day gun = Day.valueOf("PAZARTESI"); // String'i enum'a dönüştürür.
    }
}
