---
description: ConnectedTo 方法會抓取連接的 pin （如果有的話）的指標。 這個方法會實 IPin：： ConnectedTo 方法。
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: 'CBasePin. ConnectedTo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990626"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="986ba-104">CBasePin. ConnectedTo 方法</span><span class="sxs-lookup"><span data-stu-id="986ba-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="986ba-105">方法會抓取 `ConnectedTo` 連接的 pin （如果有的話）的指標。</span><span class="sxs-lookup"><span data-stu-id="986ba-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="986ba-106">這個方法會實 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法。</span><span class="sxs-lookup"><span data-stu-id="986ba-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="986ba-107">語法</span><span class="sxs-lookup"><span data-stu-id="986ba-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="986ba-108">參數</span><span class="sxs-lookup"><span data-stu-id="986ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986ba-109">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="986ba-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="986ba-110">接收其他 pin 之 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="986ba-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986ba-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="986ba-111">Return value</span></span>

<span data-ttu-id="986ba-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="986ba-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="986ba-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="986ba-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="986ba-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="986ba-114">Return code</span></span>                                                                                           | <span data-ttu-id="986ba-115">Description</span><span class="sxs-lookup"><span data-stu-id="986ba-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="986ba-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="986ba-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="986ba-117">成功。</span><span class="sxs-lookup"><span data-stu-id="986ba-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="986ba-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="986ba-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="986ba-119">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="986ba-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="986ba-120"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="986ba-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="986ba-121">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="986ba-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="986ba-122">備註</span><span class="sxs-lookup"><span data-stu-id="986ba-122">Remarks</span></span>

<span data-ttu-id="986ba-123">如果方法成功，則傳回的 **IPin** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="986ba-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="986ba-124">當您完成時，請務必放開。</span><span class="sxs-lookup"><span data-stu-id="986ba-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="986ba-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="986ba-125">Requirements</span></span>



| <span data-ttu-id="986ba-126">需求</span><span class="sxs-lookup"><span data-stu-id="986ba-126">Requirement</span></span> | <span data-ttu-id="986ba-127">值</span><span class="sxs-lookup"><span data-stu-id="986ba-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="986ba-128">標頭</span><span class="sxs-lookup"><span data-stu-id="986ba-128">Header</span></span><br/>  | <dl> <span data-ttu-id="986ba-129"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="986ba-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="986ba-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="986ba-130">Library</span></span><br/> | <dl> <span data-ttu-id="986ba-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="986ba-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="986ba-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="986ba-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986ba-133">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="986ba-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




