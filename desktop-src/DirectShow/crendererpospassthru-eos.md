---
description: EOS 方法會在結束資料流程通知之後，更新快取的時間戳記。
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: 'CRendererPosPassThru 的 Ctlutil 方法 (. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980226"
---
# <a name="crendererpospassthrueos-method"></a><span data-ttu-id="06821-103">CRendererPosPassThru. EOS 方法</span><span class="sxs-lookup"><span data-stu-id="06821-103">CRendererPosPassThru.EOS method</span></span>

<span data-ttu-id="06821-104">方法會在 `EOS` 結束資料流程通知之後，更新快取的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="06821-104">The `EOS` method updates the cached time stamps after an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="06821-105">語法</span><span class="sxs-lookup"><span data-stu-id="06821-105">Syntax</span></span>


```C++
HRESULT EOS();
```



## <a name="parameters"></a><span data-ttu-id="06821-106">參數</span><span class="sxs-lookup"><span data-stu-id="06821-106">Parameters</span></span>

<span data-ttu-id="06821-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="06821-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06821-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="06821-108">Return value</span></span>

<span data-ttu-id="06821-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="06821-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="06821-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="06821-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="06821-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="06821-111">Return code</span></span>                                                                            | <span data-ttu-id="06821-112">Description</span><span class="sxs-lookup"><span data-stu-id="06821-112">Description</span></span>                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="06821-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="06821-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="06821-114">成功。</span><span class="sxs-lookup"><span data-stu-id="06821-114">Success.</span></span><br/>                                       |
| <dl> <span data-ttu-id="06821-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="06821-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="06821-116">失敗。</span><span class="sxs-lookup"><span data-stu-id="06821-116">Failure.</span></span> <span data-ttu-id="06821-117">可能是篩選未串流處理。</span><span class="sxs-lookup"><span data-stu-id="06821-117">Possibly the filter is not streaming.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06821-118">備註</span><span class="sxs-lookup"><span data-stu-id="06821-118">Remarks</span></span>

<span data-ttu-id="06821-119">當此篩選接收資料流程結束通知時 ([**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)) ，就應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="06821-119">The filter should call this method when it receives an end-of-stream notification ([**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)).</span></span> <span data-ttu-id="06821-120">方法會將快取的時間戳記設為等於停止位置，以確保 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法會傳回資料流程結尾的正確值。</span><span class="sxs-lookup"><span data-stu-id="06821-120">The method sets both cached time stamps equal to the stop position, ensuring that the [**IMediaSeeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the correct values at the end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="06821-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="06821-121">Requirements</span></span>



| <span data-ttu-id="06821-122">需求</span><span class="sxs-lookup"><span data-stu-id="06821-122">Requirement</span></span> | <span data-ttu-id="06821-123">值</span><span class="sxs-lookup"><span data-stu-id="06821-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06821-124">標頭</span><span class="sxs-lookup"><span data-stu-id="06821-124">Header</span></span><br/>  | <dl> <span data-ttu-id="06821-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06821-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06821-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="06821-126">Library</span></span><br/> | <dl> <span data-ttu-id="06821-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="06821-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




