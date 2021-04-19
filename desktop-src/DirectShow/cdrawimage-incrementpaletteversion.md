---
description: IncrementPaletteVersion 方法會遞增元件的版本。 如果媒體類型變更為新的調色盤格式，則呼叫這個方法。
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: 'CDrawImage. IncrementPaletteVersion 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976217"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="15a93-104">CDrawImage. IncrementPaletteVersion 方法</span><span class="sxs-lookup"><span data-stu-id="15a93-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="15a93-105">`IncrementPaletteVersion`方法會遞增元件的版本。</span><span class="sxs-lookup"><span data-stu-id="15a93-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="15a93-106">如果媒體類型變更為新的調色盤格式，則呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="15a93-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a93-107">語法</span><span class="sxs-lookup"><span data-stu-id="15a93-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="15a93-108">參數</span><span class="sxs-lookup"><span data-stu-id="15a93-108">Parameters</span></span>

<span data-ttu-id="15a93-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="15a93-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15a93-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="15a93-110">Return value</span></span>

<span data-ttu-id="15a93-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="15a93-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15a93-112">備註</span><span class="sxs-lookup"><span data-stu-id="15a93-112">Remarks</span></span>

<span data-ttu-id="15a93-113">這個方法會遞增 **m \_ PaletteVersion** 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="15a93-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a93-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="15a93-114">Requirements</span></span>



| <span data-ttu-id="15a93-115">需求</span><span class="sxs-lookup"><span data-stu-id="15a93-115">Requirement</span></span> | <span data-ttu-id="15a93-116">值</span><span class="sxs-lookup"><span data-stu-id="15a93-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15a93-117">標頭</span><span class="sxs-lookup"><span data-stu-id="15a93-117">Header</span></span><br/>  | <dl> <span data-ttu-id="15a93-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="15a93-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15a93-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="15a93-119">Library</span></span><br/> | <dl> <span data-ttu-id="15a93-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="15a93-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a93-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15a93-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a93-122">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="15a93-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="15a93-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="15a93-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="15a93-124">**CDrawImage::ResetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="15a93-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




