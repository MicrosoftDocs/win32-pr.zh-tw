---
description: CDynamicOutputPin 中斷連接方法-中斷連接方法會中斷目前的 pin 連線。 這個方法會實 IPin：:D isconnect 方法。
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
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099296"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="a479b-104">CDynamicOutputPin 中斷方法</span><span class="sxs-lookup"><span data-stu-id="a479b-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="a479b-105">`Disconnect`方法會中斷目前的 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="a479b-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="a479b-106">這個方法會實 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法。</span><span class="sxs-lookup"><span data-stu-id="a479b-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a479b-107">語法</span><span class="sxs-lookup"><span data-stu-id="a479b-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="a479b-108">參數</span><span class="sxs-lookup"><span data-stu-id="a479b-108">Parameters</span></span>

<span data-ttu-id="a479b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a479b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a479b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a479b-110">Return value</span></span>

<span data-ttu-id="a479b-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a479b-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a479b-112">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="a479b-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a479b-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a479b-113">Return code</span></span>                                                                             | <span data-ttu-id="a479b-114">Description</span><span class="sxs-lookup"><span data-stu-id="a479b-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a479b-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a479b-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a479b-116">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="a479b-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="a479b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a479b-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a479b-118">成功。</span><span class="sxs-lookup"><span data-stu-id="a479b-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="a479b-119">備註</span><span class="sxs-lookup"><span data-stu-id="a479b-119">Remarks</span></span>

<span data-ttu-id="a479b-120">這個方法會覆寫 [**CBasePin：:D isconnect**](cbasepin-disconnect.md) 方法，以在篩選作用中時啟用中斷連接。</span><span class="sxs-lookup"><span data-stu-id="a479b-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="a479b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a479b-121">Requirements</span></span>



| <span data-ttu-id="a479b-122">需求</span><span class="sxs-lookup"><span data-stu-id="a479b-122">Requirement</span></span> | <span data-ttu-id="a479b-123">值</span><span class="sxs-lookup"><span data-stu-id="a479b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a479b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a479b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a479b-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a479b-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a479b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a479b-126">Library</span></span><br/> | <dl> <span data-ttu-id="a479b-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a479b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a479b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a479b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a479b-129">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="a479b-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




