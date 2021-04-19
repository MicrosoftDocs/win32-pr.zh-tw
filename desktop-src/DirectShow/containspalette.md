---
description: ContainsPalette 函式會判斷指定的 VIDEOINFOHEADER 結構是否包含調色板。
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: 'ContainsPalette 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999282"
---
# <a name="containspalette-function"></a><span data-ttu-id="3144e-103">ContainsPalette 函式</span><span class="sxs-lookup"><span data-stu-id="3144e-103">ContainsPalette function</span></span>

<span data-ttu-id="3144e-104">**ContainsPalette** 函式會判斷指定的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構是否包含調色板。</span><span class="sxs-lookup"><span data-stu-id="3144e-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="3144e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3144e-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="3144e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3144e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3144e-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="3144e-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3144e-108">[**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3144e-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3144e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3144e-109">Return value</span></span>

<span data-ttu-id="3144e-110">如果 bitdepth 為8或小於 (**bmiHeader. biBitCount**) ，或色彩索引的數目大於零 (**bmiHeader. biClrUsed**) ，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3144e-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="3144e-111">否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3144e-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3144e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3144e-112">Requirements</span></span>



| <span data-ttu-id="3144e-113">需求</span><span class="sxs-lookup"><span data-stu-id="3144e-113">Requirement</span></span> | <span data-ttu-id="3144e-114">值</span><span class="sxs-lookup"><span data-stu-id="3144e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3144e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="3144e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="3144e-116"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3144e-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3144e-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="3144e-117">Library</span></span><br/> | <dl> <span data-ttu-id="3144e-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3144e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3144e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3144e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3144e-120">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="3144e-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




