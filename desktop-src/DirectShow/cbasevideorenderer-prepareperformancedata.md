---
description: PreparePerformanceData 方法會設定 \_ 目前框架的 m trLate 和 m \_ trFrame 值。
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: 'CBaseVideoRenderer. PreparePerformanceData 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997637"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="adc7a-103">CBaseVideoRenderer. PreparePerformanceData 方法</span><span class="sxs-lookup"><span data-stu-id="adc7a-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="adc7a-104">`PreparePerformanceData`方法會設定目前框架的 **m \_ trLate** 和 **m \_ trFrame** 值。</span><span class="sxs-lookup"><span data-stu-id="adc7a-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="adc7a-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="adc7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="adc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc7a-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="adc7a-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="adc7a-108">值，指出取樣超過其到期時間的延遲時間（以參考時間單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="adc7a-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="adc7a-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="adc7a-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="adc7a-110">在參考時間單位中的幀時間。</span><span class="sxs-lookup"><span data-stu-id="adc7a-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc7a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="adc7a-111">Return value</span></span>

<span data-ttu-id="adc7a-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="adc7a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adc7a-113">備註</span><span class="sxs-lookup"><span data-stu-id="adc7a-113">Remarks</span></span>

<span data-ttu-id="adc7a-114">此成員函式會將 **m \_ trLate** 設為 *trLate* 的值，並將 **m \_ trFrame** 設定為 *trFrame* 的值。</span><span class="sxs-lookup"><span data-stu-id="adc7a-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="adc7a-115">從 [**CBaseVideoRenderer：： OnRenderStart**](cbasevideorenderer-onrenderstart.md)或 [**CBaseVideoRenderer：： OnDirectRender**](cbasevideorenderer-ondirectrender.md)呼叫 [**CBaseVideoRenderer：： RecordFrameLateness**](cbasevideorenderer-recordframelateness.md)成員函式時，它會傳遞 **m \_ trLate** 和 **m \_ trFrame** 的值來更新統計資料。</span><span class="sxs-lookup"><span data-stu-id="adc7a-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="adc7a-116">`PreparePerformanceData` 從 [**CBaseVideoRenderer：： OnWaitEnd**](cbasevideorenderer-onwaitend.md) 呼叫，以設定這些資料成員值。</span><span class="sxs-lookup"><span data-stu-id="adc7a-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc7a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="adc7a-117">Requirements</span></span>



| <span data-ttu-id="adc7a-118">需求</span><span class="sxs-lookup"><span data-stu-id="adc7a-118">Requirement</span></span> | <span data-ttu-id="adc7a-119">值</span><span class="sxs-lookup"><span data-stu-id="adc7a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adc7a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="adc7a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="adc7a-121"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="adc7a-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adc7a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="adc7a-122">Library</span></span><br/> | <dl> <span data-ttu-id="adc7a-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="adc7a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc7a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adc7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc7a-125">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="adc7a-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




