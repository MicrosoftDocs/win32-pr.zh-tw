---
description: CTransformFilter. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: 'CTransformFilter. CheckConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5927aac2fa58322c93a23489a22dc96a1e2a67f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085096"
---
# <a name="ctransformfiltercheckconnect-method"></a><span data-ttu-id="24c00-103">CTransformFilter. CheckConnect 方法</span><span class="sxs-lookup"><span data-stu-id="24c00-103">CTransformFilter.CheckConnect method</span></span>

<span data-ttu-id="24c00-104">`CheckConnect`方法會判斷是否適合使用 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="24c00-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c00-105">語法</span><span class="sxs-lookup"><span data-stu-id="24c00-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="24c00-106">參數</span><span class="sxs-lookup"><span data-stu-id="24c00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c00-107">*dir*</span><span class="sxs-lookup"><span data-stu-id="24c00-107">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="24c00-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，指定篩選上的哪個圖釘正在進行連接。</span><span class="sxs-lookup"><span data-stu-id="24c00-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying which pin on the filter is making the connection.</span></span>

</dd> <dt>

<span data-ttu-id="24c00-109">*pPin*</span><span class="sxs-lookup"><span data-stu-id="24c00-109">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="24c00-110">此連接嘗試中其他 pin 的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="24c00-110">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin in this connection attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c00-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="24c00-111">Return value</span></span>

<span data-ttu-id="24c00-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="24c00-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c00-113">備註</span><span class="sxs-lookup"><span data-stu-id="24c00-113">Remarks</span></span>

<span data-ttu-id="24c00-114">[**CTransformInputPin：： CheckConnect**](ctransforminputpin-checkconnect.md)和 [**CTransformOutputPin：： CheckConnect**](ctransformoutputpin-checkconnect.md)方法會在 pin 連接處理期間呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="24c00-114">The [**CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) and [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) methods call this method during the pin connection process.</span></span> <span data-ttu-id="24c00-115">這個方法不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="24c00-115">This method does nothing in the base class.</span></span> <span data-ttu-id="24c00-116">衍生的類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="24c00-116">The derived class can override it.</span></span> <span data-ttu-id="24c00-117">例如，衍生類別可能會查詢特定介面的其他 pin。</span><span class="sxs-lookup"><span data-stu-id="24c00-117">For example, the derived class might query the other pin for a particular interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c00-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="24c00-118">Requirements</span></span>



| <span data-ttu-id="24c00-119">需求</span><span class="sxs-lookup"><span data-stu-id="24c00-119">Requirement</span></span> | <span data-ttu-id="24c00-120">值</span><span class="sxs-lookup"><span data-stu-id="24c00-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c00-121">標頭</span><span class="sxs-lookup"><span data-stu-id="24c00-121">Header</span></span><br/>  | <dl> <span data-ttu-id="24c00-122"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="24c00-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="24c00-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="24c00-123">Library</span></span><br/> | <dl> <span data-ttu-id="24c00-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="24c00-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c00-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24c00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c00-126">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="24c00-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




