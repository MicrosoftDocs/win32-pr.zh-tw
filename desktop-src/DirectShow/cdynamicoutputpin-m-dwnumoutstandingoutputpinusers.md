---
description: 使用此 pin 的串流執行緒數目。
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'CDynamicOutputPin：： m_dwNumOutstandingOutputPinUsers 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998683"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="45383-103">CDynamicOutputPin：： m \_ dwNumOutstandingOutputPinUsers 成員</span><span class="sxs-lookup"><span data-stu-id="45383-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="45383-104">使用此 pin 的串流執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="45383-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="45383-105">語法</span><span class="sxs-lookup"><span data-stu-id="45383-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="45383-106">備註</span><span class="sxs-lookup"><span data-stu-id="45383-106">Remarks</span></span>

<span data-ttu-id="45383-107">[**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)方法會遞增此變數，而 [**CDynamicOutputPin：： StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)方法會將它遞減。</span><span class="sxs-lookup"><span data-stu-id="45383-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="45383-108">當值大於零時，某些執行緒會使用此釘選來串流資料或變更連線類型。</span><span class="sxs-lookup"><span data-stu-id="45383-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="45383-109">在這種情況下，無法封鎖 pin。</span><span class="sxs-lookup"><span data-stu-id="45383-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="45383-110">存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。</span><span class="sxs-lookup"><span data-stu-id="45383-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="45383-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="45383-111">Requirements</span></span>



| <span data-ttu-id="45383-112">需求</span><span class="sxs-lookup"><span data-stu-id="45383-112">Requirement</span></span> | <span data-ttu-id="45383-113">值</span><span class="sxs-lookup"><span data-stu-id="45383-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45383-114">標頭</span><span class="sxs-lookup"><span data-stu-id="45383-114">Header</span></span><br/>  | <dl> <span data-ttu-id="45383-115"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="45383-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45383-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="45383-116">Library</span></span><br/> | <dl> <span data-ttu-id="45383-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="45383-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45383-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45383-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45383-119">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="45383-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="45383-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="45383-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




