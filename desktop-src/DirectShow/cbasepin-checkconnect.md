---
description: CBasePin. CheckConnect 方法-CheckConnect 方法會判斷是否適合使用 pin 連接。
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: 'CBasePin. CheckConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096046"
---
# <a name="cbasepincheckconnect-method"></a><span data-ttu-id="705d5-103">CBasePin. CheckConnect 方法</span><span class="sxs-lookup"><span data-stu-id="705d5-103">CBasePin.CheckConnect method</span></span>

<span data-ttu-id="705d5-104">`CheckConnect`方法會判斷是否適合使用 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="705d5-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="705d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="705d5-105">Syntax</span></span>


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="705d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="705d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705d5-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="705d5-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="705d5-108">指向其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="705d5-108">Pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705d5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="705d5-109">Return value</span></span>

<span data-ttu-id="705d5-110">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="705d5-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="705d5-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="705d5-111">Return code</span></span>                                                                                               | <span data-ttu-id="705d5-112">Description</span><span class="sxs-lookup"><span data-stu-id="705d5-112">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="705d5-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="705d5-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="705d5-114">成功。</span><span class="sxs-lookup"><span data-stu-id="705d5-114">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="705d5-115"><dt>**VFW \_ E \_ 不正確 \_ 方向**</dt></span><span class="sxs-lookup"><span data-stu-id="705d5-115"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="705d5-116">Pin 方向不相容。</span><span class="sxs-lookup"><span data-stu-id="705d5-116">Pin directions are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="705d5-117">備註</span><span class="sxs-lookup"><span data-stu-id="705d5-117">Remarks</span></span>

<span data-ttu-id="705d5-118">在連接程式開始時，這兩個圖釘都會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="705d5-118">This method is called on both pins at the start of the connection process.</span></span> <span data-ttu-id="705d5-119">連接的 pin 會從 [**CBasePin：： Connect**](cbasepin-connect.md) 方法內呼叫它，而接收的 pin 會從 [**CBasePin：： ReceiveConnection**](cbasepin-receiveconnection.md) 方法中呼叫它。</span><span class="sxs-lookup"><span data-stu-id="705d5-119">The connecting pin calls it from within the [**CBasePin::Connect**](cbasepin-connect.md) method, and the receiving pin calls it from within the [**CBasePin::ReceiveConnection**](cbasepin-receiveconnection.md) method.</span></span>

<span data-ttu-id="705d5-120">您可以使用這個方法來判斷 *pPin* 參數所指定的 pin 是否適合用於連接。</span><span class="sxs-lookup"><span data-stu-id="705d5-120">Use this method to determine whether the pin specified by the *pPin* parameter is suitable for a connection.</span></span> <span data-ttu-id="705d5-121">如果兩個圖釘都 (輸入相同方向，或兩個輸出) 都有相同的方向，則基類會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="705d5-121">The base class returns an error if both pins have the same direction (both input, or both output).</span></span> <span data-ttu-id="705d5-122">衍生類別可以覆寫這個方法，以驗證 pin 中的其他功能。</span><span class="sxs-lookup"><span data-stu-id="705d5-122">Derived classes can override this method to verify other features in the pin.</span></span> <span data-ttu-id="705d5-123">例如， [**CBaseOutputPin**](cbaseoutputpin.md) 類別會查詢其 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="705d5-123">For example, the [**CBaseOutputPin**](cbaseoutputpin.md) class queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

<span data-ttu-id="705d5-124">如果此方法失敗，連接就會失敗，而且 pin 會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="705d5-124">If this method fails, the connection fails and the pin calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="705d5-125">使用 **BreakConnect** 來釋放中取得的任何資源 `CheckConnect` 。</span><span class="sxs-lookup"><span data-stu-id="705d5-125">Use **BreakConnect** to free any resources obtained in `CheckConnect`.</span></span> <span data-ttu-id="705d5-126">例如，如果 `CheckConnect` 呼叫 **QueryInterface** 方法，則 **BreakConnect** 必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="705d5-126">For example, if `CheckConnect` calls the **QueryInterface** method, **BreakConnect** must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="705d5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="705d5-127">Requirements</span></span>



| <span data-ttu-id="705d5-128">需求</span><span class="sxs-lookup"><span data-stu-id="705d5-128">Requirement</span></span> | <span data-ttu-id="705d5-129">值</span><span class="sxs-lookup"><span data-stu-id="705d5-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705d5-130">標頭</span><span class="sxs-lookup"><span data-stu-id="705d5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="705d5-131"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="705d5-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="705d5-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="705d5-132">Library</span></span><br/> | <dl> <span data-ttu-id="705d5-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="705d5-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="705d5-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="705d5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="705d5-135">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="705d5-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




