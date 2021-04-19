---
description: CompleteStateChange 方法會判斷轉換為暫停狀態是否已完成。
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: 'CBaseRenderer. CompleteStateChange 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977771"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="0c4ed-103">CBaseRenderer. CompleteStateChange 方法</span><span class="sxs-lookup"><span data-stu-id="0c4ed-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="0c4ed-104">`CompleteStateChange`方法會判斷轉換為暫停狀態是否已完成。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c4ed-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="0c4ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c4ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4ed-107">*OldState*</span><span class="sxs-lookup"><span data-stu-id="0c4ed-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4ed-108">轉換之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4ed-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c4ed-109">Return value</span></span>

<span data-ttu-id="0c4ed-110">\_如果轉換完成，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="0c4ed-111">否則，會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4ed-112">備註</span><span class="sxs-lookup"><span data-stu-id="0c4ed-112">Remarks</span></span>

<span data-ttu-id="0c4ed-113">[**CBaseRenderer：:P ause**](cbaserenderer-pause.md)方法會呼叫這個方法來更新狀態轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="0c4ed-114">一般而言，在篩選器收到範例之前，將不會完成轉換至暫停的作業。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="0c4ed-115">不過，在某些情況下，轉換會立即完成：例如，如果篩選器未連接，或已到達資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="0c4ed-116">這個方法會檢查各種準則，然後呼叫 [**CBaseRenderer：： Ready**](cbaserenderer-ready.md) 方法或 [**CBaseRenderer：： NotReady**](cbaserenderer-notready.md) 方法來更新轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="0c4ed-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4ed-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c4ed-117">Requirements</span></span>



| <span data-ttu-id="0c4ed-118">需求</span><span class="sxs-lookup"><span data-stu-id="0c4ed-118">Requirement</span></span> | <span data-ttu-id="0c4ed-119">值</span><span class="sxs-lookup"><span data-stu-id="0c4ed-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4ed-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0c4ed-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0c4ed-121"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0c4ed-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c4ed-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c4ed-122">Library</span></span><br/> | <dl> <span data-ttu-id="0c4ed-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0c4ed-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4ed-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c4ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4ed-125">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="0c4ed-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




