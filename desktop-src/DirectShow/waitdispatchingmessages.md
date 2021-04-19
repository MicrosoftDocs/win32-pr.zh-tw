---
description: WaitDispatchingMessages 函式會在分派視窗訊息時，等候物件收到信號。
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: 'WaitDispatchingMessages 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984016"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="6e288-103">WaitDispatchingMessages 函式</span><span class="sxs-lookup"><span data-stu-id="6e288-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="6e288-104">`WaitDispatchingMessages`函數會在分派視窗訊息時，等候物件發出信號。</span><span class="sxs-lookup"><span data-stu-id="6e288-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e288-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e288-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="6e288-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e288-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e288-107">*hObject*</span><span class="sxs-lookup"><span data-stu-id="6e288-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="6e288-108">要等候的物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e288-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="6e288-109">*dwWait*</span><span class="sxs-lookup"><span data-stu-id="6e288-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="6e288-110">逾時間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6e288-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="6e288-111">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="6e288-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6e288-112">視窗的選擇性控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e288-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="6e288-113">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6e288-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6e288-114">選擇性的視窗訊息，指定要分派的訊息。</span><span class="sxs-lookup"><span data-stu-id="6e288-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="6e288-115">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="6e288-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="6e288-116">要等候之事件的選擇性控制碼。</span><span class="sxs-lookup"><span data-stu-id="6e288-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e288-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e288-117">Return value</span></span>

<span data-ttu-id="6e288-118">從 **WaitForMultipleObjects** 函式傳回值。</span><span class="sxs-lookup"><span data-stu-id="6e288-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e288-119">備註</span><span class="sxs-lookup"><span data-stu-id="6e288-119">Remarks</span></span>

<span data-ttu-id="6e288-120">如果物件擁有視窗，則應該在等候時分派視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="6e288-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="6e288-121">這個函式可讓物件在分派訊息時等候事件、信號或其他相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="6e288-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e288-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e288-122">Requirements</span></span>



| <span data-ttu-id="6e288-123">需求</span><span class="sxs-lookup"><span data-stu-id="6e288-123">Requirement</span></span> | <span data-ttu-id="6e288-124">值</span><span class="sxs-lookup"><span data-stu-id="6e288-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e288-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6e288-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6e288-126"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e288-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6e288-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e288-127">Library</span></span><br/> | <dl> <span data-ttu-id="6e288-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e288-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e288-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e288-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e288-130">其他 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="6e288-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




