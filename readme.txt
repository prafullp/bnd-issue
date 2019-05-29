1. Make sure you have Bnd Plugin version 4.2.0 installed in Eclipse.
2. I used Java 8 as Runtime environment
3. Import the project as bnd workspace by pointing to the base directory of the project folder which is "bnd-issue".
4. After successful build of the project, go to "com.example.dependent" project and use "launch.bndrun" file to run as "Bnd OSGI Run Launcher". The execution will fail but it doesn't matter for this issue.
5. After clicking run, it will create a run configuration called "Launch.bndrun". Go to Run option and open "Run Configuration". 
6. Go to "Lanuch.bndrun" and click "source". Under default, you will see that the source projects "com.example" and "com.example.dependent" is pointing to "bin" directory rather than project root directory. Because of this Eclipse is not able to look up default source path. If you try the same in 4.1.0 bnd tools version, the path is shown correctly.