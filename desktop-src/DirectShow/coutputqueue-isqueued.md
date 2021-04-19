---
description: IsQueued 方法會判斷物件是否使用背景工作執行緒來傳遞範例。
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: 'COutputQueue. IsQueued 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47093acedb3a28d633ea2c8b0bbdbba3c1493de7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993259"
---
# <a name="coutputqueueisqueued-method"></a><span data-ttu-id="0ee0c-103">COutputQueue. IsQueued 方法</span><span class="sxs-lookup"><span data-stu-id="0ee0c-103">COutputQueue.IsQueued method</span></span>

<span data-ttu-id="0ee0c-104">`IsQueued`方法會判斷物件是否使用背景工作執行緒來傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="0ee0c-104">The `IsQueued` method determines whether the object is using a worker thread to deliver samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ee0c-105">Syntax</span></span>


```C++
BOOL IsQueued();
```



## <a name="parameters"></a><span data-ttu-id="0ee0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ee0c-106">Parameters</span></span>

<span data-ttu-id="0ee0c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0ee0c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ee0c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ee0c-108">Return value</span></span>

<span data-ttu-id="0ee0c-109">如果物件正在使用背景工作執行緒，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0ee0c-109">Returns **TRUE** if the object is using a worker thread, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee0c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ee0c-110">Requirements</span></span>



| <span data-ttu-id="0ee0c-111">需求</span><span class="sxs-lookup"><span data-stu-id="0ee0c-111">Requirement</span></span> | <span data-ttu-id="0ee0c-112">值</span><span class="sxs-lookup"><span data-stu-id="0ee0c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee0c-113">標頭</span><span class="sxs-lookup"><span data-stu-id="0ee0c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0ee0c-114"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0ee0c-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ee0c-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ee0c-115">Library</span></span><br/> | <dl> <span data-ttu-id="0ee0c-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0ee0c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee0c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ee0c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee0c-118">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="0ee0c-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




