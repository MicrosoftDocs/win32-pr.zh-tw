---
description: CompleteConnect 方法會完成 pin 連接。
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: 'CTransformFilter. CompleteConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989849"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="7a3e8-103">CTransformFilter. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="7a3e8-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="7a3e8-104">`CompleteConnect`方法會完成 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a3e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a3e8-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="7a3e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a3e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a3e8-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="7a3e8-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="7a3e8-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="7a3e8-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="7a3e8-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="7a3e8-110">此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a3e8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a3e8-111">Return value</span></span>

<span data-ttu-id="7a3e8-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a3e8-113">備註</span><span class="sxs-lookup"><span data-stu-id="7a3e8-113">Remarks</span></span>

<span data-ttu-id="7a3e8-114">[**CTransformInputPin：： CompleteConnect**](ctransforminputpin-completeconnect.md)和 [**CTransformOutputPin：： CompleteConnect**](ctransformoutputpin-completeconnect.md)方法會在 pin 連接處理期間呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="7a3e8-115">這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="7a3e8-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a3e8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a3e8-116">Requirements</span></span>



| <span data-ttu-id="7a3e8-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a3e8-117">Requirement</span></span> | <span data-ttu-id="7a3e8-118">值</span><span class="sxs-lookup"><span data-stu-id="7a3e8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3e8-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7a3e8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7a3e8-120"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7a3e8-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a3e8-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a3e8-121">Library</span></span><br/> | <dl> <span data-ttu-id="7a3e8-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7a3e8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a3e8-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a3e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a3e8-124">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="7a3e8-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




