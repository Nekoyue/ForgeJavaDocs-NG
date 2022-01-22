# Guide to build your own Forge Javadocs

This guide uses build-in tools of IntelliJ IDEA to generate Javadocs files. It may be possible to use `javadoc` and `./gradlew javadoc` commands, though I have never tried before.

1. Clone Forge repository to your local machine. The Minecraft version can be specified with e.g. `--branch 1.18.x` option.

```text
git clone https://github.com/MinecraftForge/MinecraftForge.git
```

2. Import Forge project to IntelliJ IDEA. Simply drag & drop `MinecraftForge` folder to IntelliJ IDEA's starting menu.
  
3. Run `./gradlew setup` command in terminal or select `setup` task in Gradle menu. This will set up Minecraft's source code for generating documents of `com.mojang.*` and `net.minecraft.*` packages.
  
4. Delete `./projects/clean/` and `./projects/fmlonly/` folders, otherwise they will cause conflicts during file generation.

5. Select `Tools` - `Generate JavaDoc...` in the menu bar. You may want to change the output directory and command-line arguments like follows:

```text
-encoding utf-8 -docencoding utf-8 -charset utf-8 -windowtitle "forge 1.18.1-39.0.57" -doctitle "forge 1.18.1-39.0.57"
```

<img src="https://gist.github.com/Nekoyue/b282e42f033572d7548a640d9f02b28f/raw/a33f35ba90bb299e14666736bd430c6a1658e3e2/1_GenerateJavaDocWindow.png" width="500" alt="Generate JavaDoc window"/>

6. Click OK, take a break, and then check `index.html` file in the output folder.