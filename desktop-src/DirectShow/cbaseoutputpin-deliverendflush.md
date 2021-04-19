---
description: DeliverEndFlush 方法會要求連接的輸入 pin，以結束清除作業。
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: 'CBaseOutputPin. DeliverEndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990984"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="74a9d-103">CBaseOutputPin. DeliverEndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="74a9d-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="74a9d-104">`DeliverEndFlush`方法會要求連接的輸入 pin 以結束排清作業。</span><span class="sxs-lookup"><span data-stu-id="74a9d-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="74a9d-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="74a9d-106">參數</span><span class="sxs-lookup"><span data-stu-id="74a9d-106">Parameters</span></span>

<span data-ttu-id="74a9d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="74a9d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74a9d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="74a9d-108">Return value</span></span>

<span data-ttu-id="74a9d-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="74a9d-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="74a9d-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="74a9d-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="74a9d-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="74a9d-111">Return code</span></span>                                                                                           | <span data-ttu-id="74a9d-112">Description</span><span class="sxs-lookup"><span data-stu-id="74a9d-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="74a9d-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="74a9d-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="74a9d-114">成功。</span><span class="sxs-lookup"><span data-stu-id="74a9d-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="74a9d-115"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="74a9d-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="74a9d-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="74a9d-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74a9d-117">備註</span><span class="sxs-lookup"><span data-stu-id="74a9d-117">Remarks</span></span>

<span data-ttu-id="74a9d-118">這個方法會呼叫輸入釘選上的 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="74a9d-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a9d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74a9d-119">Requirements</span></span>



| <span data-ttu-id="74a9d-120">需求</span><span class="sxs-lookup"><span data-stu-id="74a9d-120">Requirement</span></span> | <span data-ttu-id="74a9d-121">值</span><span class="sxs-lookup"><span data-stu-id="74a9d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a9d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="74a9d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="74a9d-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="74a9d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74a9d-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="74a9d-124">Library</span></span><br/> | <dl> <span data-ttu-id="74a9d-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="74a9d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74a9d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74a9d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a9d-127">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="74a9d-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




