---
description: 事件事件與 Win32 架構應用程式中的 Microsoft Windows 訊息類似。
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: ControlEvent 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852348"
---
# <a name="controlevent-overview"></a>ControlEvent 總覽

事件事件與 Win32 架構應用程式中的 Microsoft Windows 訊息類似。 但是，不是使用 [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式來建立回呼函式，而是使用函式來接收 windows 訊息和傳送 windows 訊息，而是使用使用者介面 (UI) 安裝程式和 [控制項發行控制項](control-events.md)。 您可以指定其他控制項和安裝程式來訂閱特定的控制項，然後變更訂閱控制項的屬性。 若要將工作控制項新增至對話方塊，UI 的作者會指定在 [ControlEvent 資料表](controlevent-table.md) 中進行事件的發行，並訂閱控制項以在 [EventMapping 資料表](eventmapping-table.md)中進行事件處理。

安裝程式會將下列事件發行至 [EventMapping 資料表](eventmapping-table.md)中所列的訂閱控制項。 [ProgressBar 控制項](progressbar-control.md)或[佈告欄控制項](billboard-control.md)通常會訂閱 SetProgress，其餘部分則由[文字控制項](text-control.md)訂閱。

[ActionData ControlEvent](actiondata-controlevent.md)

[ActionText ControlEvent](actiontext-controlevent.md)

[SetProgress ControlEvent](setprogress-controlevent.md)

[TimeRemaining ControlEvent](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)

當專案選取範圍移至 [SelectionTree 控制項](selectiontree-control.md) 或 [DirectoryList 控制項](directorylist-control.md)時，控制項就會發佈下列事件。 訂閱控制項必須位於相同的對話方塊上，並且列在 EventMapping 資料表中。

[IgnoreChange ControlEvent](ignorechange-controlevent.md)

[SelectionDescription ControlEvent](selectiondescription-controlevent.md)

[SelectionSize ControlEvent](selectionsize-controlevent.md)

[SelectionPath ControlEvent](selectionpath-controlevent.md)

[SelectionAction ControlEvent](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)

您可以藉由在對話方塊中與 [按鈕控制項](pushbutton-control.md) 或 [核取方塊控制項](checkbox-control.md) 互動，以使用者的意願來發行下列事件。 Checkbox 控制項只能發行 AddLocal、AddSource、Remove、Dataadapter.doaction 和 SetProperty 事件。 有了 Windows Server 2003 和更新版本隨附的 Windows Installer 版本， [SelectionTree 控制項](selectiontree-control.md) 可以發佈 Dataadapter.doaction、ControlEvent 和 SetProperty 事件。 UI 的作者應該會列出 [ControlEvent 資料表](controlevent-table.md)中的 ControlEvent。 安裝程式的 UI 處理常式是這些事件的訂閱者。

[AddLocal ControlEvent](addlocal-controlevent.md)

[AddSource ControlEvent](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent](checktargetpath-controlevent.md)

[Dataadapter.doaction ControlEvent](doaction-controlevent.md)

[EnableRollback ControlEvent](enablerollback-controlevent.md)

[EndDialog ControlEvent](enddialog-controlevent.md)

[NewDialog ControlEvent](newdialog-controlevent.md)

[重新安裝 ControlEvent](reinstall-controlevent.md)

[ReinstallMode ControlEvent](reinstallmode-controlevent.md)

[移除 ControlEvent](remove-controlevent.md)

[重設 ControlEvent](reset-controlevent.md)

[SetInstallLevel ControlEvent](setinstalllevel-controlevent.md)

[SetProperty ControlEvent](setproperty-controlevent.md)

[SetTargetPath ControlEvent](settargetpath-controlevent.md)

[SpawnDialog ControlEvent](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent](validateproductid-controlevent.md)

[按鈕控制項](pushbutton-control.md)可以將下列事件發行至位於相同對話方塊中的訂閱[SelectionTree 控制項](selectiontree-control.md)或[DirectoryList 控制項](directorylist-control.md)。 [按鈕] 控制項應列在 ControlEvent 資料表中，而且訂閱控制項應列在 [EventMapping] 資料表中。

[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent](directorylistopen-controlevent.md)

控制事件通常需要在 [*完整的 ui*](f-gly.md) 層級上執行 ui。 大部分的事件處理都不會使用 [*精簡的 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md) ，因為這些層級只會顯示非強制回應對話方塊。 ActionText、AddSource、SetProgress、TimeRemaining 和 ScriptInProgress 事件都是例外狀況，並可在精簡或基本的 UI 中運作。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

您可以從[按鈕控制項](pushbutton-control.md)或[核取方塊控制項](checkbox-control.md)發佈 ControlEvent，以執行[自訂動作](custom-actions.md)。 將記錄加入至 [ControlEvent 資料表](controlevent-table.md) ，其中包含對話方塊的名稱和發行 ControlEvent 的控制項。 此控制項應發佈 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) ，通知安裝程式執行自訂動作。 在 Windows XP 或舊版系統上，您無法從 [SelectionTree 控制項](selectiontree-control.md)發佈 ControlEvent 來執行自訂動作。

如需有關特定事件的詳細資訊，請參閱[消費者介面參考](user-interface-reference.md)中的標準[事件](control-events.md)清單。

 

 
