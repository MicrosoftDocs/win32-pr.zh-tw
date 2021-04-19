---
description: 信號的控制碼，由執行緒用來等候樣本。
ms.assetid: c64a7221-6eea-459b-b306-e6d547a233b2
title: 'COutputQueue：： m_hSem 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hSem
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 262c9997a681b8f9ba332efe1b9fb225c112b591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983012"
---
# <a name="coutputqueuem_hsem-member"></a><span data-ttu-id="97379-103">COutputQueue：： m \_ hSem 成員</span><span class="sxs-lookup"><span data-stu-id="97379-103">COutputQueue::m\_hSem member</span></span>

<span data-ttu-id="97379-104">信號的控制碼，由執行緒用來等候樣本。</span><span class="sxs-lookup"><span data-stu-id="97379-104">Handle to a semaphore, used by the thread to wait for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="97379-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97379-105">Syntax</span></span>


```C++
HANDLE m_hSem;
```



## <a name="requirements"></a><span data-ttu-id="97379-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="97379-106">Requirements</span></span>



| <span data-ttu-id="97379-107">需求</span><span class="sxs-lookup"><span data-stu-id="97379-107">Requirement</span></span> | <span data-ttu-id="97379-108">值</span><span class="sxs-lookup"><span data-stu-id="97379-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97379-109">標頭</span><span class="sxs-lookup"><span data-stu-id="97379-109">Header</span></span><br/>  | <dl> <span data-ttu-id="97379-110"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="97379-110"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="97379-111">程式庫</span><span class="sxs-lookup"><span data-stu-id="97379-111">Library</span></span><br/> | <dl> <span data-ttu-id="97379-112"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="97379-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97379-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97379-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97379-114">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="97379-114">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




