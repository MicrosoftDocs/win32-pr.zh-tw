---
description: CBaseOutputPin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: 'CBaseOutputPin. CheckConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096186"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="ac368-103">CBaseOutputPin. CheckConnect 方法</span><span class="sxs-lookup"><span data-stu-id="ac368-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="ac368-104">`CheckConnect`方法會判斷是否適合使用 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="ac368-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac368-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac368-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="ac368-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac368-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="ac368-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="ac368-108">輸入釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ac368-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac368-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac368-109">Return value</span></span>

<span data-ttu-id="ac368-110">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ac368-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="ac368-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ac368-111">Return code</span></span>                                                                                               | <span data-ttu-id="ac368-112">Description</span><span class="sxs-lookup"><span data-stu-id="ac368-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac368-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ac368-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="ac368-114">成功。</span><span class="sxs-lookup"><span data-stu-id="ac368-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="ac368-115"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="ac368-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="ac368-116">輸入 pin 不支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)。</span><span class="sxs-lookup"><span data-stu-id="ac368-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="ac368-117"><dt>**VFW \_ E \_ 不正確 \_ 方向**</dt></span><span class="sxs-lookup"><span data-stu-id="ac368-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="ac368-118">Pin 方向不相容。</span><span class="sxs-lookup"><span data-stu-id="ac368-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="ac368-119">備註</span><span class="sxs-lookup"><span data-stu-id="ac368-119">Remarks</span></span>

<span data-ttu-id="ac368-120">這個方法會呼叫基類 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法，然後查詢其 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入釘選。</span><span class="sxs-lookup"><span data-stu-id="ac368-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac368-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac368-121">Requirements</span></span>



| <span data-ttu-id="ac368-122">需求</span><span class="sxs-lookup"><span data-stu-id="ac368-122">Requirement</span></span> | <span data-ttu-id="ac368-123">值</span><span class="sxs-lookup"><span data-stu-id="ac368-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac368-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ac368-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ac368-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ac368-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ac368-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac368-126">Library</span></span><br/> | <dl> <span data-ttu-id="ac368-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ac368-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac368-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac368-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac368-129">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="ac368-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




