---
description: 停止篩選。 這個方法會實 IMediaFilter：： Stop 方法。
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: 'CTransformFilter. Stop 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999448"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="5a32a-104">CTransformFilter. Stop 方法</span><span class="sxs-lookup"><span data-stu-id="5a32a-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="5a32a-105">停止篩選。</span><span class="sxs-lookup"><span data-stu-id="5a32a-105">Stops the filter.</span></span> <span data-ttu-id="5a32a-106">這個方法會實 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a32a-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a32a-107">語法</span><span class="sxs-lookup"><span data-stu-id="5a32a-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="5a32a-108">參數</span><span class="sxs-lookup"><span data-stu-id="5a32a-108">Parameters</span></span>

<span data-ttu-id="5a32a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5a32a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a32a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a32a-110">Return value</span></span>

<span data-ttu-id="5a32a-111">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5a32a-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a32a-112">備註</span><span class="sxs-lookup"><span data-stu-id="5a32a-112">Remarks</span></span>

<span data-ttu-id="5a32a-113">在這個方法解除這兩個配置器之後，它會呼叫 [**StopStreaming**](ctransformfilter-stopstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5a32a-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="5a32a-114">**StopStreaming** 方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="5a32a-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a32a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a32a-115">Requirements</span></span>



| <span data-ttu-id="5a32a-116">需求</span><span class="sxs-lookup"><span data-stu-id="5a32a-116">Requirement</span></span> | <span data-ttu-id="5a32a-117">值</span><span class="sxs-lookup"><span data-stu-id="5a32a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a32a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5a32a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5a32a-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5a32a-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a32a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a32a-120">Library</span></span><br/> | <dl> <span data-ttu-id="5a32a-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5a32a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a32a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a32a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a32a-123">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="5a32a-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




