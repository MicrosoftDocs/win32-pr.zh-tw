---
description: ShouldSkipFrame 方法會判斷篩選是否應該卸載指定的範例。
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: 'CVideoTransformFilter. ShouldSkipFrame 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997671"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a><span data-ttu-id="69ad1-103">CVideoTransformFilter. ShouldSkipFrame 方法</span><span class="sxs-lookup"><span data-stu-id="69ad1-103">CVideoTransformFilter.ShouldSkipFrame method</span></span>

<span data-ttu-id="69ad1-104">`ShouldSkipFrame`方法會判斷篩選是否應該卸載指定的範例。</span><span class="sxs-lookup"><span data-stu-id="69ad1-104">The `ShouldSkipFrame` method determines whether the filter should drop a specified sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ad1-105">語法</span><span class="sxs-lookup"><span data-stu-id="69ad1-105">Syntax</span></span>


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="69ad1-106">參數</span><span class="sxs-lookup"><span data-stu-id="69ad1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ad1-107">*針*</span><span class="sxs-lookup"><span data-stu-id="69ad1-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="69ad1-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="69ad1-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ad1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="69ad1-109">Return value</span></span>

<span data-ttu-id="69ad1-110">如果篩選準則應該卸載此範例，則傳回 **TRUE** ; 如果篩選器應該處理此範例，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="69ad1-110">Returns **TRUE** if the filter should drop this sample, or **FALSE** if the filter should process this sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ad1-111">備註</span><span class="sxs-lookup"><span data-stu-id="69ad1-111">Remarks</span></span>

<span data-ttu-id="69ad1-112">如果符合下列條件，則此方法會傳回 **TRUE** ：</span><span class="sxs-lookup"><span data-stu-id="69ad1-112">This method returns **TRUE** if the following conditions are met:</span></span>

-   <span data-ttu-id="69ad1-113">此範例具有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="69ad1-113">The sample has time stamps.</span></span>
-   <span data-ttu-id="69ad1-114">平均解碼時間至少為框架持續時間的25%。</span><span class="sxs-lookup"><span data-stu-id="69ad1-114">The average decoding time is at least 25% of the frame duration.</span></span>
-   <span data-ttu-id="69ad1-115">轉譯器目前至少有一個最晚的框架，如同透過品質訊息所報告。</span><span class="sxs-lookup"><span data-stu-id="69ad1-115">The renderer is currently at least one frame late, as reported through quality messages.</span></span>
-   <span data-ttu-id="69ad1-116">跳到下一個主要畫面格，並不會讓框架提早抵達一個以上的畫面格。</span><span class="sxs-lookup"><span data-stu-id="69ad1-116">Skipping to the next key frame would not cause the frame to arrive more than one frame early.</span></span>

<span data-ttu-id="69ad1-117">基於此計算的目的，篩選準則會在處理資料時記錄下列資訊：</span><span class="sxs-lookup"><span data-stu-id="69ad1-117">For purposes of this calculation, the filter records the following information as it processes data:</span></span>

-   <span data-ttu-id="69ad1-118">過去20個框架的平均解碼時間 (**m \_ itrAvgDecode**) </span><span class="sxs-lookup"><span data-stu-id="69ad1-118">The average decoding time over the past 20 frames (**m\_itrAvgDecode**)</span></span>
-   <span data-ttu-id="69ad1-119">自最後一個主要畫面格之後的框架數目 (**m \_ nFramesSinceKeyFrame**) </span><span class="sxs-lookup"><span data-stu-id="69ad1-119">The number of frames since the last key frame (**m\_nFramesSinceKeyFrame**)</span></span>
-   <span data-ttu-id="69ad1-120">在主要畫面格 (**m \_ nKeyFramePeriod** 之間有多少個框架的估計) </span><span class="sxs-lookup"><span data-stu-id="69ad1-120">An estimate of how many frames there are between key frames (**m\_nKeyFramePeriod**)</span></span>

<span data-ttu-id="69ad1-121">一旦篩選器卸載框架之後，它會繼續卸載框架，直到到達下一個主要畫面格為止。</span><span class="sxs-lookup"><span data-stu-id="69ad1-121">Once the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="69ad1-122">如果這個方法傳回 **TRUE**，也會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="69ad1-122">If this method returns **TRUE**, it also sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the Filter Graph Manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ad1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="69ad1-123">Requirements</span></span>



| <span data-ttu-id="69ad1-124">需求</span><span class="sxs-lookup"><span data-stu-id="69ad1-124">Requirement</span></span> | <span data-ttu-id="69ad1-125">值</span><span class="sxs-lookup"><span data-stu-id="69ad1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ad1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="69ad1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="69ad1-127"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="69ad1-127"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="69ad1-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="69ad1-128">Library</span></span><br/> | <dl> <span data-ttu-id="69ad1-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="69ad1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ad1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69ad1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ad1-131">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="69ad1-131">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




