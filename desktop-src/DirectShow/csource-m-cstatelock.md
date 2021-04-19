---
description: 保護篩選狀態的重要區段物件。 CSource：:p StateLock helper 方法會傳回這個成員變數的指標。
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: 'CSource：： m_cStateLock 成員 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983988"
---
# <a name="csourcem_cstatelock-member"></a><span data-ttu-id="18973-104">CSource：： m \_ cStateLock 成員</span><span class="sxs-lookup"><span data-stu-id="18973-104">CSource::m\_cStateLock member</span></span>

<span data-ttu-id="18973-105">保護篩選狀態的重要區段物件。</span><span class="sxs-lookup"><span data-stu-id="18973-105">Critical section object that protects the filter state.</span></span> <span data-ttu-id="18973-106">[**CSource：:P statelock**](csource--pstatelock.md) helper 方法會傳回這個成員變數的指標。</span><span class="sxs-lookup"><span data-stu-id="18973-106">The [**CSource::pStateLock**](csource--pstatelock.md) helper method returns a pointer to this member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="18973-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18973-107">Syntax</span></span>


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a><span data-ttu-id="18973-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="18973-108">Requirements</span></span>



| <span data-ttu-id="18973-109">需求</span><span class="sxs-lookup"><span data-stu-id="18973-109">Requirement</span></span> | <span data-ttu-id="18973-110">值</span><span class="sxs-lookup"><span data-stu-id="18973-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18973-111">標頭</span><span class="sxs-lookup"><span data-stu-id="18973-111">Header</span></span><br/>  | <dl> <span data-ttu-id="18973-112"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="18973-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="18973-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="18973-113">Library</span></span><br/> | <dl> <span data-ttu-id="18973-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="18973-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18973-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18973-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18973-116">**CSource 類別**</span><span class="sxs-lookup"><span data-stu-id="18973-116">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




