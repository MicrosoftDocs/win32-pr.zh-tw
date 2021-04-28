---
description: CMsgThread。 CMsgThread 函式-函數方法。
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: 'CMsgThread. CMsgThread (Msgthrd. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095366"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="48e0c-103">CMsgThread. CMsgThread 函數</span><span class="sxs-lookup"><span data-stu-id="48e0c-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="48e0c-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="48e0c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="48e0c-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="48e0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="48e0c-106">Parameters</span></span>

<span data-ttu-id="48e0c-107">這個函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="48e0c-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e0c-108">備註</span><span class="sxs-lookup"><span data-stu-id="48e0c-108">Remarks</span></span>

<span data-ttu-id="48e0c-109">建立訊息執行緒物件並不會自動建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="48e0c-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="48e0c-110">您必須呼叫 [**CMsgThread：： CreateThread**](cmsgthread-createthread.md) 成員函式來建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="48e0c-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e0c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="48e0c-111">Requirements</span></span>



| <span data-ttu-id="48e0c-112">需求</span><span class="sxs-lookup"><span data-stu-id="48e0c-112">Requirement</span></span> | <span data-ttu-id="48e0c-113">值</span><span class="sxs-lookup"><span data-stu-id="48e0c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e0c-114">標頭</span><span class="sxs-lookup"><span data-stu-id="48e0c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="48e0c-115"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="48e0c-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48e0c-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="48e0c-116">Library</span></span><br/> | <dl> <span data-ttu-id="48e0c-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="48e0c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e0c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48e0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e0c-119">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="48e0c-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




