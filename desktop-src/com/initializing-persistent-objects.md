---
title: 初始化持續性物件
description: 初始化持續性物件
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549194"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="03b6d-103">初始化持續性物件</span><span class="sxs-lookup"><span data-stu-id="03b6d-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="03b6d-104">數個持續性物件介面 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))和 [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)，可讓用戶端將物件初始化為「全新」或「預設」狀態。</span><span class="sxs-lookup"><span data-stu-id="03b6d-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="03b6d-105">這個初始狀態與新建立的物件（沒有狀態）不同。</span><span class="sxs-lookup"><span data-stu-id="03b6d-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="03b6d-106">將物件的狀態（甚至是預設狀態）初始化可能是需要大量計算或需要大量資源的作業。</span><span class="sxs-lookup"><span data-stu-id="03b6d-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="03b6d-107">藉由分隔建立與初始化，只有在實際需要時才會執行初始化，用戶端可以避免將物件初始化為預設狀態，以立即載入先前儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="03b6d-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03b6d-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="03b6d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03b6d-109">持續性物件介面</span><span class="sxs-lookup"><span data-stu-id="03b6d-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 