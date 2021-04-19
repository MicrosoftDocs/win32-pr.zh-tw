---
description: 將專案放在佇列上。
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: 'CQueue. PutQueueObject 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995421"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="b56f1-103">CQueue. PutQueueObject 方法</span><span class="sxs-lookup"><span data-stu-id="b56f1-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="b56f1-104">將專案放在佇列上。</span><span class="sxs-lookup"><span data-stu-id="b56f1-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="b56f1-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="b56f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="b56f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b56f1-107">*object*</span><span class="sxs-lookup"><span data-stu-id="b56f1-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="b56f1-108">**T** 類型的物件 (範本類型) 。</span><span class="sxs-lookup"><span data-stu-id="b56f1-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b56f1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b56f1-109">Return value</span></span>

<span data-ttu-id="b56f1-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b56f1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b56f1-111">備註</span><span class="sxs-lookup"><span data-stu-id="b56f1-111">Remarks</span></span>

<span data-ttu-id="b56f1-112">這個方法會封鎖，直到專案的佇列中有空間為止。</span><span class="sxs-lookup"><span data-stu-id="b56f1-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="b56f1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b56f1-113">Requirements</span></span>



| <span data-ttu-id="b56f1-114">需求</span><span class="sxs-lookup"><span data-stu-id="b56f1-114">Requirement</span></span> | <span data-ttu-id="b56f1-115">值</span><span class="sxs-lookup"><span data-stu-id="b56f1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56f1-116">標頭</span><span class="sxs-lookup"><span data-stu-id="b56f1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b56f1-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b56f1-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="b56f1-118">Library</span></span><br/> | <dl> <span data-ttu-id="b56f1-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b56f1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56f1-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b56f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56f1-121">**CQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="b56f1-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




