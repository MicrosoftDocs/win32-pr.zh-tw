---
description: 此 pin 上最後一次呼叫 IPinFlowControl：： Block 方法之執行緒的識別碼。 只有當 pin 遭到封鎖時，此成員變數才有效。
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'CDynamicOutputPin：： m_dwBlockCallerThreadID 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996094"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="3a94e-104">CDynamicOutputPin：： m \_ dwBlockCallerThreadID 成員</span><span class="sxs-lookup"><span data-stu-id="3a94e-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="3a94e-105">此 pin 上最後一次呼叫 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 方法之執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a94e-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="3a94e-106">只有當 pin 遭到封鎖時，此成員變數才有效。</span><span class="sxs-lookup"><span data-stu-id="3a94e-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a94e-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a94e-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="3a94e-108">備註</span><span class="sxs-lookup"><span data-stu-id="3a94e-108">Remarks</span></span>

<span data-ttu-id="3a94e-109">存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。</span><span class="sxs-lookup"><span data-stu-id="3a94e-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a94e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a94e-110">Requirements</span></span>



| <span data-ttu-id="3a94e-111">需求</span><span class="sxs-lookup"><span data-stu-id="3a94e-111">Requirement</span></span> | <span data-ttu-id="3a94e-112">值</span><span class="sxs-lookup"><span data-stu-id="3a94e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a94e-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3a94e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3a94e-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3a94e-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3a94e-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a94e-115">Library</span></span><br/> | <dl> <span data-ttu-id="3a94e-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3a94e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a94e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a94e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a94e-118">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="3a94e-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




