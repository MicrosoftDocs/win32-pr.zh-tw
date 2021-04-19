---
description: CTransInPlaceOutputPin 類別會實 CTransInPlaceFilter 類別所使用的輸出圖釘。
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: 'CTransInPlaceOutputPin 類別 (Transip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990040"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="dfa4e-103">CTransInPlaceOutputPin 類別</span><span class="sxs-lookup"><span data-stu-id="dfa4e-103">CTransInPlaceOutputPin class</span></span>

![ctransinplaceoutputpin 類別階層](images/tsip02.png)

<span data-ttu-id="dfa4e-105">`CTransInPlaceOutputPin`類別會實 [**CTransInPlaceFilter**](ctransinplacefilter.md)類別所使用的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="dfa4e-106">一般而言，您不需要從此類別衍生。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="dfa4e-107">如果您這麼做，就必須覆寫篩選的 [**CTransInPlaceFilter：： GetPin**](ctransinplacefilter-getpin.md) 方法，以建立衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="dfa4e-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="dfa4e-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="dfa4e-109">Description</span><span class="sxs-lookup"><span data-stu-id="dfa4e-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="dfa4e-110">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="dfa4e-111">建立此釘選之篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="dfa4e-112">公用方法</span><span class="sxs-lookup"><span data-stu-id="dfa4e-112">Public Methods</span></span>                                                                  | <span data-ttu-id="dfa4e-113">Description</span><span class="sxs-lookup"><span data-stu-id="dfa4e-113">Description</span></span>                                          |
| [<span data-ttu-id="dfa4e-114">**CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="dfa4e-115">函式方法。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="dfa4e-116">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="dfa4e-117">判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="dfa4e-118">**SetAllocator**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="dfa4e-119">指定連接的配置器。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="dfa4e-120">**ConnectedIMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="dfa4e-121">抓取下游輸入圖釘的指標。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="dfa4e-122">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="dfa4e-123">捕獲釘選配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="dfa4e-124">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="dfa4e-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="dfa4e-125">Description</span><span class="sxs-lookup"><span data-stu-id="dfa4e-125">Description</span></span>                                          |
| [<span data-ttu-id="dfa4e-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="dfa4e-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="dfa4e-127">列舉釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="dfa4e-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="dfa4e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfa4e-128">Requirements</span></span>



| <span data-ttu-id="dfa4e-129">需求</span><span class="sxs-lookup"><span data-stu-id="dfa4e-129">Requirement</span></span> | <span data-ttu-id="dfa4e-130">值</span><span class="sxs-lookup"><span data-stu-id="dfa4e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa4e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="dfa4e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="dfa4e-132"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dfa4e-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dfa4e-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="dfa4e-133">Library</span></span><br/> | <dl> <span data-ttu-id="dfa4e-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dfa4e-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




