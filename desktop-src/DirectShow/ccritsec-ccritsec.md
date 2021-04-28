---
description: CCritSec。 CCritSec 函式-函數方法。
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: 'CCritSec. CCritSec (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119796"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="0ff25-103">CCritSec. CCritSec 函數</span><span class="sxs-lookup"><span data-stu-id="0ff25-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="0ff25-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0ff25-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff25-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ff25-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="0ff25-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ff25-106">Parameters</span></span>

<span data-ttu-id="0ff25-107">這個函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="0ff25-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff25-108">備註</span><span class="sxs-lookup"><span data-stu-id="0ff25-108">Remarks</span></span>

<span data-ttu-id="0ff25-109">這個方法會呼叫 [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) 函數，以初始化重要區段。</span><span class="sxs-lookup"><span data-stu-id="0ff25-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff25-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ff25-110">Requirements</span></span>



| <span data-ttu-id="0ff25-111">需求</span><span class="sxs-lookup"><span data-stu-id="0ff25-111">Requirement</span></span> | <span data-ttu-id="0ff25-112">值</span><span class="sxs-lookup"><span data-stu-id="0ff25-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff25-113">標頭</span><span class="sxs-lookup"><span data-stu-id="0ff25-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff25-114"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0ff25-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0ff25-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ff25-115">Library</span></span><br/> | <dl> <span data-ttu-id="0ff25-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0ff25-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff25-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ff25-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff25-118">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="0ff25-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

