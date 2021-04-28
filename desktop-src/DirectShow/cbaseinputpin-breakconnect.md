---
description: CBaseInputPin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: 'CBaseInputPin. BreakConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5398f675e056da2c60747c0b4eb17c475771bdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099736"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="51fbe-103">CBaseInputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="51fbe-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="51fbe-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="51fbe-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fbe-105">語法</span><span class="sxs-lookup"><span data-stu-id="51fbe-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="51fbe-106">參數</span><span class="sxs-lookup"><span data-stu-id="51fbe-106">Parameters</span></span>

<span data-ttu-id="51fbe-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="51fbe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51fbe-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="51fbe-108">Return value</span></span>

<span data-ttu-id="51fbe-109">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="51fbe-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fbe-110">備註</span><span class="sxs-lookup"><span data-stu-id="51fbe-110">Remarks</span></span>

<span data-ttu-id="51fbe-111">這個方法會覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="51fbe-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="51fbe-112">它會解除配置器，並釋放 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。</span><span class="sxs-lookup"><span data-stu-id="51fbe-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="51fbe-113">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="51fbe-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="51fbe-114">否則，您可能會造成記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="51fbe-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fbe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="51fbe-115">Requirements</span></span>



| <span data-ttu-id="51fbe-116">需求</span><span class="sxs-lookup"><span data-stu-id="51fbe-116">Requirement</span></span> | <span data-ttu-id="51fbe-117">值</span><span class="sxs-lookup"><span data-stu-id="51fbe-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fbe-118">標頭</span><span class="sxs-lookup"><span data-stu-id="51fbe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="51fbe-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="51fbe-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51fbe-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="51fbe-120">Library</span></span><br/> | <dl> <span data-ttu-id="51fbe-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="51fbe-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fbe-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51fbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fbe-123">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="51fbe-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




