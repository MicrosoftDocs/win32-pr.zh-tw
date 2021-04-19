---
description: 搜尋功能。
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'CSourceSeeking：： m_dwSeekingCaps 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992588"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="34b2c-103">CSourceSeeking：： m \_ dwSeekingCaps 成員</span><span class="sxs-lookup"><span data-stu-id="34b2c-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="34b2c-104">搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="34b2c-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b2c-105">語法</span><span class="sxs-lookup"><span data-stu-id="34b2c-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="34b2c-106">備註</span><span class="sxs-lookup"><span data-stu-id="34b2c-106">Remarks</span></span>

<span data-ttu-id="34b2c-107">依預設，此值會設定為下列旗標的位元組合：</span><span class="sxs-lookup"><span data-stu-id="34b2c-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="34b2c-108">\_搜尋 \_ CanSeekForwards</span><span class="sxs-lookup"><span data-stu-id="34b2c-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="34b2c-109">\_搜尋 \_ CanSeekBackwards</span><span class="sxs-lookup"><span data-stu-id="34b2c-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="34b2c-110">\_搜尋 \_ CanSeekAbsolute</span><span class="sxs-lookup"><span data-stu-id="34b2c-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="34b2c-111">\_搜尋 \_ CanGetStopPos</span><span class="sxs-lookup"><span data-stu-id="34b2c-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="34b2c-112">\_搜尋 \_ CanGetDuration</span><span class="sxs-lookup"><span data-stu-id="34b2c-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="34b2c-113">如果篩選支援一組不同的功能，請覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="34b2c-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b2c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="34b2c-114">Requirements</span></span>



| <span data-ttu-id="34b2c-115">需求</span><span class="sxs-lookup"><span data-stu-id="34b2c-115">Requirement</span></span> | <span data-ttu-id="34b2c-116">值</span><span class="sxs-lookup"><span data-stu-id="34b2c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b2c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="34b2c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="34b2c-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="34b2c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34b2c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="34b2c-119">Library</span></span><br/> | <dl> <span data-ttu-id="34b2c-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="34b2c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b2c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34b2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b2c-122">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="34b2c-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




