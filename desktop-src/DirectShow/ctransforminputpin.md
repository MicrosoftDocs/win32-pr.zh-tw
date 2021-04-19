---
description: CTransformInputPin 類別會實 CTransformFilter 類別所使用的輸入 pin。
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: 'CTransformInputPin 類別 (Transfrm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996501"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="e295c-103">CTransformInputPin 類別</span><span class="sxs-lookup"><span data-stu-id="e295c-103">CTransformInputPin class</span></span>

![ctransforminputpin 類別階層](images/tfrm01.png)

<span data-ttu-id="e295c-105">`CTransformInputPin`類別會實 [**CTransformFilter**](ctransformfilter.md)類別所使用的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="e295c-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="e295c-106">一般而言，您不需要從此類別衍生。</span><span class="sxs-lookup"><span data-stu-id="e295c-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="e295c-107">此類別中大部分的方法會呼叫 **CTransformFilter** 類別上的對應方法，而您可以覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e295c-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="e295c-108">如果您衍生自這個類別，您必須覆寫篩選的 [**CTransformFilter：： GetPin**](ctransformfilter-getpin.md) 方法，以建立衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e295c-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="e295c-109">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="e295c-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="e295c-110">Description</span><span class="sxs-lookup"><span data-stu-id="e295c-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e295c-111">**m \_ pTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e295c-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="e295c-112">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="e295c-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="e295c-113">公用方法</span><span class="sxs-lookup"><span data-stu-id="e295c-113">Public Methods</span></span>                                                       | <span data-ttu-id="e295c-114">Description</span><span class="sxs-lookup"><span data-stu-id="e295c-114">Description</span></span>                                                                            |
| [<span data-ttu-id="e295c-115">**CTransformInputPin**</span><span class="sxs-lookup"><span data-stu-id="e295c-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="e295c-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e295c-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="e295c-117">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="e295c-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="e295c-118">判斷 pin 連接是否合適。</span><span class="sxs-lookup"><span data-stu-id="e295c-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="e295c-119">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="e295c-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="e295c-120">釋放連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="e295c-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="e295c-121">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="e295c-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="e295c-122">完成與另一個 pin 的連接。</span><span class="sxs-lookup"><span data-stu-id="e295c-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="e295c-123">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e295c-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="e295c-124">判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e295c-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="e295c-125">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="e295c-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="e295c-126">設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e295c-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="e295c-127">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="e295c-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="e295c-128">判斷 pin 是否可以接受範例。</span><span class="sxs-lookup"><span data-stu-id="e295c-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="e295c-129">虛擬。</span><span class="sxs-lookup"><span data-stu-id="e295c-129">Virtual.</span></span>                                |
| [<span data-ttu-id="e295c-130">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="e295c-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="e295c-131">抓取目前 pin 連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e295c-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="e295c-132">IPin 方法</span><span class="sxs-lookup"><span data-stu-id="e295c-132">IPin Methods</span></span>                                                         | <span data-ttu-id="e295c-133">Description</span><span class="sxs-lookup"><span data-stu-id="e295c-133">Description</span></span>                                                                            |
| [<span data-ttu-id="e295c-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="e295c-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="e295c-135">抓取 pin 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e295c-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="e295c-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="e295c-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="e295c-137">通知 pin，不需要額外的資料。</span><span class="sxs-lookup"><span data-stu-id="e295c-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="e295c-138">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="e295c-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="e295c-139">開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="e295c-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="e295c-140">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="e295c-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="e295c-141">結束清除操作。</span><span class="sxs-lookup"><span data-stu-id="e295c-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="e295c-142">**NewSegment**</span><span class="sxs-lookup"><span data-stu-id="e295c-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="e295c-143">通知釘選將此呼叫群組為區段之後所收到的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="e295c-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="e295c-144">IMemInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="e295c-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="e295c-145">Description</span><span class="sxs-lookup"><span data-stu-id="e295c-145">Description</span></span>                                                                            |
| [<span data-ttu-id="e295c-146">**收到**</span><span class="sxs-lookup"><span data-stu-id="e295c-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="e295c-147">接收資料流程中的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="e295c-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="e295c-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="e295c-148">Requirements</span></span>



| <span data-ttu-id="e295c-149">需求</span><span class="sxs-lookup"><span data-stu-id="e295c-149">Requirement</span></span> | <span data-ttu-id="e295c-150">值</span><span class="sxs-lookup"><span data-stu-id="e295c-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e295c-151">標頭</span><span class="sxs-lookup"><span data-stu-id="e295c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e295c-152"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e295c-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e295c-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="e295c-153">Library</span></span><br/> | <dl> <span data-ttu-id="e295c-154"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e295c-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




