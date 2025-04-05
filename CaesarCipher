import java.util.Scanner;
class CaesarCipher {
    public static String encrypt(String text, int shift) {
        StringBuilder result = new StringBuilder();
        for (int i = 0; i < text.length(); i++) {
            char ch = text.charAt(i);
            if (Character.isUpperCase(ch)) {
                char encryptedChar = (char) ((ch + shift - 'A') % 26 + 'A');
                result.append(encryptedChar);
            }
            else if (Character.isLowerCase(ch)) {
                char encryptedChar = (char) ((ch + shift - 'a') % 26 + 'a');
                result.append(encryptedChar);
            } else {
                result.append(ch);
            }
        }
        return result.toString();
    }
    public static String decrypt(String text, int shift) {
        return encrypt(text, 26 - shift);
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Caesar Cipher Program");
        System.out.print("Enter the message: ");
        String message = scanner.nextLine();
        System.out.print("Enter the shift value (0-25): ");
        int shift = scanner.nextInt();
        shift = shift % 26;
        String encryptedMessage = encrypt(message, shift);
        System.out.println("Encrypted Message: " + encryptedMessage);
        String decryptedMessage = decrypt(encryptedMessage, shift);
        System.out.println("Decrypted Message: " + decryptedMessage);
        scanner.close();
    }
}
