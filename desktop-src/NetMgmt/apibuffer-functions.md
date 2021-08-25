---
title: ApiBuffer 函式
description: 網路管理 ApiBuffer 函式可用來管理具有網路管理功能之應用程式所使用的記憶體配置。
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912477"
---
# <a name="apibuffer-functions"></a>ApiBuffer 函式

網路管理 ApiBuffer 函式可用來管理具有網路管理功能之應用程式所使用的記憶體配置。 不過，一般而言，針對應用程式所使用的其他記憶體，您應該使用 [記憶體管理](/windows/desktop/Memory/memory-management-functions) 函式，而不是這些 ApiBuffer 函數。

ApiBuffer 函數如下所示。



| 函式                                                 | 描述                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | 從堆積配置記憶體。 當您需要與 **NetApiBufferFree** 函數相容時，請呼叫此函數。 |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | 釋放 **NetApiBufferAllocate** 函式所配置的記憶體和其他網路管理功能。                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | 變更 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小。                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | 傳回對 **NetApiBufferAllocate** 函式的呼叫所配置的緩衝區大小（以位元組為單位）。                     |



 

針對將資訊傳回給呼叫端的可遠端函式，RPC 執行時間程式庫會配置包含傳回信息的緩衝區。 當呼叫端處理完資訊之後，它必須呼叫 [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) 函式來釋放已配置的緩衝區。

 

 