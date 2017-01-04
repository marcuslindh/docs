---
title: Prerequisites for .NET Core on Windows | Microsoft Docs
description: Learn what dependencies you need on your Windows machine to develop and run .NET Core applications.
keywords: .NET Core, Windows, prerequisites, dependencies, Visual Studio
author: billwagner
ms.author: wiwagn
ms.date: 01/04/2017
ms.topic: article
ms.prod: .net-core
ms.devlang: dotnet
ms.assetid: c33b1241-ab66-4583-9eba-52cf51146f5a
---

# Prerequisites for .NET Core on Windows

This articles shows you what dependencies you need to deploy and run .NET Core applications on Windows machines and develop using Visual Studio.

## Supported Windows versions

.NET Core is supported on the following versions of Windows:

* Windows 7 SP1
* Windows 8.1
* Windows 10
* Windows Server 2008 R2 SP1 (Full Server or Server Core)
* Windows Server 2012 SP1 (Full Server or Server Core)
* Windows Server 2012 R2 SP1 (Full Server or Server Core)
* Windows Server 2016 (Full Server, Server Core or Nano Server)

You can see the full set of [supported operating systems](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.0.md#rtm-platform-support) in the [.NET Core 1.0.0 Release Notes](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.0.md).

## .NET Core dependencies

.NET Core requires the Visual C++ Redistributable when running on Windows. It is automatically installed for you by the .NET Core installer. However, you need to manually install the Visual C++ redistributable if you are installing .NET Core via the [installer script](https://docs.microsoft.com/en-us/dotnet/articles/core/tools/dotnet-install-script) or deploying a self-contained .NET Core application.

[Visual C++ Redistributable for Visual Studio 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48145)

* Windows 7 and Windows 2008 only
    * Make sure that your Windows installation is up-to-date and includes hotfix [KB2533623](https://support.microsoft.com/en-us/kb/2533623) installed through Windows Update.

## Visual Studio

If you want to develop .NET Core applications on Windows using Visual Studio, you'll need:

* [Visual Studio 2015 Update 3.3 or later](#visual-studio-2015).
* [NuGet Manager extension for Visual Studio](#nuget-manager-extension-for-visual-studio).
* [.NET Core Tooling Preview 2](#net-core-tools-for-visual-studio-2015).

### Visual Studio 2015

You need Visual Studio 2015 to develop .NET Core apps. You can download [Visual Studio Community 2015](https://www.visualstudio.com/downloads/) for free. 

Verify that you're running [Visual Studio 2015 Update 3.3](https://msdn.microsoft.com/library/mt752379.aspx):

* On the **Help** menu, choose **About Microsoft Visual Studio**.
* In the **About Microsoft Visual Studio** dialog, the version number should be 14.0.25424.00 or higher, and include "Update 3".
* If you don't have Update 3, you first need to download and install [Visual Studio 2015 Update 3](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs).
* If you have Update 3 but the version number is smaller than 14.0.25424.00, you need to download and install [Visual Studio 2015 Update 3.3](https://msdn.microsoft.com/library/mt752379.aspx).

You can read more about the changes in Update 3 in the [release notes](https://www.visualstudio.com/news/releasenotes/vs2015-update3-vs).

### NuGet Manager extension for Visual Studio

NuGet is the package manager for the Microsoft development platform including .NET Core. You need [NuGet 3.5.0](https://dist.nuget.org/visualstudio-2015-vsix/v3.5.0-beta/NuGet.Tools.vsix) or higher to build .NET Core apps.

### .NET Core tools for Visual Studio 2015

Download and install the [.NET Core 1.0.1 - VS 2015 Tooling Preview 2][sdk]. 

The .NET Core Tooling package installs .NET Core, project templates and other tools for Visual Studio 2015.

> [!NOTE]
Currently, you cannot download an offline installer for [.NET Core 1.0.1 - VS 2015 Tooling Preview 2][sdk]. Instead, you have to download the [regular bootstrapper][sdk] and run it with a command-line option (such as, `/layout c:\path`) to get an offline layout. After that, it can be used as an offline installer: just run the executable from the local path. Notice that because it's a full layout, this procedure downloads all the packages for all supported languages, which is around 1 GB in size.

[sdk]: https://go.microsoft.com/fwlink/?LinkID=827546
