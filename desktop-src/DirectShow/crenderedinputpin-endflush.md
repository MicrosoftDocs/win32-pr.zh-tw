---
description: EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: 'CRenderedInputPin. EndFlush 方法 (Amextra .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992968"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="08d35-104">CRenderedInputPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="08d35-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="08d35-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="08d35-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="08d35-106">這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="08d35-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d35-107">語法</span><span class="sxs-lookup"><span data-stu-id="08d35-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="08d35-108">參數</span><span class="sxs-lookup"><span data-stu-id="08d35-108">Parameters</span></span>

<span data-ttu-id="08d35-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="08d35-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08d35-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="08d35-110">Return value</span></span>

<span data-ttu-id="08d35-111">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="08d35-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d35-112">備註</span><span class="sxs-lookup"><span data-stu-id="08d35-112">Remarks</span></span>

<span data-ttu-id="08d35-113">此方法會清除任何暫止的 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="08d35-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d35-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d35-114">Requirements</span></span>



| <span data-ttu-id="08d35-115">需求</span><span class="sxs-lookup"><span data-stu-id="08d35-115">Requirement</span></span> | <span data-ttu-id="08d35-116">值</span><span class="sxs-lookup"><span data-stu-id="08d35-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d35-117">標頭</span><span class="sxs-lookup"><span data-stu-id="08d35-117">Header</span></span><br/>  | <dl> <span data-ttu-id="08d35-118"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="08d35-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08d35-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="08d35-119">Library</span></span><br/> | <dl> <span data-ttu-id="08d35-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="08d35-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d35-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d35-122">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="08d35-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




