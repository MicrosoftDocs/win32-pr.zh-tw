---
description: Reset 方法會重設物件，讓它可以接收更多資料。
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: 'COutputQueue： Reset 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985541"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="fb8e3-103">COutputQueue 重設方法</span><span class="sxs-lookup"><span data-stu-id="fb8e3-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="fb8e3-104">`Reset`方法會重設物件，讓它可以接收更多資料。</span><span class="sxs-lookup"><span data-stu-id="fb8e3-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb8e3-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="fb8e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb8e3-106">Parameters</span></span>

<span data-ttu-id="fb8e3-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fb8e3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb8e3-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb8e3-108">Return value</span></span>

<span data-ttu-id="fb8e3-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fb8e3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb8e3-110">備註</span><span class="sxs-lookup"><span data-stu-id="fb8e3-110">Remarks</span></span>

<span data-ttu-id="fb8e3-111">這個方法會將 [**COutputQueue：： m \_ hr**](coutputqueue-m-hr.md) 成員變數重設為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fb8e3-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="fb8e3-112">物件可以再次接收媒體範例;例如，在清除作業之後。</span><span class="sxs-lookup"><span data-stu-id="fb8e3-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8e3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb8e3-113">Requirements</span></span>



| <span data-ttu-id="fb8e3-114">需求</span><span class="sxs-lookup"><span data-stu-id="fb8e3-114">Requirement</span></span> | <span data-ttu-id="fb8e3-115">值</span><span class="sxs-lookup"><span data-stu-id="fb8e3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb8e3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="fb8e3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fb8e3-117"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fb8e3-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb8e3-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb8e3-118">Library</span></span><br/> | <dl> <span data-ttu-id="fb8e3-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fb8e3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb8e3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb8e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8e3-121">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="fb8e3-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




