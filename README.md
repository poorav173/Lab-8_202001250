# Lab8_202001250
## IT 314 Software Engineering
## Name: Poorav Patel
## Id: 202001250
## Date: 21/04/23
### Aim: The goal of this lab is to learn how to use JUnit to write unit tests for Java programs.

- Creating class Boa in the eclipse ide

![image](https://user-images.githubusercontent.com/84453061/233056937-5dc619d0-aed7-4c1b-a836-949fd077b4a1.png)

Boa class:

    package Tests;
@@ -49,9 +51,11 @@ Boa class:

- Making the junit test file

![image](https://user-images.githubusercontent.com/84453061/233057470-a3fcf8a0-a02d-43a7-a12b-cb268b60f59a.png)


BoaTest junit file:

        BoaTest junit file:
        package Tests;
        import static org.junit.Assert.*;
        import org.junit.Before;
        import org.junit.Test;
        public class boaTest {
            private Boa jen;
            private Boa ken;
            @Before
            public void setUp() throws Exception {
                jen = new Boa("Jennifer", 2, "grapes");
                ken = new Boa ("Kenneth", 3, "granola bars");
            }
            @Test
            public void testIsHealthy_1() {
                boolean output=jen.isHealthy();
                assertEquals(output,false);
            }
            @Test
            public void testIsHealthy_2() {
                boolean output=ken.isHealthy();
                assertEquals(output,true);
            }
            
            @Test
            public void testFitsInCage_1() {
                boolean out=jen.fitsInCage(1);
                assertEquals(out,false);
            }
            @Test
            public void testFitsInCage_2() {
                boolean out=jen.fitsInCage(3);
                assertEquals(out,true);
            }
            @Test
            public void testFitsInCage_3() {
                boolean out=ken.fitsInCage(2);
                assertEquals(out,false);
            }
            
            @Test
            public void testFitsInCage_4() {
                boolean out=ken.fitsInCage(4);
                assertEquals(out,true);
            }
            
            @Test
            public void lengthInInches_1() {
                int out=jen.lengthInInches();
                assertEquals(out,24);
            }
            
            @Test
            public void lengthInInches_2() {
                int out=ken.lengthInInches();
                assertEquals(out,36);
            }
        }
- Testing the Boa Class against the BoaTest junit file:
![image](https://user-images.githubusercontent.com/84453061/233053837-5f16e8dc-6fc9-4ae6-bd8e-c039ef65f0ce.png)
![image](https://user-images.githubusercontent.com/84453061/233054054-67c9d19b-e910-4567-bcc3-1984d7fe2fc7.png)
