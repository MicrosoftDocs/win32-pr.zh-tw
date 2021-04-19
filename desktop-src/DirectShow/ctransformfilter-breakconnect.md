---
description: BreakConnect 方法會從連接釋放 pin。
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: 'CTransformFilter. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994613"
---
# <a name="ctransformfilterbreakconnect-method"></a><span data-ttu-id="d1e0a-103">CTransformFilter. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="d1e0a-103">CTransformFilter.BreakConnect method</span></span>

<span data-ttu-id="d1e0a-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-104">The `BreakConnect` method releases a pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1e0a-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="d1e0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1e0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e0a-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="d1e0a-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e0a-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定 (輸入或輸出) 中斷的 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin connection was broken (input or output).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e0a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1e0a-109">Return value</span></span>

<span data-ttu-id="d1e0a-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e0a-111">備註</span><span class="sxs-lookup"><span data-stu-id="d1e0a-111">Remarks</span></span>

<span data-ttu-id="d1e0a-112">當 pin 連接中斷時， [**CTransformInputPin：： BreakConnect**](ctransforminputpin-breakconnect.md) 和 [**CTransformOutputPin：： BreakConnect**](ctransformoutputpin-breakconnect.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-112">The [**CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) and [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) methods call this method when a pin connection is broken.</span></span> <span data-ttu-id="d1e0a-113">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-113">This method does nothing in the base class.</span></span> <span data-ttu-id="d1e0a-114">如果您覆寫 [**CheckConnect**](ctransformfilter-checkconnect.md) 方法，請覆寫此方法以釋放在 **CheckConnect** 方法中取得的任何資源，包括介面指標。</span><span class="sxs-lookup"><span data-stu-id="d1e0a-114">If you override the [**CheckConnect**](ctransformfilter-checkconnect.md) method, override this method to release any resources obtained in the **CheckConnect** method, including interface pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e0a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1e0a-115">Requirements</span></span>



| <span data-ttu-id="d1e0a-116">需求</span><span class="sxs-lookup"><span data-stu-id="d1e0a-116">Requirement</span></span> | <span data-ttu-id="d1e0a-117">值</span><span class="sxs-lookup"><span data-stu-id="d1e0a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e0a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d1e0a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d1e0a-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d1e0a-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1e0a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1e0a-120">Library</span></span><br/> | <dl> <span data-ttu-id="d1e0a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d1e0a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e0a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1e0a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e0a-123">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="d1e0a-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




