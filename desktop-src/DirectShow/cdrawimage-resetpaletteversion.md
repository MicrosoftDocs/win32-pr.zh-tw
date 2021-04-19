---
description: ResetPaletteVersion 方法會重設元件的版本。 如果擁有篩選器的 pin 重新連接，請呼叫這個方法。
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: 'CDrawImage. ResetPaletteVersion 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995260"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="fc29c-104">CDrawImage. ResetPaletteVersion 方法</span><span class="sxs-lookup"><span data-stu-id="fc29c-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="fc29c-105">`ResetPaletteVersion`方法會重設元件的版本。</span><span class="sxs-lookup"><span data-stu-id="fc29c-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="fc29c-106">如果擁有篩選器的 pin 重新連接，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="fc29c-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc29c-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc29c-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="fc29c-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc29c-108">Parameters</span></span>

<span data-ttu-id="fc29c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fc29c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc29c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc29c-110">Return value</span></span>

<span data-ttu-id="fc29c-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fc29c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc29c-112">備註</span><span class="sxs-lookup"><span data-stu-id="fc29c-112">Remarks</span></span>

<span data-ttu-id="fc29c-113">這個方法會將 **m \_ PaletteVersion** 的值設定為預先定義的常數（ **調色板 \_ 版本**）。</span><span class="sxs-lookup"><span data-stu-id="fc29c-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc29c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc29c-114">Requirements</span></span>



| <span data-ttu-id="fc29c-115">需求</span><span class="sxs-lookup"><span data-stu-id="fc29c-115">Requirement</span></span> | <span data-ttu-id="fc29c-116">值</span><span class="sxs-lookup"><span data-stu-id="fc29c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc29c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fc29c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fc29c-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc29c-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc29c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc29c-119">Library</span></span><br/> | <dl> <span data-ttu-id="fc29c-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc29c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc29c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc29c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc29c-122">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="fc29c-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="fc29c-123">**CDrawImage::GetPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="fc29c-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="fc29c-124">**CDrawImage::IncrementPaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="fc29c-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




