---
description: GetPin 方法會抓取 pin。 CEnumPins 類別會呼叫這個方法來列舉篩選上的釘選。
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: 'CBaseFilter. GetPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999254"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="0f019-104">CBaseFilter. GetPin 方法</span><span class="sxs-lookup"><span data-stu-id="0f019-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="0f019-105">**GetPin** 方法會抓取 pin。</span><span class="sxs-lookup"><span data-stu-id="0f019-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="0f019-106">[**CEnumPins**](cenumpins.md)類別會呼叫這個方法來列舉篩選上的釘選。</span><span class="sxs-lookup"><span data-stu-id="0f019-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f019-107">語法</span><span class="sxs-lookup"><span data-stu-id="0f019-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0f019-108">參數</span><span class="sxs-lookup"><span data-stu-id="0f019-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f019-109">*n*</span><span class="sxs-lookup"><span data-stu-id="0f019-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="0f019-110">以零為基底的釘選索引。</span><span class="sxs-lookup"><span data-stu-id="0f019-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f019-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f019-111">Return value</span></span>

<span data-ttu-id="0f019-112">傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選。</span><span class="sxs-lookup"><span data-stu-id="0f019-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f019-113">備註</span><span class="sxs-lookup"><span data-stu-id="0f019-113">Remarks</span></span>

<span data-ttu-id="0f019-114">您必須在衍生類別中執行此純虛擬方法。</span><span class="sxs-lookup"><span data-stu-id="0f019-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="0f019-115">傳回這個篩選的第 *n* 個圖釘的指標，從零開始編制索引。</span><span class="sxs-lookup"><span data-stu-id="0f019-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="0f019-116">只要順序是固定的，您就可以選擇任意的索引編制順序。</span><span class="sxs-lookup"><span data-stu-id="0f019-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="0f019-117">如果篩選準則加入或刪除 pin，或在執行時間針對某個其他原因進行順序變更，請呼叫 [**CBaseFilter：： IncrementPinVersion**](cbasefilter-incrementpinversion.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0f019-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f019-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f019-118">Requirements</span></span>



| <span data-ttu-id="0f019-119">需求</span><span class="sxs-lookup"><span data-stu-id="0f019-119">Requirement</span></span> | <span data-ttu-id="0f019-120">值</span><span class="sxs-lookup"><span data-stu-id="0f019-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f019-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0f019-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0f019-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0f019-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0f019-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f019-123">Library</span></span><br/> | <dl> <span data-ttu-id="0f019-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0f019-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f019-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f019-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f019-126">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="0f019-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




