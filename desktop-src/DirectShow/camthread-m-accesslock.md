---
description: 防止其他執行緒存取執行緒的重要區段。
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'CAMThread：： m_AccessLock 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980137"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="979b7-103">CAMThread：： m \_ AccessLock 成員</span><span class="sxs-lookup"><span data-stu-id="979b7-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="979b7-104">防止其他執行緒存取執行緒的重要區段。</span><span class="sxs-lookup"><span data-stu-id="979b7-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="979b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="979b7-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="979b7-106">備註</span><span class="sxs-lookup"><span data-stu-id="979b7-106">Remarks</span></span>

<span data-ttu-id="979b7-107">[**CAMThread：： Create**](camthread-create.md)和 [**CAMThread：： CallWorker**](camthread-callworker.md)方法會保存此鎖定，以序列化執行緒上的作業。</span><span class="sxs-lookup"><span data-stu-id="979b7-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="979b7-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="979b7-108">Requirements</span></span>



| <span data-ttu-id="979b7-109">需求</span><span class="sxs-lookup"><span data-stu-id="979b7-109">Requirement</span></span> | <span data-ttu-id="979b7-110">值</span><span class="sxs-lookup"><span data-stu-id="979b7-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="979b7-111">標頭</span><span class="sxs-lookup"><span data-stu-id="979b7-111">Header</span></span><br/>  | <dl> <span data-ttu-id="979b7-112"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="979b7-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="979b7-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="979b7-113">Library</span></span><br/> | <dl> <span data-ttu-id="979b7-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="979b7-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="979b7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="979b7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979b7-116">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="979b7-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




