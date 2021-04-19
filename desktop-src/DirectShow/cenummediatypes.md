---
description: CEnumMediaTypes 類別會實作為慣用媒體類型的列舉值。
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: 'CEnumMediaTypes 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990065"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="c40de-103">CEnumMediaTypes 類別</span><span class="sxs-lookup"><span data-stu-id="c40de-103">CEnumMediaTypes class</span></span>

![cenummediatypes 類別階層](images/filter04.png)

<span data-ttu-id="c40de-105">類別會實 `CEnumMediaTypes` 作為慣用媒體類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="c40de-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="c40de-106">這個類別會實 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面。</span><span class="sxs-lookup"><span data-stu-id="c40de-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="c40de-107">它會呼叫下列 [**CBasePin**](cbasepin.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="c40de-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="c40de-108">[**CBasePin：： GetMediaType**](cbasepin-getmediatype.md)：抓取以零為基底之索引所參考的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c40de-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="c40de-109">[**CBasePin：： GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)：判斷慣用類型集合是否已變更。</span><span class="sxs-lookup"><span data-stu-id="c40de-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="c40de-110">只要 pin 改變其慣用媒體類型的清單，pin 就會遞增媒體類型的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c40de-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="c40de-111">當這種情況發生時，列舉值物件就不會再與釘選同步，而類別方法會傳回 VFW \_ E \_ 列舉不 \_ \_ \_ 同步。</span><span class="sxs-lookup"><span data-stu-id="c40de-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="c40de-112">呼叫 [**CEnumMediaTypes：： Reset**](cenummediatypes-reset.md) 方法來重新同步處理列舉值。</span><span class="sxs-lookup"><span data-stu-id="c40de-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="c40de-113">公用方法</span><span class="sxs-lookup"><span data-stu-id="c40de-113">Public Methods</span></span>                                               | <span data-ttu-id="c40de-114">Description</span><span class="sxs-lookup"><span data-stu-id="c40de-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="c40de-115">**CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="c40de-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="c40de-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="c40de-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="c40de-117">**~ CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="c40de-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="c40de-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="c40de-118">Destructor method.</span></span> <span data-ttu-id="c40de-119">虛擬。</span><span class="sxs-lookup"><span data-stu-id="c40de-119">Virtual.</span></span>                                     |
| <span data-ttu-id="c40de-120">IEnumMediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="c40de-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="c40de-121">Description</span><span class="sxs-lookup"><span data-stu-id="c40de-121">Description</span></span>                                                     |
| [<span data-ttu-id="c40de-122">**克隆**</span><span class="sxs-lookup"><span data-stu-id="c40de-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="c40de-123">使用相同的列舉狀態建立列舉值的複本。</span><span class="sxs-lookup"><span data-stu-id="c40de-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="c40de-124">**下一步**</span><span class="sxs-lookup"><span data-stu-id="c40de-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="c40de-125">抓取指定的媒體類型數目。</span><span class="sxs-lookup"><span data-stu-id="c40de-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="c40de-126">**重設**</span><span class="sxs-lookup"><span data-stu-id="c40de-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="c40de-127">將列舉序列重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="c40de-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="c40de-128">**跳過**</span><span class="sxs-lookup"><span data-stu-id="c40de-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="c40de-129">略過指定數目的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c40de-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="c40de-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c40de-130">Requirements</span></span>



| <span data-ttu-id="c40de-131">需求</span><span class="sxs-lookup"><span data-stu-id="c40de-131">Requirement</span></span> | <span data-ttu-id="c40de-132">值</span><span class="sxs-lookup"><span data-stu-id="c40de-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40de-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c40de-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c40de-134"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c40de-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c40de-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="c40de-135">Library</span></span><br/> | <dl> <span data-ttu-id="c40de-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c40de-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




