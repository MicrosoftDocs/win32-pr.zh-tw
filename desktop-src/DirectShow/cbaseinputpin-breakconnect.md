---
description: BreakConnect 方法會從連接釋放 pin。
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
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998613"
---
# <a name="cbaseinputpinbreakconnect-method"></a><span data-ttu-id="d8a7a-103">CBaseInputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="d8a7a-103">CBaseInputPin.BreakConnect method</span></span>

<span data-ttu-id="d8a7a-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8a7a-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="d8a7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8a7a-106">Parameters</span></span>

<span data-ttu-id="d8a7a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8a7a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8a7a-108">Return value</span></span>

<span data-ttu-id="d8a7a-109">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a7a-110">備註</span><span class="sxs-lookup"><span data-stu-id="d8a7a-110">Remarks</span></span>

<span data-ttu-id="d8a7a-111">這個方法會覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="d8a7a-112">它會解除配置器，並釋放 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="d8a7a-113">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="d8a7a-114">否則，您可能會造成記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="d8a7a-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a7a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8a7a-115">Requirements</span></span>



| <span data-ttu-id="d8a7a-116">需求</span><span class="sxs-lookup"><span data-stu-id="d8a7a-116">Requirement</span></span> | <span data-ttu-id="d8a7a-117">值</span><span class="sxs-lookup"><span data-stu-id="d8a7a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a7a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d8a7a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d8a7a-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d8a7a-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d8a7a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8a7a-120">Library</span></span><br/> | <dl> <span data-ttu-id="d8a7a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8a7a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a7a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8a7a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a7a-123">**CBaseInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="d8a7a-123">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




