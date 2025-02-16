public class JEcho {

public static void main(String[] args) {

boolean printNewline = true;

int posArgs = 0;

if (args.length > 0 && args[0].equals("-n")) {

printNewline = false;

posArgs = 1;

}

StringBuilder outputBuilder = new StringBuilder();

for (; posArgs < args.length; posArgs++) {

outputBuilder.append(args[posArgs]);

outputBuilder.append(" "); // Separator.

}

// Remove the trailing whitespace at the end.

int outputLength = outputBuilder.length();

if (outputLength > 0)

outputBuilder.deleteCharAt(outputBuilder.length() - 1);

String output = outputBuilder.toString();

if (printNewline)

System.out.println(output);

else

System.out.print(output);

}

}
