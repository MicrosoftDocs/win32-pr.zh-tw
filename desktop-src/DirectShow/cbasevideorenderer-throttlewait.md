---
description: ThrottleWait 方法會在每個畫面格之後插入等待期間。
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: 'CBaseVideoRenderer. ThrottleWait 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001803"
---
# <a name="cbasevideorendererthrottlewait-method"></a><span data-ttu-id="376ab-103">CBaseVideoRenderer. ThrottleWait 方法</span><span class="sxs-lookup"><span data-stu-id="376ab-103">CBaseVideoRenderer.ThrottleWait method</span></span>

<span data-ttu-id="376ab-104">方法會在 `ThrottleWait` 每個畫面格之後插入等待期間。</span><span class="sxs-lookup"><span data-stu-id="376ab-104">The `ThrottleWait` method inserts a wait period after each frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="376ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="376ab-105">Syntax</span></span>


```C++
void ThrottleWait();
```



## <a name="parameters"></a><span data-ttu-id="376ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="376ab-106">Parameters</span></span>

<span data-ttu-id="376ab-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="376ab-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="376ab-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="376ab-108">Return value</span></span>

<span data-ttu-id="376ab-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="376ab-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="376ab-110">備註</span><span class="sxs-lookup"><span data-stu-id="376ab-110">Remarks</span></span>

<span data-ttu-id="376ab-111">此成員函式會等候從 **m \_ trThrottle** 資料成員取得的時間週期。</span><span class="sxs-lookup"><span data-stu-id="376ab-111">This member function waits for a time period obtained from the **m\_trThrottle** data member.</span></span>

## <a name="requirements"></a><span data-ttu-id="376ab-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="376ab-112">Requirements</span></span>



| <span data-ttu-id="376ab-113">需求</span><span class="sxs-lookup"><span data-stu-id="376ab-113">Requirement</span></span> | <span data-ttu-id="376ab-114">值</span><span class="sxs-lookup"><span data-stu-id="376ab-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376ab-115">標頭</span><span class="sxs-lookup"><span data-stu-id="376ab-115">Header</span></span><br/>  | <dl> <span data-ttu-id="376ab-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="376ab-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="376ab-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="376ab-117">Library</span></span><br/> | <dl> <span data-ttu-id="376ab-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="376ab-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="376ab-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="376ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376ab-120">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="376ab-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




