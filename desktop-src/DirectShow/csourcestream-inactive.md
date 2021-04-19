---
description: 非使用中的方法會通知 pin，篩選已不再有效。 這個方法會覆寫 CBasePin：：非使用中的方法。 如果串流執行緒為使用中，此方法會停止它，並等候執行緒結束。
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: CSourceStream (Source. h) 的非使用中方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c4fab336f5f06d932189ee991fd190d1ae42b27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983042"
---
# <a name="csourcestreaminactive-method"></a><span data-ttu-id="d5b75-105">CSourceStream 方法</span><span class="sxs-lookup"><span data-stu-id="d5b75-105">CSourceStream.Inactive method</span></span>

<span data-ttu-id="d5b75-106">`Inactive`方法會通知 pin，篩選已不再有效。</span><span class="sxs-lookup"><span data-stu-id="d5b75-106">The `Inactive` method notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="d5b75-107">這個方法會覆寫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。</span><span class="sxs-lookup"><span data-stu-id="d5b75-107">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="d5b75-108">如果串流執行緒為使用中，此方法會停止它，並等候執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="d5b75-108">If the streaming thread is active, this method stops it and waits for the thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b75-109">語法</span><span class="sxs-lookup"><span data-stu-id="d5b75-109">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="d5b75-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5b75-110">Parameters</span></span>

<span data-ttu-id="d5b75-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d5b75-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5b75-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5b75-112">Return value</span></span>

<span data-ttu-id="d5b75-113">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d5b75-113">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b75-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5b75-114">Requirements</span></span>



| <span data-ttu-id="d5b75-115">需求</span><span class="sxs-lookup"><span data-stu-id="d5b75-115">Requirement</span></span> | <span data-ttu-id="d5b75-116">值</span><span class="sxs-lookup"><span data-stu-id="d5b75-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b75-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d5b75-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d5b75-118"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="d5b75-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d5b75-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5b75-119">Library</span></span><br/> | <dl> <span data-ttu-id="d5b75-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d5b75-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b75-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5b75-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b75-122">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="d5b75-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




