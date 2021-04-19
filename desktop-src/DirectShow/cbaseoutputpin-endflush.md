---
description: EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: 'CBaseOutputPin. EndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996034"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="5c430-104">CBaseOutputPin. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="5c430-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="5c430-105">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="5c430-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="5c430-106">這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="5c430-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c430-107">語法</span><span class="sxs-lookup"><span data-stu-id="5c430-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="5c430-108">參數</span><span class="sxs-lookup"><span data-stu-id="5c430-108">Parameters</span></span>

<span data-ttu-id="5c430-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5c430-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c430-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c430-110">Return value</span></span>

<span data-ttu-id="5c430-111">傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="5c430-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c430-112">備註</span><span class="sxs-lookup"><span data-stu-id="5c430-112">Remarks</span></span>

<span data-ttu-id="5c430-113">這個方法應該只在輸入圖釘上呼叫，因此 **CBaseOutputPin** 的執行會傳回非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="5c430-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c430-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c430-114">Requirements</span></span>



| <span data-ttu-id="5c430-115">需求</span><span class="sxs-lookup"><span data-stu-id="5c430-115">Requirement</span></span> | <span data-ttu-id="5c430-116">值</span><span class="sxs-lookup"><span data-stu-id="5c430-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c430-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5c430-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5c430-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5c430-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c430-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c430-119">Library</span></span><br/> | <dl> <span data-ttu-id="5c430-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5c430-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c430-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c430-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c430-122">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="5c430-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




