# Guide to building your own Forge Javadocs

This guide uses IntelliJ IDEA's build-in tools to generate Javadocs. An alternative way is to use `javadoc`
or `./gradlew javadoc` command, and the procedure is not covered here.

1. Clone Forge repository to your local machine. Add e.g. `--branch 1.18.x` option if needed to work with an earlier
   version of Minecraft.
    ```text
    git clone https://github.com/MinecraftForge/MinecraftForge.git
    ```

2. Open Forge project in IntelliJ IDEA. Click "Trust Project" if prompted.
   Set project SDK in `Top Menu Bar` - `File` - `Project Structure`. The IDE may sometimes do this automatically.

3. Run `./gradlew setup` command in the terminal (or select `setup` task from the Gradle menu).
   This will download Minecraft's source code and generate documents from `com.mojang.*` and `net.minecraft.*` later.

4. Delete `./projects/clean/` and `./projects/fmlonly/` folders. These files cause conflicts during Javadoc generation.

5. Select `Top Menu Bar` - `Tools` - `Generate JavaDoc...`. Choose an output directory.
   Set the command-line arguments like follows:

    ```text
    -encoding utf-8 -docencoding utf-8 -charset utf-8 -windowtitle "forge 1.19-41.0.38" -doctitle "forge 1.19-41.0.38" 
    ```

    <img src="https://gist.github.com/Nekoyue/b282e42f033572d7548a640d9f02b28f/raw/a33f35ba90bb299e14666736bd430c6a1658e3e2/1_GenerateJavaDocWindow.png" width="500" alt="Generate JavaDoc window"/>

6. Complete by clicking "OK" button and take a break. Done.
