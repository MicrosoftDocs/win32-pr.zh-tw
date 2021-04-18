---
description: Pause 方法會通知串流執行緒成為使用中狀態。
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: 'CSourceStream： Pause 方法 (Source. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996415"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="3c919-103">CSourceStream. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="3c919-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="3c919-104">`Pause`方法會通知串流執行緒成為使用中。</span><span class="sxs-lookup"><span data-stu-id="3c919-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c919-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c919-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="3c919-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c919-106">Parameters</span></span>

<span data-ttu-id="3c919-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3c919-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c919-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c919-108">Return value</span></span>

<span data-ttu-id="3c919-109">傳回 \_ [OK] 或 [E 未 \_ 預期]。</span><span class="sxs-lookup"><span data-stu-id="3c919-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c919-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c919-110">Remarks</span></span>

<span data-ttu-id="3c919-111">[**CSourceStream：： Active**](csourcestream-active.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3c919-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="3c919-112">當 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md) 方法收到此要求時，它會呼叫 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c919-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c919-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c919-113">Requirements</span></span>



| <span data-ttu-id="3c919-114">需求</span><span class="sxs-lookup"><span data-stu-id="3c919-114">Requirement</span></span> | <span data-ttu-id="3c919-115">值</span><span class="sxs-lookup"><span data-stu-id="3c919-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c919-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3c919-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3c919-117"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="3c919-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3c919-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c919-118">Library</span></span><br/> | <dl> <span data-ttu-id="3c919-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3c919-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c919-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c919-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c919-121">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="3c919-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




