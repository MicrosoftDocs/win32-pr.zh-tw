---
description: CCritSec. ~ CCritSec 的函式-函式方法。
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
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095806"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="defe3-103">CCritSec. ~ CCritSec 的函式</span><span class="sxs-lookup"><span data-stu-id="defe3-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="defe3-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="defe3-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="defe3-105">語法</span><span class="sxs-lookup"><span data-stu-id="defe3-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="defe3-106">備註</span><span class="sxs-lookup"><span data-stu-id="defe3-106">Remarks</span></span>

<span data-ttu-id="defe3-107">這個方法會呼叫 [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) 函數來刪除重要區段。</span><span class="sxs-lookup"><span data-stu-id="defe3-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="defe3-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="defe3-108">Requirements</span></span>



| <span data-ttu-id="defe3-109">需求</span><span class="sxs-lookup"><span data-stu-id="defe3-109">Requirement</span></span> | <span data-ttu-id="defe3-110">值</span><span class="sxs-lookup"><span data-stu-id="defe3-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="defe3-111">標頭</span><span class="sxs-lookup"><span data-stu-id="defe3-111">Header</span></span><br/>  | <dl> <span data-ttu-id="defe3-112"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="defe3-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="defe3-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="defe3-113">Library</span></span><br/> | <dl> <span data-ttu-id="defe3-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="defe3-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defe3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="defe3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defe3-116">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="defe3-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

