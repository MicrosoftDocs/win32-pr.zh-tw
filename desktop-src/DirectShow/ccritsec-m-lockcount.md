---
description: 此物件上的未完成鎖定數目。
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'CCritSec：： m_lockCount 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999286"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="056e4-103">CCritSec：： m \_ lockCount 成員</span><span class="sxs-lookup"><span data-stu-id="056e4-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="056e4-104">此物件上的未完成鎖定數目。</span><span class="sxs-lookup"><span data-stu-id="056e4-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="056e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="056e4-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="056e4-106">備註</span><span class="sxs-lookup"><span data-stu-id="056e4-106">Remarks</span></span>

<span data-ttu-id="056e4-107">這個成員變數只會在基類的 debug 版本中定義。</span><span class="sxs-lookup"><span data-stu-id="056e4-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="056e4-108">[重要區段調試](critical-section-debugging-functions.md)函式函數會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="056e4-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="056e4-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="056e4-109">Requirements</span></span>



| <span data-ttu-id="056e4-110">需求</span><span class="sxs-lookup"><span data-stu-id="056e4-110">Requirement</span></span> | <span data-ttu-id="056e4-111">值</span><span class="sxs-lookup"><span data-stu-id="056e4-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056e4-112">標頭</span><span class="sxs-lookup"><span data-stu-id="056e4-112">Header</span></span><br/>  | <dl> <span data-ttu-id="056e4-113"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="056e4-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="056e4-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="056e4-114">Library</span></span><br/> | <dl> <span data-ttu-id="056e4-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="056e4-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="056e4-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="056e4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056e4-117">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="056e4-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




