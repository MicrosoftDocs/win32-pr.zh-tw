---
description: 自訂動作會以與標準動作相同的方式，在順序資料表中排程。
ms.assetid: 1aea75b1-a498-405e-9208-91672455496b
title: 排序自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d86449b67809f782560e35d32b1b1e42434153ced776a27fd479a7b80a25a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039968"
---
# <a name="sequencing-custom-actions"></a>排序自訂動作

自訂動作會以與標準動作相同的方式，在順序資料表中排程。

**若要排程順序資料表中的自訂動作**

1.  在 [[順序](sequence-table-detailed-example.md)] 資料表的 [動作] 資料行中，輸入自訂動作名稱 (，這是[CustomAction](customaction-table.md)) 資料表的主要索引鍵。
2.  將自訂動作的順序，輸入至 [ [順序](sequence-table-detailed-example.md) ] 資料表的 [順序] 資料行中，相對於資料表中的其他動作。 如需順序資料表的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。
3.  若要有條件地略過該動作，請在 [ [順序](sequence-table-detailed-example.md) ] 資料表的 [條件] 資料行中輸入條件運算式。 如果運算式評估為 FALSE，則安裝程式會略過這個動作。

就像標準動作一樣，只有在內部使用者介面設定為完整層級時，才會執行 [InstallUISequence](installuisequence-table.md) 或 [AdminUISequence](adminuisequence-table.md) 中排程的自訂動作。 UI 層級是使用 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) 函數來設定。

排程在 [InstallExecuteSequence](installexecutesequence-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)或 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表中的標準和自訂動作不會進行系統變更。 相反地，安裝程式會將腳本中的執行記錄排入佇列中，以便在安裝服務期間進行後續的執行。 如果沒有安裝服務，則在這些資料表中排程的動作會在與 UI 順序相同的內容中執行。

如果安裝程式伺服器未註冊，則會在用戶端上執行自訂動作。 如果伺服器已註冊且使用完整的 UI 模式，則會在伺服器端執行自訂動作。

如果使用完整的 UI 與伺服器，則在 [InstallValidate](installvalidate-action.md) 動作之前的初始動作會在用戶端上執行，以允許完全互動。 然後執行會切換至伺服器，以重複這些動作並執行腳本執行動作。 之後會傳回用戶端的最後一個動作。

請注意，如果產品是藉由將其最上層功能設定為 [不存在] 來移除，則 [ [**移除**](remove.md) ] 屬性在 [InstallValidate](installvalidate-action.md) 動作之後可能不會完全相同。 這表示任何相依于 REMOVE = ALL 的自訂動作都必須在 InstallValidate 動作之後排序。 自訂動作可能會勾選 [移除]，以判斷產品是否已設定為完全卸載。

參考已安裝之檔案作為其來源的自訂動作（例如自訂動作類型 17 (DLL) 、自訂動作類型 18 (EXE) 、自訂動作類型 21 (JScript) ，以及自訂動作類型 22 (VBScript) ）必須遵守下列順序限制。

-   自訂動作必須在 [CostFinalize](costfinalize-action.md) 動作之後排序，才能解析參考檔案的路徑。
-   如果來源檔案尚未安裝在電腦上，延遲的 (腳本內) 自訂動作必須在 [InstallFiles](installfiles-action.md)之後排序。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallInitialize](installinitialize-action.md) 動作之後排序 nondeferred 自訂動作。

下列排序限制適用于變更或更新 Windows Installer 封裝的自訂動作。

-   如果自訂動作變更了封裝（例如將資料列加入資料表中），則必須在 [InstallInitialize](installinitialize-action.md) 動作之前排序動作。
-   如果自訂動作會產生會影響成本的變更，則應該在 [CostInitialize](costfinalize-action.md) 動作之前排序。
-   如果自訂動作變更了功能或元件的安裝狀態，則必須在 [InstallValidate](installvalidate-action.md) 動作之前排序。

 

 



