---
description: CheckStreamState 方法會判斷是否應該傳遞或捨棄媒體範例。
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: 'CBaseStreamControl. CheckStreamState 方法 (Strmctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000742"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="8e5cd-103">CBaseStreamControl. CheckStreamState 方法</span><span class="sxs-lookup"><span data-stu-id="8e5cd-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="8e5cd-104">`CheckStreamState`方法會判斷是否應該傳遞或捨棄媒體範例。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e5cd-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="8e5cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5cd-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="8e5cd-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8e5cd-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5cd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e5cd-109">Return value</span></span>

<span data-ttu-id="8e5cd-110">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-110">Returns one of the following values.</span></span>



| <span data-ttu-id="8e5cd-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8e5cd-111">Return code</span></span>                                                                                       | <span data-ttu-id="8e5cd-112">Description</span><span class="sxs-lookup"><span data-stu-id="8e5cd-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="8e5cd-113"><dt>**資料流程 \_ 捨棄**</dt></span><span class="sxs-lookup"><span data-stu-id="8e5cd-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="8e5cd-114">捨棄此範例。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="8e5cd-115"><dt>**串流 \_ 流動**</dt></span><span class="sxs-lookup"><span data-stu-id="8e5cd-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="8e5cd-116">傳遞此範例。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8e5cd-117">備註</span><span class="sxs-lookup"><span data-stu-id="8e5cd-117">Remarks</span></span>

<span data-ttu-id="8e5cd-118">當您的 pin 收到範例時，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="8e5cd-119">只有在傳回值為數據流流動時，才傳遞範例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="8e5cd-120">如果傳回值為數據流 \_ 捨棄，請捨棄範例。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="8e5cd-121">如果 pin 捨棄任何範例，則會呼叫 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法，將它所提供的下一個範例標示為不連續。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="8e5cd-122">如果您的篩選準則會執行 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) 介面，以計算所捨棄的畫面格數目，請勿將捨棄的框架計算為已卸載的框架。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="8e5cd-123">當傳回值為數據流 \_ 捨棄時，方法會封鎖，直到參考時間到達樣本的開始時間。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="8e5cd-124">這可防止您的 pin 太快捨棄樣本。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="8e5cd-125">如果已暫停篩選，則等候時間是無限的，直到篩選執行、停止或清除資料為止。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="8e5cd-126"> (篩選狀態變更和串流處理會在個別的執行緒上執行，因此不會造成任何鎖死。 ) </span><span class="sxs-lookup"><span data-stu-id="8e5cd-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="8e5cd-127">**CBaseStreamControl：： StreamControlState** 列舉的定義如下：</span><span class="sxs-lookup"><span data-stu-id="8e5cd-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="8e5cd-128">範例</span><span class="sxs-lookup"><span data-stu-id="8e5cd-128">Examples</span></span>

<span data-ttu-id="8e5cd-129">下列範例假設 pin 使用名為 m fLastSampleDiscarded 的成員變數 \_ 來追蹤不連續。</span><span class="sxs-lookup"><span data-stu-id="8e5cd-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="8e5cd-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e5cd-130">Requirements</span></span>



| <span data-ttu-id="8e5cd-131">需求</span><span class="sxs-lookup"><span data-stu-id="8e5cd-131">Requirement</span></span> | <span data-ttu-id="8e5cd-132">值</span><span class="sxs-lookup"><span data-stu-id="8e5cd-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5cd-133">標頭</span><span class="sxs-lookup"><span data-stu-id="8e5cd-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8e5cd-134"><dt>Strmctl (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8e5cd-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e5cd-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e5cd-135">Library</span></span><br/> | <dl> <span data-ttu-id="8e5cd-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8e5cd-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5cd-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e5cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5cd-138">**CBaseStreamControl 類別**</span><span class="sxs-lookup"><span data-stu-id="8e5cd-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




