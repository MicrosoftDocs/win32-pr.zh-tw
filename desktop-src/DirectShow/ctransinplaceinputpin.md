---
description: CTransInPlaceInputPin 類別會實 CTransInPlaceFilter 類別所使用的輸入 pin。
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: 'CTransInPlaceInputPin 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998751"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="e55d4-103">CTransInPlaceInputPin 類別</span><span class="sxs-lookup"><span data-stu-id="e55d4-103">CTransInPlaceInputPin class</span></span>

![ctransinplaceinputpin 類別階層](images/tsip01.png)

<span data-ttu-id="e55d4-105">`CTransInPlaceInputPin`類別會實 [**CTransInPlaceFilter**](ctransinplacefilter.md)類別所使用的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="e55d4-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="e55d4-106">一般而言，您不需要從此類別衍生。</span><span class="sxs-lookup"><span data-stu-id="e55d4-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="e55d4-107">如果您這麼做，就必須覆寫篩選的 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法，以建立衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e55d4-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="e55d4-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="e55d4-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="e55d4-109">Description</span><span class="sxs-lookup"><span data-stu-id="e55d4-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="e55d4-110">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="e55d4-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="e55d4-111">指定輸入資料流程是否為唯讀的旗標。</span><span class="sxs-lookup"><span data-stu-id="e55d4-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="e55d4-112">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="e55d4-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="e55d4-113">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="e55d4-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="e55d4-114">公用方法</span><span class="sxs-lookup"><span data-stu-id="e55d4-114">Public Methods</span></span>                                                                      | <span data-ttu-id="e55d4-115">Description</span><span class="sxs-lookup"><span data-stu-id="e55d4-115">Description</span></span>                                                |
| [<span data-ttu-id="e55d4-116">**CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="e55d4-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="e55d4-117">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e55d4-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="e55d4-118">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e55d4-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="e55d4-119">判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e55d4-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="e55d4-120">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="e55d4-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="e55d4-121">捕獲釘選配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="e55d4-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="e55d4-122">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="e55d4-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="e55d4-123">指出輸入資料流程是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="e55d4-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="e55d4-124">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="e55d4-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="e55d4-125">Description</span><span class="sxs-lookup"><span data-stu-id="e55d4-125">Description</span></span>                                                |
| [<span data-ttu-id="e55d4-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e55d4-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="e55d4-127">列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e55d4-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="e55d4-128">IMemInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="e55d4-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="e55d4-129">Description</span><span class="sxs-lookup"><span data-stu-id="e55d4-129">Description</span></span>                                                |
| [<span data-ttu-id="e55d4-130">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="e55d4-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="e55d4-131">抓取此 pin 提議的記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="e55d4-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="e55d4-132">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="e55d4-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="e55d4-133">指定連接的配置器。</span><span class="sxs-lookup"><span data-stu-id="e55d4-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="e55d4-134">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="e55d4-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="e55d4-135">抓取 pin 所要求的配置器屬性。</span><span class="sxs-lookup"><span data-stu-id="e55d4-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e55d4-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e55d4-136">Requirements</span></span>



| <span data-ttu-id="e55d4-137">需求</span><span class="sxs-lookup"><span data-stu-id="e55d4-137">Requirement</span></span> | <span data-ttu-id="e55d4-138">值</span><span class="sxs-lookup"><span data-stu-id="e55d4-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55d4-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e55d4-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e55d4-140"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e55d4-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e55d4-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="e55d4-141">Library</span></span><br/> | <dl> <span data-ttu-id="e55d4-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e55d4-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




