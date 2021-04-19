---
description: GetTrueColorType 函式會取出影片子類型的人類可讀取名稱。
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: 'GetTrueColorType 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987125"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="7e28b-103">GetTrueColorType 函式</span><span class="sxs-lookup"><span data-stu-id="7e28b-103">GetTrueColorType function</span></span>

<span data-ttu-id="7e28b-104">**GetTrueColorType** 函式會取出影片子類型的人類可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="7e28b-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e28b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e28b-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="7e28b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e28b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e28b-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="7e28b-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="7e28b-108">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標，此結構會定義點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7e28b-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e28b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e28b-109">Return value</span></span>

<span data-ttu-id="7e28b-110">傳回 MEDIASUBTYPE \_ RGB555 或 MEDIASUBTYPE \_ RGB565。</span><span class="sxs-lookup"><span data-stu-id="7e28b-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e28b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e28b-111">Requirements</span></span>



| <span data-ttu-id="7e28b-112">需求</span><span class="sxs-lookup"><span data-stu-id="7e28b-112">Requirement</span></span> | <span data-ttu-id="7e28b-113">值</span><span class="sxs-lookup"><span data-stu-id="7e28b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e28b-114">標頭</span><span class="sxs-lookup"><span data-stu-id="7e28b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7e28b-115"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7e28b-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7e28b-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e28b-116">Library</span></span><br/> | <dl> <span data-ttu-id="7e28b-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7e28b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e28b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e28b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e28b-119">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="7e28b-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




