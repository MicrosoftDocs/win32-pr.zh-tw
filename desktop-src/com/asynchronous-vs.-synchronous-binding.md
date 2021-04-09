---
title: 非同步和同步系結
description: 非同步和同步系結
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b022df239221f0a019b972067248225210e585
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683162"
---
# <a name="asynchronous-and-synchronous-binding"></a><span data-ttu-id="eb0c3-103">非同步和同步系結</span><span class="sxs-lookup"><span data-stu-id="eb0c3-103">Asynchronous and Synchronous Binding</span></span>

<span data-ttu-id="eb0c3-104">用戶端可以藉由呼叫 [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) 函式來查看是否為非同步標記。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-104">The client may check to see whether the moniker is asynchronous by calling the [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) function.</span></span> <span data-ttu-id="eb0c3-105">如果用戶端傳回 BINDF \_ 非同步旗標，而不是從後續呼叫 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 或 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)傳回物件指標或儲存體指標，則該標記會傳回 MK \_ 的 \_ 非同步來取代物件指標，而 **Null** 則取代儲存體指標。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-105">If the client returns the BINDF\_ASYNCHRONOUS flag, rather than returning an object pointer or a storage pointer from subsequent calls to [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), the moniker returns MK\_S\_ASYNCHRONOUS in place of the object pointer and **NULL** in place of the storage pointer.</span></span> <span data-ttu-id="eb0c3-106">為了回應，用戶端應該在 [**IBindStatusCallback：： OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) 和 [**IBindStatusCallback：： OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85))的執行期間，等候接收要求的物件或儲存體。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-106">In response, the client should wait to receive the requested object or storage during implementation of [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) and [**IBindStatusCallBack::OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).</span></span>

<span data-ttu-id="eb0c3-107">回呼物件也會透過 [**IBindStatusCallback：： OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85))、透過 [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))的資料可用性通知，以及有關系結作業狀態之標記的各種其他通知，來接收進度通知。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-107">The callback object also receives progress notification through [**IBindStatusCallback::OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), data availability notification through [**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), and various other notifications from the moniker about the status of the binding operation.</span></span>

<span data-ttu-id="eb0c3-108">如果用戶端不會 \_ 從 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))的標記呼叫傳回 BINDF 非同步旗標，系結作業將會同步執行，而所需的物件或儲存體將會從後續呼叫 [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 或 [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage)傳回。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-108">If the client does not return the BINDF\_ASYNCHRONOUS flag from the moniker's call to [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), the bind operation will proceed synchronously and the desired object or storage will be returned from subsequent calls to [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) or [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).</span></span> <span data-ttu-id="eb0c3-109">同樣地，如果用戶端需要同步作業，而且不想要接收任何進度通知或回呼，則可以要求非同步標記，而不是藉由執行 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85))來同步處理。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-109">Similarly, if the client desires synchronous operation and does not wish to receive any progress notifications or callbacks, it can request an asynchronous moniker to behave synchronously by not implementing [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)).</span></span> <span data-ttu-id="eb0c3-110">在這種情況下，非同步標記行為會像標準同步的標記一樣。</span><span class="sxs-lookup"><span data-stu-id="eb0c3-110">In such cases, the asynchronous moniker will behave like a standard synchronous moniker.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb0c3-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb0c3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb0c3-112">非同步名字</span><span class="sxs-lookup"><span data-stu-id="eb0c3-112">Asynchronous Monikers</span></span>](asynchronous-monikers.md)
</dt> </dl>

 

 