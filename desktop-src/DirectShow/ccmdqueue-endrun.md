---
description: EndRun 方法會切換至已停止或已暫停模式。
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: 'CCmdQueue. EndRun 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998374"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="d8e09-103">CCmdQueue. EndRun 方法</span><span class="sxs-lookup"><span data-stu-id="d8e09-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="d8e09-104">`EndRun`方法會切換至已停止或已暫停模式。</span><span class="sxs-lookup"><span data-stu-id="d8e09-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e09-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8e09-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="d8e09-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8e09-106">Parameters</span></span>

<span data-ttu-id="d8e09-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d8e09-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8e09-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8e09-108">Return value</span></span>

<span data-ttu-id="d8e09-109">傳回相依于執行的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d8e09-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e09-110">備註</span><span class="sxs-lookup"><span data-stu-id="d8e09-110">Remarks</span></span>

<span data-ttu-id="d8e09-111">在呼叫這個成員函式之後，不知道串流時間與呈現時間之間的時間對應。</span><span class="sxs-lookup"><span data-stu-id="d8e09-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="d8e09-112">呼叫 [**CCmdQueue：： Run**](ccmdqueue-run.md) 成員函式來執行此對應。</span><span class="sxs-lookup"><span data-stu-id="d8e09-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e09-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8e09-113">Requirements</span></span>



| <span data-ttu-id="d8e09-114">需求</span><span class="sxs-lookup"><span data-stu-id="d8e09-114">Requirement</span></span> | <span data-ttu-id="d8e09-115">值</span><span class="sxs-lookup"><span data-stu-id="d8e09-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e09-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d8e09-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d8e09-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d8e09-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8e09-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d8e09-118">Library</span></span><br/> | <dl> <span data-ttu-id="d8e09-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d8e09-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e09-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8e09-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e09-121">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="d8e09-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




