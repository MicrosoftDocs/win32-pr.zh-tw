---
description: CostInitialize 動作會起始安裝成本處理常式。
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: CostInitialize 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959e9e250292a44050c1f4b9feb3fb29f7530fe2a1f53aa77a62bf3680ea9eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948365"
---
# <a name="costinitialize-action"></a>CostInitialize 動作

CostInitialize 動作會起始安裝 [*成本*](c-gly.md) 處理常式。

## <a name="sequence-restrictions"></a>順序限制

任何會影響成本的標準或 [自訂](custom-actions.md) 動作，都應該在 CostInitialize 動作之前排序。 在 CostInitialize 動作之後立即呼叫 [FileCost](filecost-action.md) 動作。 然後，在 CostInitialize 動作動作之後呼叫 [CostFinalize](costfinalize-action.md) 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

CostInitialize 動作會將元件資料表和 [功能](feature-table.md) 資料表載入記憶體中。

如需安裝程式中 [*成本*](c-gly.md) 處理常式的詳細資訊，請參閱檔案 [成本](file-costing.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案成本](file-costing.md)
</dt> </dl>

 

 



