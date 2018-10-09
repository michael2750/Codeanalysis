# Codeanalysis

### 1.

The results can be seen [here](https://github.com/michael2750/Codeanalysis/tree/master/pmdresults).

We couldnt figure out how to run pmd with a specific metric, but we would like something like:

- [Codestyle](https://github.com/michael2750/Codeanalysis/blob/master/pmdresults/pmdcodestyle.txt)

  (1) java-controversial/AvoidFinalLocalVariable
  
  (2) java-naming/VariableNamingConventions
  
  (3) java-naming/MethodNamingConventions
  
  (4) java-unnecessary/UnnecessaryModifier
  
  (5) java-design/FieldDeclarationsShouldBeAtStartOfClass
  
- [Performance](https://github.com/michael2750/Codeanalysis/blob/master/pmdresults/pmdperformance.txt)

  (6) java-optimizations/AvoidInstantiatingObjectsInLoops
 
- [Design](https://github.com/michael2750/Codeanalysis/blob/master/pmdresults/pmddesign.txt)

  (7) java-coupling/CouplingBetweenObjects
  
  (8) java-design/FinalFieldCouldBeStatic
  
  (9) java-coupling/LawOfDemeter
  
  (10) java-coupling/ExcessiveImports
  
We have chosen all the checks above as some of the errors we got in our pmd-report and some checks for the use of general mistakes when we create a program.

### 2.

- [Netbeans profiler (screenshot)](https://github.com/michael2750/Codeanalysis/blob/master/NetbeansProfilerResults.PNG)

![](https://github.com/michael2750/Codeanalysis/blob/master/Bottleneck.PNG)

The lib call wich took the longest was: org.netbeans.lib.profiler.server.ProfilerServer.activate(String, int, int, int). This is for our logger function in inputhandler() which catches an exception and logs it. This method (if an InputMismatchException appears) makes a thread.sleep wich sleeps before logging the error message.

