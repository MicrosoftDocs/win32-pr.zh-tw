---
description: MakePalette 方法會從色彩表以影片格式建立邏輯調色板。
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: 'CImagePalette. MakePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989699"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="92526-103">CImagePalette. MakePalette 方法</span><span class="sxs-lookup"><span data-stu-id="92526-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="92526-104">`MakePalette`方法會從色彩表以影片格式建立邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="92526-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="92526-105">語法</span><span class="sxs-lookup"><span data-stu-id="92526-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="92526-106">參數</span><span class="sxs-lookup"><span data-stu-id="92526-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92526-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="92526-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="92526-108">包含 color 資料表之 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="92526-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="92526-109">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="92526-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="92526-110">字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="92526-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="92526-111">若要使用主顯示器裝置，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="92526-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92526-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="92526-112">Return value</span></span>

<span data-ttu-id="92526-113">如果成功，則傳回檔色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="92526-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="92526-114">否則，會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="92526-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92526-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="92526-115">Requirements</span></span>



| <span data-ttu-id="92526-116">需求</span><span class="sxs-lookup"><span data-stu-id="92526-116">Requirement</span></span> | <span data-ttu-id="92526-117">值</span><span class="sxs-lookup"><span data-stu-id="92526-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92526-118">標頭</span><span class="sxs-lookup"><span data-stu-id="92526-118">Header</span></span><br/>  | <dl> <span data-ttu-id="92526-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="92526-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92526-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="92526-120">Library</span></span><br/> | <dl> <span data-ttu-id="92526-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="92526-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92526-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92526-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92526-123">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="92526-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




