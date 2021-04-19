---
description: GetDueHandle 方法會捕獲要發出信號的事件控制碼。
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: 'CCmdQueue. GetDueHandle 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991527"
---
# <a name="ccmdqueuegetduehandle-method"></a><span data-ttu-id="faa12-103">CCmdQueue. GetDueHandle 方法</span><span class="sxs-lookup"><span data-stu-id="faa12-103">CCmdQueue.GetDueHandle method</span></span>

<span data-ttu-id="faa12-104">`GetDueHandle`方法會捕獲要發出信號的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="faa12-104">The `GetDueHandle` method retrieves the event handle to be signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa12-105">語法</span><span class="sxs-lookup"><span data-stu-id="faa12-105">Syntax</span></span>


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a><span data-ttu-id="faa12-106">參數</span><span class="sxs-lookup"><span data-stu-id="faa12-106">Parameters</span></span>

<span data-ttu-id="faa12-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="faa12-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="faa12-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="faa12-108">Return value</span></span>

<span data-ttu-id="faa12-109">傳回事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="faa12-109">Returns the event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa12-110">備註</span><span class="sxs-lookup"><span data-stu-id="faa12-110">Remarks</span></span>

<span data-ttu-id="faa12-111">每當有延遲的命令要執行時，就會傳回事件控制碼 (當 [**CCmdQueue：： GetDueCommand**](ccmdqueue-getduecommand.md) 不會封鎖) 時。</span><span class="sxs-lookup"><span data-stu-id="faa12-111">Return the event handle whenever there are deferred commands that are due for execution (when [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) will not block).</span></span>

## <a name="requirements"></a><span data-ttu-id="faa12-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="faa12-112">Requirements</span></span>



| <span data-ttu-id="faa12-113">需求</span><span class="sxs-lookup"><span data-stu-id="faa12-113">Requirement</span></span> | <span data-ttu-id="faa12-114">值</span><span class="sxs-lookup"><span data-stu-id="faa12-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa12-115">標頭</span><span class="sxs-lookup"><span data-stu-id="faa12-115">Header</span></span><br/>  | <dl> <span data-ttu-id="faa12-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="faa12-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="faa12-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="faa12-117">Library</span></span><br/> | <dl> <span data-ttu-id="faa12-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="faa12-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa12-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faa12-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa12-120">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="faa12-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




