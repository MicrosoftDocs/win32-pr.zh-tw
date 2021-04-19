---
description: Connect 方法會完成輸出釘選的連接。
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: 'CPullPin 連接方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980151"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="bc9dd-103">CPullPin 方法</span><span class="sxs-lookup"><span data-stu-id="bc9dd-103">CPullPin.Connect method</span></span>

<span data-ttu-id="bc9dd-104">`Connect`方法會完成輸出釘選的連接。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc9dd-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="bc9dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc9dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc9dd-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="bc9dd-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="bc9dd-108">輸出釘選的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="bc9dd-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="bc9dd-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="bc9dd-110">輸入釘選配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc9dd-111">*bSync*</span><span class="sxs-lookup"><span data-stu-id="bc9dd-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="bc9dd-112">指定是否要使用同步讀取的布林值。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="bc9dd-113">若 **為 TRUE**，則 pin 會在輸出釘選上執行同步讀取作業。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="bc9dd-114">如果 **為 FALSE**，則表示 pin 會發出非同步讀取要求。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc9dd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc9dd-115">Return value</span></span>

<span data-ttu-id="bc9dd-116">傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="bc9dd-117">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-117">Possible values include the following.</span></span>



| <span data-ttu-id="bc9dd-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc9dd-118">Return code</span></span>                                                                                               | <span data-ttu-id="bc9dd-119">Description</span><span class="sxs-lookup"><span data-stu-id="bc9dd-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc9dd-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9dd-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="bc9dd-121">成功。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="bc9dd-122"><dt>**VFW \_ E \_ 已 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9dd-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bc9dd-123">輸入 pin 已連線。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="bc9dd-124"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9dd-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="bc9dd-125">輸出 pin 不會公開 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc9dd-126">備註</span><span class="sxs-lookup"><span data-stu-id="bc9dd-126">Remarks</span></span>

<span data-ttu-id="bc9dd-127">在輸入 pin 的連接進程期間，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="bc9dd-128">如果方法失敗，則 pin 應會使連接失敗。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="bc9dd-129">這個方法會查詢 **IAsyncReader** 介面的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="bc9dd-130">如果成功，則會呼叫 [**CPullPin：:D ecideallocator**](cpullpin-decideallocator.md) 來協調連接的配置器。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="bc9dd-131">如果您的輸入 pin 有慣用的配置器，請在 *pAlloc* 參數中指定它; **DecideAllocator** 方法會將這個指標傳遞給輸出釘選的 [**IAsyncReader：： RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) 方法。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="bc9dd-132">否則，請將 *pAlloc* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="bc9dd-133">如果 *bSync* 的值為 **TRUE**， **CPullPin** 物件會藉由呼叫輸出釘選的 [**IAsyncReader：： SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)，來建立同步讀取要求。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="bc9dd-134">否則，它會呼叫 [**IAsyncReader：： Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) 方法來產生重迭的讀取要求。</span><span class="sxs-lookup"><span data-stu-id="bc9dd-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9dd-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc9dd-135">Requirements</span></span>



| <span data-ttu-id="bc9dd-136">需求</span><span class="sxs-lookup"><span data-stu-id="bc9dd-136">Requirement</span></span> | <span data-ttu-id="bc9dd-137">值</span><span class="sxs-lookup"><span data-stu-id="bc9dd-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9dd-138">標頭</span><span class="sxs-lookup"><span data-stu-id="bc9dd-138">Header</span></span><br/>  | <dl> <span data-ttu-id="bc9dd-139"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc9dd-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="bc9dd-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc9dd-140">Library</span></span><br/> | <dl> <span data-ttu-id="bc9dd-141"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bc9dd-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9dd-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc9dd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9dd-143">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="bc9dd-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




