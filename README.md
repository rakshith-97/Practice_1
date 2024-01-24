# Practice_1
Practice_1
package practice;

import org.openqa.selenium.By;
import org.openqa.selenium.Dimension;
import org.openqa.selenium.Point;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class Manu {
	
	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "./software/chromedriver.exe");
		
		WebDriver driver=new ChromeDriver();
		
		driver.get("https://www.facebook.com/");
		
		WebElement ele=driver.findElement(By.xpath("//input[@id='email']"));
		
		Boolean a=ele.isDisplayed();
		
		if(a)
		{
			System.out.println("Textfield is present");
			
	
		}else
		{
			System.out.println("Textfield is not Present");
		
		}
		
		boolean b=ele.isEnabled();
		
		if(b)
		
		{
			System.out.println("Textfield is Enabled");
			
	
		}else
		{
			System.out.println("Textfield is Disabled");
			
		}
		
		boolean c=ele.isSelected();
		
		if(c)
			
		{
		System.out.println("Seleceted");
		}else
		{
			System.out.println("Not Seleceted");
	     }
		WebElement rak=driver.findElement(By.xpath("//button[@type='submit']"));
		
		String x=rak.getText();
		
		System.out.println(x);
		
		WebElement ar=driver.findElement(By.xpath("//a[.='Forgotten password?']"));
		
		String y=ar.getAttribute("href");
		System.out.println(y);
		
		Point z=ar.getLocation();
		
		int p=z.getX();
		int q=z.getY();
		System.out.println(p);
		System.out.println(q);
		
		String size=ar.getCssValue("font-size");
		
		System.out.println(size);
		
		Dimension t= ar.getSize();
		int e=t.height;
		int d=t.width;
		System.out.println(e);
		System.out.println(d);
		
		
		
		
		
		
		
		
		
		
		
	
	}

}
