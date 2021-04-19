---
description: ThreadExists 方法會查詢執行緒是否存在。
ms.assetid: 16be31c5-fae0-45d7-905d-4a2eef1ed819
title: 'CAMThread. ThreadExists 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadExists
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32e727d8beb984a660c82ec0e1398b7f13eb4af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995381"
---
# <a name="camthreadthreadexists-method"></a><span data-ttu-id="49148-103">CAMThread. ThreadExists 方法</span><span class="sxs-lookup"><span data-stu-id="49148-103">CAMThread.ThreadExists method</span></span>

<span data-ttu-id="49148-104">`ThreadExists`方法會查詢執行緒是否存在。</span><span class="sxs-lookup"><span data-stu-id="49148-104">The `ThreadExists` method queries whether the thread exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="49148-105">語法</span><span class="sxs-lookup"><span data-stu-id="49148-105">Syntax</span></span>


```C++
BOOL ThreadExists();
```



## <a name="parameters"></a><span data-ttu-id="49148-106">參數</span><span class="sxs-lookup"><span data-stu-id="49148-106">Parameters</span></span>

<span data-ttu-id="49148-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="49148-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49148-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="49148-108">Return value</span></span>

<span data-ttu-id="49148-109">如果執行緒存在，則傳回 **TRUE** ，如果執行緒不存在則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="49148-109">Returns **TRUE** if the thread exists, or **FALSE** if the thread does not exist.</span></span>

## <a name="requirements"></a><span data-ttu-id="49148-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="49148-110">Requirements</span></span>



| <span data-ttu-id="49148-111">需求</span><span class="sxs-lookup"><span data-stu-id="49148-111">Requirement</span></span> | <span data-ttu-id="49148-112">值</span><span class="sxs-lookup"><span data-stu-id="49148-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49148-113">標頭</span><span class="sxs-lookup"><span data-stu-id="49148-113">Header</span></span><br/>  | <dl> <span data-ttu-id="49148-114"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="49148-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="49148-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="49148-115">Library</span></span><br/> | <dl> <span data-ttu-id="49148-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="49148-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49148-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49148-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49148-118">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="49148-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




