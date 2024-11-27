import java.util.Scanner;

public class JavaQuizz {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        String[] questions = {
            "1. Who is coordinator? (A. gupi, B. hasnat, C. saddam, D. enun)",
            "2. What is 2 + 42? (A. 44, B. 33, C. 66, D. 6)",
            "3. What is 51%2? (A. 1, B. 2, C. 3, D. 4 )",
            "4. What is 24/3? (A. 14, B. 8, C. 6, D. 13)",
            "5. Which is an odd number? (A. 55, B. 90, C. 44, D. 52)"
        };

        char[] correctAnswers = {'B', 'A', 'A', 'B', 'A'};
        double score = 0;

        
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            System.out.print("Your answer (A/B/C/D): ");
            char answer = scanner.next().toUpperCase().charAt(0);

            if (answer == correctAnswers[i]) {
                score ++;
            } else {
                score --;
            }
        }

        System.out.printf("Your final score: %.2f\n", score);
        scanner.close();
    }
}
