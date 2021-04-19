---
description: Receive 方法會將媒體範例傳遞給輸入 pin。
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: 'COutputQueue 的 Receive 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989264"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="95dbd-103">COutputQueue 接收方法</span><span class="sxs-lookup"><span data-stu-id="95dbd-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="95dbd-104">方法會將 `Receive` 媒體範例傳遞給輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="95dbd-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="95dbd-105">語法</span><span class="sxs-lookup"><span data-stu-id="95dbd-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="95dbd-106">參數</span><span class="sxs-lookup"><span data-stu-id="95dbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95dbd-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="95dbd-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="95dbd-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="95dbd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95dbd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="95dbd-109">Return value</span></span>

<span data-ttu-id="95dbd-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="95dbd-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="95dbd-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="95dbd-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="95dbd-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="95dbd-112">Return code</span></span>                                                                             | <span data-ttu-id="95dbd-113">Description</span><span class="sxs-lookup"><span data-stu-id="95dbd-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95dbd-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="95dbd-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="95dbd-115">在處理這個範例之前，收到的資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="95dbd-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="95dbd-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="95dbd-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="95dbd-117">成功。</span><span class="sxs-lookup"><span data-stu-id="95dbd-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="95dbd-118">備註</span><span class="sxs-lookup"><span data-stu-id="95dbd-118">Remarks</span></span>

<span data-ttu-id="95dbd-119">這個方法會呼叫 [**COutputQueue：： ReceiveMultiple**](coutputqueue-receivemultiple.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="95dbd-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="95dbd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="95dbd-120">Requirements</span></span>



| <span data-ttu-id="95dbd-121">需求</span><span class="sxs-lookup"><span data-stu-id="95dbd-121">Requirement</span></span> | <span data-ttu-id="95dbd-122">值</span><span class="sxs-lookup"><span data-stu-id="95dbd-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95dbd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="95dbd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="95dbd-124"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="95dbd-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95dbd-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="95dbd-125">Library</span></span><br/> | <dl> <span data-ttu-id="95dbd-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="95dbd-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95dbd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95dbd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95dbd-128">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="95dbd-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




