---
title: 非同步和同步的名字標記
description: 非同步和同步的名字標記
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553358"
---
# <a name="asynchronous-and-synchronous-monikers"></a>非同步和同步的名字標記

標準、同步 OLE 標記的用戶端通常會建立並保存該標記的參考，以及要在系結期間使用的系結內容。 下圖顯示使用傳統的標記時所牽涉到的元件。

![此圖顯示連接至系結內容的用戶端，或系統提供之任何標記的用戶端。](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

用戶端通常會藉由呼叫像是 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker)、 [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)或 [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) 等函式來建立標準的名字，因為它們可以透過 [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) 和 [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream)儲存至持續性儲存體中。 您也可以藉由呼叫 [**IBindHost：： CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) 方法，從容器物件取得標記。 用戶端會藉由呼叫 [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) 函式來建立系結內容，然後使用 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)的呼叫，將系結內容傳遞至標記。

如下圖所示，非同步標記的用戶端也會建立及保存要在系結期間使用的標記和系結內容的參考。

![顯示用戶端提供的、Monker 提供和系統提供的連接的圖表。](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

為了取得非同步行為，用戶端會在系結狀態回呼物件上執行 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面，並呼叫 [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) 函數或 [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) 函式，以向系結內容註冊這個介面。 在 [**IBindStatusCallback：： OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85))方法的呼叫中，此標記會傳遞其 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85))介面的指標。 用戶端會在從 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) 方法的標記呼叫傳回時，告知非同步名字。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步名字](asynchronous-monikers.md)
</dt> </dl>

 

 