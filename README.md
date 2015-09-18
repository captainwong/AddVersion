File "VersionNo.h" must exsists in project directory, content must be like "major.minor.revision.build", e.g. "1.0.0.2345".
After execute the 


1.AddMajorVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini M 1
2.AddMinorVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini m 1
3.AddRevisionVersion: $(ProjectDir)VersionNo.h $(ProjectDir)VersionNo.ini r 1
4.After build:
	In visual studio, go through Project -- property -- build event -- after build -- command line:  
	paste "$(ProjectDir)AfterBuild.bat" $(ProjectDir) $(TargetDir) b 1