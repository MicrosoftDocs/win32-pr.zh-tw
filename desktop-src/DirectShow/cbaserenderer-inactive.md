---
description: 當狀態切換為 [已停止] 時，會呼叫非使用中的方法。
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: 'CBaseRenderer：非使用中方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992153"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="f7ee1-103">CBaseRenderer 方法</span><span class="sxs-lookup"><span data-stu-id="f7ee1-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="f7ee1-104">`Inactive`當狀態切換為 [已停止] 時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="f7ee1-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ee1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7ee1-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="f7ee1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7ee1-106">Parameters</span></span>

<span data-ttu-id="f7ee1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f7ee1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7ee1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7ee1-108">Return value</span></span>

<span data-ttu-id="f7ee1-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f7ee1-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7ee1-110">備註</span><span class="sxs-lookup"><span data-stu-id="f7ee1-110">Remarks</span></span>

<span data-ttu-id="f7ee1-111">輸入的 pin 會從它自己的 [**CRendererInputPin：：非**](crendererinputpin-inactive.md) 使用中的方法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f7ee1-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="f7ee1-112">篩選準則會呼叫 [**CBaseRenderer：： ClearPendingSample**](cbaserenderer-clearpendingsample.md) 方法，以釋放最新的範例。</span><span class="sxs-lookup"><span data-stu-id="f7ee1-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ee1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7ee1-113">Requirements</span></span>



| <span data-ttu-id="f7ee1-114">需求</span><span class="sxs-lookup"><span data-stu-id="f7ee1-114">Requirement</span></span> | <span data-ttu-id="f7ee1-115">值</span><span class="sxs-lookup"><span data-stu-id="f7ee1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ee1-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f7ee1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f7ee1-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f7ee1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7ee1-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7ee1-118">Library</span></span><br/> | <dl> <span data-ttu-id="f7ee1-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f7ee1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ee1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7ee1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ee1-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="f7ee1-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




