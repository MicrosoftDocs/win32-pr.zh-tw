---
description: 當 pin 成功封鎖或使用者取消暫止的區塊時，會發出信號的事件。
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'CDynamicOutputPin：： m_hNotifyCallerPinBlockedEvent 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997634"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="8c3ef-103">CDynamicOutputPin：： m \_ hNotifyCallerPinBlockedEvent 成員</span><span class="sxs-lookup"><span data-stu-id="8c3ef-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="8c3ef-104">當 pin 成功封鎖或使用者取消暫止的區塊時，會發出信號的事件。</span><span class="sxs-lookup"><span data-stu-id="8c3ef-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c3ef-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="8c3ef-106">備註</span><span class="sxs-lookup"><span data-stu-id="8c3ef-106">Remarks</span></span>

<span data-ttu-id="8c3ef-107">存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。</span><span class="sxs-lookup"><span data-stu-id="8c3ef-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3ef-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c3ef-108">Requirements</span></span>



| <span data-ttu-id="8c3ef-109">需求</span><span class="sxs-lookup"><span data-stu-id="8c3ef-109">Requirement</span></span> | <span data-ttu-id="8c3ef-110">值</span><span class="sxs-lookup"><span data-stu-id="8c3ef-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3ef-111">標頭</span><span class="sxs-lookup"><span data-stu-id="8c3ef-111">Header</span></span><br/>  | <dl> <span data-ttu-id="8c3ef-112"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8c3ef-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c3ef-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c3ef-113">Library</span></span><br/> | <dl> <span data-ttu-id="8c3ef-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c3ef-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c3ef-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c3ef-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3ef-116">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="8c3ef-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




