---
description: 當篩選參數切換為暫停狀態時，就會呼叫 StartStreaming 方法。 這個方法會覆寫 CTransformFilter：： StartStreaming 方法。
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: 'CVideoTransformFilter. StartStreaming 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989717"
---
# <a name="cvideotransformfilterstartstreaming-method"></a><span data-ttu-id="4c9e2-104">CVideoTransformFilter. StartStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="4c9e2-104">CVideoTransformFilter.StartStreaming method</span></span>

<span data-ttu-id="4c9e2-105">`StartStreaming`當篩選參數切換為暫停狀態時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="4c9e2-105">The `StartStreaming` method is called when the filter switches to the paused state.</span></span> <span data-ttu-id="4c9e2-106">這個方法會覆寫 [**CTransformFilter：： StartStreaming**](ctransformfilter-startstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c9e2-106">This method overrides the [**CTransformFilter::StartStreaming**](ctransformfilter-startstreaming.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c9e2-107">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="4c9e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c9e2-108">Parameters</span></span>

<span data-ttu-id="4c9e2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4c9e2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c9e2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c9e2-110">Return value</span></span>

<span data-ttu-id="4c9e2-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4c9e2-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9e2-112">備註</span><span class="sxs-lookup"><span data-stu-id="4c9e2-112">Remarks</span></span>

<span data-ttu-id="4c9e2-113">這個方法會重設所有的效能統計資料。</span><span class="sxs-lookup"><span data-stu-id="4c9e2-113">This method resets all of the performance statistics.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9e2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c9e2-114">Requirements</span></span>



| <span data-ttu-id="4c9e2-115">需求</span><span class="sxs-lookup"><span data-stu-id="4c9e2-115">Requirement</span></span> | <span data-ttu-id="4c9e2-116">值</span><span class="sxs-lookup"><span data-stu-id="4c9e2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9e2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="4c9e2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4c9e2-118"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4c9e2-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4c9e2-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c9e2-119">Library</span></span><br/> | <dl> <span data-ttu-id="4c9e2-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4c9e2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9e2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c9e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9e2-122">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4c9e2-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




