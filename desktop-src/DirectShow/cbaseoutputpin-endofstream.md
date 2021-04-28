---
description: CBaseOutputPin. EndOfStream 方法-EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: 'CBaseOutputPin. EndOfStream 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096146"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="18a41-104">CBaseOutputPin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="18a41-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="18a41-105">`EndOfStream`方法會通知 pin，不需要任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="18a41-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="18a41-106">這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="18a41-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a41-107">語法</span><span class="sxs-lookup"><span data-stu-id="18a41-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="18a41-108">參數</span><span class="sxs-lookup"><span data-stu-id="18a41-108">Parameters</span></span>

<span data-ttu-id="18a41-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="18a41-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18a41-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="18a41-110">Return value</span></span>

<span data-ttu-id="18a41-111">傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="18a41-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="18a41-112">備註</span><span class="sxs-lookup"><span data-stu-id="18a41-112">Remarks</span></span>

<span data-ttu-id="18a41-113">這個方法應該只在輸入圖釘上呼叫，因此 **CBaseOutputPin** 的執行會傳回非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="18a41-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="18a41-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="18a41-114">Requirements</span></span>



| <span data-ttu-id="18a41-115">需求</span><span class="sxs-lookup"><span data-stu-id="18a41-115">Requirement</span></span> | <span data-ttu-id="18a41-116">值</span><span class="sxs-lookup"><span data-stu-id="18a41-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a41-117">標頭</span><span class="sxs-lookup"><span data-stu-id="18a41-117">Header</span></span><br/>  | <dl> <span data-ttu-id="18a41-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="18a41-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="18a41-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="18a41-119">Library</span></span><br/> | <dl> <span data-ttu-id="18a41-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="18a41-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18a41-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18a41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a41-122">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="18a41-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




