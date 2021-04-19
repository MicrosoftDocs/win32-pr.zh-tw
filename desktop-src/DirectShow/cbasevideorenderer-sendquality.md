---
description: SendQuality 方法會傳送品質訊息，以指出供應商應該如何處理品質。
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: 'CBaseVideoRenderer. SendQuality 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a6ae7228be0f3012c49d652d11bf2c1c3bfc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983976"
---
# <a name="cbasevideorenderersendquality-method"></a><span data-ttu-id="1fb31-103">CBaseVideoRenderer. SendQuality 方法</span><span class="sxs-lookup"><span data-stu-id="1fb31-103">CBaseVideoRenderer.SendQuality method</span></span>

<span data-ttu-id="1fb31-104">`SendQuality`方法會傳送品質訊息，以指出供應商應該如何處理品質。</span><span class="sxs-lookup"><span data-stu-id="1fb31-104">The `SendQuality` method sends a quality message to indicate what the supplier should do about quality.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb31-105">語法</span><span class="sxs-lookup"><span data-stu-id="1fb31-105">Syntax</span></span>


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a><span data-ttu-id="1fb31-106">參數</span><span class="sxs-lookup"><span data-stu-id="1fb31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb31-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="1fb31-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="1fb31-108">框架延遲的時間量。</span><span class="sxs-lookup"><span data-stu-id="1fb31-108">Amount of time by which the frame is late.</span></span>

</dd> <dt>

<span data-ttu-id="1fb31-109">*trRealStream*</span><span class="sxs-lookup"><span data-stu-id="1fb31-109">*trRealStream*</span></span> 
</dt> <dd>

<span data-ttu-id="1fb31-110">Currentstream 時間。</span><span class="sxs-lookup"><span data-stu-id="1fb31-110">Currentstream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb31-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fb31-111">Return value</span></span>

<span data-ttu-id="1fb31-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1fb31-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb31-113">備註</span><span class="sxs-lookup"><span data-stu-id="1fb31-113">Remarks</span></span>

<span data-ttu-id="1fb31-114">此成員函式會傳送上游的品質控制訊息來控制品質管制。</span><span class="sxs-lookup"><span data-stu-id="1fb31-114">This member function sends a quality control message upstream to control quality management.</span></span> <span data-ttu-id="1fb31-115">品質訊息的本質 (也就是，是否要減少或增加) 的樣本數目是否可在此衍生類別的品質管制執行中決定 (請參閱 [**CBaseVideoRenderer：： ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1fb31-115">The nature of the quality message (that is, whether to reduce or increase the number of samples) is determined in the quality management implementation in this derived class (see [**CBaseVideoRenderer::ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb31-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fb31-116">Requirements</span></span>



| <span data-ttu-id="1fb31-117">需求</span><span class="sxs-lookup"><span data-stu-id="1fb31-117">Requirement</span></span> | <span data-ttu-id="1fb31-118">值</span><span class="sxs-lookup"><span data-stu-id="1fb31-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb31-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1fb31-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1fb31-120"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1fb31-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fb31-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="1fb31-121">Library</span></span><br/> | <dl> <span data-ttu-id="1fb31-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1fb31-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb31-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fb31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb31-124">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="1fb31-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




