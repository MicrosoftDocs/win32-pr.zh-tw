---
description: BlockOutputPin 方法會封鎖釘選。
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: 'CDynamicOutputPin. BlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999400"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="81bdb-103">CDynamicOutputPin. BlockOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="81bdb-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="81bdb-104">`BlockOutputPin`方法會封鎖釘選。</span><span class="sxs-lookup"><span data-stu-id="81bdb-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="81bdb-105">當 pin 遭到封鎖時， [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法會等候 pin 變成解除封鎖。</span><span class="sxs-lookup"><span data-stu-id="81bdb-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="81bdb-106">封鎖狀態可防止輸出圖釘傳遞範例、變更其輸出格式，或自行重新連接。</span><span class="sxs-lookup"><span data-stu-id="81bdb-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bdb-107">語法</span><span class="sxs-lookup"><span data-stu-id="81bdb-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="81bdb-108">參數</span><span class="sxs-lookup"><span data-stu-id="81bdb-108">Parameters</span></span>

<span data-ttu-id="81bdb-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="81bdb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81bdb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="81bdb-110">Return value</span></span>

<span data-ttu-id="81bdb-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="81bdb-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81bdb-112">備註</span><span class="sxs-lookup"><span data-stu-id="81bdb-112">Remarks</span></span>

<span data-ttu-id="81bdb-113">在呼叫這個方法之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。</span><span class="sxs-lookup"><span data-stu-id="81bdb-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="81bdb-114">如果串流執行緒正在使用 pin，以傳遞資料或變更連接，請勿呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="81bdb-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="81bdb-115">若要檢查串流執行緒是否正在使用 pin，請呼叫 [**CDynamicOutputPin：： StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="81bdb-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="81bdb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="81bdb-116">Requirements</span></span>



| <span data-ttu-id="81bdb-117">需求</span><span class="sxs-lookup"><span data-stu-id="81bdb-117">Requirement</span></span> | <span data-ttu-id="81bdb-118">值</span><span class="sxs-lookup"><span data-stu-id="81bdb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81bdb-119">標頭</span><span class="sxs-lookup"><span data-stu-id="81bdb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="81bdb-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81bdb-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81bdb-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="81bdb-121">Library</span></span><br/> | <dl> <span data-ttu-id="81bdb-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81bdb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81bdb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81bdb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bdb-124">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="81bdb-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




