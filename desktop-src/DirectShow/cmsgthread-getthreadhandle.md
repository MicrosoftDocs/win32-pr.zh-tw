---
description: 在 CMsgThread 物件中抓取執行緒的控制碼。
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: 'CMsgThread. GetThreadHandle 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992943"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="53cf0-103">CMsgThread. GetThreadHandle 方法</span><span class="sxs-lookup"><span data-stu-id="53cf0-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="53cf0-104">在 [**CMsgThread**](cmsgthread.md) 物件中抓取執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53cf0-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cf0-105">語法</span><span class="sxs-lookup"><span data-stu-id="53cf0-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="53cf0-106">參數</span><span class="sxs-lookup"><span data-stu-id="53cf0-106">Parameters</span></span>

<span data-ttu-id="53cf0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="53cf0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53cf0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="53cf0-108">Return value</span></span>

<span data-ttu-id="53cf0-109">傳回執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="53cf0-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="53cf0-110">備註</span><span class="sxs-lookup"><span data-stu-id="53cf0-110">Remarks</span></span>

<span data-ttu-id="53cf0-111">執行緒控制碼可以傳遞給 wait 函數，例如 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)。</span><span class="sxs-lookup"><span data-stu-id="53cf0-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="53cf0-112">執行緒已結束時，執行緒控制碼會發出信號。</span><span class="sxs-lookup"><span data-stu-id="53cf0-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="53cf0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="53cf0-113">Requirements</span></span>



| <span data-ttu-id="53cf0-114">需求</span><span class="sxs-lookup"><span data-stu-id="53cf0-114">Requirement</span></span> | <span data-ttu-id="53cf0-115">值</span><span class="sxs-lookup"><span data-stu-id="53cf0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53cf0-116">標頭</span><span class="sxs-lookup"><span data-stu-id="53cf0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="53cf0-117"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="53cf0-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="53cf0-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="53cf0-118">Library</span></span><br/> | <dl> <span data-ttu-id="53cf0-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="53cf0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53cf0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53cf0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cf0-121">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="53cf0-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

