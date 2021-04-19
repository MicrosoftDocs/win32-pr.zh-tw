---
description: 函式方法。
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
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996250"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="6e44b-103">CAMThread. CAMThread 函數</span><span class="sxs-lookup"><span data-stu-id="6e44b-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="6e44b-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6e44b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e44b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e44b-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="6e44b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e44b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e44b-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="6e44b-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6e44b-108">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="6e44b-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6e44b-109">如果函式失敗，此參數會收到錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6e44b-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="6e44b-110">如果發生這種情況，則物件不是處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e44b-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="6e44b-111">為了與舊版 strmbase 回溯相容，此參數預設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6e44b-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="6e44b-112">不過，最好是傳遞非 **Null** 值，讓呼叫端可以檢查物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e44b-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e44b-113">備註</span><span class="sxs-lookup"><span data-stu-id="6e44b-113">Remarks</span></span>

<span data-ttu-id="6e44b-114">此函數不會建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="6e44b-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="6e44b-115">若要建立執行緒，請呼叫 [**CAMThread：： create**](camthread-create.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e44b-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e44b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e44b-116">Requirements</span></span>



| <span data-ttu-id="6e44b-117">需求</span><span class="sxs-lookup"><span data-stu-id="6e44b-117">Requirement</span></span> | <span data-ttu-id="6e44b-118">值</span><span class="sxs-lookup"><span data-stu-id="6e44b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e44b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="6e44b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6e44b-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e44b-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6e44b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e44b-121">Library</span></span><br/> | <dl> <span data-ttu-id="6e44b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6e44b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e44b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e44b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e44b-124">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="6e44b-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




