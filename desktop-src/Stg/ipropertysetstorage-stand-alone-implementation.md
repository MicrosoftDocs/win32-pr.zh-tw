---
title: IPropertySetStorage-獨立執行
description: 系統提供的 IPropertySetStorage 獨立執行包括 IPropertyStorage 和 IPropertySetStorage 的實作為。
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd Stg.，實施
- IPropertySetStorage Strctd Stg.，獨立部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023583"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="4b5e6-105">IPropertySetStorage-獨立執行</span><span class="sxs-lookup"><span data-stu-id="4b5e6-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="4b5e6-106">系統提供的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 獨立執行包括 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 和 **IPropertySetStorage** 的實作為。[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 是在屬性集儲存體中讀取和寫入屬性的介面。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="4b5e6-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 是在儲存體中建立和開啟屬性集的介面。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="4b5e6-108">[**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)和 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面也會在獨立的執行中提供。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="4b5e6-109">若要使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的獨立執行，請先取得系統提供的獨立執行的指標，並將系統提供的實作為您的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="4b5e6-110">若要取得 **IPropertySetStorage** 之獨立執行的指標，請呼叫 [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) 函數，並提供 *pStorage* 參數，以指定將包含屬性集的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="4b5e6-111">這個函式會為指定的儲存物件提供新 **IPropertySetStorage** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="4b5e6-112">獨立的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 執行會在任何儲存物件上建立屬性集，而不只是在複合檔案儲存體上建立。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="4b5e6-113">獨立的執行不相依于複合檔案，並且可搭配任何結構化儲存體的執行使用。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="4b5e6-114">呼叫端提供的結構化儲存體有任何限制適用于這個屬性集的執行。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="4b5e6-115">例如，如果您提供簡單模式的儲存體給 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)，所產生的 **IPropertySetStorage** 將會受到所提供 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的限制。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="4b5e6-116">如需此介面之複合檔案執行的詳細資訊，請參閱 [IPropertySetStorage-複合檔案執行](ipropertysetstorage-compound-file-implementation.md)一節。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4b5e6-117">使用時機</span><span class="sxs-lookup"><span data-stu-id="4b5e6-117">When to Use</span></span>

<span data-ttu-id="4b5e6-118">呼叫 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 的方法，以建立、開啟及刪除任何結構化儲存體中的屬性集。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="4b5e6-119">另外還有一種方法，它會提供指向 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 列舉值的指標，可用來列舉儲存區中的屬性集。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="4b5e6-120">獨立的執行也會提供 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 和 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper 函式（除了 [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 和 [**open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) 方法），以建立和開啟屬性集。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="4b5e6-121">這兩個函式會新增 PROPSETFLAG \_ 無緩衝值的支援，讓您可以直接將變更寫入屬性集，而不是在快取中緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="4b5e6-122">如需詳細資訊，請參閱 [**PROPSETFLAG 常數**](propsetflag-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="4b5e6-123">方法</span><span class="sxs-lookup"><span data-stu-id="4b5e6-123">Methods</span></span>

<span data-ttu-id="4b5e6-124">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)的獨立執行支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="4b5e6-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="4b5e6-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="4b5e6-126">在儲存體中建立新的屬性集，並將指標傳回屬性集上的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="4b5e6-127">如果您打算使用 PROPSETFLAG \_ 無緩衝的值，請改用 [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) 函式來建立並開啟新的屬性集，並在屬性集上取得 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面之獨立執行的指標。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="4b5e6-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage：： Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="4b5e6-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="4b5e6-129">在儲存體中開啟現有的屬性集，並將指標傳回屬性集上的 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="4b5e6-130">如果您打算使用 PROPSETFLAG \_ 無緩衝的值，請改用 [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) 函式來取得指定之屬性集上 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 獨立執行的指標。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="4b5e6-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage：:D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="4b5e6-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="4b5e6-132">刪除這個屬性集儲存體中設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="4b5e6-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="4b5e6-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="4b5e6-134">建立可用於列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構的物件。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="4b5e6-135">每個 **STATPROPSETSTG** 結構都會提供單一屬性集的相關資料。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="4b5e6-136">DocumentSummaryInformation 和使用者設定的屬性集是唯一的，因為它在單一基礎資料流程中可能有兩個屬性集區段。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="4b5e6-137">如需詳細資訊，請參閱 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md) 。</span><span class="sxs-lookup"><span data-stu-id="4b5e6-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4b5e6-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b5e6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b5e6-139">IPropertyStorage-獨立執行</span><span class="sxs-lookup"><span data-stu-id="4b5e6-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="4b5e6-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="4b5e6-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="4b5e6-142">**IStorage：： EnumElements**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="4b5e6-143">**PROPSETFLAG 常數**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="4b5e6-144">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="4b5e6-145">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="4b5e6-146">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="4b5e6-147">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="4b5e6-148">**STGM 常數**</span><span class="sxs-lookup"><span data-stu-id="4b5e6-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 