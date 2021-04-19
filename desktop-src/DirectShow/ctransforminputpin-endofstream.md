---
description: EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: 'CTransformInputPin. EndOfStream 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978738"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="ea817-104">CTransformInputPin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="ea817-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="ea817-105">`EndOfStream`方法會通知 pin，不需要任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="ea817-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="ea817-106">這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="ea817-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea817-107">語法</span><span class="sxs-lookup"><span data-stu-id="ea817-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="ea817-108">參數</span><span class="sxs-lookup"><span data-stu-id="ea817-108">Parameters</span></span>

<span data-ttu-id="ea817-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ea817-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea817-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea817-110">Return value</span></span>

<span data-ttu-id="ea817-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ea817-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ea817-112">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="ea817-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ea817-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea817-113">Return code</span></span>                                                                                           | <span data-ttu-id="ea817-114">Description</span><span class="sxs-lookup"><span data-stu-id="ea817-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="ea817-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea817-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="ea817-116">成功。</span><span class="sxs-lookup"><span data-stu-id="ea817-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="ea817-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ea817-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="ea817-118">Pin 目前正在排清。</span><span class="sxs-lookup"><span data-stu-id="ea817-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="ea817-119"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="ea817-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ea817-120">輸出針腳未連接。</span><span class="sxs-lookup"><span data-stu-id="ea817-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="ea817-121"><dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="ea817-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="ea817-122">發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea817-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="ea817-123"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="ea817-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="ea817-124">已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="ea817-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="ea817-125">備註</span><span class="sxs-lookup"><span data-stu-id="ea817-125">Remarks</span></span>

<span data-ttu-id="ea817-126">這個方法會呼叫篩選準則的 [**CTransformFilter：： EndOfStream**](ctransformfilter-endofstream.md) 方法，以傳遞下游的結束資料流程通知。</span><span class="sxs-lookup"><span data-stu-id="ea817-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea817-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea817-127">Requirements</span></span>



| <span data-ttu-id="ea817-128">需求</span><span class="sxs-lookup"><span data-stu-id="ea817-128">Requirement</span></span> | <span data-ttu-id="ea817-129">值</span><span class="sxs-lookup"><span data-stu-id="ea817-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea817-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ea817-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ea817-131"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ea817-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea817-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea817-132">Library</span></span><br/> | <dl> <span data-ttu-id="ea817-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ea817-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




