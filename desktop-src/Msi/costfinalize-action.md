---
description: CostFinalize 動作會結束由 CostInitialize 動作開始的內部安裝成本處理常式。
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: CostFinalize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975475"
---
# <a name="costfinalize-action"></a>CostFinalize 動作

CostFinalize 動作會結束由 [CostInitialize](costinitialize-action.md)動作開始的內部安裝 [*成本*](c-gly.md)處理常式。

## <a name="sequence-restrictions"></a>順序限制

任何會影響成本的標準或 [自訂動作](custom-actions.md) ，都應該在 [CostInitialize](costinitialize-action.md) 動作之前排序。 在 CostInitialize 動作之後立即呼叫 [FileCost](filecost-action.md) 動作，然後呼叫 CostFinalize 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。

CostFinalize 動作必須在啟動任何使用者介面順序之前執行，讓使用者能夠查看或修改 [功能](feature-table.md) 資料表選取專案或目錄。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

CostFinalize 動作會查詢 [條件](condition-table.md) 資料表，以判斷要安裝的功能。 [元件](component-table.md)資料表中的每個元件都會進行成本計算。

CostFinalize 動作也會先確認所有目標目錄都是可寫入的，然後才允許安裝繼續進行。

> [!Note]  
> 在 [系統管理安裝](administrative-installation.md)期間，CostFinalize 會設定所有安裝的功能，但功能 [資料表](feature-table.md)的 [層級] 資料行中有0個撰寫的功能除外。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案成本](file-costing.md)
</dt> </dl>

 

 



