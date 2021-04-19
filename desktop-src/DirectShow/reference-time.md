---
description: 參考 \_ 時間資料類型會定義 DirectShow 中參考時間的單位。 參考時間的每個單位為100毫微秒。
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: 'REFERENCE_TIME (Strmif) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983188"
---
# <a name="reference_time"></a><span data-ttu-id="b7bad-104">參考 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="b7bad-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="b7bad-105">**參考 \_ 時間** 資料類型會定義 DirectShow 中參考時間的單位。</span><span class="sxs-lookup"><span data-stu-id="b7bad-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="b7bad-106">參考時間的每個單位為100毫微秒。</span><span class="sxs-lookup"><span data-stu-id="b7bad-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="b7bad-107">備註</span><span class="sxs-lookup"><span data-stu-id="b7bad-107">Remarks</span></span>

<span data-ttu-id="b7bad-108">**參考 \_ 時間** 資料類型是64位整數。</span><span class="sxs-lookup"><span data-stu-id="b7bad-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="b7bad-109">參考時間通常是以下列其中一個基準來測量：</span><span class="sxs-lookup"><span data-stu-id="b7bad-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="b7bad-110">絕對時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="b7bad-110">An absolute clock time.</span></span> <span data-ttu-id="b7bad-111">在此情況下，基準將視時鐘的執行而定。</span><span class="sxs-lookup"><span data-stu-id="b7bad-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="b7bad-112">如需詳細資訊，請參閱 [參考時鐘](reference-clocks.md)。</span><span class="sxs-lookup"><span data-stu-id="b7bad-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="b7bad-113">相對於開始播放。</span><span class="sxs-lookup"><span data-stu-id="b7bad-113">Relative to the start of playback.</span></span>

<span data-ttu-id="b7bad-114">如需參考時間的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="b7bad-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7bad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7bad-115">Requirements</span></span>



| <span data-ttu-id="b7bad-116">需求</span><span class="sxs-lookup"><span data-stu-id="b7bad-116">Requirement</span></span> | <span data-ttu-id="b7bad-117">值</span><span class="sxs-lookup"><span data-stu-id="b7bad-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bad-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b7bad-118">Header</span></span><br/> | <dl> <span data-ttu-id="b7bad-119"><dt>Strmif (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="b7bad-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7bad-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7bad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bad-121">DirectShow 資料類型</span><span class="sxs-lookup"><span data-stu-id="b7bad-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




