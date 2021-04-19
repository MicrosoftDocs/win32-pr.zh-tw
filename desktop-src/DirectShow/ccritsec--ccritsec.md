---
description: 函式方法。
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: 'CCritSec. ~ CCritSec (Wxutil 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983136"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="d95d5-103">CCritSec. ~ CCritSec 的函式</span><span class="sxs-lookup"><span data-stu-id="d95d5-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="d95d5-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="d95d5-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="d95d5-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="d95d5-106">備註</span><span class="sxs-lookup"><span data-stu-id="d95d5-106">Remarks</span></span>

<span data-ttu-id="d95d5-107">這個方法會呼叫 [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) 函數來刪除重要區段。</span><span class="sxs-lookup"><span data-stu-id="d95d5-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95d5-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="d95d5-108">Requirements</span></span>



| <span data-ttu-id="d95d5-109">需求</span><span class="sxs-lookup"><span data-stu-id="d95d5-109">Requirement</span></span> | <span data-ttu-id="d95d5-110">值</span><span class="sxs-lookup"><span data-stu-id="d95d5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d95d5-111">標頭</span><span class="sxs-lookup"><span data-stu-id="d95d5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d95d5-112"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d95d5-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d95d5-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="d95d5-113">Library</span></span><br/> | <dl> <span data-ttu-id="d95d5-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d95d5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95d5-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d95d5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95d5-116">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="d95d5-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

