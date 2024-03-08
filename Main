
import java.awt.AWTException;
import java.awt.Robot;
import java.awt.event.KeyEvent;
import java.io.IOException;

public class Main {

    public static void main(String[] args) throws IOException, AWTException, InterruptedException {
        String username = "your username";
        String password = "your password";
        String location = "C:\\Riot Games\\Riot Client\\RiotClientServices.exe"; // riot client location

        Robot robot = new Robot();
        Runtime.getRuntime().exec(location);
        Thread.sleep(5000);
        write(username);
        robot.keyPress(KeyEvent.VK_TAB);
        robot.keyRelease(KeyEvent.VK_TAB);
        write(password);
        robot.keyPress(KeyEvent.VK_ENTER);
        robot.keyRelease(KeyEvent.VK_ENTER);

    }

    public static void write(String a) throws AWTException {
        Robot robot = new Robot();
        for (char a1 : a.toCharArray()) {
            int code = KeyEvent.getExtendedKeyCodeForChar(a1);
            if (Character.isUpperCase(a1)) {
                robot.keyPress(KeyEvent.VK_SHIFT);
            }
            robot.keyPress(code);
            robot.keyRelease(code);
            if (Character.isUpperCase(code)) {
                robot.keyRelease(KeyEvent.VK_SHIFT);
            }
        }
    }

}
