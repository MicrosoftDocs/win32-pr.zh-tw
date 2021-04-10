---
title: COM)  (持續性物件介面
description: 持續性物件會執行一個或多個持續性物件介面。
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933670"
---
# <a name="persistent-object-interfaces"></a><span data-ttu-id="97bfd-103">持續性物件介面</span><span class="sxs-lookup"><span data-stu-id="97bfd-103">Persistent Object Interfaces</span></span>

<span data-ttu-id="97bfd-104">持續性物件會執行一個或多個 *持續性物件介面*。</span><span class="sxs-lookup"><span data-stu-id="97bfd-104">A persistent object implements one or more *persistent object interfaces*.</span></span> <span data-ttu-id="97bfd-105">用戶端會使用持續性物件介面，來告知這些物件何時以及要儲存其狀態的位置。</span><span class="sxs-lookup"><span data-stu-id="97bfd-105">Clients use persistent object interfaces to tell those objects when and where to store their state.</span></span> <span data-ttu-id="97bfd-106">所有的持續性物件介面都是衍生自 [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)，因此任何實作為持續性物件介面的物件也會實作為 **IPersist**。</span><span class="sxs-lookup"><span data-stu-id="97bfd-106">All persistent object interfaces are derived from [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), so any object that implements any persistent object interface also implements **IPersist**.</span></span>

<span data-ttu-id="97bfd-107">目前已定義下列持續性物件介面：</span><span class="sxs-lookup"><span data-stu-id="97bfd-107">The following persistent object interfaces are currently defined:</span></span>

-   [<span data-ttu-id="97bfd-108">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="97bfd-108">**IPersistStream**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [<span data-ttu-id="97bfd-109">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="97bfd-109">**IPersistStreamInit**</span></span>](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [<span data-ttu-id="97bfd-110">**IPersistStorage**</span><span class="sxs-lookup"><span data-stu-id="97bfd-110">**IPersistStorage**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [<span data-ttu-id="97bfd-111">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="97bfd-111">**IPersistFile**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   <span data-ttu-id="97bfd-112">[**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97bfd-112">[**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))</span></span>
-   <span data-ttu-id="97bfd-113">[IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97bfd-113">[IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))</span></span>
-   <span data-ttu-id="97bfd-114">[IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97bfd-114">[IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))</span></span>

<span data-ttu-id="97bfd-115">實施者會根據物件的使用方式，選擇物件支援的持續性物件介面。</span><span class="sxs-lookup"><span data-stu-id="97bfd-115">Implementers choose which persistent object interfaces an object supports depending on how the object is to be used.</span></span> <span data-ttu-id="97bfd-116">藉由不支援任何持續性物件介面，實施者實際上會說：「這個物件的狀態無法持續儲存」。</span><span class="sxs-lookup"><span data-stu-id="97bfd-116">By not supporting any persistent object interfaces, the implementer is effectively saying, "This object's state cannot be persistently stored."</span></span> <span data-ttu-id="97bfd-117">藉由支援一或多個持續性物件介面，實施者實際上會說：「這個物件的狀態可以持續儲存在一或多個資料存放區媒體中」。</span><span class="sxs-lookup"><span data-stu-id="97bfd-117">By supporting one or more persistent object interfaces, the implementer is effectively saying, "This object's state can be persistently stored in one or more data store mediums."</span></span>

<span data-ttu-id="97bfd-118">例如，下表列出數個允許不同持續性物件介面支援的物件類型。</span><span class="sxs-lookup"><span data-stu-id="97bfd-118">For example, the following table lists several object types that allow support for different persistent object interfaces.</span></span>



| <span data-ttu-id="97bfd-119">類別</span><span class="sxs-lookup"><span data-stu-id="97bfd-119">Category</span></span>                            | <span data-ttu-id="97bfd-120">通常支援持續性物件介面</span><span class="sxs-lookup"><span data-stu-id="97bfd-120">Persistent object interfaces typically supported</span></span>                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97bfd-121">名字</span><span class="sxs-lookup"><span data-stu-id="97bfd-121">Monikers</span></span><br/>                 | [<span data-ttu-id="97bfd-122">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="97bfd-122">**IPersistStream**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| <span data-ttu-id="97bfd-123">OLE 內嵌物件</span><span class="sxs-lookup"><span data-stu-id="97bfd-123">OLE embeddable objects</span></span><br/>   | <span data-ttu-id="97bfd-124">[**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="97bfd-124">[**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)</span></span><br/>                                                                                                              |
| <span data-ttu-id="97bfd-125">ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="97bfd-125">ActiveX controls</span></span><br/>         | <span data-ttu-id="97bfd-126">[**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、IPersistMemory、IPersistPropertyBag、 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97bfd-126">[**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))</span></span><br/> |
| <span data-ttu-id="97bfd-127">ActiveX 檔物件</span><span class="sxs-lookup"><span data-stu-id="97bfd-127">ActiveX document objects</span></span><br/> | <span data-ttu-id="97bfd-128">[**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)、 [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="97bfd-128">[**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)</span></span><br/>                                                                                                              |



 

<span data-ttu-id="97bfd-129">用戶端實施者也可以選擇用戶端可以使用的持續性物件介面。</span><span class="sxs-lookup"><span data-stu-id="97bfd-129">Client implementers can also choose which persistent object interfaces the client can use.</span></span> <span data-ttu-id="97bfd-130">用戶端使用的介面通常是由用戶端可以儲存本身資料的位置所決定。</span><span class="sxs-lookup"><span data-stu-id="97bfd-130">The interfaces a client uses is usually determined by where the client can store its own data.</span></span> <span data-ttu-id="97bfd-131">只能將其資料儲存在一般檔案中的用戶端，可能只會使用 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)、 [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))和 IPersistPropertyBag。</span><span class="sxs-lookup"><span data-stu-id="97bfd-131">A client that can store its data only in a flat file will probably use only [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), and IPersistPropertyBag.</span></span> <span data-ttu-id="97bfd-132"> (**IPersistStreamInit** 可以在大部分的應用程式中取代 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ，因為它包含該定義並新增初始化方法。 ) 可將其資料儲存至結構化儲存體檔案的用戶端，也會使用 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)。</span><span class="sxs-lookup"><span data-stu-id="97bfd-132">(**IPersistStreamInit** can replace [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in most applications, because it contains that definition and adds an initialization method.) A client that can save its data to a structured storage file will, in addition, use [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).</span></span>

## <a name="related-topics"></a><span data-ttu-id="97bfd-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="97bfd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97bfd-134">初始化持續性物件</span><span class="sxs-lookup"><span data-stu-id="97bfd-134">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)
</dt> </dl>

 

