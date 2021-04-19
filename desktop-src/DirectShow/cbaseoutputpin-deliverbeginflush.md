---
description: DeliverBeginFlush 方法會要求連接的輸入 pin，以開始進行清除作業。
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
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991197"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="d6ed4-103">CBaseOutputPin. DeliverBeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="d6ed4-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="d6ed4-104">`DeliverBeginFlush`方法會要求連接的輸入 pin，以開始進行清除操作。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ed4-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6ed4-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="d6ed4-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6ed4-106">Parameters</span></span>

<span data-ttu-id="d6ed4-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6ed4-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6ed4-108">Return value</span></span>

<span data-ttu-id="d6ed4-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d6ed4-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="d6ed4-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d6ed4-111">Return code</span></span>                                                                                           | <span data-ttu-id="d6ed4-112">Description</span><span class="sxs-lookup"><span data-stu-id="d6ed4-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d6ed4-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ed4-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d6ed4-114">成功。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d6ed4-115"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ed4-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d6ed4-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6ed4-117">備註</span><span class="sxs-lookup"><span data-stu-id="d6ed4-117">Remarks</span></span>

<span data-ttu-id="d6ed4-118">這個方法會呼叫輸入釘選上的 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="d6ed4-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ed4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6ed4-119">Requirements</span></span>



| <span data-ttu-id="d6ed4-120">需求</span><span class="sxs-lookup"><span data-stu-id="d6ed4-120">Requirement</span></span> | <span data-ttu-id="d6ed4-121">值</span><span class="sxs-lookup"><span data-stu-id="d6ed4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ed4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d6ed4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d6ed4-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6ed4-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6ed4-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6ed4-124">Library</span></span><br/> | <dl> <span data-ttu-id="d6ed4-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d6ed4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6ed4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6ed4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ed4-127">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="d6ed4-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




