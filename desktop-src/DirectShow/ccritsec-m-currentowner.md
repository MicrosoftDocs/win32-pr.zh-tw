---
description: 擁有線程的執行緒識別碼。
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'CCritSec：： m_currentOwner 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984847"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="d73ef-103">CCritSec：： m \_ currentOwner 成員</span><span class="sxs-lookup"><span data-stu-id="d73ef-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="d73ef-104">擁有線程的執行緒識別碼。</span><span class="sxs-lookup"><span data-stu-id="d73ef-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="d73ef-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="d73ef-106">備註</span><span class="sxs-lookup"><span data-stu-id="d73ef-106">Remarks</span></span>

<span data-ttu-id="d73ef-107">這個成員變數只會在基類的 debug 版本中定義。</span><span class="sxs-lookup"><span data-stu-id="d73ef-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="d73ef-108">[重要區段調試函數](critical-section-debugging-functions.md)會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="d73ef-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73ef-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="d73ef-109">Requirements</span></span>



| <span data-ttu-id="d73ef-110">需求</span><span class="sxs-lookup"><span data-stu-id="d73ef-110">Requirement</span></span> | <span data-ttu-id="d73ef-111">值</span><span class="sxs-lookup"><span data-stu-id="d73ef-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73ef-112">標頭</span><span class="sxs-lookup"><span data-stu-id="d73ef-112">Header</span></span><br/>  | <dl> <span data-ttu-id="d73ef-113"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d73ef-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d73ef-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="d73ef-114">Library</span></span><br/> | <dl> <span data-ttu-id="d73ef-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d73ef-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d73ef-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d73ef-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73ef-117">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="d73ef-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




