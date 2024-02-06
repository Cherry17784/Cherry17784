package demo;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
//import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class Github {

	public static void main(String[] args) throws InterruptedException {
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		Thread.sleep(3000);
		driver.get("https://www.google.com/");
		Thread.sleep(3000);
		driver.get("https://github.com/");
		driver.findElement(By.linkText("Sign in")).click();		
		Thread.sleep(3000);
		driver.findElement(By.id("login_field")).sendKeys("Cherry17784");
		Thread.sleep(3000);
		driver.findElement(By.id("password")).sendKeys("charan@17784");
		Thread.sleep(3000);
		driver.findElement(By.cssSelector("input[type = 'submit']")).click();
		Thread.sleep(3000);
		driver.findElement(By.className("AppHeader-user")).click();
		Thread.sleep(3000);
		driver.findElement(By.linkText("Your profile")).click();
		Thread.sleep(3000);
		driver.findElement(By.cssSelector("button[class=\"btn btn-block js-profile-editable-edit-button\"]")).click();
		Thread.sleep(3000);
		driver.findElement(By.name("user[profile_name]")).sendKeys("Sricharan K");
		Thread.sleep(3000);
		driver.findElement(By.name("user[profile_name]")).clear();
		Thread.sleep(3000);
		driver.findElement(By.name("user[profile_bio]")).sendKeys("Manual Testing Engineer");
		Thread.sleep(3000);
		driver.findElement(By.name("user[profile_bio]")).clear();
		Thread.sleep(3000);
		driver.findElement(By.cssSelector("[class = 'Button--primary Button--small Button d-inline-flex']")).click();
		Thread.sleep(3000);
		driver.findElement(By.className("AppHeader-user")).click();
		Thread.sleep(3000);
		driver.findElement(By.linkText("Sign out")).click();
		Thread.sleep(3000);
		driver.findElement(By.cssSelector("input[class='btn btn-large width-full text-center mt-3 btn-danger']")).click();
		Thread.sleep(3000);
		driver.quit();
	}

}
