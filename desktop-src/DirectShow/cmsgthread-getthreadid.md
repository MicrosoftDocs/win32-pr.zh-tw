---
description: 抓取執行緒的識別碼。
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: 'CMsgThread. GetThreadID 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994322"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="08975-103">CMsgThread. GetThreadID 方法</span><span class="sxs-lookup"><span data-stu-id="08975-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="08975-104">抓取執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="08975-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="08975-105">語法</span><span class="sxs-lookup"><span data-stu-id="08975-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="08975-106">參數</span><span class="sxs-lookup"><span data-stu-id="08975-106">Parameters</span></span>

<span data-ttu-id="08975-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="08975-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08975-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="08975-108">Return value</span></span>

<span data-ttu-id="08975-109">傳回 **m \_ ThreadId** 私用資料成員。</span><span class="sxs-lookup"><span data-stu-id="08975-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="08975-110">備註</span><span class="sxs-lookup"><span data-stu-id="08975-110">Remarks</span></span>

<span data-ttu-id="08975-111">此函數會傳回工作者執行緒的 Microsoft Win32 識別碼。</span><span class="sxs-lookup"><span data-stu-id="08975-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="08975-112">您可以在背景工作執行緒或用戶端執行緒上呼叫這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="08975-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="08975-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="08975-113">Requirements</span></span>



| <span data-ttu-id="08975-114">需求</span><span class="sxs-lookup"><span data-stu-id="08975-114">Requirement</span></span> | <span data-ttu-id="08975-115">值</span><span class="sxs-lookup"><span data-stu-id="08975-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08975-116">標頭</span><span class="sxs-lookup"><span data-stu-id="08975-116">Header</span></span><br/>  | <dl> <span data-ttu-id="08975-117"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="08975-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08975-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="08975-118">Library</span></span><br/> | <dl> <span data-ttu-id="08975-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="08975-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08975-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08975-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08975-121">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="08975-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




