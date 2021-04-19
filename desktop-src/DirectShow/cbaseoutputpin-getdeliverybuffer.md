---
description: GetDeliveryBuffer 方法會抓取包含空緩衝區的媒體範例。
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: 'CBaseOutputPin. GetDeliveryBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991188"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="c5856-103">CBaseOutputPin. GetDeliveryBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="c5856-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="c5856-104">`GetDeliveryBuffer`方法會抓取包含空緩衝區的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="c5856-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5856-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5856-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c5856-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5856-107">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="c5856-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c5856-108">接收緩衝區 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="c5856-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c5856-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="c5856-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c5856-110">範例開始時間的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c5856-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5856-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="c5856-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="c5856-112">樣本的結束時間指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="c5856-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5856-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c5856-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c5856-114">[**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)介面所支援之旗標的位元組合。</span><span class="sxs-lookup"><span data-stu-id="c5856-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5856-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5856-115">Return value</span></span>

<span data-ttu-id="c5856-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c5856-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c5856-117">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="c5856-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="c5856-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5856-118">Return code</span></span>                                                                                   | <span data-ttu-id="c5856-119">Description</span><span class="sxs-lookup"><span data-stu-id="c5856-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="c5856-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c5856-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c5856-121">成功。</span><span class="sxs-lookup"><span data-stu-id="c5856-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="c5856-122"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="c5856-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="c5856-123">沒有可用的配置器。</span><span class="sxs-lookup"><span data-stu-id="c5856-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5856-124">備註</span><span class="sxs-lookup"><span data-stu-id="c5856-124">Remarks</span></span>

<span data-ttu-id="c5856-125">這個方法會在配置器上呼叫 **IMemAllocator：： GetBuffer** 方法，並將參數傳遞給該方法。</span><span class="sxs-lookup"><span data-stu-id="c5856-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5856-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5856-126">Requirements</span></span>



| <span data-ttu-id="c5856-127">需求</span><span class="sxs-lookup"><span data-stu-id="c5856-127">Requirement</span></span> | <span data-ttu-id="c5856-128">值</span><span class="sxs-lookup"><span data-stu-id="c5856-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5856-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c5856-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c5856-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c5856-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c5856-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5856-131">Library</span></span><br/> | <dl> <span data-ttu-id="c5856-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c5856-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5856-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5856-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5856-134">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="c5856-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




