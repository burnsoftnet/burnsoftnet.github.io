[<--Home](README.md)
# Programmatically set program to 'run as administrator'

You need to compile your application with a manifest to do this.

First, create a manifest file (basically "MyApplication.exe.manifest") and put this in it:

`‌<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity version="1.0.0.0" processorArchitecture="X86" name="My Application" type="win32"/>
  <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
      <requestedPrivileges>
        <requestedExecutionLevel level="requireAdministrator"/>
      </requestedPrivileges>
    </security>
  </trustInfo>
</assembly>`

Then add this to your project's post-build event:

`‌"$(DevEnvDir)..\..\SDK\v2.0\bin\mt.exe" -manifest "$(ProjectDir)$(TargetName).exe.manifest" –outputresource:"$(TargetDir)$(TargetFileName)";#1`

As long as the manifest is included in your project, this should work with little to no adjustments.

You do not need to have the file copy on build, just store it with the rest of the project and when the application is complied it will include the manifest file.

Gathered from: Kasracer (KrisSiegel.com) URL Source: http://www.vbforums.com/showthread.php?t=510403