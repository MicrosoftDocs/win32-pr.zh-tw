---
description: 中斷連接方法會中斷目前的 pin 連線。 這個方法會實 IPin：:D isconnect 方法。
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: 'CDynamicOutputPin 連接方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000938"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="42c71-104">CDynamicOutputPin 中斷方法</span><span class="sxs-lookup"><span data-stu-id="42c71-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="42c71-105">`Disconnect`方法會中斷目前的 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="42c71-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="42c71-106">這個方法會實 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法。</span><span class="sxs-lookup"><span data-stu-id="42c71-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c71-107">語法</span><span class="sxs-lookup"><span data-stu-id="42c71-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="42c71-108">參數</span><span class="sxs-lookup"><span data-stu-id="42c71-108">Parameters</span></span>

<span data-ttu-id="42c71-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="42c71-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42c71-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="42c71-110">Return value</span></span>

<span data-ttu-id="42c71-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="42c71-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="42c71-112">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="42c71-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="42c71-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42c71-113">Return code</span></span>                                                                             | <span data-ttu-id="42c71-114">Description</span><span class="sxs-lookup"><span data-stu-id="42c71-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="42c71-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="42c71-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="42c71-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="42c71-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="42c71-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42c71-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="42c71-118">成功。</span><span class="sxs-lookup"><span data-stu-id="42c71-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="42c71-119">備註</span><span class="sxs-lookup"><span data-stu-id="42c71-119">Remarks</span></span>

<span data-ttu-id="42c71-120">這個方法會覆寫 [**CBasePin：:D isconnect**](cbasepin-disconnect.md) 方法，以在篩選作用中時啟用中斷連接。</span><span class="sxs-lookup"><span data-stu-id="42c71-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c71-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="42c71-121">Requirements</span></span>



| <span data-ttu-id="42c71-122">需求</span><span class="sxs-lookup"><span data-stu-id="42c71-122">Requirement</span></span> | <span data-ttu-id="42c71-123">值</span><span class="sxs-lookup"><span data-stu-id="42c71-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c71-124">標頭</span><span class="sxs-lookup"><span data-stu-id="42c71-124">Header</span></span><br/>  | <dl> <span data-ttu-id="42c71-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="42c71-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42c71-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="42c71-126">Library</span></span><br/> | <dl> <span data-ttu-id="42c71-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="42c71-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c71-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42c71-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c71-129">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="42c71-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




