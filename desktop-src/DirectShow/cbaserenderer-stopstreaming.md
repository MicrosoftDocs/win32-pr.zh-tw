---
description: 當篩選參數切換到執行中狀態時，StopStreaming 方法會停止串流。
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: 'CBaseRenderer. StopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979475"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="f3295-103">CBaseRenderer. StopStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="f3295-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="f3295-104">`StopStreaming`當篩選參數切換到執行中狀態時，此方法會停止串流。</span><span class="sxs-lookup"><span data-stu-id="f3295-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3295-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3295-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="f3295-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3295-106">Parameters</span></span>

<span data-ttu-id="f3295-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f3295-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3295-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3295-108">Return value</span></span>

<span data-ttu-id="f3295-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f3295-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3295-110">備註</span><span class="sxs-lookup"><span data-stu-id="f3295-110">Remarks</span></span>

<span data-ttu-id="f3295-111">這個方法會呼叫 [**CBaseRenderer：： OnStopStreaming**](cbaserenderer-onstopstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f3295-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="f3295-112">該方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="f3295-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3295-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3295-113">Requirements</span></span>



| <span data-ttu-id="f3295-114">需求</span><span class="sxs-lookup"><span data-stu-id="f3295-114">Requirement</span></span> | <span data-ttu-id="f3295-115">值</span><span class="sxs-lookup"><span data-stu-id="f3295-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3295-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f3295-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f3295-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f3295-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3295-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3295-118">Library</span></span><br/> | <dl> <span data-ttu-id="f3295-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f3295-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3295-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3295-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3295-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="f3295-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




