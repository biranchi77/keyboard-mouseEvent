# keyboard-mouseEvent
package web_driver;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class Keyboard_mouse_event {

	public static void main(String[] args) throws Throwable {
		// TODO Auto-generated method stub
		System.setProperty( "webdriver.chrome.driver","E:\\Chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.manage().deleteAllCookies();
		driver.get("https://www.google.com/");
		Thread.sleep(2000);
		Actions ac = new Actions(driver);
		driver.findElement(By.name("q")).sendKeys("selenium opening");
		Thread.sleep(2000);
		//press down arrow
		ac.sendKeys(Keys.ARROW_DOWN).perform();
		Thread.sleep(2000);
		ac.sendKeys(Keys.ARROW_DOWN).perform();
		Thread.sleep(2000);
		ac.sendKeys(Keys.ARROW_DOWN).perform();
		Thread.sleep(2000);
		ac.sendKeys(Keys.ENTER).perform();
		
		driver.quit();

	}

}
