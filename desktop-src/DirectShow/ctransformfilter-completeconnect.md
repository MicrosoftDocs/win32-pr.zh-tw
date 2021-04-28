---
description: CTransformFilter. CompleteConnect 方法-CompleteConnect 方法會完成 pin 連接。
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095166"
---
# <a name="ctransformfiltercompleteconnect-method"></a><span data-ttu-id="fc56b-103">CTransformFilter. CompleteConnect 方法</span><span class="sxs-lookup"><span data-stu-id="fc56b-103">CTransformFilter.CompleteConnect method</span></span>

<span data-ttu-id="fc56b-104">`CompleteConnect`方法會完成 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="fc56b-104">The `CompleteConnect` method completes a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc56b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc56b-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="fc56b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc56b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc56b-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="fc56b-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="fc56b-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。</span><span class="sxs-lookup"><span data-stu-id="fc56b-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="fc56b-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="fc56b-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="fc56b-110">此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fc56b-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc56b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc56b-111">Return value</span></span>

<span data-ttu-id="fc56b-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fc56b-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc56b-113">備註</span><span class="sxs-lookup"><span data-stu-id="fc56b-113">Remarks</span></span>

<span data-ttu-id="fc56b-114">[**CTransformInputPin：： CompleteConnect**](ctransforminputpin-completeconnect.md)和 [**CTransformOutputPin：： CompleteConnect**](ctransformoutputpin-completeconnect.md)方法會在 pin 連接處理期間呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="fc56b-114">The [**CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) and [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="fc56b-115">這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="fc56b-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc56b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc56b-116">Requirements</span></span>



| <span data-ttu-id="fc56b-117">需求</span><span class="sxs-lookup"><span data-stu-id="fc56b-117">Requirement</span></span> | <span data-ttu-id="fc56b-118">值</span><span class="sxs-lookup"><span data-stu-id="fc56b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc56b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fc56b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fc56b-120"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc56b-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fc56b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc56b-121">Library</span></span><br/> | <dl> <span data-ttu-id="fc56b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc56b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc56b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc56b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc56b-124">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="fc56b-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




