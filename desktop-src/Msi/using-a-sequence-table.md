---
description: 撰寫順序資料表是開發安裝程式封裝不可或缺的一部分，因為這些資料表會指定控制安裝程式和顯示使用者介面對話方塊之標準動作的執行順序。
ms.assetid: db9a9cae-2a66-4e0d-a981-8de66d7c2a13
title: 使用順序資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16adf47a554bf70298b0efc893847f84eafd6e97313b09ba9ea3182398cdd97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809008"
---
# <a name="using-a-sequence-table"></a>使用順序資料表

撰寫順序資料表是開發安裝程式封裝不可或缺的一部分，因為這些資料表會指定控制安裝程式和顯示使用者介面對話方塊之 [標準動作](standard-actions.md) 的執行順序。

有三種模式的安裝模式，以及每個模式的順序資料表有兩種類型。

安裝程式目前支援的三種不同安裝模式如下：

-   簡單安裝
-   系統管理安裝
-   公告安裝

順序資料表各有三個欄位： Action、Condition 和 Sequence。 [動作] 欄位的名稱是標準或自訂動作，或是使用者定義的對話方塊或安裝程式執行的順序。 [條件] 欄位可讓作者指定邏輯運算式，以控制是否執行或顯示動作或使用者定義的對話方塊。 如果條件欄位為空白或包含評估結果為 True 的運算式，則會執行或顯示動作或對話方塊。 如果運算式評估為 False，則會略過動作或對話方塊。 [順序] 欄位指定在資料表中執行每個動作或使用者定義之對話方塊的順序。

上述每一種安裝模式都會處理使用者介面順序資料表和執行順序資料表。 只有當安裝程式是以設定為 [縮小] 或 [完整] 的使用者介面顯示層級進行初始化時，才會處理使用者介面順序資料表。 如需使用者介面顯示層級的詳細資訊，請參閱 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 參考。

使用者介面順序資料表通常包含與收集系統資訊（透過使用者介面顯示給使用者的系統資訊）相關的標準動作。 將外鍵記錄到使用者介面順序資料表之 [動作] 欄位中 [對話方塊資料表](dialog-table.md) 的對話方塊名稱，即可顯示使用者介面。 然後，使用者有機會修改或接受系統資訊，然後開始安裝，這會在執行順序表處理時發生。

在簡單的安裝過程中，會執行 [安裝](install-action.md) 最上層動作，進而處理 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。

系統管理員通常會透過網路系統管理員起始系統管理安裝，為個別使用者和使用者群組指派及安裝應用程式。 在這種安裝類型期間，系統會執行系統 [管理員](admin-action.md) 的最上層動作來處理 [AdminUISequence 資料表](adminuisequence-table.md) 和 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。

若要 [通告](advertisement.md) 應用程式或功能，必須使用 [通告](advertise-action.md) 動作起始安裝程式。 在這種類型的安裝過程中，會處理 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md) 。

撰寫任何順序資料表時，最好的作法是使用下列主題中建議序列的標準動作序號。 對於順序資料表（例如 [ForceReboot](forcereboot-action.md)、 [ValidateProductID](validateproductid-action.md)和 [InstallExecute](installexecute-action.md)）中沒有標準位置的標準動作，請使用為十的倍數的序號，將動作識別為標準動作。 若為自訂動作，請使用不是10倍數的序號，以區別順序資料表中的標準動作。

如需每個順序資料表的建議動作順序，請參閱下列主題：

-   [建議的 InstallUISequence](suggested-installuisequence.md)
-   [建議的 InstallExecuteSequence](suggested-installexecutesequence.md)
-   [建議的 AdminUISequence](suggested-adminuisequence.md)
-   [建議的 AdminExecuteSequence](suggested-adminexecutesequence.md)
-   [建議的 AdvtUISequence](suggested-advtuisequence.md)
-   [建議的 AdvtExecuteSequence](suggested-advtexecutesequence.md)

如需順序資料表以及標準動作執行方式的詳細描述，請參閱 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

* * Windows Installer 3.0 和更新版本： * *

從 Windows Installer 3.0 開始，修補封裝可以包含[MsiPatchSequence 資料表](msipatchsequence-table.md)。 此表格包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的小型更新修補程式順序。 如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。

> [!Note]
>
> [合併模組](merge-modules.md) 可能包含 [合併模組資料庫資料表](merge-module-database-tables.md) ，這些資料表會修改目標 .msi 檔的動作順序資料表。 將模組合併到資料庫中可以修改 sequence 資料表中的資訊，但不會將這些資料表加入 .msi 檔案中。 如需詳細資訊，請參閱 [撰寫合併模組順序資料表](authoring-merge-module-sequence-tables.md)。

 

 

 



