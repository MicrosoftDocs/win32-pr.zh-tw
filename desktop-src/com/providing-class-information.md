---
title: 提供類別資訊
description: 提供類別資訊
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092262"
---
# <a name="providing-class-information"></a><span data-ttu-id="616c2-103">提供類別資訊</span><span class="sxs-lookup"><span data-stu-id="616c2-103">Providing Class Information</span></span>

<span data-ttu-id="616c2-104">這通常適用于物件的用戶端檢查物件的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="616c2-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="616c2-105">根據物件的 CLSID，用戶端可以使用登錄專案找出物件的類型程式庫，然後在符合 CLSID 的程式庫中掃描 coclass 專案的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="616c2-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="616c2-106">不過，並非所有物件都有 CLSID，不過它們仍然需要提供類型資訊。</span><span class="sxs-lookup"><span data-stu-id="616c2-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="616c2-107">此外，用戶端可以輕鬆地要求物件提供其類型資訊，而不是透過所有冗長工作從登錄專案中解壓縮相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="616c2-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="616c2-108">這項功能在處理可連線物件上的連出介面時相當重要。</span><span class="sxs-lookup"><span data-stu-id="616c2-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="616c2-109"> (如需可連線物件如何提供這項功能的詳細資訊，請參閱 [使用 IProvideClassInfo](using-iprovideclassinfo.md) 。 ) </span><span class="sxs-lookup"><span data-stu-id="616c2-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="616c2-110">在這些情況下，用戶端可以查詢 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 或 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)的物件。</span><span class="sxs-lookup"><span data-stu-id="616c2-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="616c2-111">如果這些介面存在，用戶端會呼叫 [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) 方法來取得介面的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="616c2-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="616c2-112">藉由執行 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 或 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)，物件指定它可以提供整個類別的型別資訊。也就是說，它在其類型程式庫的 coclass 區段中所描述的內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="616c2-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="616c2-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) 會傳回對應至物件之 coclass 資訊的 **ITypeInfo** 指標。</span><span class="sxs-lookup"><span data-stu-id="616c2-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="616c2-114">透過這個 **ITypeInfo** 指標，用戶端可以檢查所有物件的傳入和傳出介面定義。</span><span class="sxs-lookup"><span data-stu-id="616c2-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="616c2-115">物件也可以提供 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)。</span><span class="sxs-lookup"><span data-stu-id="616c2-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="616c2-116">**Iprovideclassinfo2.getguid** 介面是 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)的簡單延伸，可讓您快速且輕鬆地針對其預設事件集取得物件的輸出介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="616c2-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="616c2-117">**Iprovideclassinfo2.getguid** 衍生自 **IProvideClassInfo**。</span><span class="sxs-lookup"><span data-stu-id="616c2-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="616c2-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="616c2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616c2-119">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="616c2-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




