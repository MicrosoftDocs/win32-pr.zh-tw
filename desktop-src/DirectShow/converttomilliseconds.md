---
description: ConvertToMilliseconds 函數會將參考時間轉換成毫秒。
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: 'ConvertToMilliseconds 函式 (Refclock) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984310"
---
# <a name="converttomilliseconds-function"></a><span data-ttu-id="46d56-103">ConvertToMilliseconds 函式</span><span class="sxs-lookup"><span data-stu-id="46d56-103">ConvertToMilliseconds function</span></span>

<span data-ttu-id="46d56-104">`ConvertToMilliseconds`函數會將參考時間轉換成毫秒。</span><span class="sxs-lookup"><span data-stu-id="46d56-104">The `ConvertToMilliseconds` function converts a reference time to milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d56-105">語法</span><span class="sxs-lookup"><span data-stu-id="46d56-105">Syntax</span></span>


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a><span data-ttu-id="46d56-106">參數</span><span class="sxs-lookup"><span data-stu-id="46d56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d56-107">*RT* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="46d56-107">*RT* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="46d56-108">參考時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="46d56-108">Reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d56-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="46d56-109">Return value</span></span>

<span data-ttu-id="46d56-110">傳回轉換為毫秒的參考時間。</span><span class="sxs-lookup"><span data-stu-id="46d56-110">Returns the reference time converted to milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d56-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d56-111">Requirements</span></span>



| <span data-ttu-id="46d56-112">需求</span><span class="sxs-lookup"><span data-stu-id="46d56-112">Requirement</span></span> | <span data-ttu-id="46d56-113">值</span><span class="sxs-lookup"><span data-stu-id="46d56-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d56-114">標頭</span><span class="sxs-lookup"><span data-stu-id="46d56-114">Header</span></span><br/>  | <dl> <span data-ttu-id="46d56-115"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="46d56-115"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46d56-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="46d56-116">Library</span></span><br/> | <dl> <span data-ttu-id="46d56-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="46d56-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d56-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d56-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d56-119">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="46d56-119">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




