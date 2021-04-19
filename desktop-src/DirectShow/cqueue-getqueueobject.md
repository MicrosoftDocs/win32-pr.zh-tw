---
description: 從佇列中取出下一個專案。
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: 'CQueue. GetQueueObject 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000913"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="591a7-103">CQueue. GetQueueObject 方法</span><span class="sxs-lookup"><span data-stu-id="591a7-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="591a7-104">從佇列中取出下一個專案。</span><span class="sxs-lookup"><span data-stu-id="591a7-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="591a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="591a7-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="591a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="591a7-106">Parameters</span></span>

<span data-ttu-id="591a7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="591a7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="591a7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="591a7-108">Return value</span></span>

<span data-ttu-id="591a7-109">傳回類型為 **T** (範本類型) 的物件。</span><span class="sxs-lookup"><span data-stu-id="591a7-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="591a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="591a7-110">Remarks</span></span>

<span data-ttu-id="591a7-111">這個方法會封鎖，直到佇列上有可用的專案為止。</span><span class="sxs-lookup"><span data-stu-id="591a7-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="591a7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="591a7-112">Requirements</span></span>



| <span data-ttu-id="591a7-113">需求</span><span class="sxs-lookup"><span data-stu-id="591a7-113">Requirement</span></span> | <span data-ttu-id="591a7-114">值</span><span class="sxs-lookup"><span data-stu-id="591a7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="591a7-115">標頭</span><span class="sxs-lookup"><span data-stu-id="591a7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="591a7-116"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="591a7-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="591a7-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="591a7-117">Library</span></span><br/> | <dl> <span data-ttu-id="591a7-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="591a7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="591a7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="591a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591a7-120">**CQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="591a7-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




