JC = javac
RM = rm
JAVAS = *.java

# main class name
MAINCLASS = principal

app: $(JAVAS) manifest
	$(JC) *.java # "COMPILING JAVA FILES"
	jar cfm app.jar Manifest.txt *.class # "CREATING JAR FILE"
	$(RM) *.class # "REMOVING FILES .class"

# CREATING MANIFEST FILE
manifest:
	touch Manifest.txt
	echo Main-Class: $(MAINCLASS) >> Manifest.txt

# 'make run' runs the file 
run: app.jar
	java -jar app.jar # running

# 'make clean'
clean: app.jar
	$(RM) app.jar # deleting executable file

	