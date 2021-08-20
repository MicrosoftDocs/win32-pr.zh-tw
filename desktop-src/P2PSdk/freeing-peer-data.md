---
description: 對等基礎結構函數傳回的所有指標都必須使用 PeerGraphFreeData 或 PeerFreeData 來釋放。
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: 釋放對等資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9492fec9a22da8252188a75d6d4cee73d2055d29f47e25fc7d55a26cc7909c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794575"
---
# <a name="freeing-peer-data"></a>釋放對等資料

對等基礎結構函數傳回的所有指標都必須使用 [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) 或 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)來釋放。 這些函式只能針對對等基礎結構函數直接傳回的結構呼叫。 請勿呼叫不同的 FreeData 函式來釋放嵌套指標，例如，請勿在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構的指標上呼叫 FreeData 函數。

## <a name="example-of-freeing-data"></a>釋放資料的範例

下列程式碼片段示範如何取出與圖形相關聯的屬性，然後釋放傳回的資料。


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



