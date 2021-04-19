---
description: 檢查方法會檢查是否已設定事件，而不會封鎖。
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: 'CAMEvent： Check 方法 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974929"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="bb9c1-103">CAMEvent 檢查方法</span><span class="sxs-lookup"><span data-stu-id="bb9c1-103">CAMEvent.Check method</span></span>

<span data-ttu-id="bb9c1-104">`Check`方法會檢查是否已設定事件，而不會封鎖。</span><span class="sxs-lookup"><span data-stu-id="bb9c1-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb9c1-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="bb9c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb9c1-106">Parameters</span></span>

<span data-ttu-id="bb9c1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bb9c1-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb9c1-108">備註</span><span class="sxs-lookup"><span data-stu-id="bb9c1-108">Remarks</span></span>

<span data-ttu-id="bb9c1-109">如果已設定事件，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bb9c1-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="bb9c1-110">這個方法會呼叫 [**CAMEvent：： Wait**](camevent-wait.md) 方法，其時間為零。</span><span class="sxs-lookup"><span data-stu-id="bb9c1-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="bb9c1-111">如果物件是自動重設事件，這個方法會重設事件。</span><span class="sxs-lookup"><span data-stu-id="bb9c1-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9c1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb9c1-112">Requirements</span></span>



| <span data-ttu-id="bb9c1-113">需求</span><span class="sxs-lookup"><span data-stu-id="bb9c1-113">Requirement</span></span> | <span data-ttu-id="bb9c1-114">值</span><span class="sxs-lookup"><span data-stu-id="bb9c1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9c1-115">標頭</span><span class="sxs-lookup"><span data-stu-id="bb9c1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bb9c1-116"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bb9c1-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bb9c1-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb9c1-117">Library</span></span><br/> | <dl> <span data-ttu-id="bb9c1-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bb9c1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9c1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb9c1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9c1-120">**CAMEvent 類別**</span><span class="sxs-lookup"><span data-stu-id="bb9c1-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




