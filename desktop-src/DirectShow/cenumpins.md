---
description: CEnumPins 類別會為 pin 實作為列舉值。
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: 'CEnumPins 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994363"
---
# <a name="cenumpins-class"></a><span data-ttu-id="5f5de-103">CEnumPins 類別</span><span class="sxs-lookup"><span data-stu-id="5f5de-103">CEnumPins class</span></span>

![cenumpins 類別階層](images/filter03.png)

<span data-ttu-id="5f5de-105">`CEnumPins`類別會為 pin 實作為列舉值。</span><span class="sxs-lookup"><span data-stu-id="5f5de-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="5f5de-106">這個類別會實 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面。</span><span class="sxs-lookup"><span data-stu-id="5f5de-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="5f5de-107">它會呼叫下列 [**CBaseFilter**](cbasefilter.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="5f5de-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="5f5de-108">[**CBaseFilter：： GetPin**](cbasefilter-getpin.md)：抓取篩選上的釘選，以零為基底的索引參考。</span><span class="sxs-lookup"><span data-stu-id="5f5de-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="5f5de-109">[**CBaseFilter：： GetPinCount**](cbasefilter-getpincount.md)：抓取篩選上的釘選總數。</span><span class="sxs-lookup"><span data-stu-id="5f5de-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="5f5de-110">[**CBaseFilter：： GetPinVersion**](cbasefilter-getpinversion.md)：判斷釘選是否已變更。</span><span class="sxs-lookup"><span data-stu-id="5f5de-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="5f5de-111">如果篩選動態建立或終結 pin，則會在 pin 變更時遞增 pin 版本。</span><span class="sxs-lookup"><span data-stu-id="5f5de-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="5f5de-112">如果版本號碼變更，列舉值物件就不會再與篩選準則同步。</span><span class="sxs-lookup"><span data-stu-id="5f5de-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="5f5de-113">列舉值不同步之後，中的方法會傳回 `CEnumPins` VFW \_ E \_ 列舉不 \_ \_ \_ 同步。</span><span class="sxs-lookup"><span data-stu-id="5f5de-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="5f5de-114">呼叫 [**CEnumPins：： Reset**](cenumpins-reset.md) 方法來重新同步處理列舉值。</span><span class="sxs-lookup"><span data-stu-id="5f5de-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="5f5de-115">公用方法</span><span class="sxs-lookup"><span data-stu-id="5f5de-115">Public Methods</span></span>                             | <span data-ttu-id="5f5de-116">Description</span><span class="sxs-lookup"><span data-stu-id="5f5de-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="5f5de-117">**CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="5f5de-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="5f5de-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="5f5de-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="5f5de-119">**~ CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="5f5de-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="5f5de-120">函式方法。</span><span class="sxs-lookup"><span data-stu-id="5f5de-120">Destructor method.</span></span> <span data-ttu-id="5f5de-121">虛擬。</span><span class="sxs-lookup"><span data-stu-id="5f5de-121">Virtual.</span></span>                                     |
| <span data-ttu-id="5f5de-122">IEnumPins 方法</span><span class="sxs-lookup"><span data-stu-id="5f5de-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="5f5de-123">Description</span><span class="sxs-lookup"><span data-stu-id="5f5de-123">Description</span></span>                                                     |
| [<span data-ttu-id="5f5de-124">**克隆**</span><span class="sxs-lookup"><span data-stu-id="5f5de-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="5f5de-125">使用相同的列舉狀態建立列舉值的複本。</span><span class="sxs-lookup"><span data-stu-id="5f5de-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="5f5de-126">**下一步**</span><span class="sxs-lookup"><span data-stu-id="5f5de-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="5f5de-127">抓取指定的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="5f5de-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="5f5de-128">**重設**</span><span class="sxs-lookup"><span data-stu-id="5f5de-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="5f5de-129">將列舉序列重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="5f5de-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="5f5de-130">**跳過**</span><span class="sxs-lookup"><span data-stu-id="5f5de-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="5f5de-131">略過指定的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="5f5de-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="5f5de-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f5de-132">Requirements</span></span>



| <span data-ttu-id="5f5de-133">需求</span><span class="sxs-lookup"><span data-stu-id="5f5de-133">Requirement</span></span> | <span data-ttu-id="5f5de-134">值</span><span class="sxs-lookup"><span data-stu-id="5f5de-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5de-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5f5de-135">Header</span></span><br/>  | <dl> <span data-ttu-id="5f5de-136"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5f5de-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f5de-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f5de-137">Library</span></span><br/> | <dl> <span data-ttu-id="5f5de-138"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5f5de-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




