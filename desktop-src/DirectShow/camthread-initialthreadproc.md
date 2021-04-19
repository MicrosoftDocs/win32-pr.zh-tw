---
description: InitialThreadProc 方法會呼叫主要執行緒程式。
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: " (Wxutil 的 CAMThread.InitialThreadProc 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001916"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="73b1b-103">CAMThread.InitialThreadProc 方法</span><span class="sxs-lookup"><span data-stu-id="73b1b-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="73b1b-104">`InitialThreadProc`方法會呼叫主要執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="73b1b-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b1b-105">語法</span><span class="sxs-lookup"><span data-stu-id="73b1b-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="73b1b-106">參數</span><span class="sxs-lookup"><span data-stu-id="73b1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b1b-107">*光伏*</span><span class="sxs-lookup"><span data-stu-id="73b1b-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="73b1b-108">`this` 指標。</span><span class="sxs-lookup"><span data-stu-id="73b1b-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b1b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="73b1b-109">Return value</span></span>

<span data-ttu-id="73b1b-110">傳回 [**CAMThread：： ThreadProc**](camthread-threadproc.md)所傳回的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="73b1b-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="73b1b-111">衍生的類別會定義此值。</span><span class="sxs-lookup"><span data-stu-id="73b1b-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73b1b-112">備註</span><span class="sxs-lookup"><span data-stu-id="73b1b-112">Remarks</span></span>

<span data-ttu-id="73b1b-113">[**CAMThread：： Create**](camthread-create.md)方法會在建立執行緒時，針對執行緒程式使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="73b1b-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="73b1b-114">它使用 `this` 指標做為執行緒引數。</span><span class="sxs-lookup"><span data-stu-id="73b1b-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="73b1b-115">這個方法會呼叫 [**CAMThread：： CoInitializeHelper**](camthread-coinitializehelper.md) 方法，然後再 ThreadProc。</span><span class="sxs-lookup"><span data-stu-id="73b1b-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b1b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="73b1b-116">Requirements</span></span>



| <span data-ttu-id="73b1b-117">需求</span><span class="sxs-lookup"><span data-stu-id="73b1b-117">Requirement</span></span> | <span data-ttu-id="73b1b-118">值</span><span class="sxs-lookup"><span data-stu-id="73b1b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b1b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="73b1b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="73b1b-120"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="73b1b-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="73b1b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="73b1b-121">Library</span></span><br/> | <dl> <span data-ttu-id="73b1b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="73b1b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b1b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73b1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b1b-124">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="73b1b-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




