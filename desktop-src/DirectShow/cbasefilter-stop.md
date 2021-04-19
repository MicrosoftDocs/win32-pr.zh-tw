---
description: Stop 方法會停止篩選。 這個方法會實 IMediaFilter：： Stop 方法。
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: 'CBaseFilter. Stop 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992927"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="99bb3-104">CBaseFilter. Stop 方法</span><span class="sxs-lookup"><span data-stu-id="99bb3-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="99bb3-105">`Stop`方法會停止篩選。</span><span class="sxs-lookup"><span data-stu-id="99bb3-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="99bb3-106">這個方法會實 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。</span><span class="sxs-lookup"><span data-stu-id="99bb3-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bb3-107">語法</span><span class="sxs-lookup"><span data-stu-id="99bb3-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="99bb3-108">參數</span><span class="sxs-lookup"><span data-stu-id="99bb3-108">Parameters</span></span>

<span data-ttu-id="99bb3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="99bb3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99bb3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="99bb3-110">Return value</span></span>

<span data-ttu-id="99bb3-111">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="99bb3-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bb3-112">備註</span><span class="sxs-lookup"><span data-stu-id="99bb3-112">Remarks</span></span>

<span data-ttu-id="99bb3-113">這個方法會在每個篩選器的連接釘上呼叫 [**CBasePin：：非**](cbasepin-inactive.md) 使用中的方法。</span><span class="sxs-lookup"><span data-stu-id="99bb3-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="99bb3-114">它也會將篩選準則的狀態設定為 [ \_ 已停止]。</span><span class="sxs-lookup"><span data-stu-id="99bb3-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="99bb3-115">當篩選準則停止時，它應該會拒絕上游的範例、停止傳遞範例下游、關閉工作者執行緒，以及釋出用於串流處理的任何資源。</span><span class="sxs-lookup"><span data-stu-id="99bb3-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bb3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="99bb3-116">Requirements</span></span>



| <span data-ttu-id="99bb3-117">需求</span><span class="sxs-lookup"><span data-stu-id="99bb3-117">Requirement</span></span> | <span data-ttu-id="99bb3-118">值</span><span class="sxs-lookup"><span data-stu-id="99bb3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99bb3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="99bb3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99bb3-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="99bb3-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="99bb3-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="99bb3-121">Library</span></span><br/> | <dl> <span data-ttu-id="99bb3-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="99bb3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99bb3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99bb3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bb3-124">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="99bb3-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




