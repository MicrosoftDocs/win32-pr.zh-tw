---
description: 當狀態切換為 [已暫停] 或 [執行中] 時，會呼叫使用中的方法。
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: 'CBaseRenderer 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992969"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="9f94a-103">CBaseRenderer 方法</span><span class="sxs-lookup"><span data-stu-id="9f94a-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="9f94a-104">`Active`當狀態切換為已暫停或正在執行時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="9f94a-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f94a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f94a-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="9f94a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f94a-106">Parameters</span></span>

<span data-ttu-id="9f94a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9f94a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f94a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f94a-108">Return value</span></span>

<span data-ttu-id="9f94a-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9f94a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f94a-110">備註</span><span class="sxs-lookup"><span data-stu-id="9f94a-110">Remarks</span></span>

<span data-ttu-id="9f94a-111">輸入的 pin 會從自己的 [**CRendererInputPin：： Active**](crendererinputpin-active.md) 方法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9f94a-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="9f94a-112">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="9f94a-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f94a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f94a-113">Requirements</span></span>



| <span data-ttu-id="9f94a-114">需求</span><span class="sxs-lookup"><span data-stu-id="9f94a-114">Requirement</span></span> | <span data-ttu-id="9f94a-115">值</span><span class="sxs-lookup"><span data-stu-id="9f94a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f94a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9f94a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9f94a-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9f94a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f94a-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f94a-118">Library</span></span><br/> | <dl> <span data-ttu-id="9f94a-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9f94a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f94a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f94a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f94a-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="9f94a-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




