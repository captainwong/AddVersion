File "VersionNo.h" must exsists in project directory, content must be like "major.minor.revision.build", e.g. "1.0.0.2345".

After execute the command, it will generate a file names "VersionNo.ini" in folder "Debug" or "Release" based on your current project setting.

The file "VersionNo.ini" could be used in nsis bat file to make an installer.


1.AddMajorVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini M 1

2.AddMinorVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini m 1

3.AddRevisionVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini r 1

4.After build:
	In visual studio, go through Project -- property -- build event -- after build -- command line:  
	"$(ProjectDir)AfterBuild.bat" $(ProjectDir) $(TargetDir)