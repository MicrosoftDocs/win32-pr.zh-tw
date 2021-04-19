---
description: GetRequestParam 方法會抓取最新的要求。
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: 'CAMThread. GetRequestParam 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dd6584123663bb36f1db4771fb3f86d7ac4f5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979492"
---
# <a name="camthreadgetrequestparam-method"></a><span data-ttu-id="33dc2-103">CAMThread. GetRequestParam 方法</span><span class="sxs-lookup"><span data-stu-id="33dc2-103">CAMThread.GetRequestParam method</span></span>

<span data-ttu-id="33dc2-104">方法會抓取 `GetRequestParam` 最新的要求。</span><span class="sxs-lookup"><span data-stu-id="33dc2-104">The `GetRequestParam` method retrieves the latest request.</span></span>

## <a name="syntax"></a><span data-ttu-id="33dc2-105">語法</span><span class="sxs-lookup"><span data-stu-id="33dc2-105">Syntax</span></span>


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a><span data-ttu-id="33dc2-106">參數</span><span class="sxs-lookup"><span data-stu-id="33dc2-106">Parameters</span></span>

<span data-ttu-id="33dc2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="33dc2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33dc2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="33dc2-108">Return value</span></span>

<span data-ttu-id="33dc2-109">傳回最近傳遞給 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法的參數值。</span><span class="sxs-lookup"><span data-stu-id="33dc2-109">Returns the value of the parameter that was passed most recently to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dc2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="33dc2-110">Requirements</span></span>



| <span data-ttu-id="33dc2-111">需求</span><span class="sxs-lookup"><span data-stu-id="33dc2-111">Requirement</span></span> | <span data-ttu-id="33dc2-112">值</span><span class="sxs-lookup"><span data-stu-id="33dc2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33dc2-113">標頭</span><span class="sxs-lookup"><span data-stu-id="33dc2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="33dc2-114"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="33dc2-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="33dc2-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="33dc2-115">Library</span></span><br/> | <dl> <span data-ttu-id="33dc2-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="33dc2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33dc2-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33dc2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33dc2-118">**CAMThread 類別**</span><span class="sxs-lookup"><span data-stu-id="33dc2-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




