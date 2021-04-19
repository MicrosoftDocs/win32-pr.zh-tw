---
description: 重要區段的指標。
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'CBaseMediaFilter：： m_pLock 成員 (Amfilter .h) '
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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997018"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="78653-103">CBaseMediaFilter：： m \_ pLock 成員</span><span class="sxs-lookup"><span data-stu-id="78653-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="78653-104">重要區段的指標。</span><span class="sxs-lookup"><span data-stu-id="78653-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="78653-105">語法</span><span class="sxs-lookup"><span data-stu-id="78653-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="78653-106">備註</span><span class="sxs-lookup"><span data-stu-id="78653-106">Remarks</span></span>

<span data-ttu-id="78653-107">重要區段會在狀態轉換期間保留 ([**CBaseMediaFilter：： Run**](cbasemediafilter-run.md)、 [**CBaseMediaFilter：:P ause**](cbasemediafilter-pause.md)、 [**CBaseMediaFilter：： Stop**](cbasemediafilter-stop.md)) 、存取參考時鐘 ([**CBaseMediaFilter：： SetSyncSource**](cbasemediafilter-setsyncsource.md)、 [**CBaseMediaFilter：： GetSyncSource**](cbasemediafilter-getsyncsource.md)) 和 [**CBaseMediaFilter：： IsActive**](cbasemediafilter-isactive.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="78653-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78653-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="78653-108">Requirements</span></span>



| <span data-ttu-id="78653-109">需求</span><span class="sxs-lookup"><span data-stu-id="78653-109">Requirement</span></span> | <span data-ttu-id="78653-110">值</span><span class="sxs-lookup"><span data-stu-id="78653-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78653-111">標頭</span><span class="sxs-lookup"><span data-stu-id="78653-111">Header</span></span><br/>  | <dl> <span data-ttu-id="78653-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="78653-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78653-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="78653-113">Library</span></span><br/> | <dl> <span data-ttu-id="78653-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="78653-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78653-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78653-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78653-116">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="78653-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




