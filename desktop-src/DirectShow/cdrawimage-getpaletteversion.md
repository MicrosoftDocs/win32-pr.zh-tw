---
description: GetPaletteVersion 方法會抓取目前的調色板版本。
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: 'CDrawImage. GetPaletteVersion 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987948"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="28a6e-103">CDrawImage. GetPaletteVersion 方法</span><span class="sxs-lookup"><span data-stu-id="28a6e-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="28a6e-104">方法會抓取 `GetPaletteVersion` 目前的調色板版本。</span><span class="sxs-lookup"><span data-stu-id="28a6e-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a6e-105">語法</span><span class="sxs-lookup"><span data-stu-id="28a6e-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="28a6e-106">參數</span><span class="sxs-lookup"><span data-stu-id="28a6e-106">Parameters</span></span>

<span data-ttu-id="28a6e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="28a6e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28a6e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="28a6e-108">Return value</span></span>

<span data-ttu-id="28a6e-109">傳回 **m \_ PaletteVersion** 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="28a6e-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a6e-110">備註</span><span class="sxs-lookup"><span data-stu-id="28a6e-110">Remarks</span></span>

<span data-ttu-id="28a6e-111">只有當配置器是 [**CImageAllocator**](cimageallocator.md) 物件時，這個方法所傳回的值才適用。</span><span class="sxs-lookup"><span data-stu-id="28a6e-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a6e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="28a6e-112">Requirements</span></span>



| <span data-ttu-id="28a6e-113">需求</span><span class="sxs-lookup"><span data-stu-id="28a6e-113">Requirement</span></span> | <span data-ttu-id="28a6e-114">值</span><span class="sxs-lookup"><span data-stu-id="28a6e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a6e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="28a6e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="28a6e-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="28a6e-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28a6e-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="28a6e-117">Library</span></span><br/> | <dl> <span data-ttu-id="28a6e-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="28a6e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a6e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28a6e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a6e-120">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="28a6e-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="28a6e-121">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="28a6e-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="28a6e-122">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="28a6e-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




