---
description: ReceiveMultiple 方法會將一批媒體範例傳遞給輸入圖釘。
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: 'COutputQueue. ReceiveMultiple 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982077"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="ddc87-103">COutputQueue. ReceiveMultiple 方法</span><span class="sxs-lookup"><span data-stu-id="ddc87-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="ddc87-104">方法會將 `ReceiveMultiple` 一批媒體範例傳遞給輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="ddc87-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc87-105">語法</span><span class="sxs-lookup"><span data-stu-id="ddc87-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="ddc87-106">參數</span><span class="sxs-lookup"><span data-stu-id="ddc87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc87-107">*ppSamples*</span><span class="sxs-lookup"><span data-stu-id="ddc87-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc87-108">範例陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="ddc87-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="ddc87-109">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="ddc87-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc87-110">陣列中的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="ddc87-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="ddc87-111">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="ddc87-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc87-112">變數的指標，此變數會接收成功傳遞的樣本數。</span><span class="sxs-lookup"><span data-stu-id="ddc87-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc87-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ddc87-113">Return value</span></span>

<span data-ttu-id="ddc87-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ddc87-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ddc87-115">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="ddc87-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ddc87-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ddc87-116">Return code</span></span>                                                                             | <span data-ttu-id="ddc87-117">Description</span><span class="sxs-lookup"><span data-stu-id="ddc87-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ddc87-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc87-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ddc87-119">在處理這個範例之前，收到的資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="ddc87-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="ddc87-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ddc87-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ddc87-121">成功。</span><span class="sxs-lookup"><span data-stu-id="ddc87-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="ddc87-122">備註</span><span class="sxs-lookup"><span data-stu-id="ddc87-122">Remarks</span></span>

<span data-ttu-id="ddc87-123">如果物件使用執行緒，這個方法會將陣列中傳遞的所有範例排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ddc87-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="ddc87-124">否則，方法會在輸入釘選上呼叫 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。</span><span class="sxs-lookup"><span data-stu-id="ddc87-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc87-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddc87-125">Requirements</span></span>



| <span data-ttu-id="ddc87-126">需求</span><span class="sxs-lookup"><span data-stu-id="ddc87-126">Requirement</span></span> | <span data-ttu-id="ddc87-127">值</span><span class="sxs-lookup"><span data-stu-id="ddc87-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc87-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ddc87-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ddc87-129"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ddc87-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ddc87-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ddc87-130">Library</span></span><br/> | <dl> <span data-ttu-id="ddc87-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ddc87-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc87-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddc87-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc87-133">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="ddc87-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




