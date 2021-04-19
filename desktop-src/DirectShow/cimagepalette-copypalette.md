---
description: CopyPalette 方法會將元件從任何 VIDEOINFO 結構複製到任何調色盤 VIDEOINFO 結構。
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: 'CImagePalette. CopyPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997736"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="9846f-103">CImagePalette. CopyPalette 方法</span><span class="sxs-lookup"><span data-stu-id="9846f-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="9846f-104">`CopyPalette`方法會將 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的元件複製到任何調色盤 **VIDEOINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="9846f-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9846f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9846f-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="9846f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9846f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9846f-107">*.Psrc*</span><span class="sxs-lookup"><span data-stu-id="9846f-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="9846f-108">來源媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="9846f-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="9846f-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="9846f-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="9846f-110">目的地媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="9846f-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9846f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9846f-111">Return value</span></span>

<span data-ttu-id="9846f-112">\_如果已複製元件，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="9846f-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="9846f-113">\_如果來源或目的地媒體類型沒有調色板，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="9846f-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="9846f-114">備註</span><span class="sxs-lookup"><span data-stu-id="9846f-114">Remarks</span></span>

<span data-ttu-id="9846f-115">*PDest* 媒體類型必須是調色盤格式，且色彩深度為8位或更少。</span><span class="sxs-lookup"><span data-stu-id="9846f-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="9846f-116">*.Psrc* 媒體類型可以是任何具有調色板的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)類型，包括具有調色板專案的 YUV 和真色彩格式。</span><span class="sxs-lookup"><span data-stu-id="9846f-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="9846f-117">方法會將 *.psrc* 中的調色板專案複製到新的調色板，並將新的調色板附加至 *pDest*。</span><span class="sxs-lookup"><span data-stu-id="9846f-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9846f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9846f-118">Requirements</span></span>



| <span data-ttu-id="9846f-119">需求</span><span class="sxs-lookup"><span data-stu-id="9846f-119">Requirement</span></span> | <span data-ttu-id="9846f-120">值</span><span class="sxs-lookup"><span data-stu-id="9846f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9846f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9846f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9846f-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9846f-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9846f-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="9846f-123">Library</span></span><br/> | <dl> <span data-ttu-id="9846f-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9846f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9846f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9846f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9846f-126">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="9846f-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




