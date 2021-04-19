---
description: 保護封鎖狀態的重要區段。
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'CDynamicOutputPin：： m_BlockStateLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978703"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="c174e-103">CDynamicOutputPin：： m \_ BlockStateLock 成員</span><span class="sxs-lookup"><span data-stu-id="c174e-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="c174e-104">保護封鎖狀態的重要區段。</span><span class="sxs-lookup"><span data-stu-id="c174e-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c174e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c174e-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="c174e-106">備註</span><span class="sxs-lookup"><span data-stu-id="c174e-106">Remarks</span></span>

<span data-ttu-id="c174e-107">使用下列任何成員變數之前，請先保留此重要區段：</span><span class="sxs-lookup"><span data-stu-id="c174e-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="c174e-108">**CDynamicOutputPin：： m \_ BlockState**</span><span class="sxs-lookup"><span data-stu-id="c174e-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="c174e-109">**CDynamicOutputPin：： m \_ dwBlockCallerThreadID**</span><span class="sxs-lookup"><span data-stu-id="c174e-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="c174e-110">**CDynamicOutputPin：： m \_ dwNumOutstandingOutputPinUsers**</span><span class="sxs-lookup"><span data-stu-id="c174e-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="c174e-111">**CDynamicOutputPin：： m \_ hNotifyCallerPinBlockedEvent**</span><span class="sxs-lookup"><span data-stu-id="c174e-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="c174e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c174e-112">Requirements</span></span>



| <span data-ttu-id="c174e-113">需求</span><span class="sxs-lookup"><span data-stu-id="c174e-113">Requirement</span></span> | <span data-ttu-id="c174e-114">值</span><span class="sxs-lookup"><span data-stu-id="c174e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c174e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c174e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c174e-116"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c174e-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c174e-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="c174e-117">Library</span></span><br/> | <dl> <span data-ttu-id="c174e-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c174e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c174e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c174e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c174e-120">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="c174e-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




