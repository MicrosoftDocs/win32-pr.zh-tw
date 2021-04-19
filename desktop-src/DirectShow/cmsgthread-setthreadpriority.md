---
description: 使用 Microsoft Win32 SetThreadPriority 函式，將執行緒的優先順序設定為新的值。
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: 'CMsgThread. SetThreadPriority 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981408"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="749f5-103">CMsgThread. SetThreadPriority 方法</span><span class="sxs-lookup"><span data-stu-id="749f5-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="749f5-104">使用 Microsoft Win32 **SetThreadPriority** 函式，將執行緒的優先順序設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="749f5-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="749f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="749f5-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="749f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="749f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="749f5-107">*nPriority*</span><span class="sxs-lookup"><span data-stu-id="749f5-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="749f5-108">執行緒的優先權。</span><span class="sxs-lookup"><span data-stu-id="749f5-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="749f5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="749f5-109">Return value</span></span>

<span data-ttu-id="749f5-110">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="749f5-110">Returns one of the following values.</span></span>



| <span data-ttu-id="749f5-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="749f5-111">Return code</span></span>                                                                              | <span data-ttu-id="749f5-112">Description</span><span class="sxs-lookup"><span data-stu-id="749f5-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="749f5-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="749f5-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="749f5-114">已成功設定優先順序。</span><span class="sxs-lookup"><span data-stu-id="749f5-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="749f5-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="749f5-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="749f5-116">未設定優先權。</span><span class="sxs-lookup"><span data-stu-id="749f5-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="749f5-117">備註</span><span class="sxs-lookup"><span data-stu-id="749f5-117">Remarks</span></span>

<span data-ttu-id="749f5-118">用戶端和背景工作執行緒可以呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="749f5-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="749f5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="749f5-119">Requirements</span></span>



| <span data-ttu-id="749f5-120">需求</span><span class="sxs-lookup"><span data-stu-id="749f5-120">Requirement</span></span> | <span data-ttu-id="749f5-121">值</span><span class="sxs-lookup"><span data-stu-id="749f5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="749f5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="749f5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="749f5-123"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="749f5-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="749f5-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="749f5-124">Library</span></span><br/> | <dl> <span data-ttu-id="749f5-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="749f5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="749f5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="749f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749f5-127">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="749f5-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




