---
description: 用來表示事件種類的列舉。
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 事件種類列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385672"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span data-ttu-id="287a2-103"><span id="vspixengine.eventtype"></span>事件種類列舉</span><span class="sxs-lookup"><span data-stu-id="287a2-103"><span id="vspixengine.eventtype"></span>EVENTTYPE enumeration</span></span>

<span data-ttu-id="287a2-104">用來表示事件種類的列舉。</span><span class="sxs-lookup"><span data-stu-id="287a2-104">An enum used to indicate the type of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="287a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="287a2-105">Syntax</span></span>

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a><span data-ttu-id="287a2-106">常數</span><span class="sxs-lookup"><span data-stu-id="287a2-106">Constants</span></span>

<span data-ttu-id="287a2-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET \_ 無**</span><span class="sxs-lookup"><span data-stu-id="287a2-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET\_NONE**</span></span>  
<span data-ttu-id="287a2-108">對應至無事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-108">A value that corresponds to no event.</span></span>

<span data-ttu-id="287a2-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="287a2-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="287a2-110">對應至會話開始事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-110">A value that corresponds to a session start event.</span></span>

<span data-ttu-id="287a2-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET \_ SESSIONEND**</span><span class="sxs-lookup"><span data-stu-id="287a2-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET\_SESSIONEND**</span></span>  
<span data-ttu-id="287a2-112">對應至會話結束事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-112">A value that corresponds to a session end event.</span></span>

<span data-ttu-id="287a2-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET \_ PROCESSSTART**</span><span class="sxs-lookup"><span data-stu-id="287a2-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="287a2-114">對應至進程開始事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-114">A value that corresponds to a process start event.</span></span>

<span data-ttu-id="287a2-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET \_ PROCESSEND**</span><span class="sxs-lookup"><span data-stu-id="287a2-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET\_PROCESSEND**</span></span>  
<span data-ttu-id="287a2-116">對應至處理常式結束事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-116">A value that corresponds to a process end event.</span></span>

<span data-ttu-id="287a2-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET \_ FRAMEBEGIN**</span><span class="sxs-lookup"><span data-stu-id="287a2-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="287a2-118">對應至框架開始事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-118">A value that corresponds to a frame begin event.</span></span>

<span data-ttu-id="287a2-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET \_ FRAMEEND**</span><span class="sxs-lookup"><span data-stu-id="287a2-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET\_FRAMEEND**</span></span>  
<span data-ttu-id="287a2-120">對應至框架結束事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-120">A value that corresponds to a frame end event.</span></span> <span data-ttu-id="287a2-121">未使用。</span><span class="sxs-lookup"><span data-stu-id="287a2-121">Not used.</span></span>

<span data-ttu-id="287a2-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET \_ USEREVENTBEGIN**</span><span class="sxs-lookup"><span data-stu-id="287a2-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="287a2-123">對應至使用者事件開始事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-123">A value that corresponds to a user-event begin event.</span></span>

<span data-ttu-id="287a2-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET \_ USEREVENTEND**</span><span class="sxs-lookup"><span data-stu-id="287a2-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="287a2-125">對應至使用者事件結束事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-125">A value that corresponds to a user-event end event.</span></span> <span data-ttu-id="287a2-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="287a2-126">Not used.</span></span>

<span data-ttu-id="287a2-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="287a2-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET\_USERMARKER**</span></span>  
<span data-ttu-id="287a2-128">對應至使用者標記事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-128">A value that corresponds to a user-marker event.</span></span>

<span data-ttu-id="287a2-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="287a2-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET\_CALL**</span></span>  
<span data-ttu-id="287a2-130">對應至呼叫事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-130">A value that corresponds to a call event.</span></span>

<span data-ttu-id="287a2-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET \_ OBJECTCREATION**</span><span class="sxs-lookup"><span data-stu-id="287a2-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="287a2-132">對應至物件建立事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-132">A value that corresponds to an object creation event.</span></span>

<span data-ttu-id="287a2-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ OBJECTPOPULATION**</span><span class="sxs-lookup"><span data-stu-id="287a2-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="287a2-134">對應至物件人口事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-134">A value that corresponds to an object population event.</span></span>

<span data-ttu-id="287a2-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET \_ CALLSYNC**</span><span class="sxs-lookup"><span data-stu-id="287a2-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET\_CALLSYNC**</span></span>  

<span data-ttu-id="287a2-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET \_ 繪圖**</span><span class="sxs-lookup"><span data-stu-id="287a2-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET\_DRAW**</span></span>  
<span data-ttu-id="287a2-137">對應至繪製呼叫事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-137">A value that corresponds to a draw call event.</span></span>

<span data-ttu-id="287a2-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET \_ 分派**</span><span class="sxs-lookup"><span data-stu-id="287a2-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET\_DISPATCH**</span></span>  
<span data-ttu-id="287a2-139">對應至分派事件的值。</span><span class="sxs-lookup"><span data-stu-id="287a2-139">A value that corresponds to a dispatch event.</span></span>

## <a name="requirements"></a><span data-ttu-id="287a2-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="287a2-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="287a2-141">標頭</span><span class="sxs-lookup"><span data-stu-id="287a2-141">Header</span></span></p></td><td><span data-ttu-id="287a2-142">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="287a2-142">Vspixengine.h</span></span></td></tr></tbody></table>
