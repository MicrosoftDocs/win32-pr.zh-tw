---
description: 等候方法會封鎖，直到事件收到信號為止，或直到發生超時為止。
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: 'CAMEvent. Wait 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980159"
---
# <a name="cameventwait-method"></a><span data-ttu-id="eafaa-103">CAMEvent. Wait 方法</span><span class="sxs-lookup"><span data-stu-id="eafaa-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="eafaa-104">`Wait`方法會封鎖，直到事件收到信號為止，或直到發生超時為止。</span><span class="sxs-lookup"><span data-stu-id="eafaa-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="eafaa-105">語法</span><span class="sxs-lookup"><span data-stu-id="eafaa-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="eafaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="eafaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafaa-107">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="eafaa-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="eafaa-108">選擇性的超時值（以毫碼錶示）。</span><span class="sxs-lookup"><span data-stu-id="eafaa-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafaa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eafaa-109">Return value</span></span>

<span data-ttu-id="eafaa-110">如果事件已發出信號，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="eafaa-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="eafaa-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="eafaa-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafaa-112">備註</span><span class="sxs-lookup"><span data-stu-id="eafaa-112">Remarks</span></span>

<span data-ttu-id="eafaa-113">如果是自動重設事件，當此方法傳回時，事件會重設為未收到信號狀態。</span><span class="sxs-lookup"><span data-stu-id="eafaa-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="eafaa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="eafaa-114">Requirements</span></span>



| <span data-ttu-id="eafaa-115">需求</span><span class="sxs-lookup"><span data-stu-id="eafaa-115">Requirement</span></span> | <span data-ttu-id="eafaa-116">值</span><span class="sxs-lookup"><span data-stu-id="eafaa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafaa-117">標頭</span><span class="sxs-lookup"><span data-stu-id="eafaa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eafaa-118"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eafaa-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="eafaa-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="eafaa-119">Library</span></span><br/> | <dl> <span data-ttu-id="eafaa-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eafaa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafaa-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eafaa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eafaa-122">**CAMEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="eafaa-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




