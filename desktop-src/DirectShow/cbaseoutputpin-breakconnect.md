---
description: BreakConnect 方法會從連接釋放 pin。
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: 'CBaseOutputPin. BreakConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ea23d6f74032c3fd2608209d1d1f4cd2babf121
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987188"
---
# <a name="cbaseoutputpinbreakconnect-method"></a><span data-ttu-id="4ada8-103">CBaseOutputPin. BreakConnect 方法</span><span class="sxs-lookup"><span data-stu-id="4ada8-103">CBaseOutputPin.BreakConnect method</span></span>

<span data-ttu-id="4ada8-104">`BreakConnect`方法會從連接釋放 pin。</span><span class="sxs-lookup"><span data-stu-id="4ada8-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ada8-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ada8-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="4ada8-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ada8-106">Parameters</span></span>

<span data-ttu-id="4ada8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4ada8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ada8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ada8-108">Return value</span></span>

<span data-ttu-id="4ada8-109">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4ada8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ada8-110">備註</span><span class="sxs-lookup"><span data-stu-id="4ada8-110">Remarks</span></span>

<span data-ttu-id="4ada8-111">這個方法會覆寫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4ada8-111">This method overrides the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="4ada8-112">它會解除配置器，並釋放 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 和 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面。</span><span class="sxs-lookup"><span data-stu-id="4ada8-112">It decommits the allocator and releases the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) and [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces.</span></span>

<span data-ttu-id="4ada8-113">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="4ada8-113">If you override this method, call the base-class method from your overriding method.</span></span> <span data-ttu-id="4ada8-114">否則，您可能會造成記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="4ada8-114">Otherwise, you might cause memory leaks.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ada8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ada8-115">Requirements</span></span>



| <span data-ttu-id="4ada8-116">需求</span><span class="sxs-lookup"><span data-stu-id="4ada8-116">Requirement</span></span> | <span data-ttu-id="4ada8-117">值</span><span class="sxs-lookup"><span data-stu-id="4ada8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ada8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4ada8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4ada8-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4ada8-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4ada8-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ada8-120">Library</span></span><br/> | <dl> <span data-ttu-id="4ada8-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4ada8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ada8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ada8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ada8-123">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="4ada8-123">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




