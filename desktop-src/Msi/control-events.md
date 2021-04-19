---
description: ControlEvent 指定安裝程式所要採取的動作，或對話方塊中一或多個控制項的屬性變更。 如需有關事件的詳細資訊，請參閱 ControlEvent 總覽。
ms.assetid: 8768acaa-884b-428f-a14e-3f39f8ea4ad5
title: 控制 (Windows Installer) 的事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e8d9e6a8cea9a02b303040d06da346800912e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980346"
---
# <a name="control-events-windows-installer"></a>控制 (Windows Installer) 的事件

ControlEvent 指定安裝程式所要採取的動作，或對話方塊中一或多個控制項的屬性變更。 如需有關事件的詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。

下表提供有關特定事件的詳細資訊連結。



| 控制項事件                                                       | ControlEvent 的簡短描述                                                                                                                                                                             |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ActionData](actiondata-controlevent.md)                           | 將資料發佈至最新的動作。                                                                                                                                                                          |
| [ActionText](actiontext-controlevent.md)                           | 發佈目前動作的名稱。                                                                                                                                                                     |
| [AddLocal](addlocal-controlevent.md)                               | 通知安裝程式在本機執行功能。                                                                                                                                                               |
| [AddSource](addsource-controlevent.md)                             | 通知安裝程式從其來源執行功能。                                                                                                                                                     |
| [CheckExistingTargetPath](checkexistingtargetpath-controlevent.md) | 通知安裝程式確認可以撰寫路徑。                                                                                                                                                |
| [CheckTargetPath](checktargetpath-controlevent.md)                 | 通知安裝程式確認路徑有效。                                                                                                                                                      |
| [DirectoryListNew](directorylistnew-controlevent.md)               | 通知 DirectoryList 控制項建立新資料夾。                                                                                                                                                    |
| [DirectoryListOpen](directorylistopen-controlevent.md)             | 選取 DirectoryList 控制項中的目錄。                                                                                                                                                           |
| [DirectoryListUp](directorylistup-controlevent.md)                 | 通知 DirectoryList 控制項選取目前目錄的父系。                                                                                                                             |
| [Dataadapter.doaction](doaction-controlevent.md)                               | 對話方塊會通知安裝程式執行自訂動作。                                                                                                                                                 |
| [EnableRollback](enablerollback-controlevent.md)                   | 用來關閉和開啟復原功能。                                                                                                                                                                |
| [EndDialog](enddialog-controlevent.md)                             | 通知安裝程式移除強制回應對話方塊。                                                                                                                                                          |
| [IgnoreChange](ignorechange-controlevent.md)                       | 當資料夾已反白顯示但未開啟時，由 DirectoryList 控制項發佈。                                                                                                                           |
| [MsiLaunchApp](msilaunchapp-controlevent.md)                       | 此控制項事件會執行指定的檔案。**[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/>                                                       |
| [MsiPrint](msiprint-controlevent.md)                               | 讓使用者可以列印 [ScrollableText 控制項](scrollabletext-control.md)的內容。**[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。<br/> |
| [NewDialog](newdialog-controlevent.md)                             | 通知安裝程式將強制回應對話方塊變更為另一個對話方塊。                                                                                                                                  |
| [安裝](reinstall-controlevent.md)                             | 起始功能的重新安裝。                                                                                                                                                                       |
| [ReinstallMode](reinstallmode-controlevent.md)                     | 指定重新安裝期間的驗證模式。                                                                                                                                                        |
| [移除](remove-controlevent.md)                                   | 選取要移除的功能時，通知安裝程式。                                                                                                                                                |
| [重設](reset-controlevent.md)                                     | 將所有屬性值重設為建立對話方塊時所使用的預設值。                                                                                                                    |
| [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)       | 您可以使用 [重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal) 來關閉所有具有檔案使用中的應用程式，並在安裝結束時重新開機它們。                                                              |
| [ScriptInProgress](scriptinprogress-controlevent.md)               | 在編譯執行腳本時顯示字串。                                                                                                                                                     |
| [SelectionAction](selectionaction-controlevent.md)                 | 由 SelectionTree 發佈以描述專案。                                                                                                                                                               |
| [SelectionBrowse](selectionbrowse-controlevent.md)                 | 由 SelectionTree 發佈以產生對話方塊。                                                                                                                                                             |
| [SelectionDescription](selectiondescription-controlevent.md)       | 由 SelectionTree 發佈，以在功能資料表的 [描述] 欄位中提供字串。                                                                                                                 |
| [SelectionNoItems](selectionnoitems-controlevent.md)               | 供 SelectionTree 用來刪除文字或停用按鈕。                                                                                                                                                      |
| [SelectionPath](selectionpath-controlevent.md)                     | 由 SelectionTree 發行以提供專案的路徑。                                                                                                                                                    |
| [SelectionPathOn](selectionpathon-controlevent.md)                 | 由 SelectionTree 發佈，指出是否有與功能相關聯的路徑。                                                                                                                     |
| [SelectionSize](selectionsize-controlevent.md)                     | 由 SelectionTree 控制項發行以提供專案的大小。                                                                                                                                            |
| [SetInstallLevel](setinstalllevel-controlevent.md)                 | 安裝程式會將安裝層級變更為指定的值。                                                                                                                                                |
| [SetProgress](setprogress-controlevent.md)                         | 由安裝程式發行以提供安裝進度。                                                                                                                                                  |
| [SetProperty](setproperty-controlevent.md)                         | 設定指定的屬性。                                                                                                                                                                                    |
| [SetTargetPath](settargetpath-controlevent.md)                     | 通知安裝程式檢查並設定路徑。                                                                                                                                                               |
| [SpawnDialog](spawndialog-controlevent.md)                         | 通知安裝程式建立強制回應對話方塊的子系。                                                                                                                                                      |
| [SpawnWaitDialog](spawnwaitdialog-controlevent.md)                 | 觸發指定的對話方塊。                                                                                                                                                                              |
| [TimeRemaining](timeremaining-controlevent.md)                     | 由安裝程式發佈，以提供進度順序中剩餘的時間。                                                                                                                            |
| [ValidateProductID](validateproductid-controlevent.md)             | 將 ProductID 設定為完整的產品識別碼。                                                                                                                                                                        |



 

 

