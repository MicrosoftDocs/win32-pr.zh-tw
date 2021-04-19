---
description: 使用 Microsoft Win32 GetThreadPriority 函式來取得目前背景工作執行緒的優先權。
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: 'CMsgThread. GetThreadPriority 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978633"
---
# <a name="cmsgthreadgetthreadpriority-method"></a><span data-ttu-id="771cb-103">CMsgThread. GetThreadPriority 方法</span><span class="sxs-lookup"><span data-stu-id="771cb-103">CMsgThread.GetThreadPriority method</span></span>

<span data-ttu-id="771cb-104">使用 Microsoft Win32 **GetThreadPriority** 函式來取得目前背景工作執行緒的優先權。</span><span class="sxs-lookup"><span data-stu-id="771cb-104">Uses the Microsoft Win32 **GetThreadPriority** function to retrieve the priority of the current worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="771cb-105">語法</span><span class="sxs-lookup"><span data-stu-id="771cb-105">Syntax</span></span>


```C++
int GetThreadPriority();
```



## <a name="parameters"></a><span data-ttu-id="771cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="771cb-106">Parameters</span></span>

<span data-ttu-id="771cb-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="771cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="771cb-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="771cb-108">Return value</span></span>

<span data-ttu-id="771cb-109">以整數形式傳回執行緒優先權。</span><span class="sxs-lookup"><span data-stu-id="771cb-109">Returns the thread priority as an integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="771cb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="771cb-110">Requirements</span></span>



| <span data-ttu-id="771cb-111">需求</span><span class="sxs-lookup"><span data-stu-id="771cb-111">Requirement</span></span> | <span data-ttu-id="771cb-112">值</span><span class="sxs-lookup"><span data-stu-id="771cb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="771cb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="771cb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="771cb-114"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="771cb-114"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="771cb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="771cb-115">Library</span></span><br/> | <dl> <span data-ttu-id="771cb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="771cb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="771cb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="771cb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771cb-118">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="771cb-118">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




