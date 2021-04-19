---
description: DisconnectInternal 方法會中斷目前的 pin 連接。
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: 'CBasePin. DisconnectInternal 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983092"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="dde19-103">CBasePin. DisconnectInternal 方法</span><span class="sxs-lookup"><span data-stu-id="dde19-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="dde19-104">`DisconnectInternal`方法會中斷目前的 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="dde19-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde19-105">語法</span><span class="sxs-lookup"><span data-stu-id="dde19-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="dde19-106">參數</span><span class="sxs-lookup"><span data-stu-id="dde19-106">Parameters</span></span>

<span data-ttu-id="dde19-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dde19-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dde19-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dde19-108">Return value</span></span>

<span data-ttu-id="dde19-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dde19-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dde19-110">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="dde19-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="dde19-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dde19-111">Return code</span></span>                                                                                         | <span data-ttu-id="dde19-112">Description</span><span class="sxs-lookup"><span data-stu-id="dde19-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dde19-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="dde19-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="dde19-114">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="dde19-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="dde19-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dde19-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="dde19-116">成功。</span><span class="sxs-lookup"><span data-stu-id="dde19-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="dde19-117"><dt>**VFW \_ E \_ 未 \_ 停止**</dt></span><span class="sxs-lookup"><span data-stu-id="dde19-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="dde19-118">篩選準則為使用中，且 pin 不支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="dde19-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dde19-119">備註</span><span class="sxs-lookup"><span data-stu-id="dde19-119">Remarks</span></span>

<span data-ttu-id="dde19-120">[**CBasePin：:D isconnect**](cbasepin-disconnect.md)方法會將中斷進程委派給這個方法。</span><span class="sxs-lookup"><span data-stu-id="dde19-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="dde19-121">這個方法會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="dde19-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="dde19-122">此外，它也會釋放其他 pin 的參考計數，由 [**CBasePin：： m \_ 連接**](cbasepin-m-connected.md) 的成員變數所持有。</span><span class="sxs-lookup"><span data-stu-id="dde19-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde19-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dde19-123">Requirements</span></span>



| <span data-ttu-id="dde19-124">需求</span><span class="sxs-lookup"><span data-stu-id="dde19-124">Requirement</span></span> | <span data-ttu-id="dde19-125">值</span><span class="sxs-lookup"><span data-stu-id="dde19-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde19-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dde19-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dde19-127"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dde19-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dde19-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="dde19-128">Library</span></span><br/> | <dl> <span data-ttu-id="dde19-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dde19-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde19-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dde19-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde19-131">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="dde19-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




