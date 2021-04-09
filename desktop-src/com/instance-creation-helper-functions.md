---
title: 實例建立 Helper 函數
description: 實例建立 Helper 函數
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024139"
---
# <a name="instance-creation-helper-functions"></a><span data-ttu-id="0aae0-103">實例建立 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="0aae0-103">Instance Creation Helper Functions</span></span>

<span data-ttu-id="0aae0-104">在舊版的 COM 中，用來建立物件實例的主要機制是 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。</span><span class="sxs-lookup"><span data-stu-id="0aae0-104">In previous releases of COM, the primary mechanism used to create an object instance was the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="0aae0-105">此函式會封裝建立類別物件的程式，並使用該物件建立新的實例和釋放類別物件。</span><span class="sxs-lookup"><span data-stu-id="0aae0-105">This function encapsulates the process of creating a class object, using that to create a new instance and releasing the class object.</span></span> <span data-ttu-id="0aae0-106">這種類型的另一個函式是更特定的 [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)，這是可建立類別物件並抓取所要求物件之指標的 OLE 複合檔案協助程式。</span><span class="sxs-lookup"><span data-stu-id="0aae0-106">Another function of this kind is the more specific [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate), the OLE compound document helper that creates a class object and retrieves a pointer to a requested object.</span></span>

<span data-ttu-id="0aae0-107">為了使在分散式系統上建立實例的程式更順暢，COM 引進四個重要的新實例建立機制：</span><span class="sxs-lookup"><span data-stu-id="0aae0-107">To smooth the process of instance creation on distributed systems, COM has introduced four important new instance creation mechanisms:</span></span>

-   <span data-ttu-id="0aae0-108">類別的名字和 [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)</span><span class="sxs-lookup"><span data-stu-id="0aae0-108">Class monikers and [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)</span></span>
-   [<span data-ttu-id="0aae0-109">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="0aae0-109">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="0aae0-110">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="0aae0-110">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="0aae0-111">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="0aae0-111">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

<span data-ttu-id="0aae0-112">類別的「標記」（class）可讓您識別物件的類別，而且通常會與另一個標記（例如檔案的標記）搭配使用，以指出物件的位置。</span><span class="sxs-lookup"><span data-stu-id="0aae0-112">A class moniker permits you to identify the class of an object and is typically used with another moniker, like a file moniker, to indicate the location of the object.</span></span> <span data-ttu-id="0aae0-113">這可讓您系結至物件，並指定要為該物件啟動的伺服器。</span><span class="sxs-lookup"><span data-stu-id="0aae0-113">This permits you to bind to an object and specify the server that is to be launched for that object.</span></span> <span data-ttu-id="0aae0-114">類別的標記也可以撰寫至支援系結至 [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) 介面的名字標記右邊。</span><span class="sxs-lookup"><span data-stu-id="0aae0-114">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="0aae0-115">如需詳細資訊，請參閱 [類別的名字](class-monikers.md)。</span><span class="sxs-lookup"><span data-stu-id="0aae0-115">For more information, see [Class Monikers](class-monikers.md).</span></span>

<span data-ttu-id="0aae0-116">[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) 延伸了 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ，讓您能夠在指定的遠端電腦上建立與指定 CLSID 相關聯的單一未初始化物件。</span><span class="sxs-lookup"><span data-stu-id="0aae0-116">[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) extends [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to make it possible to create a single uninitialized object associated with the given CLSID on a specified remote machine.</span></span> <span data-ttu-id="0aae0-117">此外，除了要求單一介面並取得該介面的單一指標之外， **CoCreateInstanceEx** 還可讓您查詢多個介面，並 (（如果有) 的話），以在單次往返中接收這些介面的指標，進而減少機器之間的來回行程。</span><span class="sxs-lookup"><span data-stu-id="0aae0-117">In addition, rather than requesting a single interface and obtaining a single pointer to that interface, **CoCreateInstanceEx** makes it possible to query for multiple interfaces and (if available) receive pointers to them in a single round-trip, thus permitting fewer round-trips between machines.</span></span> <span data-ttu-id="0aae0-118">這樣可讓遠端物件互動更加有效率。</span><span class="sxs-lookup"><span data-stu-id="0aae0-118">This can make remote object interaction much more efficient.</span></span> <span data-ttu-id="0aae0-119">若要這樣做，函數會使用多個 [**\_ QI**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="0aae0-119">To do this, the function uses an array of [**MULTI\_QI**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) structures.</span></span>

<span data-ttu-id="0aae0-120">透過 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) 建立物件仍然需要透過呼叫其中一個初始化 (介面來初始化物件，例如 [**IPersistStorage：： Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)) 。</span><span class="sxs-lookup"><span data-stu-id="0aae0-120">Creating an object through [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) still requires that the object be initialized through a call to one of the initialization interfaces (such as [**IPersistStorage::Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)).</span></span> <span data-ttu-id="0aae0-121">Helper 函式 [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) 和 [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) 會封裝 **CoCreateInstanceEx** 的實例建立能力和初始化，並將前者從檔案和後者（從儲存體）封裝。</span><span class="sxs-lookup"><span data-stu-id="0aae0-121">The helper functions [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) encapsulate both the instance creation power of **CoCreateInstanceEx** and the initialization, the former from a file and the latter from a storage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aae0-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="0aae0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aae0-123">透過類別物件建立物件</span><span class="sxs-lookup"><span data-stu-id="0aae0-123">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 