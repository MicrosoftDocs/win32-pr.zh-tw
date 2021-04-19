---
description: 當篩選停止串流時，會呼叫 OnStopStreaming 方法。
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: 'CBaseRenderer. OnStopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991026"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="363ce-103">CBaseRenderer. OnStopStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="363ce-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="363ce-104">`OnStopStreaming`當篩選停止串流時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="363ce-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="363ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="363ce-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="363ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="363ce-106">Parameters</span></span>

<span data-ttu-id="363ce-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="363ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="363ce-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="363ce-108">Return value</span></span>

<span data-ttu-id="363ce-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="363ce-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="363ce-110">備註</span><span class="sxs-lookup"><span data-stu-id="363ce-110">Remarks</span></span>

<span data-ttu-id="363ce-111">[**CBaseRenderer：： StopStreaming**](cbaserenderer-stopstreaming.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="363ce-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="363ce-112">它不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="363ce-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="363ce-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="363ce-113">Requirements</span></span>



| <span data-ttu-id="363ce-114">需求</span><span class="sxs-lookup"><span data-stu-id="363ce-114">Requirement</span></span> | <span data-ttu-id="363ce-115">值</span><span class="sxs-lookup"><span data-stu-id="363ce-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="363ce-116">標頭</span><span class="sxs-lookup"><span data-stu-id="363ce-116">Header</span></span><br/>  | <dl> <span data-ttu-id="363ce-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="363ce-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="363ce-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="363ce-118">Library</span></span><br/> | <dl> <span data-ttu-id="363ce-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="363ce-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363ce-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="363ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363ce-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="363ce-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




