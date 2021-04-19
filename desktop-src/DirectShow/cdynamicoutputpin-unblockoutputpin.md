---
description: UnblockOutputPin 方法會解除封鎖 pin。 當 pin 解除封鎖時，它可以傳遞範例、變更其輸出格式，以及重新連接本身。
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: 'CDynamicOutputPin. UnblockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994833"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="64ce1-104">CDynamicOutputPin. UnblockOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="64ce1-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="64ce1-105">方法會解除 `UnblockOutputPin` 封鎖 pin。</span><span class="sxs-lookup"><span data-stu-id="64ce1-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="64ce1-106">當 pin 解除封鎖時，它可以傳遞範例、變更其輸出格式，以及重新連接本身。</span><span class="sxs-lookup"><span data-stu-id="64ce1-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ce1-107">語法</span><span class="sxs-lookup"><span data-stu-id="64ce1-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="64ce1-108">參數</span><span class="sxs-lookup"><span data-stu-id="64ce1-108">Parameters</span></span>

<span data-ttu-id="64ce1-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="64ce1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64ce1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="64ce1-110">Return value</span></span>

<span data-ttu-id="64ce1-111">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="64ce1-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="64ce1-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="64ce1-112">Return code</span></span>                                                                             | <span data-ttu-id="64ce1-113">Description</span><span class="sxs-lookup"><span data-stu-id="64ce1-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="64ce1-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="64ce1-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="64ce1-115">Pin 已解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="64ce1-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="64ce1-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="64ce1-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="64ce1-117">成功。</span><span class="sxs-lookup"><span data-stu-id="64ce1-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="64ce1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="64ce1-118">Requirements</span></span>



| <span data-ttu-id="64ce1-119">需求</span><span class="sxs-lookup"><span data-stu-id="64ce1-119">Requirement</span></span> | <span data-ttu-id="64ce1-120">值</span><span class="sxs-lookup"><span data-stu-id="64ce1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ce1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="64ce1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="64ce1-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="64ce1-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="64ce1-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="64ce1-123">Library</span></span><br/> | <dl> <span data-ttu-id="64ce1-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="64ce1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ce1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64ce1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ce1-126">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="64ce1-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




