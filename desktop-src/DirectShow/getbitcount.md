---
description: GetBitCount 函式會傳回指定的影片子類型所使用的每個圖元位數。 此函數僅適用于未壓縮的 RGB 子類型。
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: 'GetBitCount 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992174"
---
# <a name="getbitcount-function"></a><span data-ttu-id="9a068-104">GetBitCount 函式</span><span class="sxs-lookup"><span data-stu-id="9a068-104">GetBitCount function</span></span>

<span data-ttu-id="9a068-105">此函式會傳回 `GetBitCount` 指定的影片子類型所使用的每個圖元位數。</span><span class="sxs-lookup"><span data-stu-id="9a068-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="9a068-106">此函數僅適用于未壓縮的 RGB 子類型。</span><span class="sxs-lookup"><span data-stu-id="9a068-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a068-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a068-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="9a068-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a068-109">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="9a068-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="9a068-110">影片子類型 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="9a068-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a068-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a068-111">Return value</span></span>

<span data-ttu-id="9a068-112">傳回這個子類型的每個圖元位數，如果無法辨識子類型，則值 **USHRT \_ MAX** 。</span><span class="sxs-lookup"><span data-stu-id="9a068-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a068-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a068-113">Requirements</span></span>



| <span data-ttu-id="9a068-114">需求</span><span class="sxs-lookup"><span data-stu-id="9a068-114">Requirement</span></span> | <span data-ttu-id="9a068-115">值</span><span class="sxs-lookup"><span data-stu-id="9a068-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a068-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9a068-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9a068-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9a068-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9a068-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a068-118">Library</span></span><br/> | <dl> <span data-ttu-id="9a068-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9a068-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a068-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a068-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a068-121">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="9a068-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




