---
description: ShouldDrawSampleNow 方法會判斷是否應該繪製影片，而不需要使用時鐘來設定計時器建議連結。
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: 'CBaseVideoRenderer. ShouldDrawSampleNow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992814"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="637fd-103">CBaseVideoRenderer. ShouldDrawSampleNow 方法</span><span class="sxs-lookup"><span data-stu-id="637fd-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="637fd-104">此 `ShouldDrawSampleNow` 方法會決定是否應繪製影片，而不需要使用時鐘來設定計時器建議連結。</span><span class="sxs-lookup"><span data-stu-id="637fd-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="637fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="637fd-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="637fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="637fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="637fd-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="637fd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="637fd-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="637fd-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="637fd-109">*ptrStart*</span><span class="sxs-lookup"><span data-stu-id="637fd-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="637fd-110">開始呈現的時間指標。</span><span class="sxs-lookup"><span data-stu-id="637fd-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="637fd-111">*ptrEnd*</span><span class="sxs-lookup"><span data-stu-id="637fd-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="637fd-112">停止轉譯的時間指標。</span><span class="sxs-lookup"><span data-stu-id="637fd-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="637fd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="637fd-113">Return value</span></span>

<span data-ttu-id="637fd-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="637fd-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="637fd-115">傳回 \_ [OK] 表示一次繪製一次，而不等候，S \_ FALSE 表示在時間 *ptrStart* 繪製，或使用錯誤表示不繪製樣本; 也就是說，略過以節省時間。</span><span class="sxs-lookup"><span data-stu-id="637fd-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="637fd-116">備註</span><span class="sxs-lookup"><span data-stu-id="637fd-116">Remarks</span></span>

<span data-ttu-id="637fd-117">此成員函式會覆寫 [**CBaseRenderer：： ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)。</span><span class="sxs-lookup"><span data-stu-id="637fd-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="637fd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="637fd-118">Requirements</span></span>



| <span data-ttu-id="637fd-119">需求</span><span class="sxs-lookup"><span data-stu-id="637fd-119">Requirement</span></span> | <span data-ttu-id="637fd-120">值</span><span class="sxs-lookup"><span data-stu-id="637fd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637fd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="637fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="637fd-122"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="637fd-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="637fd-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="637fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="637fd-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="637fd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637fd-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="637fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637fd-126">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="637fd-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




