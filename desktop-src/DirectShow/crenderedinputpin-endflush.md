---
description: CRenderedInputPin. EndFlush 方法-EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
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
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098916"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="6b46e-104">CRenderedInputPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="6b46e-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="6b46e-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="6b46e-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="6b46e-106">這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="6b46e-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b46e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6b46e-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="6b46e-108">參數</span><span class="sxs-lookup"><span data-stu-id="6b46e-108">Parameters</span></span>

<span data-ttu-id="6b46e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6b46e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b46e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b46e-110">Return value</span></span>

<span data-ttu-id="6b46e-111">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b46e-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b46e-112">備註</span><span class="sxs-lookup"><span data-stu-id="6b46e-112">Remarks</span></span>

<span data-ttu-id="6b46e-113">此方法會清除任何暫止的 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6b46e-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b46e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b46e-114">Requirements</span></span>



| <span data-ttu-id="6b46e-115">需求</span><span class="sxs-lookup"><span data-stu-id="6b46e-115">Requirement</span></span> | <span data-ttu-id="6b46e-116">值</span><span class="sxs-lookup"><span data-stu-id="6b46e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b46e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6b46e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6b46e-118"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6b46e-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b46e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b46e-119">Library</span></span><br/> | <dl> <span data-ttu-id="6b46e-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6b46e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b46e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b46e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b46e-122">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="6b46e-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




