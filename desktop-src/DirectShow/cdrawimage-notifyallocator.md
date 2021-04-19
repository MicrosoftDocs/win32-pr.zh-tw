---
description: NotifyAllocator 方法會通知 CDrawImage 物件，連接的配置器是否為 CImageAllocator 物件。
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: 'CDrawImage. NotifyAllocator 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996027"
---
# <a name="cdrawimagenotifyallocator-method"></a><span data-ttu-id="1c87d-103">CDrawImage. NotifyAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="1c87d-103">CDrawImage.NotifyAllocator method</span></span>

<span data-ttu-id="1c87d-104">`NotifyAllocator`方法會通知 **CDrawImage** 物件，連接的配置器是否為 [**CImageAllocator**](cimageallocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="1c87d-104">The `NotifyAllocator` method informs the **CDrawImage** object whether the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c87d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c87d-105">Syntax</span></span>


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="1c87d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c87d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c87d-107">*bUsingImageAllocator*</span><span class="sxs-lookup"><span data-stu-id="1c87d-107">*bUsingImageAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="1c87d-108">指出正在使用哪種配置器類型的布林值。</span><span class="sxs-lookup"><span data-stu-id="1c87d-108">Boolean value that indicates what kind of allocator is being used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c87d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c87d-109">Return value</span></span>

<span data-ttu-id="1c87d-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1c87d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c87d-111">備註</span><span class="sxs-lookup"><span data-stu-id="1c87d-111">Remarks</span></span>

<span data-ttu-id="1c87d-112">當 pin 同意配置器之後，擁有篩選應呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1c87d-112">The owning filter should call this method after the pins agree to an allocator.</span></span> <span data-ttu-id="1c87d-113">如果篩選準則知道配置器是 **CImageAllocator** 物件，則應該使用 **TRUE** 值來呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="1c87d-113">If the filter knows the allocator is a **CImageAllocator** object, it should call this method with the value **TRUE**.</span></span> <span data-ttu-id="1c87d-114"> (通常只有當篩選準則擁有有問題的配置器時，才會知道此篩選準則 ) 。否則，它應該使用值 **FALSE** 來呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="1c87d-114">(Typically, the filter will know this only if it owns the allocator in question.) Otherwise, it should call this method with the value **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c87d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c87d-115">Requirements</span></span>



| <span data-ttu-id="1c87d-116">需求</span><span class="sxs-lookup"><span data-stu-id="1c87d-116">Requirement</span></span> | <span data-ttu-id="1c87d-117">值</span><span class="sxs-lookup"><span data-stu-id="1c87d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c87d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1c87d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1c87d-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1c87d-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c87d-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c87d-120">Library</span></span><br/> | <dl> <span data-ttu-id="1c87d-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1c87d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c87d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c87d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c87d-123">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="1c87d-123">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="1c87d-124">**CDrawImage：:D rawImage**</span><span class="sxs-lookup"><span data-stu-id="1c87d-124">**CDrawImage::DrawImage**</span></span>](cdrawimage-drawimage.md)
</dt> </dl>

 

 




