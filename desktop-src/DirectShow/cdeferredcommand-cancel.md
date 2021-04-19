---
description: Cancel 方法會取消先前已排入佇列的 CDeferredCommand：： Invoke 要求。
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: 'CDeferredCommand. Cancel 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984875"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="8c4ba-103">CDeferredCommand. Cancel 方法</span><span class="sxs-lookup"><span data-stu-id="8c4ba-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="8c4ba-104">`Cancel`方法會取消先前已排入佇列的 [**CDeferredCommand：： Invoke**](cdeferredcommand-invoke.md)要求。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c4ba-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="8c4ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c4ba-106">Parameters</span></span>

<span data-ttu-id="8c4ba-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c4ba-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c4ba-108">Return value</span></span>

<span data-ttu-id="8c4ba-109">\_ \_ \_ 如果 **m \_ pQueue** 為 **Null**，則傳回 VFW E 已取消。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="8c4ba-110">如果呼叫產生錯誤，則從 [**CCmdQueue：： Remove**](ccmdqueue-remove.md)傳回 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="8c4ba-111">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c4ba-112">備註</span><span class="sxs-lookup"><span data-stu-id="8c4ba-112">Remarks</span></span>

<span data-ttu-id="8c4ba-113">此成員函式會實 [**IDeferredCommand：： Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) 方法。</span><span class="sxs-lookup"><span data-stu-id="8c4ba-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4ba-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c4ba-114">Requirements</span></span>



| <span data-ttu-id="8c4ba-115">需求</span><span class="sxs-lookup"><span data-stu-id="8c4ba-115">Requirement</span></span> | <span data-ttu-id="8c4ba-116">值</span><span class="sxs-lookup"><span data-stu-id="8c4ba-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4ba-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8c4ba-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8c4ba-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8c4ba-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c4ba-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c4ba-119">Library</span></span><br/> | <dl> <span data-ttu-id="8c4ba-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c4ba-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4ba-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c4ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4ba-122">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="8c4ba-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




