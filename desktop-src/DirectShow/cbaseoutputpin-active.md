---
description: 使用中的方法會通知釘選篩選現在為使用中狀態。
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
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985574"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="4a013-103">CBaseOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="4a013-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="4a013-104">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="4a013-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a013-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a013-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="4a013-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a013-106">Parameters</span></span>

<span data-ttu-id="4a013-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4a013-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a013-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a013-108">Return value</span></span>

<span data-ttu-id="4a013-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4a013-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a013-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="4a013-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4a013-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4a013-111">Return code</span></span>                                                                                          | <span data-ttu-id="4a013-112">Description</span><span class="sxs-lookup"><span data-stu-id="4a013-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4a013-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4a013-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="4a013-114">成功。</span><span class="sxs-lookup"><span data-stu-id="4a013-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="4a013-115"><dt>**VFW \_ E \_ NO 配置器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a013-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="4a013-116">沒有配置器可供使用。</span><span class="sxs-lookup"><span data-stu-id="4a013-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a013-117">備註</span><span class="sxs-lookup"><span data-stu-id="4a013-117">Remarks</span></span>

<span data-ttu-id="4a013-118">這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4a013-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="4a013-119">它會在配置器上呼叫 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) 方法，以配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4a013-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="4a013-120">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="4a013-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a013-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a013-121">Requirements</span></span>



| <span data-ttu-id="4a013-122">需求</span><span class="sxs-lookup"><span data-stu-id="4a013-122">Requirement</span></span> | <span data-ttu-id="4a013-123">值</span><span class="sxs-lookup"><span data-stu-id="4a013-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a013-124">標頭</span><span class="sxs-lookup"><span data-stu-id="4a013-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4a013-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4a013-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a013-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a013-126">Library</span></span><br/> | <dl> <span data-ttu-id="4a013-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4a013-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a013-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a013-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a013-129">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="4a013-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




