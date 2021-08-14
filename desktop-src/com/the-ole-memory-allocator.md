---
title: OLE 記憶體配置器
description: OLE 記憶體配置器
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0be9cb16459787aa1fd56a691c8475f4d81ba359ecec690f2178e4f5e83cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103645"
---
# <a name="the-ole-memory-allocator"></a>OLE 記憶體配置器

COM 程式庫提供記憶體配置器的實作為安全線程。  (也就是說，在多執行緒情況下，它不會造成問題 ) 。每當配置的記憶體區塊擁有權透過 COM 介面或在用戶端與 COM 程式庫之間傳遞時，您就必須使用這個 COM 配置器來配置記憶體。 物件的內部配置可以使用任何所需的配置配置，但是 COM 記憶體配置器是一個方便、有效率且安全線程的配置器。

對 API 函式 [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) 的呼叫會提供 OLE 配置器的指標，這是 [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) 介面的實作為。 不過，呼叫 helper 函式 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)、 [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)和 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)會更有效率，這會包裝取得工作記憶體配置器的指標、呼叫對應的 **IMalloc** 方法，然後釋放配置器的指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理記憶體配置](managing-memory-allocation.md)
</dt> <dt>

[COM 程式庫](the-com-library.md)
</dt> </dl>

 

 