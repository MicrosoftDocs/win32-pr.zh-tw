---
description: PrepareReceive 方法會準備篩選以轉譯範例。
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: 'CBaseRenderer. PrepareReceive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991025"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="a907d-103">CBaseRenderer. PrepareReceive 方法</span><span class="sxs-lookup"><span data-stu-id="a907d-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="a907d-104">`PrepareReceive`方法會準備篩選以呈現範例。</span><span class="sxs-lookup"><span data-stu-id="a907d-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a907d-105">語法</span><span class="sxs-lookup"><span data-stu-id="a907d-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="a907d-106">參數</span><span class="sxs-lookup"><span data-stu-id="a907d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a907d-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="a907d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a907d-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a907d-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a907d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a907d-109">Return value</span></span>

<span data-ttu-id="a907d-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a907d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a907d-111">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="a907d-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="a907d-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a907d-112">Return code</span></span>                                                                                             | <span data-ttu-id="a907d-113">Description</span><span class="sxs-lookup"><span data-stu-id="a907d-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="a907d-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a907d-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="a907d-115">成功。</span><span class="sxs-lookup"><span data-stu-id="a907d-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="a907d-116"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="a907d-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="a907d-117">失敗。</span><span class="sxs-lookup"><span data-stu-id="a907d-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="a907d-118"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="a907d-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="a907d-119">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a907d-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="a907d-120"><dt>**已 \_ 拒絕 VFW 電子 \_ 範例 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a907d-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="a907d-121">篩選器正在卸載此範例。</span><span class="sxs-lookup"><span data-stu-id="a907d-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a907d-122">備註</span><span class="sxs-lookup"><span data-stu-id="a907d-122">Remarks</span></span>

<span data-ttu-id="a907d-123">篩選會在呈現範例之前，從 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法內呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a907d-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="a907d-124">如果篩選器正在執行，這個方法會排程轉譯的範例。</span><span class="sxs-lookup"><span data-stu-id="a907d-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="a907d-125">如果篩選已經有暫止的範例，或已到達資料流程結尾，則方法會傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="a907d-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="a907d-126">上游篩選器可能未正確地序列化其串流呼叫。</span><span class="sxs-lookup"><span data-stu-id="a907d-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="a907d-127">如果排程演算法判斷應該卸載範例 (請參閱 [**CBaseRenderer：： ScheduleSample**](cbaserenderer-schedulesample.md)) ，方法會傳回已拒絕的 VFW \_ E \_ 範例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a907d-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="a907d-128">但是，輸入 pin 的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法不會將此錯誤碼傳遞給上游篩選器，因為卸載範例並不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="a907d-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a907d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a907d-129">Requirements</span></span>



| <span data-ttu-id="a907d-130">需求</span><span class="sxs-lookup"><span data-stu-id="a907d-130">Requirement</span></span> | <span data-ttu-id="a907d-131">值</span><span class="sxs-lookup"><span data-stu-id="a907d-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a907d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a907d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a907d-133"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a907d-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a907d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a907d-134">Library</span></span><br/> | <dl> <span data-ttu-id="a907d-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a907d-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a907d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a907d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a907d-137">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="a907d-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




