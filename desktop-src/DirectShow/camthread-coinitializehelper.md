---
description: CoInitializeHelper 方法會線上程的開頭呼叫 CoInitializeEx 函數。
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: 'CAMThread. CoInitializeHelper 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997687"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="dac45-103">CAMThread. CoInitializeHelper 方法</span><span class="sxs-lookup"><span data-stu-id="dac45-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="dac45-104">`CoInitializeHelper`方法會線上程的開頭呼叫 CoInitializeEx 函數。</span><span class="sxs-lookup"><span data-stu-id="dac45-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac45-105">語法</span><span class="sxs-lookup"><span data-stu-id="dac45-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="dac45-106">參數</span><span class="sxs-lookup"><span data-stu-id="dac45-106">Parameters</span></span>

<span data-ttu-id="dac45-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dac45-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dac45-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dac45-108">Return value</span></span>

<span data-ttu-id="dac45-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dac45-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dac45-110">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="dac45-110">The following are possible values.</span></span>



| <span data-ttu-id="dac45-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dac45-111">Return code</span></span>                                                                             | <span data-ttu-id="dac45-112">Description</span><span class="sxs-lookup"><span data-stu-id="dac45-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="dac45-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="dac45-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dac45-114">無法使用 CoInitializeEx 函數。</span><span class="sxs-lookup"><span data-stu-id="dac45-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="dac45-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dac45-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dac45-116">成功。</span><span class="sxs-lookup"><span data-stu-id="dac45-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="dac45-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="dac45-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="dac45-118">失敗。</span><span class="sxs-lookup"><span data-stu-id="dac45-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="dac45-119">備註</span><span class="sxs-lookup"><span data-stu-id="dac45-119">Remarks</span></span>

<span data-ttu-id="dac45-120">[**CAMThread：： InitialThreadProc**](camthread-initialthreadproc.md)方法會呼叫此 helper 方法，此方法會呼叫 CoInitializeEx 函數。</span><span class="sxs-lookup"><span data-stu-id="dac45-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="dac45-121">它會使用 COINIT \_ disable \_ OLE1DDE 旗標來停用動態資料交換 (DDE) 。</span><span class="sxs-lookup"><span data-stu-id="dac45-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="dac45-122">如需詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="dac45-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac45-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dac45-123">Requirements</span></span>



| <span data-ttu-id="dac45-124">需求</span><span class="sxs-lookup"><span data-stu-id="dac45-124">Requirement</span></span> | <span data-ttu-id="dac45-125">值</span><span class="sxs-lookup"><span data-stu-id="dac45-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac45-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dac45-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dac45-127"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dac45-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dac45-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="dac45-128">Library</span></span><br/> | <dl> <span data-ttu-id="dac45-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dac45-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac45-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dac45-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac45-131">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="dac45-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




