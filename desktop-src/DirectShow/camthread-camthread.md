---
description: CAMThread。 CAMThread 函式-函數方法。
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: 'CAMThread. CAMThread (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096406"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="536ad-103">CAMThread. CAMThread 函數</span><span class="sxs-lookup"><span data-stu-id="536ad-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="536ad-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="536ad-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="536ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="536ad-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="536ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="536ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="536ad-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="536ad-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="536ad-108">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="536ad-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="536ad-109">如果函式失敗，此參數會收到錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="536ad-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="536ad-110">如果發生這種情況，則物件不是處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="536ad-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="536ad-111">為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="536ad-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="536ad-112">不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="536ad-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="536ad-113">備註</span><span class="sxs-lookup"><span data-stu-id="536ad-113">Remarks</span></span>

<span data-ttu-id="536ad-114">此函數不會建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="536ad-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="536ad-115">若要建立執行緒，請呼叫 [**CAMThread：： create**](camthread-create.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="536ad-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="536ad-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="536ad-116">Requirements</span></span>



| <span data-ttu-id="536ad-117">需求</span><span class="sxs-lookup"><span data-stu-id="536ad-117">Requirement</span></span> | <span data-ttu-id="536ad-118">值</span><span class="sxs-lookup"><span data-stu-id="536ad-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536ad-119">標頭</span><span class="sxs-lookup"><span data-stu-id="536ad-119">Header</span></span><br/>  | <dl> <span data-ttu-id="536ad-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="536ad-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="536ad-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="536ad-121">Library</span></span><br/> | <dl> <span data-ttu-id="536ad-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="536ad-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="536ad-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="536ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536ad-124">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="536ad-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




