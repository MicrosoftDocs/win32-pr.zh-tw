---
description: 對等基礎結構函數傳回的所有指標都必須使用 PeerGraphFreeData 或 PeerFreeData 來釋放。
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: 釋放對等資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026755"
---
# <a name="freeing-peer-data"></a><span data-ttu-id="4ba78-103">釋放對等資料</span><span class="sxs-lookup"><span data-stu-id="4ba78-103">Freeing Peer Data</span></span>

<span data-ttu-id="4ba78-104">對等基礎結構函數傳回的所有指標都必須使用 [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) 或 [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)來釋放。</span><span class="sxs-lookup"><span data-stu-id="4ba78-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="4ba78-105">這些函式只能針對對等基礎結構函數直接傳回的結構呼叫。</span><span class="sxs-lookup"><span data-stu-id="4ba78-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="4ba78-106">請勿呼叫不同的 FreeData 函式來釋放嵌套指標，例如，請勿在 [**對等 \_ 記錄**](/windows/desktop/api/P2P/ns-p2p-peer_record) 結構的指標上呼叫 FreeData 函數。</span><span class="sxs-lookup"><span data-stu-id="4ba78-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="4ba78-107">釋放資料的範例</span><span class="sxs-lookup"><span data-stu-id="4ba78-107">Example of Freeing Data</span></span>

<span data-ttu-id="4ba78-108">下列程式碼片段示範如何取出與圖形相關聯的屬性，然後釋放傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="4ba78-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


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



 

 



