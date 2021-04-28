---
description: CBaseOutputPin. DeliverBeginFlush 方法-DeliverBeginFlush 方法會要求連接的輸入 pin，以開始進行清除操作。
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: 'CBaseOutputPin. DeliverBeginFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099516"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="35414-103">CBaseOutputPin. DeliverBeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="35414-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="35414-104">`DeliverBeginFlush`方法會要求連接的輸入 pin，以開始進行清除操作。</span><span class="sxs-lookup"><span data-stu-id="35414-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="35414-105">語法</span><span class="sxs-lookup"><span data-stu-id="35414-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="35414-106">參數</span><span class="sxs-lookup"><span data-stu-id="35414-106">Parameters</span></span>

<span data-ttu-id="35414-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="35414-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35414-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="35414-108">Return value</span></span>

<span data-ttu-id="35414-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="35414-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="35414-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="35414-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="35414-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="35414-111">Return code</span></span>                                                                                           | <span data-ttu-id="35414-112">Description</span><span class="sxs-lookup"><span data-stu-id="35414-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="35414-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="35414-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="35414-114">成功。</span><span class="sxs-lookup"><span data-stu-id="35414-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="35414-115"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="35414-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="35414-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="35414-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35414-117">備註</span><span class="sxs-lookup"><span data-stu-id="35414-117">Remarks</span></span>

<span data-ttu-id="35414-118">這個方法會呼叫輸入釘選上的 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="35414-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="35414-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="35414-119">Requirements</span></span>



| <span data-ttu-id="35414-120">需求</span><span class="sxs-lookup"><span data-stu-id="35414-120">Requirement</span></span> | <span data-ttu-id="35414-121">值</span><span class="sxs-lookup"><span data-stu-id="35414-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35414-122">標頭</span><span class="sxs-lookup"><span data-stu-id="35414-122">Header</span></span><br/>  | <dl> <span data-ttu-id="35414-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35414-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="35414-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="35414-124">Library</span></span><br/> | <dl> <span data-ttu-id="35414-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35414-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35414-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35414-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35414-127">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="35414-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




