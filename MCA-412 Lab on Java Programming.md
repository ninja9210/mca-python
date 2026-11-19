# MCA-412 Lab on Java Programming

## Assignment 01: - Implement a program that demonstrates program structure of java with use of arithmetical and 21 logical implementation.

```java
public class Demo
{
    public static void main(String[] args)
    {
        int a = 20;
        int b = 8;
        System.out.println("Arithmetic Operations:");
        System.out.println("a + b = " + (a + b));
        System.out.println("a - b = " + (a - b));
        System.out.println("a * b = " + (a * b));
        System.out.println("a / b = " + (a / b));
        System.out.println("a % b = " + (a % b));
        boolean x = true;
        boolean y = false;
        System.out.println("\nLogical Operations:");
        System.out.println("x && y = " + (x && y));
        System.out.println("x || y = " + (x || y));
        System.out.println("!x = " + (!x));
        System.out.println("\nCombination Example:");
        System.out.println("(a > b) && (b > 0) = " + ((a > b) && (b > 0)));
        System.out.println("(a < b) || (a == 20) = " + ((a < b) || (a == 20)));
    }
}
```

---

## Assignment 02: - Implement a program that demonstrates string operations using String and String Buffer class.

```java
public class StringOperationsDemo
{
    public static void main(String[] args)
    {
        String str1 = "Hello";
        String str2 = "World";
        String str3 = " Java Programming ";

        System.out.println("---- String Class Operations ----");

        System.out.println("Original String str1: " + str1);

        System.out.println("Length of str1: " + str1.length());

        System.out.println("Concatenation: " + str1.concat(" ").concat(str2));

        System.out.println("Character at index 1 of str1: " + str1.charAt(1));

        System.out.println("Substring (1–4): " + str1.substring(1, 4));

        System.out.println("Upper case: " + str1.toUpperCase());

        System.out.println("Lower case: " + str1.toLowerCase());

        System.out.println("Trimmed str3: '" + str3.trim() + "'");

        System.out.println("Replace 'l' with 'p': " + str1.replace('l', 'p'));

        System.out.println("str1 equals 'Hello'? " + str1.equals("Hello"));

        System.out.println("str1equalsIgnoreCase 'hello'? " + str1.equalsIgnoreCase("hello"));

        System.out.println("str2 starts with 'W'? " + str2.startsWith("W"));
        System.out.println("str2 ends with 'd'? " + str2.endsWith("d"));

        System.out.println("Index of 'l' in str1: " + str1.indexOf('l'));

        StringBuffer sb = new StringBuffer("OpenAI");

        System.out.println("\n---- StringBuffer Operations ----");
        System.out.println("Original StringBuffer: " + sb);

        sb.append(" GPT");
        System.out.println("After append: " + sb);

        sb.insert(6, " Chat");
        System.out.println("After insert: " + sb);

        sb.replace(0, 5, "Closed");
        System.out.println("After replace: " + sb);

        sb.delete(0, 6);
        System.out.println("After delete first 6 chars: " + sb);

        sb.reverse();
        System.out.println("After reverse: " + sb);

        System.out.println("Buffer capacity: " + sb.capacity());
        System.out.println("Buffer length: " + sb.length());
    }
}
```

---

## Assignment 03: - Implement a program that demonstrates inner class and static fields.

```java
public class Demo
{
    private static int count = 0;
    private String name;

    public Demo(String name)
    {
        this.name = name;
        count++;
    }

    public void showName()
    {
        System.out.println("Outer object name: " + name);
    }

    public class Inner
    {
        public void display()
        {
            System.out.println("Inner can see outer name: " + name);
            System.out.println("Total objects created (static): " + count);
        }
    }

    public static void main(String[] args)
    {
        Demo d1 = new Demo("First");
        Demo d2 = new Demo("Second");

        d1.showName();
        d2.showName();

        Demo.Inner i1 = d1.new Inner();
        i1.display();

        Demo.Inner i2 = d2.new Inner();
        i2.display();

        System.out.println("Static count = " + Demo.count);
    }
}
```

---

## Assignment 04: - Implement a program that demonstrate inheritance, polymorphism.

```java
class Animal
{
    public void sound()
    {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal
{
    public void sound()
    {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal
{
    public void sound()
    {
        System.out.println("Cat meows");
    }
}

public class DemoInheritance
{
    public static void main(String[] args)
    {
        Animal a1 = new Dog();
        Animal a2 = new Cat();

        a1.sound();
        a2.sound();

        Dog d = new Dog();
        d.sound();

        Cat c = new Cat();
        c.sound();
    }
}
```

---

## Assignment 05: - Implement a program that demonstrates 2D shapes on frames.

```java
import javax.swing.*;
import java.awt.*;

public class ShapesDemo extends JFrame
{
    public ShapesDemo()
    {
        setTitle("2D Shapes Demo");
        setSize(600, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }

    public void paint(Graphics g)
    {
        super.paint(g);
        Graphics2D g2 = (Graphics2D) g;

        g2.setColor(Color.RED);
        g2.drawLine(50, 80, 200, 80);

        g2.setColor(Color.BLUE);
        g2.drawRect(50, 120, 150, 80);

        g2.setColor(Color.GREEN);
        g2.drawOval(250, 120, 150, 80);

        g2.setColor(Color.MAGENTA);
        g2.drawOval(50, 260, 100, 100);

        g2.setColor(Color.ORANGE);
        g2.drawArc(250, 260, 120, 100, 0, 180);

        g2.setColor(Color.CYAN);
        g2.fillRect(420, 120, 100, 80);
    }

    public static void main(String[] args)
    {
        new ShapesDemo();
    }
}
```

---

## Assignment 06: - Implement a program that demonstrates color and fonts.

```java
import java.awt.*;
import javax.swing.*;

public class ColorFontExample extends JPanel
{
    protected void paintComponent(Graphics g)
    {
        super.paintComponent(g);

        setBackground(Color.BLACK);

        g.setColor(Color.RED);
        g.setFont(new Font("Serif", Font.BOLD, 24));
        g.drawString("Bold Red Text", 40, 60);

        g.setColor(Color.GREEN);
        g.setFont(new Font("Arial", Font.ITALIC, 20));
        g.drawString("Italic Green Text", 40, 100);

        g.setColor(Color.BLUE);
        g.setFont(new Font("Courier New", Font.PLAIN, 22));
        g.drawString("Plain Blue Text", 40, 140);
    }

    public static void main(String args[])
    {
        JFrame frame = new JFrame("Color & Font Example");
        frame.setSize(400, 250);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.add(new ColorFontExample());
        frame.setVisible(true);
    }
}
```

---

## Assignment 07: - Implement a program to illustrate use of various swing components.

```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class SwingComponentsDemo extends JFrame
{
    public SwingComponentsDemo()
    {
        setTitle("Swing Components Demo");
        setSize(500, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new FlowLayout());

        JLabel label = new JLabel("Enter your name: ");
        add(label);

        JTextField textField = new JTextField(15);
        add(textField);

        JButton button = new JButton("Click Me");
        add(button);

        JCheckBox checkBox = new JCheckBox("I agree");
        add(checkBox);

        JRadioButton male = new JRadioButton("Male");
        JRadioButton female = new JRadioButton("Female");
        ButtonGroup genderGroup = new ButtonGroup();
        genderGroup.add(male);
        genderGroup.add(female);
        add(male);
        add(female);

        String[] countries = {"India", "USA", "UK", "Canada"};
        JComboBox<String> comboBox = new JComboBox<>(countries);
        add(comboBox);

        JTextArea textArea = new JTextArea(5, 20);
        JScrollPane scrollPane = new JScrollPane(textArea);
        add(scrollPane);

        button.addActionListener(new ActionListener()
        {
            public void actionPerformed(ActionEvent e)
            {
                String name = textField.getText();
                String gender = male.isSelected() ? "Male" : (female.isSelected() ? "Female" : "Not selected");
                String country = (String) comboBox.getSelectedItem();
                String agree = checkBox.isSelected() ? "Agreed" : "Not Agreed";

                textArea.setText("Name: " + name +
                        "\nGender: " + gender +
                        "\nCountry: " + country +
                        "\nAgreement: " + agree);
            }
        });

        setVisible(true);
    }

    public static void main(String args[])
    {
        new SwingComponentsDemo();
    }
}
```

---

## Assignment 08: - Implement a program that demonstrates use of dialog box and menus.

```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MenuDialogDemo extends JFrame
{
    public MenuDialogDemo()
    {
        setTitle("Menu and Dialog Demo");
        setSize(400, 300);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JMenuBar menuBar = new JMenuBar();

        JMenu fileMenu = new JMenu("File");
        JMenuItem newItem = new JMenuItem("New");
        JMenuItem exitItem = new JMenuItem("Exit");
        fileMenu.add(newItem);
        fileMenu.add(exitItem);

        JMenu helpMenu = new JMenu("Help");
        JMenuItem aboutItem = new JMenuItem("About");
        helpMenu.add(aboutItem);

        menuBar.add(fileMenu);
        menuBar.add(helpMenu);
        setJMenuBar(menuBar);

        newItem.addActionListener(e -> {
            JOptionPane.showMessageDialog(this,
                    "New File Created!",
                    "Information",
                    JOptionPane.INFORMATION_MESSAGE);
        });

        exitItem.addActionListener(e -> {
            int choice = JOptionPane.showConfirmDialog(this,
                    "Do you really want to exit?",
                    "Confirm Exit",
                    JOptionPane.YES_NO_OPTION);
            if (choice == JOptionPane.YES_OPTION)
            {
                System.exit(0);
            }
        });

        aboutItem.addActionListener(e -> {
            String name = JOptionPane.showInputDialog(this,
                    "Enter your name:",
                    "Input Dialog",
                    JOptionPane.QUESTION_MESSAGE);
            if (name != null && !name.trim().isEmpty())
            {
                JOptionPane.showMessageDialog(this,
                        "Hello, " + name + "!\nWelcome to the Menu & Dialog Demo.",
                        "About", JOptionPane.PLAIN_MESSAGE);
            }
        });

        setVisible(true);
    }

    public static void main(String[] args)
    {
        new MenuDialogDemo();
    }
}
```

---

## Assignment 09: - Implement a program that demonstrates event handling for various types of events.

### 1. ActionEvent (FactorialDemo)
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class FactorialDemo extends JFrame implements ActionListener
{
    JLabel resultLabel;
    JTextField inputField;

    public FactorialDemo()
    {
        setTitle("Factorial Example");
        setSize(350,150);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new FlowLayout());

        add(new JLabel("Enter a number:"));
        inputField = new JTextField(10);
        add(inputField);

        JButton button = new JButton("Find Factorial");
        button.addActionListener(this);
        add(button);

        resultLabel = new JLabel("");
        add(resultLabel);

        setVisible(true);
    }

    public void actionPerformed(ActionEvent e)
    {
        try
        {
            int num = Integer.parseInt(inputField.getText());
            long fact = 1;
            for(int i=1; i<=num; i++)
            {
                fact *= i;
            }
            resultLabel.setText("Factorial of " + num + " = " + fact);
        }
        catch (NumberFormatException ex)
        {
            resultLabel.setText("Please enter a valid integer!");
        }
    }

    public static void main(String[] args)
    {
        new FactorialDemo();
    }
}
```

### 2. KeyEvent (KeyEventDemo)
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class KeyEventDemo extends JFrame implements KeyListener
{
    JLabel label;

    public KeyEventDemo()
    {
        setTitle("KeyEvent Example");
        setSize(300,150);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new FlowLayout());

        JTextField field = new JTextField(10);
        field.addKeyListener(this);
        add(field);

        label = new JLabel("Type something...");
        add(label);

        setVisible(true);
    }

    public void keyTyped(KeyEvent e)
    {
        label.setText("Typed: " + e.getKeyChar());
    }

    public void keyPressed(KeyEvent e)
    {
        System.out.println("Key Pressed");
    }

    public void keyReleased(KeyEvent e)
    {
        System.out.println("Key Released");
    }

    public static void main(String[] args)
    {
        new KeyEventDemo();
    }
}
```

### 3. MouseEvent (MouseEventDemo)
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class MouseEventDemo extends JFrame implements MouseListener
{
    JLabel label;

    public MouseEventDemo()
    {
        setTitle("MouseEvent Example");
        setSize(300,200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JPanel panel = new JPanel();
        panel.setBackground(Color.LIGHT_GRAY);
        panel.addMouseListener(this);
        add(panel);

        label = new JLabel("Click or move the mouse inside panel");
        panel.add(label);

        setVisible(true);
    }

    public void mouseClicked(MouseEvent e)
    {
        label.setText("Clicked at ("+e.getX()+","+e.getY()+")");
    }

    public void mousePressed(MouseEvent e)
    {
        System.out.println("mousePressed");
    }

    public void mouseReleased(MouseEvent e)
    {
        System.out.println("mouseReleased");
    }

    public void mouseEntered(MouseEvent e)
    {
        label.setText("Mouse Entered");
    }

    public void mouseExited(MouseEvent e)
    {
        label.setText("Mouse Exited");
    }

    public static void main(String[] args)
    {
        new MouseEventDemo();
    }
}
```

### 4. WindowEvent (WindowEventDemo)
```java
import javax.swing.*;
import java.awt.event.*;

public class WindowEventDemo extends JFrame implements WindowListener
{
    JLabel label;

    public WindowEventDemo()
    {
        setTitle("WindowEvent Example");
        setSize(300,150);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        label = new JLabel("Watch window events in console");
        add(label);

        addWindowListener(this);
        setVisible(true);
    }

    public void windowOpened(WindowEvent e)
    {
        System.out.println("Window Opened");
    }

    public void windowClosing(WindowEvent e)
    {
        System.out.println("Window Closing");
    }

    public void windowClosed(WindowEvent e)
    {
        System.out.println("Window Closed");
    }

    public void windowIconified(WindowEvent e)
    {
        System.out.println("Window Minimized");
    }

    public void windowDeiconified(WindowEvent e)
    {
        System.out.println("Window Restored");
    }

    public void windowActivated(WindowEvent e)
    {
        System.out.println("Window Activated");
    }

    public void windowDeactivated(WindowEvent e)
    {
        System.out.println("Window Deactivated");
    }

    public static void main(String[] args)
    {
        new WindowEventDemo();
    }
}
```

---

## Assignment 10: - Implement a program to illustrate multithreading

```java
class Task1 extends Thread
{
    public void run()
    {
        for (int i = 1; i <= 5; i++)
        {
            System.out.println("Task 1 - Count: " + i);
            try
            {
                Thread.sleep(500);
            }
            catch (InterruptedException e)
            {
                System.out.println(e);
            }
        }
        System.out.println("Task 1 completed!");
    }
}

class Task2 implements Runnable
{
    public void run()
    {
        for (int i = 1; i <= 5; i++)
        {
            System.out.println("Task 2 - Count: " + i);
            try
            {
                Thread.sleep(700);
            }
            catch (InterruptedException e)
            {
                System.out.println(e);
            }
        }
        System.out.println("Task 2 completed!");
    }
}

public class MultithreadingDemo
{
    public static void main(String[] args)
    {
        Task1 t1 = new Task1();
        Thread t2 = new Thread(new Task2());

        t1.start();
        t2.start();

        for (int i = 1; i <= 5; i++)
        {
            System.out.println("Main Thread - Count: " + i);
            try
            {
                Thread.sleep(600);
            }
            catch (InterruptedException e)
            {
                System.out.println(e);
            }
        }
        System.out.println("Main Thread completed!");
    }
}
```

---

## Assignment 11: - Implement a program to illustrate exception handling.

```java
public class ExceptionHandlingDemo
{
    public static void main(String[] args)
    {
        try
        {
            int num1 = 10;
            int num2 = 0;

            System.out.println("Before division...");
            int result = num1 / num2;
            System.out.println("Result: " + result);
        }
        catch (ArithmeticException e)
        {
            System.out.println("Error: Division by zero is not allowed!");
        }
        catch (Exception e)
        {
            System.out.println("An unexpected error occurred: " + e);
        }
        finally
        {
            System.out.println("Finally block executed program ends safely.");
        }

        System.out.println("Program continues after exception handling...");
    }
}
```

---

## Assignment 12: - Implement a program to demonstrate use of File class.

### 1. FileDemo
```java
import java.io.File;

public class FileDemo
{
    public static void main(String[] args)
    {
        File file = new File("example.txt");

        System.out.println("File Name: " + file.getName());
        System.out.println("File Path: " + file.getPath());
        System.out.println("Absolute Path: " + file.getAbsolutePath());
        System.out.println("Parent Directory: " + file.getParent());
        System.out.println("------------------------------------");

        if (file.exists())
        {
            System.out.println("File already exists.");
            System.out.println("Is it readable? " + file.canRead());
            System.out.println("Is it writable? " + file.canWrite());
            System.out.println("Is it executable? " + file.canExecute());
            System.out.println("File size: " + file.length() + " bytes");
        }
        else
        {
            System.out.println("File does not exist. Creating new file...");
            try
            {
                boolean created = file.createNewFile();
                if (created)
                    System.out.println("File created successfully!");
                else
                    System.out.println("Failed to create file.");
            }
            catch (Exception e)
            {
                System.out.println("Error: " + e.getMessage());
            }
        }
    }
}
```

### 2. FileWriteCopyDemo
```java
//Program: Create, Write, and Copy File Content
import java.io.*;

public class FileWriteCopyDemo
{
    public static void main(String[] args)
    {
        try
        {
            File file1 = new File("source.txt");
            FileWriter writer = new FileWriter(file1);
            writer.write("Hello, this is a demo of File Handling in Java.\n");
            writer.write("We are copying this text into another file.");
            writer.close();
            System.out.println("Data written to source.txt successfully.");

            File file2 = new File("destination.txt");
            FileWriter writer2 = new FileWriter(file2);
            FileReader reader = new FileReader(file1);
            BufferedReader br = new BufferedReader(reader);
            String line;

            while ((line = br.readLine()) != null)
            {
                writer2.write(line + "\n");
            }

            br.close();
            writer2.close();
            System.out.println("Content copied from source.txt to destination.txt successfully!");
        }
        catch (IOException e)
        {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```

---

## Assignment 13: - Implement a program that demonstrates JDBC on application.

```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.sql.*;

public class JDBCFrameDemo extends JFrame implements ActionListener
{
    JTextField t1, t2;
    JButton insertBtn, updateBtn, deleteBtn, clearBtn;
    Connection conn;
    PreparedStatement pst;

    public JDBCFrameDemo()
    {
        setTitle("JDBC with MS Access Demo");
        setSize(400, 300);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new GridLayout(5, 2, 10, 10));

        add(new JLabel("Student Name:"));
        t1 = new JTextField();
        add(t1);

        add(new JLabel("Student Age:"));
        t2 = new JTextField();
        add(t2);

        insertBtn = new JButton("Insert");
        updateBtn = new JButton("Update");
        deleteBtn = new JButton("Delete");
        clearBtn = new JButton("Clear");

        add(insertBtn);
        add(updateBtn);
        add(deleteBtn);
        add(clearBtn);

        insertBtn.addActionListener(this);
        updateBtn.addActionListener(this);
        deleteBtn.addActionListener(this);
        clearBtn.addActionListener(this);

        connectDB();
        setVisible(true);
    }

    void connectDB()
    {
        try
        {
            Class.forName("net.ucanaccess.jdbc.UcanaccessDriver");
            conn = DriverManager.getConnection("jdbc:ucanaccess://D:/JDBCApp/StudentDB.accdb");
            JOptionPane.showMessageDialog(this, "Database Connected Successfully!");
        }
        catch (Exception e)
        {
            JOptionPane.showMessageDialog(this, "Connection Error: " + e.getMessage());
        }
    }

    @Override
    public void actionPerformed(ActionEvent ae)
    {
        String name = t1.getText();
        String ageText = t2.getText();
        try
        {
            if (ae.getSource() == insertBtn)
            {
                pst = conn.prepareStatement("INSERT INTO Student (Name, Age) VALUES (?, ?)");
                pst.setString(1, name);
                pst.setInt(2, Integer.parseInt(ageText));
                pst.executeUpdate();
                JOptionPane.showMessageDialog(this, "Record Inserted Successfully!");
            }
            else if (ae.getSource() == updateBtn)
            {
                String id = JOptionPane.showInputDialog("Enter Student ID to Update:");
                pst = conn.prepareStatement("UPDATE Student SET Name=?, Age=? WHERE ID=?");
                pst.setString(1, name);
                pst.setInt(2, Integer.parseInt(ageText));
                pst.setInt(3, Integer.parseInt(id));
                pst.executeUpdate();
                JOptionPane.showMessageDialog(this, "Record Updated Successfully!");
            }
            else if (ae.getSource() == deleteBtn)
            {
                String id = JOptionPane.showInputDialog("Enter Student ID to Delete:");
                pst = conn.prepareStatement("DELETE FROM Student WHERE ID=?");
                pst.setInt(1, Integer.parseInt(id));
                pst.executeUpdate();
                JOptionPane.showMessageDialog(this, "Record Deleted Successfully!");
            }
            else if (ae.getSource() == clearBtn)
            {
                t1.setText("");
                t2.setText("");
            }
        }
        catch (Exception e)
        {
            JOptionPane.showMessageDialog(this, "Error: " + e.getMessage());
        }
    }

    public static void main(String[] args)
    {
        new JDBCFrameDemo();
    }
}
```

### Setup & Run Instructions:
* **Download UCanAccess:** Go to `https://ucanaccess.sourceforge.net/site.html` and download the latest version ZIP file (e.g., `UCanAccess-5.0.1.zip`).
* **Extract and Add JAR Files:**
  * `ucanaccess-5.0.1.jar`
  * `lib/commons-lang-2.6.jar`
  * `lib/commons-logging-1.1.3.jar`
  * `lib/hsqldb.jar`
  * `lib/jackcess-3.0.1.jar`
* **Run Application:**
```bash
javac -cp ".;lib/*" JDBCFrameDemo.java
java -cp ".;lib/*" JDBCFrameDemo
```

---

## Assignment 14: -

### 1. Student.java
```java
package student;

public class Student
{
    protected int rollNo;
    protected String name;

    public Student(int rollNo, String name)
    {
        this.rollNo = rollNo;
        this.name = name;
    }

    public void displayStudent()
    {
        System.out.println("Roll No : " + rollNo);
        System.out.println("Name : " + name);
    }
}
```

### 2. Marks.java
```java
package student;

public class Marks extends Student
{
    private int m1, m2, m3;

    public Marks(int rollNo, String name, int m1, int m2, int m3)
    {
        super(rollNo, name);
        this.m1 = m1;
        this.m2 = m2;
        this.m3 = m3;
    }

    public void displayResult()
    {
        displayStudent();
        System.out.println("Marks : " + m1 + ", " + m2 + ", " + m3);
        System.out.println("Total : " + (m1 + m2 + m3));
    }
}
```

### 3. MainApp.java
```java
import student.Marks;

public class MainApp
{
    public static void main(String[] args)
    {
        Marks obj = new Marks(101, "Rahul", 78, 85, 90);
        obj.displayResult();
    }
}
```

### Compilation and Run
```bash
javac student/Student.java
javac student/Marks.java
java MainApp
```