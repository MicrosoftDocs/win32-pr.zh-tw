---
description: CTransformOutputPin 類別會實 CTransformFilter 類別所使用的輸出圖釘。
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: 'CTransformOutputPin 類別 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993650"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="df1fe-103">CTransformOutputPin 類別</span><span class="sxs-lookup"><span data-stu-id="df1fe-103">CTransformOutputPin class</span></span>

![ctransformoutputpin 類別階層](images/tfrm02.png)

<span data-ttu-id="df1fe-105">`CTransformOutputPin`類別會實 [**CTransformFilter**](ctransformfilter.md)類別所使用的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="df1fe-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="df1fe-106">一般而言，您不需要從此類別衍生。</span><span class="sxs-lookup"><span data-stu-id="df1fe-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="df1fe-107">此類別中大部分的方法會呼叫 **CTransformFilter** 類別上的對應方法，而您可以覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="df1fe-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="df1fe-108">如果您衍生自這個類別，您必須覆寫篩選的 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法，以建立衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="df1fe-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="df1fe-109">這個類別會透過 [**CPosPassThru**](cpospassthru.md)物件公開 **IMediaSeeking** 和 **IMediaPosition** 介面。</span><span class="sxs-lookup"><span data-stu-id="df1fe-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="df1fe-110">它會將所有搜尋要求傳遞至下一個篩選上游。</span><span class="sxs-lookup"><span data-stu-id="df1fe-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="df1fe-111">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="df1fe-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="df1fe-112">Description</span><span class="sxs-lookup"><span data-stu-id="df1fe-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="df1fe-113">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="df1fe-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="df1fe-114">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="df1fe-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="df1fe-115">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="df1fe-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="df1fe-116">Description</span><span class="sxs-lookup"><span data-stu-id="df1fe-116">Description</span></span>                                              |
| [<span data-ttu-id="df1fe-117">**m \_ pPosition**</span><span class="sxs-lookup"><span data-stu-id="df1fe-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="df1fe-118">要傳遞向上游傳遞搜尋命令的 Helper 物件。</span><span class="sxs-lookup"><span data-stu-id="df1fe-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="df1fe-119">公用方法</span><span class="sxs-lookup"><span data-stu-id="df1fe-119">Public Methods</span></span>                                                           | <span data-ttu-id="df1fe-120">Description</span><span class="sxs-lookup"><span data-stu-id="df1fe-120">Description</span></span>                                              |
| [<span data-ttu-id="df1fe-121">**CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="df1fe-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="df1fe-122">函式方法。</span><span class="sxs-lookup"><span data-stu-id="df1fe-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="df1fe-123">**~ CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="df1fe-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="df1fe-124">函式方法。</span><span class="sxs-lookup"><span data-stu-id="df1fe-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="df1fe-125">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="df1fe-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="df1fe-126">判斷 pin 連接是否合適。</span><span class="sxs-lookup"><span data-stu-id="df1fe-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="df1fe-127">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="df1fe-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="df1fe-128">釋放連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="df1fe-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="df1fe-129">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="df1fe-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="df1fe-130">完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="df1fe-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="df1fe-131">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="df1fe-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="df1fe-132">判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="df1fe-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="df1fe-133">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="df1fe-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="df1fe-134">設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="df1fe-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="df1fe-135">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="df1fe-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="df1fe-136">設定緩衝區需求。</span><span class="sxs-lookup"><span data-stu-id="df1fe-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="df1fe-137">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="df1fe-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="df1fe-138">依索引值抓取慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="df1fe-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="df1fe-139">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="df1fe-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="df1fe-140">抓取目前 pin 連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="df1fe-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="df1fe-141">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="df1fe-141">IPin Methods</span></span>                                                             | <span data-ttu-id="df1fe-142">Description</span><span class="sxs-lookup"><span data-stu-id="df1fe-142">Description</span></span>                                              |
| [<span data-ttu-id="df1fe-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="df1fe-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="df1fe-144">抓取 pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="df1fe-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="df1fe-145">IQualityControl 方法</span><span class="sxs-lookup"><span data-stu-id="df1fe-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="df1fe-146">Description</span><span class="sxs-lookup"><span data-stu-id="df1fe-146">Description</span></span>                                              |
| [<span data-ttu-id="df1fe-147">**Notify**</span><span class="sxs-lookup"><span data-stu-id="df1fe-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="df1fe-148">通知 pin 已要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="df1fe-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="df1fe-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="df1fe-149">Requirements</span></span>



| <span data-ttu-id="df1fe-150">需求</span><span class="sxs-lookup"><span data-stu-id="df1fe-150">Requirement</span></span> | <span data-ttu-id="df1fe-151">值</span><span class="sxs-lookup"><span data-stu-id="df1fe-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df1fe-152">標頭</span><span class="sxs-lookup"><span data-stu-id="df1fe-152">Header</span></span><br/>  | <dl> <span data-ttu-id="df1fe-153"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="df1fe-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="df1fe-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="df1fe-154">Library</span></span><br/> | <dl> <span data-ttu-id="df1fe-155"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="df1fe-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




