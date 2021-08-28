---
description: FileCostaction 會起始動態 costingof 標準安裝動作。
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: FileCost 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b49cbb4357b33ebe735eaff501f1c155c411bc969c7fea96a1cab7417c803a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947051"
---
# <a name="filecost-action"></a>FileCost 動作

FileCostaction 會起始標準安裝動作的動態 [*成本*](c-gly.md)。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="sequence-restrictions"></a>順序限制

任何會影響成本的標準或 [自訂動作](custom-actions.md) ，都應該在 [CostInitialize](costinitialize-action.md) 動作之前排序。 在 CostInitialize 動作之後立即呼叫 FileCost 動作。 然後，在 CostInitialize 動作之後呼叫 [CostFinalize](costfinalize-action.md) 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。

[CostInitialize](costinitialize-action.md)動作必須在 FileCost 動作之前執行。 然後，安裝程式會以每個元件為基礎，判斷檔案 [資料表中](file-table.md) 每個檔案的磁碟空間成本， (查看 [元件表格](component-table.md)) ，同時採用 [*磁片*](v-gly.md) 區叢集以及可能需要覆寫的現有檔案。 也會考慮使用或釋放磁碟空間的所有動作。 如果找到現有的檔案，則會執行檔案版本檢查，以判斷是否真的需要安裝新的檔案。 如果現有的檔案是相同或更高的版本號碼，則不會覆寫現有的檔案，也不會產生任何磁碟空間成本。 在所有情況下，安裝程式都會使用版本號碼檢查的結果來設定每個檔案的安裝狀態。

FileCost 動作會使用 theinstaller 來初始化成本計算。 在執行 [CostFinalize](costfinalize-action.md)動作之前，不會發生實際的動態 [*成本*](c-gly.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案成本](file-costing.md)
</dt> </dl>

 

 



