---
description: CBaseOutputPin 方法-使用中的方法會通知釘選篩選現在為使用中狀態。
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: 'CBaseOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096206"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="db706-103">CBaseOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="db706-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="db706-104">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="db706-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="db706-105">語法</span><span class="sxs-lookup"><span data-stu-id="db706-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="db706-106">參數</span><span class="sxs-lookup"><span data-stu-id="db706-106">Parameters</span></span>

<span data-ttu-id="db706-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="db706-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db706-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="db706-108">Return value</span></span>

<span data-ttu-id="db706-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="db706-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="db706-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="db706-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="db706-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db706-111">Return code</span></span>                                                                                          | <span data-ttu-id="db706-112">Description</span><span class="sxs-lookup"><span data-stu-id="db706-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="db706-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="db706-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="db706-114">成功。</span><span class="sxs-lookup"><span data-stu-id="db706-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="db706-115"><dt>**VFW \_ E \_ NO 配置器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db706-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="db706-116">沒有配置器可供使用。</span><span class="sxs-lookup"><span data-stu-id="db706-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db706-117">備註</span><span class="sxs-lookup"><span data-stu-id="db706-117">Remarks</span></span>

<span data-ttu-id="db706-118">這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="db706-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="db706-119">它會在配置器上呼叫 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) 方法，以配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="db706-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="db706-120">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="db706-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db706-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="db706-121">Requirements</span></span>



| <span data-ttu-id="db706-122">需求</span><span class="sxs-lookup"><span data-stu-id="db706-122">Requirement</span></span> | <span data-ttu-id="db706-123">值</span><span class="sxs-lookup"><span data-stu-id="db706-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db706-124">標頭</span><span class="sxs-lookup"><span data-stu-id="db706-124">Header</span></span><br/>  | <dl> <span data-ttu-id="db706-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="db706-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="db706-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="db706-126">Library</span></span><br/> | <dl> <span data-ttu-id="db706-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="db706-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db706-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db706-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db706-129">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="db706-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




