---
description: DoBufferProcessingLoop 方法會產生媒體資料，並將其傳遞至下游輸入 pin。
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: 'CSourceStream. DoBufferProcessingLoop 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983088"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="6eb78-103">CSourceStream. DoBufferProcessingLoop 方法</span><span class="sxs-lookup"><span data-stu-id="6eb78-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="6eb78-104">`DoBufferProcessingLoop`方法會產生媒體資料，並將其傳遞至下游輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="6eb78-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb78-105">語法</span><span class="sxs-lookup"><span data-stu-id="6eb78-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="6eb78-106">參數</span><span class="sxs-lookup"><span data-stu-id="6eb78-106">Parameters</span></span>

<span data-ttu-id="6eb78-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6eb78-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6eb78-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eb78-108">Return value</span></span>

<span data-ttu-id="6eb78-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6eb78-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6eb78-110">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="6eb78-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6eb78-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6eb78-111">Return code</span></span>                                                                             | <span data-ttu-id="6eb78-112">Description</span><span class="sxs-lookup"><span data-stu-id="6eb78-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6eb78-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6eb78-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6eb78-114">執行緒收到停止要求。</span><span class="sxs-lookup"><span data-stu-id="6eb78-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="6eb78-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6eb78-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6eb78-116">資料流程已結束，或下游篩選不接受範例。</span><span class="sxs-lookup"><span data-stu-id="6eb78-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6eb78-117">備註</span><span class="sxs-lookup"><span data-stu-id="6eb78-117">Remarks</span></span>

<span data-ttu-id="6eb78-118">這個方法會實處理資料並將它傳遞給下游的主要迴圈。</span><span class="sxs-lookup"><span data-stu-id="6eb78-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="6eb78-119">每次通過迴圈時，方法都會從配置器取出空白媒體範例。</span><span class="sxs-lookup"><span data-stu-id="6eb78-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="6eb78-120">它會將範例傳遞給 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6eb78-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="6eb78-121">衍生類別必須執行的 **FillBuffer** 方法會產生媒體資料，並將它放在範例緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="6eb78-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="6eb78-122">當發生下列任何情況時，迴圈就會結束：</span><span class="sxs-lookup"><span data-stu-id="6eb78-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="6eb78-123">輸入 pin 的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法會拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="6eb78-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="6eb78-124">**FillBuffer** 方法會傳回 \_ FALSE，表示資料流程的結尾，或傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6eb78-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="6eb78-125">執行緒收到 [**CSourceStream：： Stop**](csourcestream-stop.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="6eb78-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="6eb78-126">`DoBufferProcessingLoop`方法會處理結束資料流程的通知。</span><span class="sxs-lookup"><span data-stu-id="6eb78-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="6eb78-127">如果發生錯誤，它會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="6eb78-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb78-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eb78-128">Requirements</span></span>



| <span data-ttu-id="6eb78-129">需求</span><span class="sxs-lookup"><span data-stu-id="6eb78-129">Requirement</span></span> | <span data-ttu-id="6eb78-130">值</span><span class="sxs-lookup"><span data-stu-id="6eb78-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb78-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6eb78-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb78-132"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="6eb78-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6eb78-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="6eb78-133">Library</span></span><br/> | <dl> <span data-ttu-id="6eb78-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6eb78-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb78-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eb78-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb78-136">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="6eb78-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




