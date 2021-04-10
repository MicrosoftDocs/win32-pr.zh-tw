---
description: InstallValidate 動作會確認成本已屬性化的所有磁片區都有足夠的空間可進行安裝。 如果有任何磁片區是磁碟空間不足的情況，InstallValidate 動作就會結束安裝，併發生嚴重錯誤。
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: InstallValidate 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194546"
---
# <a name="installvalidate-action"></a>InstallValidate 動作

InstallValidate 動作會確認 [*成本*](c-gly.md)已屬性化的所有 [*磁片*](v-gly.md)區都有足夠的空間可進行安裝。 如果有任何磁片區是磁碟空間不足的情況，InstallValidate 動作就會結束安裝，併發生嚴重錯誤。

InstallValidate 動作也會在使用中進程目前正在使用一或多個要覆寫或移除的檔案時，通知使用者。 如需詳細資訊，請參閱 [系統重新開機](system-reboots.md)。

## <a name="sequence-restrictions"></a>順序限制

[CostFinalize](costfinalize-action.md)動作和任何 UI 對話方塊序列，可讓使用者修改選取狀態和（或）目錄，應該在 InstallValidate 動作之前排序。

變更功能或元件安裝狀態的[自訂動作](custom-actions.md)必須在 InstallValidate 動作之前排序。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

一般來說，當使用者嘗試起始檔案的複製時，較早的 UI 對話方塊順序應該與 InstallValidate 動作執行相同的驗證。 如果選取的磁片區沒有足夠的空間可進行安裝，此 UI 對話方塊順序應該會顯示 [ **磁碟空間不足** ] 對話方塊。 如果磁碟空間不足，則應該以防止使用者繼續安裝的方式來撰寫 UI 對話方塊。 在無訊息安裝的情況下，沒有任何使用者介面，且如果磁碟空間不足，InstallValidate 動作就會終止安裝。 如果啟用記錄功能，則會在記錄檔中記錄提前終止的原因。

如果在檔案的任何程式中開啟檔案以供執行或修改，則會將專案加入至內部 FilesInUse [*資料表。*](c-gly.md) FilesInUse 資料表包含檔案的名稱和完整路徑的資料行。 當 InstallValidate 動作執行時，安裝程式會查詢 FilesInUse 資料表中的專案，並使用該檔案來決定進程的名稱。 InstallValidate 動作會針對此查詢所識別的每個唯一程式，將一筆記錄加入 [ListBox](listbox-table.md) 使用者介面資料表中。 記錄包含每個資料行中的下列值：

**屬性**： FileInUseProcess

 

**值**： *進程的名稱*

 

**Text**： *流程主視窗標題中包含的文字*

InstallValidate 動作接著會顯示 [ **使用中** 的檔案] 對話方塊。 此對話方塊會顯示必須關閉的處理常式，以避免重新開機系統以取代使用中檔案的需求。

InstallValidate 動作會使用 [保留名稱[FilesInUse](filesinuse-dialog.md) ] 對話方塊來查詢已撰寫之對話方塊的[對話方塊](dialog-table.md)資料表，並加以顯示。 此對話方塊必須包含與名為 FileInUseProcess 的屬性系結的 [ListBox](listbox-control.md) 控制項。 依照慣例，這個對話方塊會有 [結束 **]、[****重試**] 或 [**略** 過] 按鈕，但這是由 UI 作者所撰寫。 每個按鈕都應系結至[ControlEvent](controlevent-table.md)資料表中的[EndDialog](enddialog-controlevent.md) ControlEvent。 InstallValidate 動作會依照下列其中一個[EndDialog](enddialog-controlevent.md)引數（與使用者推送的按鈕相關聯）的指示，以下列方式回應[dataadapter.doaction](doaction-controlevent.md) ControlEvent 所傳回的值：

**重試**：已清除新增至 [ListBox](listbox-table.md) 資料表的所有值，並重複整個檔案 [*成本*](c-gly.md) 程式，重新檢查仍在使用中的檔案。 如果有一或多個進程仍識別為使用要覆寫或刪除的檔案，則會重複此程式;否則，InstallValidate 會將控制權傳回給安裝程式，其狀態為 msiDoActionStatusSuccess。

**Exit**： InstallValidate 動作會立即將控制權傳回給安裝程式，其狀態為 msiDoActionStatusUserExit。 這會結束安裝。

**任何其他傳回值**： InstallValidate 動作會立即將控制權傳回給安裝程式，其狀態為 msiDoActionStatusSuccess。 在此情況下，因為有一或多個檔案仍在使用中，所以後續的 [InstallFiles](installfiles-action.md) 和/或 [InstallAdminPackage](installadminpackage-action.md) 動作必須排程在系統重新開機時，要取代或刪除) 的 (使用中檔案。

如果資料庫中沒有 [ListBox](listbox-table.md) 資料表，InstallValidate 會以無訊息方式結束，而不會發生錯誤。

分號是轉換、來源和修補程式的清單分隔符號，不應該用在這些檔案名或路徑中。

在唯讀位置中標示為唯讀的檔案永遠不會被安裝程式使用。

如果使用者介面層級為「基本」，則會向使用者顯示包含「**中止**」和「**重試**」按鈕的預設 [**磁碟空間不足**] 對話方塊。

 

 



