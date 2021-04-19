---
description: UsingImageAllocator 方法會指出目前的配置器是否為 CImageAllocator 物件。
ms.assetid: 842bbcbc-2cc8-4e9d-b6c0-e07f7e472ca1
title: 'CDrawImage. UsingImageAllocator 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UsingImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a61b4ece94c9c52a0f769a29ec32a26c08b33ee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987984"
---
# <a name="cdrawimageusingimageallocator-method"></a><span data-ttu-id="1a452-103">CDrawImage. UsingImageAllocator 方法</span><span class="sxs-lookup"><span data-stu-id="1a452-103">CDrawImage.UsingImageAllocator method</span></span>

<span data-ttu-id="1a452-104">`UsingImageAllocator`方法會指出目前的配置器是否為 [**CImageAllocator**](cimageallocator.md)物件。</span><span class="sxs-lookup"><span data-stu-id="1a452-104">The `UsingImageAllocator` method indicates whether the current allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a452-105">語法</span><span class="sxs-lookup"><span data-stu-id="1a452-105">Syntax</span></span>


```C++
BOOL UsingImageAllocator();
```



## <a name="parameters"></a><span data-ttu-id="1a452-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a452-106">Parameters</span></span>

<span data-ttu-id="1a452-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1a452-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a452-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a452-108">Return value</span></span>

<span data-ttu-id="1a452-109">如果目前的配置器是 **CImageAllocator** 物件，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1a452-109">Returns **TRUE** if the current allocator is a **CImageAllocator** object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a452-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a452-110">Requirements</span></span>



| <span data-ttu-id="1a452-111">需求</span><span class="sxs-lookup"><span data-stu-id="1a452-111">Requirement</span></span> | <span data-ttu-id="1a452-112">值</span><span class="sxs-lookup"><span data-stu-id="1a452-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a452-113">標頭</span><span class="sxs-lookup"><span data-stu-id="1a452-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1a452-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1a452-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a452-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a452-115">Library</span></span><br/> | <dl> <span data-ttu-id="1a452-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1a452-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a452-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a452-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a452-118">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="1a452-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="1a452-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="1a452-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> </dl>

 

 




