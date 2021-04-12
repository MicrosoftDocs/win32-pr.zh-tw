---
title: 屬性和屬性集
description: 雖然自動化和 Microsoft ActiveX 控制項提供的執行時間屬性種類很重要，但它們並不直接滿足儲存儲存在檔案系統中之物件資訊的需求。
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、屬性和屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372682"
---
# <a name="properties-and-property-sets"></a><span data-ttu-id="c295e-104">屬性和屬性集</span><span class="sxs-lookup"><span data-stu-id="c295e-104">Properties and Property Sets</span></span>

<span data-ttu-id="c295e-105">雖然自動化和 Microsoft ActiveX 控制項提供的執行時間屬性種類很重要，但它們並不直接滿足儲存儲存在檔案系統中之物件資訊的需求。</span><span class="sxs-lookup"><span data-stu-id="c295e-105">While the kinds of run-time properties that Automation and Microsoft ActiveX Controls offer are important, they do not directly address the need to store information with objects persistently stored in the file system.</span></span> <span data-ttu-id="c295e-106">這些實體可能包含 (結構化、複合) 、目錄和摘要目錄等檔案。</span><span class="sxs-lookup"><span data-stu-id="c295e-106">These entities could include files (structured, compound, and so forth), directories, and summary catalogs.</span></span> <span data-ttu-id="c295e-107">COM 同時提供這些持續性屬性的標準序列化格式，以及一組可讓您建立及操作屬性集及其屬性的介面和函式。</span><span class="sxs-lookup"><span data-stu-id="c295e-107">COM provides both a standard serialized format for these persistent properties, and a set of interfaces and functions that allow you to create and manipulate the property sets and their properties.</span></span>

<span data-ttu-id="c295e-108">持續性屬性會儲存為集合，且一或多個集合可能會與檔案系統實體相關聯。</span><span class="sxs-lookup"><span data-stu-id="c295e-108">Persistent properties are stored as sets, and one or more sets may be associated with a file system entity.</span></span> <span data-ttu-id="c295e-109">這些持續性屬性集會用來儲存適合當做更精細值集合來表示的資料。</span><span class="sxs-lookup"><span data-stu-id="c295e-109">These persistent property sets are intended to be used to store data that is suited to being represented as a collection of fine-grained values.</span></span> <span data-ttu-id="c295e-110">它們並不是用來做為大型的資料基底。</span><span class="sxs-lookup"><span data-stu-id="c295e-110">They are not intended to be used as a large data base.</span></span> <span data-ttu-id="c295e-111">它們可用來儲存有關系統上物件的摘要資訊，然後可供任何其他瞭解如何解讀該屬性集的物件存取。</span><span class="sxs-lookup"><span data-stu-id="c295e-111">They can be used to store summary information about an object on the system, which can then be accessed by any other object that understands how to interpret that property set.</span></span>

<span data-ttu-id="c295e-112">先前的 COM 版本指定的內容和用法非常少，但卻定義了序列化格式，可讓開發人員將屬性和屬性集儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。</span><span class="sxs-lookup"><span data-stu-id="c295e-112">Previous versions of COM specified very little with respect to properties and their usage, but did define a serialized format that allowed developers to store properties and property sets in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance.</span></span> <span data-ttu-id="c295e-113">也定義了單一屬性集的屬性識別碼和語義（用於檔的摘要資訊）。</span><span class="sxs-lookup"><span data-stu-id="c295e-113">The property identifiers and semantics of a single property set, used for summary information about a document, were also defined.</span></span> <span data-ttu-id="c295e-114">屆時，必須以資料流程的形式直接建立和操作該結構。</span><span class="sxs-lookup"><span data-stu-id="c295e-114">At that time, it was necessary to create and manipulate that structure directly as a data stream.</span></span> <span data-ttu-id="c295e-115">請參閱 [結構化儲存體序列化屬性集格式](structured-storage-serialized-property-set-format.md)。</span><span class="sxs-lookup"><span data-stu-id="c295e-115">See [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).</span></span>

<span data-ttu-id="c295e-116">不過，現在 COM 定義了兩個主要介面來管理屬性集：</span><span class="sxs-lookup"><span data-stu-id="c295e-116">Now, however, COM defines two primary interfaces to manage property sets:</span></span>

-   [<span data-ttu-id="c295e-117">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="c295e-117">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [<span data-ttu-id="c295e-118">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="c295e-118">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

<span data-ttu-id="c295e-119">當這些介面在支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面 (（例如複合檔案) ）的物件上執行時，不再需要直接處理序列化格式。</span><span class="sxs-lookup"><span data-stu-id="c295e-119">It is no longer necessary to deal with the serialized format directly when these interfaces are implemented on an object that supports the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface (such as compound files).</span></span> <span data-ttu-id="c295e-120">透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 寫入屬性會建立完全符合 COM 屬性集格式的資料，如透過 **IStorage** 方法所查看。</span><span class="sxs-lookup"><span data-stu-id="c295e-120">Writing properties through [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates data that exactly conforms to the COM property set format, as viewed through **IStorage** methods.</span></span> <span data-ttu-id="c295e-121">反之也是如此，使用 **IStorage** 寫入 COM 屬性集格式的屬性會透過 **IPropertySetStorage** 和 **IPropertyStorage** (顯示，不過您無法預期寫入 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 並讓屬性通過 **IPropertyStorage** 立即可用，反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="c295e-121">The converse is also true — properties written to the COM property set format using **IStorage** are visible through **IPropertySetStorage** and **IPropertyStorage** (although you cannot expect to write to [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) and have the properties through **IPropertyStorage** immediately available, or vice versa).</span></span>

<span data-ttu-id="c295e-122">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面會定義建立及管理屬性集的方法。</span><span class="sxs-lookup"><span data-stu-id="c295e-122">The [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface defines methods that create and manage property sets.</span></span> <span data-ttu-id="c295e-123">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面會直接操控屬性集內的屬性。</span><span class="sxs-lookup"><span data-stu-id="c295e-123">The [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface directly manipulates the properties within a property set.</span></span> <span data-ttu-id="c295e-124">藉由呼叫這些介面的方法，應用程式開發人員可以管理任何適用于指定檔案系統實體的屬性集。</span><span class="sxs-lookup"><span data-stu-id="c295e-124">By calling the methods of these interfaces, an application developer can manage whatever property sets are appropriate for a given file system entity.</span></span> <span data-ttu-id="c295e-125">使用這些介面可為屬性提供一個微調的讀取和寫入執行，而不是在每個應用程式中都有一個執行，例如 incessant 搜尋的效能瓶頸。</span><span class="sxs-lookup"><span data-stu-id="c295e-125">Use of these interfaces provides one tuned reading and writing implementation for properties, rather than having an implementation in each application, where there could be performance bottlenecks such as incessant seeking.</span></span> <span data-ttu-id="c295e-126">您可以執行介面以增強效能，因此可以更快速地讀取和寫入屬性，例如更有效率的快取。</span><span class="sxs-lookup"><span data-stu-id="c295e-126">You can implement the interfaces to enhance performance, so properties can be read and written more quickly by, for example, more efficient caching.</span></span> <span data-ttu-id="c295e-127">此外， **IPropertyStorage** 和 **IPropertySetStorage** 可讓您在不支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的實體上操作屬性，不過一般而言，大部分的應用程式都不會這麼做。</span><span class="sxs-lookup"><span data-stu-id="c295e-127">Furthermore, **IPropertyStorage** and **IPropertySetStorage** make it possible to manipulate properties on entities that do not support [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), although in general, most applications will not do so.</span></span>

<span data-ttu-id="c295e-128">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="c295e-128">This section contains the following topics:</span></span>

-   [<span data-ttu-id="c295e-129">摘要資訊屬性集</span><span class="sxs-lookup"><span data-stu-id="c295e-129">The Summary Information Property Set</span></span>](the-summary-information-property-set.md)
-   [<span data-ttu-id="c295e-130">預先定義的屬性集格式識別碼</span><span class="sxs-lookup"><span data-stu-id="c295e-130">Predefined Property Set Format Identifiers</span></span>](predefined-property-set-format-identifiers.md)
-   [<span data-ttu-id="c295e-131">DocumentSummaryInformation 和使用者設定的屬性集</span><span class="sxs-lookup"><span data-stu-id="c295e-131">The DocumentSummaryInformation and UserDefined Property Sets</span></span>](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a><span data-ttu-id="c295e-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c295e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c295e-133">COM 中的屬性集執行</span><span class="sxs-lookup"><span data-stu-id="c295e-133">Property Set Implementations in COM</span></span>](property-set-implementations-in-com.md)
</dt> <dt>

[<span data-ttu-id="c295e-134">屬性集考慮</span><span class="sxs-lookup"><span data-stu-id="c295e-134">Property Set Considerations</span></span>](property-set-considerations.md)
</dt> <dt>

[<span data-ttu-id="c295e-135">管理屬性</span><span class="sxs-lookup"><span data-stu-id="c295e-135">Managing Properties</span></span>](managing-properties.md)
</dt> <dt>

[<span data-ttu-id="c295e-136">管理屬性集</span><span class="sxs-lookup"><span data-stu-id="c295e-136">Managing Property Sets</span></span>](managing-property-sets.md)
</dt> <dt>

[<span data-ttu-id="c295e-137">儲存屬性集</span><span class="sxs-lookup"><span data-stu-id="c295e-137">Storing Property Sets</span></span>](storing-property-sets.md)
</dt> <dt>

[<span data-ttu-id="c295e-138">效能特色</span><span class="sxs-lookup"><span data-stu-id="c295e-138">Performance Characteristics</span></span>](performance-characteristics.md)
</dt> </dl>

 

 




