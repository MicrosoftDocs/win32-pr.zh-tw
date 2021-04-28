---
description: CImagePalette。 CImagePalette 函式-函數方法。
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: 'CImagePalette. CImagePalette (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085676"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="e3714-103">CImagePalette. CImagePalette 函數</span><span class="sxs-lookup"><span data-stu-id="e3714-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="e3714-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="e3714-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3714-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3714-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="e3714-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3714-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3714-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="e3714-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="e3714-108">擁有篩選準則的指標。</span><span class="sxs-lookup"><span data-stu-id="e3714-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="e3714-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="e3714-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="e3714-110">**CBaseWindow** 物件的指標，此物件會管理要實現調色板的視窗。</span><span class="sxs-lookup"><span data-stu-id="e3714-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="e3714-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e3714-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3714-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="e3714-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="e3714-113">**CDrawImage** 物件的指標，該物件會繪製影片影像。</span><span class="sxs-lookup"><span data-stu-id="e3714-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="e3714-114">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e3714-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3714-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3714-115">Requirements</span></span>



| <span data-ttu-id="e3714-116">需求</span><span class="sxs-lookup"><span data-stu-id="e3714-116">Requirement</span></span> | <span data-ttu-id="e3714-117">值</span><span class="sxs-lookup"><span data-stu-id="e3714-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3714-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e3714-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e3714-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e3714-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3714-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3714-120">Library</span></span><br/> | <dl> <span data-ttu-id="e3714-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e3714-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3714-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3714-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3714-123">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="e3714-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




