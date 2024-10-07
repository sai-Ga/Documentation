# Java Maven Project Setup with Selenium in Eclipse

This guide will help you set up a Java project using Maven in Eclipse and integrate Selenium for automated testing.

## Steps to Create a Maven Project and Add Selenium Dependency in Eclipse

### 1. Convert Java Project to Maven
- Open Eclipse IDE.
- If you have an existing Java project, right-click on the project in the Project Explorer.
- Select **Configure** > **Convert to Maven Project**.
- Follow the prompts to create a `pom.xml` file.

### 2. Search for Selenium Java Dependency
- Open your web browser and go to [mvnrepository.com](https://mvnrepository.com).
- In the search bar, type **Selenium Java** and press Enter.

### 3. Get the Latest Dependency Code
- Locate the latest version of the Selenium Java dependency on mvnrepository.com.
- Cross-check the latest version on the official Selenium downloads page: [Selenium Downloads](https://www.selenium.dev/downloads/).
- Copy the dependency code snippet, which should look something like this:

    ```xml
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>YOUR_LATEST_VERSION</version>
    </dependency>
    ```

### 4. Add Dependency to `pom.xml`
- In Eclipse, locate the `pom.xml` file in the root of your Maven project.
- Open the `pom.xml` file.
- Inside the `<dependencies>` section, paste the copied dependency code. Ensure it looks like this:

    ```xml
    <dependencies>
        <!-- Other dependencies -->
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>YOUR_LATEST_VERSION</version>
        </dependency>
    </dependencies>
    ```

- Save the `pom.xml` file.

### 5. Build Maven Project
- In Eclipse, right-click on the project in the Project Explorer.
- Select **Run As** > **Maven Build...**.
- In the dialog that appears, enter **`package`** as the goal and click **Run**.

### 6. Verify Build Success
- Check the Console view in Eclipse for the build output.
- If you see **BUILD SUCCESS**, you’re ready to start programming with Selenium!
- If the build fails, you may need to downgrade the Selenium version by one version:
  - Go back to mvnrepository.com and select the previous version.
  - Update the `<version>` in your `pom.xml` accordingly, then repeat the build step.

## Conclusion
You have successfully set up a Maven project with Selenium in Eclipse. Start writing your test scripts and enjoy automated testing!

