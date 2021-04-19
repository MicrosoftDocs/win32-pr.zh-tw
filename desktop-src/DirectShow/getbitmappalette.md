---
description: GetBitmapPalette 函數會傳回 VIDEOINFOHEADER 結構中的第一個調色板專案。
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: 'GetBitmapPalette 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999233"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="baa31-103">GetBitmapPalette 函式</span><span class="sxs-lookup"><span data-stu-id="baa31-103">GetBitmapPalette function</span></span>

<span data-ttu-id="baa31-104">函數會傳回 `GetBitmapPalette` [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構中的第一個調色板專案。</span><span class="sxs-lookup"><span data-stu-id="baa31-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa31-105">語法</span><span class="sxs-lookup"><span data-stu-id="baa31-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="baa31-106">參數</span><span class="sxs-lookup"><span data-stu-id="baa31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa31-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="baa31-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="baa31-108">[**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="baa31-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa31-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="baa31-109">Return value</span></span>

<span data-ttu-id="baa31-110">傳回第一個調色板專案的指標。</span><span class="sxs-lookup"><span data-stu-id="baa31-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa31-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="baa31-111">Requirements</span></span>



| <span data-ttu-id="baa31-112">需求</span><span class="sxs-lookup"><span data-stu-id="baa31-112">Requirement</span></span> | <span data-ttu-id="baa31-113">值</span><span class="sxs-lookup"><span data-stu-id="baa31-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa31-114">標頭</span><span class="sxs-lookup"><span data-stu-id="baa31-114">Header</span></span><br/>  | <dl> <span data-ttu-id="baa31-115"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="baa31-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="baa31-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="baa31-116">Library</span></span><br/> | <dl> <span data-ttu-id="baa31-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="baa31-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




