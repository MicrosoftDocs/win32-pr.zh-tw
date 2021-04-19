---
description: 重要區段物件的指標。
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'CSourceSeeking：： m_pLock 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994758"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="7436f-103">CSourceSeeking：： m \_ pLock 成員</span><span class="sxs-lookup"><span data-stu-id="7436f-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="7436f-104">重要區段物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7436f-104">Pointer to a critical section object.</span></span> <span data-ttu-id="7436f-105">`CSourceSeeking`類別會使用此重要區段來同步處理開始和停止時間、持續時間和速率變數的存取。</span><span class="sxs-lookup"><span data-stu-id="7436f-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="7436f-106">此變數會在函式方法中初始化。請參閱 [**CSourceSeeking：： CSourceSeeking**](csourceseeking-csourceseeking.md)。</span><span class="sxs-lookup"><span data-stu-id="7436f-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7436f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7436f-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="7436f-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="7436f-108">Requirements</span></span>



| <span data-ttu-id="7436f-109">需求</span><span class="sxs-lookup"><span data-stu-id="7436f-109">Requirement</span></span> | <span data-ttu-id="7436f-110">值</span><span class="sxs-lookup"><span data-stu-id="7436f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7436f-111">標頭</span><span class="sxs-lookup"><span data-stu-id="7436f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="7436f-112"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7436f-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7436f-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="7436f-113">Library</span></span><br/> | <dl> <span data-ttu-id="7436f-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7436f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7436f-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7436f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7436f-116">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="7436f-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




