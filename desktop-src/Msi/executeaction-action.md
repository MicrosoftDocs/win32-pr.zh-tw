---
description: ExecuteAction 動作會使用 EXECUTEACTION 屬性來起始執行順序，以判斷要執行哪一種類型的安裝。
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: ExecuteAction 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469280"
---
# <a name="executeaction-action"></a>ExecuteAction 動作

ExecuteAction 動作會使用 [**ExecuteAction**](executeaction.md) 屬性來起始執行順序，以判斷要執行哪一種類型的安裝。

## <a name="sequence-restrictions"></a>順序限制

在開始安裝所需的所有資訊收集完成之後，應該將這個動作排序。 在 [InstallUISequence 資料表](installuisequence-table.md)和 [AdminUISequence 資料表](adminuisequence-table.md)中的 ExecuteAction 動作之後，可能會排序其他動作。 順序通常會以 [*成本*](c-gly.md) 動作開頭，例如 [CostInitialize 動作](costinitialize-action.md)，後面接著使用者介面動作，再接著 ExecuteAction 動作。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

如果已啟用安裝程式服務，則會以系統許可權執行 ExecuteAction 動作。 最上層的動作（例如 [ [安裝動作](install-action.md)]、[ [公告動作](advertise-action.md)] 和 [ [管理員] 動作](admin-action.md) ）包含判斷呼叫 ExecuteAction 動作是否需要執行執行順序或使用者介面順序的內部邏輯。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InstallUISequence 資料表](installuisequence-table.md)
</dt> <dt>

[AdminUISequence 資料表](adminuisequence-table.md)
</dt> <dt>

[CostInitialize 動作](costinitialize-action.md)
</dt> </dl>

 

 



