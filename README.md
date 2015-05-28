Ext_RestFrames
=================

Package is a wrapper class to get the RestFrames package compiled in a RootCore environment. 

## Issues

If you see an issue like

```
compiling Ext_RestFrames
WARNING: package Ext_RestFrames doesn't request pedantic compilation
WARNING: fix this by setting 'PACKAGE_PEDANTIC = 1' in Makefile.RootCore
configuring Ext_RestFrames
  testing location: %%%LOCAL%%%
trying manual install
/share/home/kratsg/RestFramesAnalysis/RootCoreBin/download/Ext_RestFrames/tarball
/cvmfs/atlas.cern.ch/repo/sw/ASG/AnalysisBase/2.3.12/RootCore/scripts/external_download.sh: line 3: cd: crogan-RestFrames-cf9e419: No such file or directory
    failed: installation of Ext_RestFrames failed
RootCore: Error failed to find valid Ext_RestFrames installation in %%%LOCAL%%%
RootCore: Error failed to execute /share/home/kratsg/RestFramesAnalysis/Ext_RestFrames/cmt/precompile.RootCore
```

The way to fix this is to clean out your `download` folder inside `$ROOTCOREBIN` by something like

```
rm -rf RootCoreBin/download/Ext_RestFrames/*
```
