# Double Agent Project Abstract

## Introduction

[Double Agent](https://sourceforge.net/projects/doubleagent) is an Open Source 
alternative to Microsoft™ Agent that allows Agent applications to work on Windows 7.

- It emulates the Microsoft™ Agent server and the Microsoft™ Agent
  ActiveX control.
- It supports existing Microsoft™ Agent version 2.0 characters,
  including Microsoft™ Office Assistant characters.
- It implements the Agent Server and Agent ActiveX Control programming
  interfaces, so it can be used with no changes to existing
  applications.
- For development and testing purposes, it also runs on Windows® XP and
  Windows® Vista.
- It's available in both 32–bit and 64–bit versions.

## Components

Double Agent currently includes the following:

| Feature | Description | File(s) |
| ------- | ----------- | ------- |
| Core Components | Implements the all of the basic functionality for the character, balloon, property pages, etc. | dacore.dll |
| Server | Implements the Agent Server interfaces.<br />This includes loading and unloading characters, tracking characters, requests, and clients, showing property sheets, etc. | `daserver.exe` |
| ActiveX Control | Implements the Agent ActiveX Control.<br />The control conforms to Microsoft's ActiveX standard and is compatible with any programming language that can use ActiveX controls.  This includes C++, C#, Visual Basic (Version 6 and .NET), HTML, and various scripting languages. | `dacontrol.dll` |
| Explorer Extensions | Provides the character file (`.ACS` and `.ACG`) property page for Windows Explorer.<br /> Also provides a Control Panel extension for managing Double Agent. | `dashell.dll` |
| International | The Microsoft™ Agent international components consist of a resource module (<code>agt<em>xxxx</em>.dll</code>) and a help file (<code>agt<em>xxxx</em>.hlp</code>), where *xxxx* is a hexadecimal language code.<br />Double Agent uses these resource modules to support languages other than English.  However, the help files are unusable since the `.HLP` help format is no longer supported. | `agtxxxx.dll` |
| Interop Assemblies | The Double Agent package includes **Interop Assemblies** that allow the Agent Server and Agent ActiveX Control to *interoperate* with Windows .NET.  There is a set of interop assemblies for Double Agent, and another set for Microsoft™ Agent.<br />These assemblies are provided for convenience only.  Programmers can use them or create their own interop assemblies. | `DoubleAgentCtl.dll`<br />`AxDoubleAgentCtl.dll`<br />`DoubleAgentSvr.dll`<br />`AgentObjects.dll`<br />`AxAgentObjects.dll`<br />`AgentServerObjects.dll` |

## Licensing

Double Agent is licensed under the **GNU Public License** as follows:

- The Server and ActiveX Control components are covered by the **GNU
  Lesser General Public License**.  This means that proprietary
  applications may use and distribute the Server and ActiveX Control
  components.
- All other components are covered by the **GNU General Public
  License**.  This means that any application that binds directly (using
  static link, dynamic link, COM, or any other mechanizm) to any other
  component **must** be an open source application.  Specifically, no
  proprietary application may directly call any function in the *Core
  Components*.
- Each source file is marked to indicate which licence it uses.  No
  source code covered by the **GNU General Public License** may be used
  in any form (modified or unmodified) in any proprietary application.

For more information, please refer to the GNU license documents
accompanying this software, or visit  <http://www.gnu.org>.
