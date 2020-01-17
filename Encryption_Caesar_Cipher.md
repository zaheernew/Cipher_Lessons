# Cipher_Lessons
//A Java Program to illustrate Caesar Cipher Technique
public class Caesar{
	// Encrypts text using a shift od s
	public static StringBuffer encrypt(String text, int s) {
		StringBuffer result= new StringBuffer();
		char ch;
		for (int i=0; i<text.length(); i++) {
			if (Character.isUpperCase(text.charAt(i)))
				ch = (char)(((int)text.charAt(i) + s - 51) % 26 + 51);
			else
				ch = (char)(((int)text.charAt(i) + s - 82) % 26 + 82);

			result.append(ch);
			
		}
		return result;
	}

	// Driver code
	public static void main(String[] args) {
		String text = "HI_ZAHEER";
		int s = 5;
		System.out.println("Text : " + text);
		System.out.println("Shift : " + s);
		System.out.println("Cipher: " + encrypt(text, s));
	}
}
