---
description: 抓取包含要求的佇列 CMsg 物件。
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: 'CMsgThread. GetThreadMsg 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984093"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="10a7c-103">CMsgThread. GetThreadMsg 方法</span><span class="sxs-lookup"><span data-stu-id="10a7c-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="10a7c-104">抓取包含要求的佇列 [**CMsg**](cmsg.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="10a7c-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="10a7c-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="10a7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="10a7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a7c-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="10a7c-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="10a7c-108">已配置之 [**CMsg**](cmsg.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="10a7c-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a7c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="10a7c-109">Return value</span></span>

<span data-ttu-id="10a7c-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10a7c-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10a7c-111">備註</span><span class="sxs-lookup"><span data-stu-id="10a7c-111">Remarks</span></span>

<span data-ttu-id="10a7c-112">此成員函式會從背景工作執行緒的私用 [**ThreadProc**](camthread-threadproc.md) 函式呼叫，以取得下一個成員函式。</span><span class="sxs-lookup"><span data-stu-id="10a7c-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="10a7c-113">*Msg* 參數應指向已配置的 [**CMsg**](cmsg.md)物件，該物件將會填入佇列中下一個要求的參數。</span><span class="sxs-lookup"><span data-stu-id="10a7c-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="10a7c-114">如果沒有已排入佇列的要求，此成員函式會封鎖，直到下一個要求排入佇列 (呼叫 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md) 成員函數) 。</span><span class="sxs-lookup"><span data-stu-id="10a7c-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="10a7c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10a7c-115">Requirements</span></span>



| <span data-ttu-id="10a7c-116">需求</span><span class="sxs-lookup"><span data-stu-id="10a7c-116">Requirement</span></span> | <span data-ttu-id="10a7c-117">值</span><span class="sxs-lookup"><span data-stu-id="10a7c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a7c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="10a7c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="10a7c-119"><dt>Msgthrd (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="10a7c-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="10a7c-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="10a7c-120">Library</span></span><br/> | <dl> <span data-ttu-id="10a7c-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="10a7c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10a7c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10a7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a7c-123">**CMsgThread 類別**</span><span class="sxs-lookup"><span data-stu-id="10a7c-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




