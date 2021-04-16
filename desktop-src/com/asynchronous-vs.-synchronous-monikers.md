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
# <a name="asynchronous-and-synchronous-monikers"></a><span data-ttu-id="444ac-103">非同步和同步的名字標記</span><span class="sxs-lookup"><span data-stu-id="444ac-103">Asynchronous and Synchronous Monikers</span></span>

<span data-ttu-id="444ac-104">標準、同步 OLE 標記的用戶端通常會建立並保存該標記的參考，以及要在系結期間使用的系結內容。</span><span class="sxs-lookup"><span data-stu-id="444ac-104">A client of a standard, synchronous OLE moniker typically creates and holds a reference to the moniker, as well as the bind-context to be used during binding.</span></span> <span data-ttu-id="444ac-105">下圖顯示使用傳統的標記時所牽涉到的元件。</span><span class="sxs-lookup"><span data-stu-id="444ac-105">The components involved in using traditional monikers are shown in the following diagram.</span></span>

![此圖顯示連接至系結內容的用戶端，或系統提供之任何標記的用戶端。](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

<span data-ttu-id="444ac-107">用戶端通常會藉由呼叫像是 [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker)、 [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)或 [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) 等函式來建立標準的名字，因為它們可以透過 [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) 和 [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream)儲存至持續性儲存體中。</span><span class="sxs-lookup"><span data-stu-id="444ac-107">Clients typically create standard monikers by calling functions such as [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker), or [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) or, because they are can be saved to persistent storage, through [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) and [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream).</span></span> <span data-ttu-id="444ac-108">您也可以藉由呼叫 [**IBindHost：： CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) 方法，從容器物件取得標記。</span><span class="sxs-lookup"><span data-stu-id="444ac-108">Monikers may also be obtained from a container object by calling the [**IBindHost::CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) method.</span></span> <span data-ttu-id="444ac-109">用戶端會藉由呼叫 [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) 函式來建立系結內容，然後使用 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)的呼叫，將系結內容傳遞至標記。</span><span class="sxs-lookup"><span data-stu-id="444ac-109">Clients create bind contexts by calling the [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) function and then pass the bind context to the moniker with calls to [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span>

<span data-ttu-id="444ac-110">如下圖所示，非同步標記的用戶端也會建立及保存要在系結期間使用的標記和系結內容的參考。</span><span class="sxs-lookup"><span data-stu-id="444ac-110">As shown in the following diagram, a client of an asynchronous moniker also creates and holds a reference to the moniker and bind context to be used during binding.</span></span>

![顯示用戶端提供的、Monker 提供和系統提供的連接的圖表。](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

<span data-ttu-id="444ac-112">為了取得非同步行為，用戶端會在系結狀態回呼物件上執行 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面，並呼叫 [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) 函數或 [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) 函式，以向系結內容註冊這個介面。</span><span class="sxs-lookup"><span data-stu-id="444ac-112">To get asynchronous behavior, the client implements the [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interface on a bind-status-callback object and calls either the [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) function or the [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) function to register this interface with the bind context.</span></span> <span data-ttu-id="444ac-113">在 [**IBindStatusCallback：： OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85))方法的呼叫中，此標記會傳遞其 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85))介面的指標。</span><span class="sxs-lookup"><span data-stu-id="444ac-113">The moniker passes a pointer to its [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) interface in a call to the [**IBindStatusCallback::OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) method.</span></span> <span data-ttu-id="444ac-114">用戶端會在從 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) 方法的標記呼叫傳回時，告知非同步名字。</span><span class="sxs-lookup"><span data-stu-id="444ac-114">The client tells the asynchronous moniker how it wants to bind on return from the moniker's call to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="444ac-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="444ac-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="444ac-116">非同步名字</span><span class="sxs-lookup"><span data-stu-id="444ac-116">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 