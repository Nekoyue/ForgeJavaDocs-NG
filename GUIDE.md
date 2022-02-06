# Guide to build your own Forge Javadocs

This guide uses build-in tools of IntelliJ IDEA to generate Javadocs files. Some alternative ways could be `javadoc` and `./gradlew javadoc` commands.

1. Clone Forge repository to your local machine. Add e.g. `--branch 1.18.x` option in case you need to specify a Minecraft version.

```text
git clone https://github.com/MinecraftForge/MinecraftForge.git
```

2. Import Forge project to IntelliJ IDEA. Simply drag & drop `MinecraftForge` folder to IntelliJ IDEA's starting menu. Click on "Trust Project" if prompted.
  
3. Run `./gradlew setup` command in terminal (or select `setup` task in Gradle menu.) This will download Minecraft's source code for generating documentation of `com.mojang.*` and `net.minecraft.*` packages.
  
4. Delete `./projects/clean/` and `./projects/fmlonly/` folders. These files cause conflicts during file generation.

5. Select `Tools` - `Generate JavaDoc...` in the menu bar. You may need to change the output directory and command-line arguments like follows:

```text
-encoding utf-8 -docencoding utf-8 -charset utf-8 -windowtitle "forge 1.18.1-39.0.57" -doctitle "forge 1.18.1-39.0.57"
```

<img src="https://gist.github.com/Nekoyue/b282e42f033572d7548a640d9f02b28f/raw/a33f35ba90bb299e14666736bd430c6a1658e3e2/1_GenerateJavaDocWindow.png" width="500" alt="Generate JavaDoc window"/>

6. Complete by clicking "OK" button, take a break. The document can be opened with `index.html` file in the output folder.
