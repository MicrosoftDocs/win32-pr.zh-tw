---
description: ResetMediaTime 方法會將快取的時間戳記重設為零。
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: 'CRendererPosPassThru. ResetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999201"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="0c651-103">CRendererPosPassThru. ResetMediaTime 方法</span><span class="sxs-lookup"><span data-stu-id="0c651-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="0c651-104">方法會將快取 `ResetMediaTime` 的時間戳記重設為零。</span><span class="sxs-lookup"><span data-stu-id="0c651-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c651-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c651-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="0c651-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c651-106">Parameters</span></span>

<span data-ttu-id="0c651-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0c651-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c651-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c651-108">Return value</span></span>

<span data-ttu-id="0c651-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0c651-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c651-110">備註</span><span class="sxs-lookup"><span data-stu-id="0c651-110">Remarks</span></span>

<span data-ttu-id="0c651-111">每當 [**CRendererPosPassThru：： RegisterMediaTime**](crendererpospassthru-registermediatime.md) 方法所快取的時間戳記變成無效時，篩選準則就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0c651-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="0c651-112">具體而言，它應該呼叫這個方法來回應 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 和 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c651-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="0c651-113">呼叫這個方法之後， [**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md) 方法會針對開始和結束時間傳回零。</span><span class="sxs-lookup"><span data-stu-id="0c651-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c651-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c651-114">Requirements</span></span>



| <span data-ttu-id="0c651-115">需求</span><span class="sxs-lookup"><span data-stu-id="0c651-115">Requirement</span></span> | <span data-ttu-id="0c651-116">值</span><span class="sxs-lookup"><span data-stu-id="0c651-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c651-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0c651-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0c651-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0c651-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c651-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c651-119">Library</span></span><br/> | <dl> <span data-ttu-id="0c651-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0c651-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




