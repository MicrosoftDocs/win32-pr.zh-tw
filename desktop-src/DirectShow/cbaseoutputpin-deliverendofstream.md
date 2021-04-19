---
description: DeliverEndOfStream 方法會將資料流程結束通知傳遞至連線的輸入 pin。
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: 'CBaseOutputPin. DeliverEndOfStream 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998671"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="7f4c7-103">CBaseOutputPin. DeliverEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="7f4c7-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="7f4c7-104">方法會將 `DeliverEndOfStream` 資料流程結束通知傳遞至連接的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f4c7-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="7f4c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f4c7-106">Parameters</span></span>

<span data-ttu-id="7f4c7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f4c7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f4c7-108">Return value</span></span>

<span data-ttu-id="7f4c7-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7f4c7-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="7f4c7-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7f4c7-111">Return code</span></span>                                                                                           | <span data-ttu-id="7f4c7-112">Description</span><span class="sxs-lookup"><span data-stu-id="7f4c7-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f4c7-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4c7-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7f4c7-114">成功。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="7f4c7-115"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4c7-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7f4c7-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f4c7-117">備註</span><span class="sxs-lookup"><span data-stu-id="7f4c7-117">Remarks</span></span>

<span data-ttu-id="7f4c7-118">這個方法會呼叫輸入釘選上的 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f4c7-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4c7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f4c7-119">Requirements</span></span>



| <span data-ttu-id="7f4c7-120">需求</span><span class="sxs-lookup"><span data-stu-id="7f4c7-120">Requirement</span></span> | <span data-ttu-id="7f4c7-121">值</span><span class="sxs-lookup"><span data-stu-id="7f4c7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4c7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7f4c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7f4c7-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f4c7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7f4c7-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f4c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="7f4c7-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f4c7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4c7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f4c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4c7-127">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="7f4c7-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




