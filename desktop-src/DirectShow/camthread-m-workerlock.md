---
description: 鎖定執行緒之間共用之資料的重要區段。
ms.assetid: 87966d7d-6677-462f-93bc-fedda7f0bdcf
title: 'CAMThread：： m_WorkerLock 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WorkerLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fce6c2ff2a7857f6cb69ce3bb92fe2b6f24bcbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998891"
---
# <a name="camthreadm_workerlock-member"></a><span data-ttu-id="997fc-103">CAMThread：： m \_ WorkerLock 成員</span><span class="sxs-lookup"><span data-stu-id="997fc-103">CAMThread::m\_WorkerLock member</span></span>

<span data-ttu-id="997fc-104">鎖定執行緒之間共用之資料的重要區段。</span><span class="sxs-lookup"><span data-stu-id="997fc-104">Critical section that locks data shared among threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="997fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="997fc-105">Syntax</span></span>


```C++
CCritSec m_WorkerLock;
```



## <a name="requirements"></a><span data-ttu-id="997fc-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="997fc-106">Requirements</span></span>



| <span data-ttu-id="997fc-107">需求</span><span class="sxs-lookup"><span data-stu-id="997fc-107">Requirement</span></span> | <span data-ttu-id="997fc-108">值</span><span class="sxs-lookup"><span data-stu-id="997fc-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="997fc-109">標頭</span><span class="sxs-lookup"><span data-stu-id="997fc-109">Header</span></span><br/>  | <dl> <span data-ttu-id="997fc-110"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="997fc-110"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="997fc-111">程式庫</span><span class="sxs-lookup"><span data-stu-id="997fc-111">Library</span></span><br/> | <dl> <span data-ttu-id="997fc-112"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="997fc-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997fc-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="997fc-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997fc-114">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="997fc-114">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




