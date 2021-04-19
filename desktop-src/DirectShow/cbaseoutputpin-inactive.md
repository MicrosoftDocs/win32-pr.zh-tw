---
description: 非使用中的方法會通知 pin，篩選已不再有效。
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: 'CBaseOutputPin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afec15e295e5c14cfb3d9efa6e733d1dc288b319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990990"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="b36cc-103">CBaseOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="b36cc-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="b36cc-104">`Inactive`方法會通知 pin，篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="b36cc-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="b36cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="b36cc-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="b36cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="b36cc-106">Parameters</span></span>

<span data-ttu-id="b36cc-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b36cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b36cc-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b36cc-108">Return value</span></span>

<span data-ttu-id="b36cc-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b36cc-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b36cc-110">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="b36cc-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b36cc-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b36cc-111">Return code</span></span>                                                                                          | <span data-ttu-id="b36cc-112">Description</span><span class="sxs-lookup"><span data-stu-id="b36cc-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b36cc-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b36cc-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="b36cc-114">成功。</span><span class="sxs-lookup"><span data-stu-id="b36cc-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="b36cc-115"><dt>**VFW \_ E \_ NO 配置器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b36cc-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="b36cc-116">沒有記憶體配置器可用。</span><span class="sxs-lookup"><span data-stu-id="b36cc-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b36cc-117">備註</span><span class="sxs-lookup"><span data-stu-id="b36cc-117">Remarks</span></span>

<span data-ttu-id="b36cc-118">這個方法會覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。</span><span class="sxs-lookup"><span data-stu-id="b36cc-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="b36cc-119">它會呼叫 [**IMemAllocator：:D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) 方法來取消認可記憶體配置器。</span><span class="sxs-lookup"><span data-stu-id="b36cc-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="b36cc-120">如果您覆寫這個方法，請從您的覆寫方法中呼叫基類方法。</span><span class="sxs-lookup"><span data-stu-id="b36cc-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36cc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b36cc-121">Requirements</span></span>



| <span data-ttu-id="b36cc-122">需求</span><span class="sxs-lookup"><span data-stu-id="b36cc-122">Requirement</span></span> | <span data-ttu-id="b36cc-123">值</span><span class="sxs-lookup"><span data-stu-id="b36cc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b36cc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b36cc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b36cc-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b36cc-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b36cc-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b36cc-126">Library</span></span><br/> | <dl> <span data-ttu-id="b36cc-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b36cc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b36cc-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b36cc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b36cc-129">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="b36cc-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




