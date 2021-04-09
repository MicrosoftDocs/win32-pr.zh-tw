---
title: COM 中的屬性集執行
description: COM 中的屬性集執行
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- 結構化儲存體 Strctd Stg.，使用屬性集在 COM 中使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933341"
---
# <a name="property-set-implementations-in-com"></a><span data-ttu-id="f960c-104">COM 中的屬性集執行</span><span class="sxs-lookup"><span data-stu-id="f960c-104">Property Set Implementations in COM</span></span>

<span data-ttu-id="f960c-105">雖然不會完全使用持續性屬性集的可能性，但目前有兩個主要用途：</span><span class="sxs-lookup"><span data-stu-id="f960c-105">While the potential for uses of persistent property sets is not fully tapped, there are currently two primary uses:</span></span>

-   <span data-ttu-id="f960c-106">使用檔等物件儲存摘要資訊</span><span class="sxs-lookup"><span data-stu-id="f960c-106">Storing summary information with an object such as a document</span></span>
-   <span data-ttu-id="f960c-107">傳送物件之間的屬性資料</span><span class="sxs-lookup"><span data-stu-id="f960c-107">Transferring property data between objects</span></span>

<span data-ttu-id="f960c-108">COM 屬性集的設計目的，是要將適合表示的資料儲存為較精細值的中等大小集合。</span><span class="sxs-lookup"><span data-stu-id="f960c-108">COM property sets were designed to store data that is suited to representation as a moderately sized collection of fine-grained values.</span></span> <span data-ttu-id="f960c-109">如果資料集太大而無法執行，則應該將它們分成不同的資料流程、儲存體及/或屬性集。</span><span class="sxs-lookup"><span data-stu-id="f960c-109">Data sets that are too large for this to be feasible should be broken into separate streams, storages, and/or property sets.</span></span> <span data-ttu-id="f960c-110">COM 屬性集資料格式並非用來提供許多小型物件的資料庫替代。</span><span class="sxs-lookup"><span data-stu-id="f960c-110">The COM property set data format was not meant to provide a substitute for a database of many tiny objects.</span></span>

<span data-ttu-id="f960c-111">COM 提供各種物件的屬性集介面，以及三個 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="f960c-111">COM provides implementations of the property set interfaces for various objects, along with three helper functions.</span></span> <span data-ttu-id="f960c-112">下一節將說明這些執行的一些效能特性。</span><span class="sxs-lookup"><span data-stu-id="f960c-112">The following section describes some performance characteristics of these implementations.</span></span> <span data-ttu-id="f960c-113">如需特定介面的詳細資訊，以及如何取得這些介面的指標，請參閱 COM 參考一節中的下列內容：</span><span class="sxs-lookup"><span data-stu-id="f960c-113">For more information on specific interfaces and how to get a pointer to these interfaces, refer to the following in the COM reference section:</span></span>

-   [<span data-ttu-id="f960c-114">IPropertySetStorage –複合檔案執行</span><span class="sxs-lookup"><span data-stu-id="f960c-114">IPropertySetStorage–Compound File Implementation</span></span>](ipropertysetstorage-compound-file-implementation.md)

    <span data-ttu-id="f960c-115">複合檔案的實作為提供 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面，也提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="f960c-115">The compound file implementation, which provides the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interfaces, also provides the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces.</span></span> <span data-ttu-id="f960c-116">由於 **IStorage** 的複合檔案執行， **IPropertySetStorage** 介面可透過呼叫 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得。</span><span class="sxs-lookup"><span data-stu-id="f960c-116">Given a compound file implementation of **IStorage**, the **IPropertySetStorage** interface can be obtained by calling [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span>

-   [<span data-ttu-id="f960c-117">IPropertySetStorage – NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="f960c-117">IPropertySetStorage–NTFS File System Implementation</span></span>](ipropertysetstorage-ntfs-file-system-implementation.md)

    <span data-ttu-id="f960c-118">您也可以針對非複合檔案的 NTFS 檔案取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="f960c-118">The [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces can also be obtained for NTFS files that are not compound files.</span></span> <span data-ttu-id="f960c-119">因此，您可以針對 NTFS 磁片區上的所有檔案取得這些介面。</span><span class="sxs-lookup"><span data-stu-id="f960c-119">Therefore, it is possible to obtain these interfaces for all files on an NTFS volume.</span></span>

-   [<span data-ttu-id="f960c-120">IPropertySetStorage –獨立執行</span><span class="sxs-lookup"><span data-stu-id="f960c-120">IPropertySetStorage–Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)

    <span data-ttu-id="f960c-121">當 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的這個執行具現化時，它會獲得支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f960c-121">When this implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is instantiated, it is given a pointer to an object that supports the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="f960c-122">然後，它會在該儲存物件內操作屬性集的儲存。</span><span class="sxs-lookup"><span data-stu-id="f960c-122">It then manipulates property set storages within that storage object.</span></span> <span data-ttu-id="f960c-123">因此，可以存取和操作任何支援之物件上的屬性集。</span><span class="sxs-lookup"><span data-stu-id="f960c-123">Thus, it is possible to access and manipulate property sets on any object that supports .</span></span>

-   [<span data-ttu-id="f960c-124">IPropertySetStorage 實行考慮</span><span class="sxs-lookup"><span data-stu-id="f960c-124">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)

    <span data-ttu-id="f960c-125">提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行時，需要考慮幾個問題。</span><span class="sxs-lookup"><span data-stu-id="f960c-125">There are several issues to consider in providing an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="f960c-126">請參閱 COM 參考一節中的這些 *執行考慮* 。</span><span class="sxs-lookup"><span data-stu-id="f960c-126">Please refer to these *Implementation Considerations* in the COM Reference section.</span></span>

<span data-ttu-id="f960c-127">此外，還有四個 helper 函式，其設計目的是為了協助處理已從屬性集中讀取的屬性， (為 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構) ：</span><span class="sxs-lookup"><span data-stu-id="f960c-127">In addition, there are four helper functions, designed to aid in dealing with properties that have been read from a property set into memory (into a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure):</span></span>

-   [<span data-ttu-id="f960c-128">**PropVariantInit**</span><span class="sxs-lookup"><span data-stu-id="f960c-128">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="f960c-129">**PropVariantClear**</span><span class="sxs-lookup"><span data-stu-id="f960c-129">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="f960c-130">**FreePropVariantArray**</span><span class="sxs-lookup"><span data-stu-id="f960c-130">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="f960c-131">**PropVariantCopy**</span><span class="sxs-lookup"><span data-stu-id="f960c-131">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

<span data-ttu-id="f960c-132">下列各節會更詳細地討論 COM 中的屬性集執行：</span><span class="sxs-lookup"><span data-stu-id="f960c-132">The following sections discuss property set implementations in COM in greater detail:</span></span>

-   [<span data-ttu-id="f960c-133">管理屬性集</span><span class="sxs-lookup"><span data-stu-id="f960c-133">Managing Property Sets</span></span>](managing-property-sets.md)
-   [<span data-ttu-id="f960c-134">屬性集考慮</span><span class="sxs-lookup"><span data-stu-id="f960c-134">Property Set Considerations</span></span>](property-set-considerations.md)
-   [<span data-ttu-id="f960c-135">儲存屬性集</span><span class="sxs-lookup"><span data-stu-id="f960c-135">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="f960c-136">效能特色</span><span class="sxs-lookup"><span data-stu-id="f960c-136">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="f960c-137">執行摘要資訊屬性集</span><span class="sxs-lookup"><span data-stu-id="f960c-137">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)
-   [<span data-ttu-id="f960c-138">IPropertySetStorage 實行考慮</span><span class="sxs-lookup"><span data-stu-id="f960c-138">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)

 

 