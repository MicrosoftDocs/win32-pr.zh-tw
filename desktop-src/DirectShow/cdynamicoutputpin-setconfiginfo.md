---
description: SetConfigInfo 方法會指定 IGraphConfig 指標和 stop 事件。
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: 'CDynamicOutputPin. SetConfigInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977498"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="e4307-103">CDynamicOutputPin. SetConfigInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e4307-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="e4307-104">`SetConfigInfo`方法會指定 [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)指標和停止事件。</span><span class="sxs-lookup"><span data-stu-id="e4307-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4307-105">語法</span><span class="sxs-lookup"><span data-stu-id="e4307-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="e4307-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4307-107">*pGraphConfig*</span><span class="sxs-lookup"><span data-stu-id="e4307-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="e4307-108">[**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)介面的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="e4307-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4307-109">*hStopEvent*</span><span class="sxs-lookup"><span data-stu-id="e4307-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="e4307-110">當篩選準則停止時所發出之事件的控制碼，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e4307-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4307-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4307-111">Return value</span></span>

<span data-ttu-id="e4307-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e4307-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4307-113">備註</span><span class="sxs-lookup"><span data-stu-id="e4307-113">Remarks</span></span>

<span data-ttu-id="e4307-114">篩選器加入篩選圖形時，必須呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e4307-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="e4307-115">篩選圖形管理員支援 **IGraphConfig**。</span><span class="sxs-lookup"><span data-stu-id="e4307-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="e4307-116">針對 *hStopEvent* 參數，建立手動重設事件。</span><span class="sxs-lookup"><span data-stu-id="e4307-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="e4307-117">當篩選準則離開篩選圖形時，請針對這兩個參數，以 **Null** 呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e4307-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4307-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4307-118">Requirements</span></span>



| <span data-ttu-id="e4307-119">需求</span><span class="sxs-lookup"><span data-stu-id="e4307-119">Requirement</span></span> | <span data-ttu-id="e4307-120">值</span><span class="sxs-lookup"><span data-stu-id="e4307-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4307-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e4307-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e4307-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e4307-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4307-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4307-123">Library</span></span><br/> | <dl> <span data-ttu-id="e4307-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e4307-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4307-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4307-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4307-126">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="e4307-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




