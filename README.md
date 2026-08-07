import java.util.Scanner;

public class KidsHealthyEatingTracker {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("=========================================");
        System.out.println("      KIDS HEALTHY EATING TRACKER");
        System.out.println("=========================================");

        System.out.print("Enter Child Name: ");
        String name = sc.nextLine();

        System.out.print("Enter Age: ");
        int age = sc.nextInt();

        int score = 100;

        System.out.print("\nHow many glasses of water did you drink today? ");
        int water = sc.nextInt();

        if (water < 8) {
            score -= 10;
        }

        System.out.print("How many servings of fruits did you eat? ");
        int fruits = sc.nextInt();

        if (fruits < 2) {
            score -= 10;
        }

        System.out.print("How many servings of vegetables did you eat? ");
        int vegetables = sc.nextInt();

        if (vegetables < 2) {
            score -= 10;
        }

        System.out.print("Did you eat junk food today? (1=Yes, 0=No): ");
        int junk = sc.nextInt();

        if (junk == 1) {
            score -= 20;
        }

        System.out.print("Exercise duration (minutes): ");
        int exercise = sc.nextInt();

        if (exercise < 30) {
            score -= 15;
        }

        System.out.print("Hours of sleep: ");
        int sleep = sc.nextInt();

        if (sleep < 8) {
            score -= 15;
        }

        System.out.println("\n=========== DAILY REPORT ===========");
        System.out.println("Name        : " + name);
        System.out.println("Age         : " + age);
        System.out.println("Health Score: " + score + "/100");

        if (score >= 90) {
            System.out.println("🏆 Excellent Healthy Eater!");
        } else if (score >= 75) {
            System.out.println("🥈 Good Job! Keep improving.");
        } else if (score >= 60) {
            System.out.println("🥉 Fair! Try healthier choices.");
        } else {
            System.out.println("⚠ Please improve your eating habits.");
        }

        System.out.println("\nHealthy Tips:");
        System.out.println("✔ Drink 8 glasses of water.");
        System.out.println("✔ Eat fruits and vegetables daily.");
        System.out.println("✔ Avoid sugary drinks.");
        System.out.println("✔ Exercise for at least 30 minutes.");
        System.out.println("✔ Sleep 8–10 hours every night.");

        sc.close();
    }
}
