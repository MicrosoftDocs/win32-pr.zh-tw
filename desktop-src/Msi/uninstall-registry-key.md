---
description: Windows Installer 屬性的清單，提供以 Uninstall 登錄機碼撰寫的值。
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows卸載登錄機碼的安裝程式屬性
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810317"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows卸載登錄機碼的安裝程式屬性

下列安裝程式屬性會提供在登錄機碼下寫入的值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **卸載**

這些值會儲存在應用程式的產品代碼 GUID 所識別的子機碼中。



| 值               | Windows安裝程式屬性                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName**](productname.md) 屬性                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | 衍生自 [**ProductVersion**](productversion.md) 屬性                                                                                                                                                                                                                                                                                                       |
| Publisher           | [**製造商**](manufacturer.md) 屬性                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | 衍生自 [**ProductVersion**](productversion.md) 屬性                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | 衍生自 [**ProductVersion**](productversion.md) 屬性                                                                                                                                                                                                                                                                                                       |
| 版本             | 衍生自 [**ProductVersion**](productversion.md) 屬性                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**ARPHELPLINK**](arphelplink.md) 屬性                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | [**ARPHELPTELEPHONE**](arphelptelephone.md) 屬性                                                                                                                                                                                                                                                                                                                |
| InstallDate         | 此產品上次收到服務的時間。 每次在產品中套用或移除修補程式，或使用/v [命令列選項](command-line-options.md) 來修復產品時，就會取代這個屬性的值。 如果產品未收到維修或修補程式，此內容會包含此產品在這部電腦上的安裝時間。 |
| InstallLocation     | [**ARPINSTALLLOCATION**](arpinstalllocation.md) 屬性                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir**](sourcedir.md) 屬性                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | [**ARPURLINFOABOUT**](arpurlinfoabout.md) 屬性                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) 屬性                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md) 屬性                                                                                                                                                                                                                                                                                                    |
| 註解            | [**ARPCOMMENTS**](arpcomments.md) 屬性 <br/> 提供給 [ **新增或移除程式** ] 控制台的批註。<br/>                                                                                                                                                                                                                                |
| Contact             | [**ARPCONTACT**](arpcontact.md) 屬性 <br/> 提供給 [ **新增或移除程式** ] 控制台的連絡人。<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | 由 Windows Installer 決定和設定。                                                                                                                                                                                                                                                                                                                         |
| 語言            | [**ProductLanguage**](productlanguage.md) 屬性                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | 由 Windows Installer 決定和設定。                                                                                                                                                                                                                                                                                                                         |
| 讀我檔案              | [**ARPREADME**](arpreadme.md) 屬性 <br/> 提供給 [ **新增或移除程式** ] 控制台的讀我檔案。<br/>                                                                                                                                                                                                                                      |
| UninstallString     | 由 Windows Installer 決定和設定。                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md) 屬性                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[使用 Windows Installer 設定新增/移除程式](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[屬性參考](property-reference.md)
</dt> <dt>

[使用屬性](using-properties.md)
</dt> </dl>

 

 




