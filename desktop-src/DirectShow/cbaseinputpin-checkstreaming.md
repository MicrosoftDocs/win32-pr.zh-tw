---
description: 判斷 pin 是否可以接受範例。
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: 'CBaseInputPin. CheckStreaming 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975733"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="3565a-103">CBaseInputPin. CheckStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="3565a-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="3565a-104">判斷 pin 是否可以接受範例。</span><span class="sxs-lookup"><span data-stu-id="3565a-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="3565a-105">語法</span><span class="sxs-lookup"><span data-stu-id="3565a-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="3565a-106">參數</span><span class="sxs-lookup"><span data-stu-id="3565a-106">Parameters</span></span>

<span data-ttu-id="3565a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3565a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3565a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3565a-108">Return value</span></span>

<span data-ttu-id="3565a-109">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3565a-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3565a-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3565a-110">Return code</span></span>                                                                                           | <span data-ttu-id="3565a-111">Description</span><span class="sxs-lookup"><span data-stu-id="3565a-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3565a-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3565a-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3565a-113">成功。</span><span class="sxs-lookup"><span data-stu-id="3565a-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3565a-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3565a-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="3565a-115">Pin 目前正在排清。</span><span class="sxs-lookup"><span data-stu-id="3565a-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="3565a-116"><dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="3565a-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="3565a-117">發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="3565a-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="3565a-118"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="3565a-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="3565a-119">已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="3565a-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="3565a-120">備註</span><span class="sxs-lookup"><span data-stu-id="3565a-120">Remarks</span></span>

<span data-ttu-id="3565a-121">衍生類別可以覆寫這個方法，以執行進一步的檢查。</span><span class="sxs-lookup"><span data-stu-id="3565a-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="3565a-122">在覆寫方法中，也呼叫基類執行。</span><span class="sxs-lookup"><span data-stu-id="3565a-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="3565a-123">[**CBaseInputPin：： Receive 方法會**](cbaseinputpin-receive.md)呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3565a-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="3565a-124">您也應該覆寫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法，以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3565a-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="3565a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3565a-125">Requirements</span></span>



| <span data-ttu-id="3565a-126">需求</span><span class="sxs-lookup"><span data-stu-id="3565a-126">Requirement</span></span> | <span data-ttu-id="3565a-127">值</span><span class="sxs-lookup"><span data-stu-id="3565a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3565a-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3565a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3565a-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3565a-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3565a-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="3565a-130">Library</span></span><br/> | <dl> <span data-ttu-id="3565a-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3565a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3565a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3565a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3565a-133">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="3565a-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




