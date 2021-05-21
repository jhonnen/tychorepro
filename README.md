`mvn validate` fails with 

```
[ERROR] Internal error: java.lang.RuntimeException: org.osgi.framework.BundleException: Bundle bundle cannot be resolved:bundle [100]
[ERROR]   Unresolved requirement: Require-Bundle: com.collabnet.subversion.merge
[ERROR]     -> Bundle-SymbolicName: com.collabnet.subversion.merge; bundle-version="4.2.0.1"; singleton:="true"
[ERROR]        com.collabnet.subversion.merge [1]
[ERROR]          Unresolved requirement: Require-Bundle: org.eclipse.jdt.core
[ERROR] -> [Help 1]
org.apache.maven.InternalErrorException: Internal error: java.lang.RuntimeException: org.osgi.framework.BundleException: Bundle bundle cannot be resolved:bundle [100]
  Unresolved requirement: Require-Bundle: com.collabnet.subversion.merge
    -> Bundle-SymbolicName: com.collabnet.subversion.merge; bundle-version="4.2.0.1"; singleton:="true"
       com.collabnet.subversion.merge [1]
         Unresolved requirement: Require-Bundle: org.eclipse.jdt.core

    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:120)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:64)
    at jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:564)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
Caused by: java.lang.RuntimeException: org.osgi.framework.BundleException: Bundle bundle cannot be resolved:bundle [100]
  Unresolved requirement: Require-Bundle: com.collabnet.subversion.merge
    -> Bundle-SymbolicName: com.collabnet.subversion.merge; bundle-version="4.2.0.1"; singleton:="true"
       com.collabnet.subversion.merge [1]
         Unresolved requirement: Require-Bundle: org.eclipse.jdt.core

    at org.eclipse.tycho.core.osgitools.OsgiBundleProject.getResolverState (OsgiBundleProject.java:284)
    at org.eclipse.tycho.core.osgitools.OsgiBundleProject.resolveClassPath (OsgiBundleProject.java:177)
    at org.eclipse.tycho.core.resolver.DefaultTychoResolver.resolveProject (DefaultTychoResolver.java:142)
    at org.eclipse.tycho.core.maven.TychoMavenLifecycleParticipant.lambda$resolveProjects$0 (TychoMavenLifecycleParticipant.java:127)
    at java.util.stream.ForEachOps$ForEachOp$OfRef.accept (ForEachOps.java:183)
    at java.util.stream.WhileOps$1$1.accept (WhileOps.java:99)
    at java.util.ArrayList$ArrayListSpliterator.tryAdvance (ArrayList.java:1602)
    at java.util.stream.ReferencePipeline.forEachWithCancel (ReferencePipeline.java:127)
    at java.util.stream.AbstractPipeline.copyIntoWithCancel (AbstractPipeline.java:502)
    at java.util.stream.AbstractPipeline.copyInto (AbstractPipeline.java:488)
    at java.util.stream.AbstractPipeline.wrapAndCopyInto (AbstractPipeline.java:474)
    at java.util.stream.ForEachOps$ForEachOp.evaluateSequential (ForEachOps.java:150)
    at java.util.stream.ForEachOps$ForEachOp$OfRef.evaluateSequential (ForEachOps.java:173)
    at java.util.stream.AbstractPipeline.evaluate (AbstractPipeline.java:234)
    at java.util.stream.ReferencePipeline.forEach (ReferencePipeline.java:497)
    at org.eclipse.tycho.core.maven.TychoMavenLifecycleParticipant.resolveProjects (TychoMavenLifecycleParticipant.java:158)
    at org.eclipse.tycho.core.maven.TychoMavenLifecycleParticipant.afterProjectsRead (TychoMavenLifecycleParticipant.java:102)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:264)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:192)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:105)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:64)
    at jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:564)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
Caused by: org.osgi.framework.BundleException: Bundle bundle cannot be resolved:bundle [100]
  Unresolved requirement: Require-Bundle: com.collabnet.subversion.merge
    -> Bundle-SymbolicName: com.collabnet.subversion.merge; bundle-version="4.2.0.1"; singleton:="true"
       com.collabnet.subversion.merge [1]
         Unresolved requirement: Require-Bundle: org.eclipse.jdt.core

    at org.eclipse.tycho.core.osgitools.EquinoxResolver.assertResolved (EquinoxResolver.java:423)
    at org.eclipse.tycho.core.osgitools.EquinoxResolver.newResolvedState (EquinoxResolver.java:127)
    at org.eclipse.tycho.core.osgitools.OsgiBundleProject.getResolverState (OsgiBundleProject.java:281)
    at org.eclipse.tycho.core.osgitools.OsgiBundleProject.resolveClassPath (OsgiBundleProject.java:177)
    at org.eclipse.tycho.core.resolver.DefaultTychoResolver.resolveProject (DefaultTychoResolver.java:142)
    at java.util.stream.ForEachOps$ForEachOp$OfRef.accept (ForEachOps.java:183)
    at java.util.stream.WhileOps$1$1.accept (WhileOps.java:99)
    at java.util.ArrayList$ArrayListSpliterator.tryAdvance (ArrayList.java:1602)
    at java.util.stream.ReferencePipeline.forEachWithCancel (ReferencePipeline.java:127)
    at java.util.stream.AbstractPipeline.copyIntoWithCancel (AbstractPipeline.java:502)
    at java.util.stream.AbstractPipeline.copyInto (AbstractPipeline.java:488)
    at java.util.stream.AbstractPipeline.wrapAndCopyInto (AbstractPipeline.java:474)
    at java.util.stream.ForEachOps$ForEachOp.evaluateSequential (ForEachOps.java:150)
    at java.util.stream.ForEachOps$ForEachOp$OfRef.evaluateSequential (ForEachOps.java:173)
    at java.util.stream.AbstractPipeline.evaluate (AbstractPipeline.java:234)
    at java.util.stream.ReferencePipeline.forEach (ReferencePipeline.java:497)
    at org.eclipse.tycho.core.maven.TychoMavenLifecycleParticipant.resolveProjects (TychoMavenLifecycleParticipant.java:158)
    at org.eclipse.tycho.core.maven.TychoMavenLifecycleParticipant.afterProjectsRead (TychoMavenLifecycleParticipant.java:102)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:264)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:192)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:105)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:957)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:289)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:193)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at jdk.internal.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:64)
    at jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:564)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/InternalErrorException
```


while `mvn validate -Dtycho.version=2.2.0` works.
