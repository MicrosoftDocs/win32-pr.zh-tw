---
description: 使用中的方法會通知釘選篩選現在為使用中狀態。 這個方法會覆寫 CBasePin：： Active 方法。
ms.assetid: 2e0c773a-1165-4da2-8acc-fe553663408d
title: 'CRendererInputPin 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10df7a68fef8cde3d33a654554509ce26145f8e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993370"
---
# <a name="crendererinputpinactive-method"></a><span data-ttu-id="c1df2-104">CRendererInputPin 方法</span><span class="sxs-lookup"><span data-stu-id="c1df2-104">CRendererInputPin.Active method</span></span>

<span data-ttu-id="c1df2-105">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="c1df2-105">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="c1df2-106">這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c1df2-106">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1df2-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1df2-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="c1df2-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1df2-108">Parameters</span></span>

<span data-ttu-id="c1df2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c1df2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1df2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1df2-110">Return value</span></span>

<span data-ttu-id="c1df2-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c1df2-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1df2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1df2-112">Requirements</span></span>



| <span data-ttu-id="c1df2-113">需求</span><span class="sxs-lookup"><span data-stu-id="c1df2-113">Requirement</span></span> | <span data-ttu-id="c1df2-114">值</span><span class="sxs-lookup"><span data-stu-id="c1df2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1df2-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c1df2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c1df2-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c1df2-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1df2-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1df2-117">Library</span></span><br/> | <dl> <span data-ttu-id="c1df2-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c1df2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1df2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1df2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1df2-120">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="c1df2-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




