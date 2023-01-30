# Guide to building your own Forge Javadocs

This guide uses IntelliJ IDEA's build-in tools to generate Javadocs. There may be alternative ways to use `javadoc`
or `./gradlew javadoc`, and the procedure is not covered here.

1. Clone the Forge repository to your local machine. Specify an e.g. `--branch 1.18.x` option to work with an earlier version.
    ```text
    git clone --depth 1 https://github.com/MinecraftForge/MinecraftForge.git 
    ```

2. Open Forge project in IntelliJ IDEA. Click "Trust Project" if prompted.
   Set up the project SDK from `Top Menu Bar` - `File` - `Project Structure`. IDE sometimes does this automatically.

3. Run `./gradlew setup` command in the terminal (or select `setup` task from the Gradle menu).
   Source code from Minecraft and other relevant packages will be included later in the Javadoc.

4. Delete `./projects/clean/` and `./projects/fmlonly/` folders. These files cause conflicts during Javadoc generation.

5. Select `Top Menu Bar` - `Tools` - `Generate JavaDoc...`. Choose an output directory.
   Set the command-line arguments like follows:

    ```text
    -encoding utf-8 -docencoding utf-8 -charset utf-8 -windowtitle "forge 1.19.3-44.1.4" -doctitle "forge 1.19.3-44.1.4" 
    ```

    <img src="https://gist.githubusercontent.com/Nekoyue/b282e42f033572d7548a640d9f02b28f/raw/7bf941af87c7cbea1ed15ee7eae413fbd32bc6bb/1_GenerateJavaDocWindow.png" width="500" alt="Generate JavaDoc window"/>

6. Complete by clicking "OK" button and take a break. Done.
