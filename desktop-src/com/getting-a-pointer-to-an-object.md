---
title: 取得物件的指標
description: 取得物件的指標
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0476d36390e7077e7fdd75eef8d95e8173683891
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2020
ms.locfileid: "106991099"
---
# <a name="getting-a-pointer-to-an-object"></a><span data-ttu-id="c4962-103">取得物件的指標</span><span class="sxs-lookup"><span data-stu-id="c4962-103">Getting a Pointer to an Object</span></span>

<span data-ttu-id="c4962-104">因為 COM 沒有嚴格的類別模型，所以用戶端有四種方式可以具現化或取得物件介面的指標：</span><span class="sxs-lookup"><span data-stu-id="c4962-104">Because COM does not have a strict class model, there are four ways that a client can instantiate or get a pointer to an interface on an object:</span></span>

-   <span data-ttu-id="c4962-105">呼叫 COM 程式庫函式，此函式會建立預先決定之類型的物件。也就是說，函式只會傳回特定物件類別的一個特定介面指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-105">Call a COM library function that creates an object of a predetermined type; that is, the function will return a pointer to only one specific interface for a specific object class.</span></span>
-   <span data-ttu-id="c4962-106">呼叫 COM 程式庫函式，此函式可以根據類別識別碼 (CLSID) 來建立物件，並傳回所要求的任何介面指標類型。</span><span class="sxs-lookup"><span data-stu-id="c4962-106">Call a COM library function that can create an object based on a class identifier (CLSID) and that returns any type of interface pointer requested.</span></span>
-   <span data-ttu-id="c4962-107">呼叫某些介面的方法，以建立另一個物件 (或連接到現有的物件) 並傳回該個別物件上的介面指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-107">Call a method of some interface that creates another object (or connects to an existing one) and returns an interface pointer on that separate object.</span></span>
-   <span data-ttu-id="c4962-108">使用介面來執行物件，讓其他物件將其介面指標直接傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="c4962-108">Implement an object with an interface through which other objects pass their interface pointer to the client directly.</span></span>

<span data-ttu-id="c4962-109">如需取得第一個物件之後，在物件上取得其他介面之指標的詳細資訊，請參閱 [QueryInterface：在物件中導覽](queryinterface--navigating-in-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="c4962-109">For information on getting pointers to other interfaces on an object after you have the first one, see [QueryInterface: Navigating in an Object](queryinterface--navigating-in-an-object.md).</span></span>

## <a name="creating-an-object-of-a-predetermined-type"></a><span data-ttu-id="c4962-110">建立預先決定類型的物件</span><span class="sxs-lookup"><span data-stu-id="c4962-110">Creating an Object of a Predetermined Type</span></span>

<span data-ttu-id="c4962-111">有許多 COM 函式（例如 [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc)）會傳回特定介面實的指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-111">There are numerous COM functions, such as [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), that return pointers to specific interface implementations.</span></span> <span data-ttu-id="c4962-112"> (**CoGetMalloc** 會抓取標準 COM 記憶體配置器的指標。 ) 這些都是協助程式函式，且大部分的函式會在相關的特定區域（例如儲存體或資料傳輸）下，在本檔的參考區段中加以描述。</span><span class="sxs-lookup"><span data-stu-id="c4962-112">(**CoGetMalloc** retrieves a pointer to the standard COM memory allocator.) Most of these are helper functions, and most of these functions are described in the reference sections of this documentation, under the specific area they are related to, such as storage or data transfer.</span></span>

## <a name="creating-an-object-based-on-a-clsid"></a><span data-ttu-id="c4962-113">根據 CLSID 建立物件</span><span class="sxs-lookup"><span data-stu-id="c4962-113">Creating an Object Based on a CLSID</span></span>

<span data-ttu-id="c4962-114">有幾個函式（假設有 CLSID），用戶端可以呼叫來建立物件實例，並取得其指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-114">There are several functions that, given a CLSID, a client can call to create an object instance and get a pointer to it.</span></span> <span data-ttu-id="c4962-115">所有這些函式都是以函式 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)為基礎，此函式會建立類別物件並提供指向介面的指標，該介面可讓您建立該類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c4962-115">All of these functions are based on the function [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), which creates a class object and supplies a pointer to an interface that allows you to create instances of that class.</span></span> <span data-ttu-id="c4962-116">雖然必須有指出伺服器所在之系統的資訊，但用戶端不需要包含該資訊。</span><span class="sxs-lookup"><span data-stu-id="c4962-116">While there must be information that says which system the server resides on, there is no need for that information to be contained in the client.</span></span> <span data-ttu-id="c4962-117">用戶端只需要知道 CLSID，絕對不能是伺服器程式碼的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="c4962-117">The client needs to know only the CLSID and never the absolute path of the server code.</span></span> <span data-ttu-id="c4962-118">如需詳細資訊，請參閱 [透過類別物件建立物件](creating-an-object-through-a-class-object.md)。</span><span class="sxs-lookup"><span data-stu-id="c4962-118">For more information, see [Creating an Object Through a Class Object](creating-an-object-through-a-class-object.md).</span></span>

## <a name="returning-a-pointer-to-a-separate-object"></a><span data-ttu-id="c4962-119">將指標傳回給個別的物件</span><span class="sxs-lookup"><span data-stu-id="c4962-119">Returning a Pointer to a Separate Object</span></span>

<span data-ttu-id="c4962-120">許多會將指標傳回給個別物件的介面方法，是建立並傳回 *列舉值物件* 之指標的許多介面方法，可讓您判斷物件所維護的指定類型有多少專案。</span><span class="sxs-lookup"><span data-stu-id="c4962-120">Among the many interface methods that return a pointer to a separate object are several that create and return a pointer to an *enumerator object*, which allows you to determine how many items of a given type an object maintains.</span></span> <span data-ttu-id="c4962-121">COM 會定義介面，以列舉各種不同的專案，例如字串、重要結構、名字和 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-121">COM defines interfaces for enumerating a wide variety of items, such as strings, important structures, monikers, and [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface pointers.</span></span> <span data-ttu-id="c4962-122">建立列舉值實例並取得其介面指標的一般方式，就是從另一個介面呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="c4962-122">The typical way to create an enumerator instance and get a pointer to its interface is to call a method from another interface.</span></span> <span data-ttu-id="c4962-123">例如， [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面會定義兩個方法（ [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) 和 [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)），以傳回兩個不同列舉物件上介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-123">For example, the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface defines two methods, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) and [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), that return pointers to interfaces on two different enumeration objects.</span></span> <span data-ttu-id="c4962-124">方法的 COM 中有許多其他範例會傳回物件的指標，例如 OLE 複合檔案介面 [**IOleObject：： GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)，在內嵌或連結的物件上呼叫時，會傳回容器物件的 [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)執行指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-124">There are many other examples in COM of methods that return pointers to objects, such as the OLE compound document interface [**IOleObject::GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), which, when called on the embedded or linked object, returns a pointer to the container object's implementation of [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite).</span></span>

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a><span data-ttu-id="c4962-125">執行將介面指標直接傳遞至用戶端的物件</span><span class="sxs-lookup"><span data-stu-id="c4962-125">Implementing an Object Through Which to Pass an Interface Pointer Directly to the Client</span></span>

<span data-ttu-id="c4962-126">當兩個物件（例如，OLE 複合檔案容器和伺服器）需要雙向通訊時，每個物件都會執行包含介面方法的物件，而介面方法可透過此方法將介面指標傳遞至另一個物件。</span><span class="sxs-lookup"><span data-stu-id="c4962-126">When two objects, such as an OLE compound document container and server, need bidirectional communication, each implements an object containing an interface method through which it can pass an interface pointer to the other object.</span></span> <span data-ttu-id="c4962-127">執行物件也是所建立物件的用戶端，接著可以呼叫方法，並取得傳遞的指標。</span><span class="sxs-lookup"><span data-stu-id="c4962-127">The implementing object, which is also the client of the created object, can then call the method and get the pointer that was passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4962-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4962-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4962-129">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="c4962-129">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="c4962-130">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="c4962-130">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 




