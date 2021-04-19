---
description: GetSubtypeName 函式會取出影片子類型的人類可讀取名稱。
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: 'GetSubtypeName 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995016"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="ef8d3-103">GetSubtypeName 函式</span><span class="sxs-lookup"><span data-stu-id="ef8d3-103">GetSubtypeName function</span></span>

<span data-ttu-id="ef8d3-104">函 `GetSubtypeName` 式會抓取影片子類型的人類可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="ef8d3-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef8d3-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="ef8d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef8d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8d3-107">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="ef8d3-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="ef8d3-108">影片子類型 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="ef8d3-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8d3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef8d3-109">Return value</span></span>

<span data-ttu-id="ef8d3-110">傳回包含名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="ef8d3-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8d3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef8d3-111">Requirements</span></span>



| <span data-ttu-id="ef8d3-112">需求</span><span class="sxs-lookup"><span data-stu-id="ef8d3-112">Requirement</span></span> | <span data-ttu-id="ef8d3-113">值</span><span class="sxs-lookup"><span data-stu-id="ef8d3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8d3-114">標頭</span><span class="sxs-lookup"><span data-stu-id="ef8d3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ef8d3-115"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ef8d3-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ef8d3-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef8d3-116">Library</span></span><br/> | <dl> <span data-ttu-id="ef8d3-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ef8d3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8d3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef8d3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8d3-119">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="ef8d3-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




