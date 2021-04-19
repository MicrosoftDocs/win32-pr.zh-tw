---
description: 如果在執行安裝之後，您必須確認已安裝特定功能、元件或檔案，請在安裝期間開啟詳細資訊記錄選項。 請參閱 Windows Installer 記錄和命令列選項。
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: 檢查功能、元件、檔案的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979769"
---
# <a name="checking-the-installation-of-features-components-files"></a>檢查功能、元件、檔案的安裝

如果在執行安裝之後，您必須確認已安裝特定功能、元件或檔案，請在安裝期間開啟詳細資訊記錄選項。 請參閱 [Windows Installer 記錄](windows-installer-logging.md) 和 [命令列選項](command-line-options.md)。

詳細資訊記錄檔包含安裝套件可能安裝的每個功能和元件的專案。 記錄檔會指出該功能或元件在安裝之前的狀態、安裝所要求的狀態，以及安裝程式離開功能或元件的狀態。 記錄檔中的功能和元件專案會顯示為下列範例。

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

此詳細資訊記錄檔指出：

-   執行封裝之前，QuickTest 功能和元件的安裝狀態不存在
-   套件要求本機安裝這些
-   在執行封裝之後，功能和元件都會保持在本機安裝的狀態。

記錄檔中的「已安裝」標籤是指功能或元件目前的安裝狀態，「要求」指的是功能或元件的要求安裝狀態。 「動作」是指功能或元件的實際動作狀態。

下表列出可能出現在記錄檔中的元件或功能狀態。



| 記錄項目              | Description                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| 要求： Null          | 沒有要求。                                                                                                     |
| Action： Null           | 未採取任何動作。                                                                                                |
| 已安裝：不存在      | 目前未安裝元件或功能。                                                                |
| 要求：不存在        | 安裝要求元件或功能已卸載。                                                      |
| 動作：不存在         | 安裝程式會實際卸載元件或功能。                                                             |
| 已安裝：本機       | 目前已安裝元件或功能以執行本機。                                                       |
| 要求：本機         | 安裝要求元件或功能可在本機執行。                                           |
| 動作：本機          | 安裝程式會實際安裝元件或功能以執行本機。                                                  |
| 已安裝：來源      | 元件或功能目前已安裝成從來源執行。                                                 |
| 要求：來源      | 安裝會要求安裝元件或功能以從來源執行。                                |
| 動作：來源         | 安裝程式實際上會安裝從來源執行的元件或功能。                                        |
| 已安裝：公告   | 功能目前已公告。 元件永遠不會公佈。                                               |
| 要求：公告     | 安裝要求功能是以公告功能的形式安裝。                                            |
| 動作：公告      | 安裝程式會實際將此功能安裝為已公告的功能。                                               |
| 要求：重新安裝     | 安裝要求功能已重新安裝。 元件不會使用重新安裝狀態。                            |
| 動作：重新安裝      | 安裝程式會實際重新安裝功能。                                                                          |
| 已安裝：目前     | 功能目前是以預設撰寫的安裝狀態安裝。                                           |
| 要求：目前       | 安裝要求功能是以預設撰寫的安裝狀態安裝。                               |
| 動作：目前        | 安裝程式會實際以預設撰寫的安裝狀態安裝該功能。                                  |
| Action： FileAbsent     | 安裝程式會實際卸載元件的檔案，並保留已安裝元件的所有其他資源。      |
| Action： HKCRAbsent     | 安裝程式會實際移除元件的 HKCR 資訊。 檔案和非 HKCR 資訊仍然存在。                  |
| Action： HKCRFileAbsent | 安裝程式會實際移除元件的 HKCR 資訊和檔案。 元件的其他所有資源都會保留下來。 |



 

詳細資訊記錄檔中有套件可能安裝的每個檔案的專案。 記錄檔會告知檔案已完成的作業，並提供一些說明。 記錄檔中的檔案專案會如下列範例所示。

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

此記錄檔表示安裝程式不會覆寫現有的 Testdb.exe 檔案，因為現有的檔案與所安裝的版本相同。

> [!Note]  
> 如果您需要撰寫安裝套件，以在安裝期間在使用者電腦上搜尋現有的檔案或目錄，請使用 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)中所述的方法。

 

 

 



