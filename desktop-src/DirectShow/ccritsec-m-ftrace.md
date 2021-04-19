---
description: 指定是否要追蹤此鎖定的布林值。
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'CCritSec：： m_fTrace 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987949"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="8712d-103">CCritSec：： m \_ fTrace 成員</span><span class="sxs-lookup"><span data-stu-id="8712d-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="8712d-104">指定是否要追蹤此鎖定的布林值。</span><span class="sxs-lookup"><span data-stu-id="8712d-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="8712d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8712d-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="8712d-106">備註</span><span class="sxs-lookup"><span data-stu-id="8712d-106">Remarks</span></span>

<span data-ttu-id="8712d-107">這個成員變數只會在基類的 debug 版本中定義。</span><span class="sxs-lookup"><span data-stu-id="8712d-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="8712d-108">如果值為 **TRUE**，會將鎖定狀態的追蹤寫入至 debug 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="8712d-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="8712d-109">重要區段的 (偵錯工具記錄必須為使用 ) 中。如需詳細資訊，請參閱 [**DbgLockTrace**](dbglocktrace.md)。</span><span class="sxs-lookup"><span data-stu-id="8712d-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8712d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8712d-110">Requirements</span></span>



| <span data-ttu-id="8712d-111">需求</span><span class="sxs-lookup"><span data-stu-id="8712d-111">Requirement</span></span> | <span data-ttu-id="8712d-112">值</span><span class="sxs-lookup"><span data-stu-id="8712d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8712d-113">標頭</span><span class="sxs-lookup"><span data-stu-id="8712d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="8712d-114"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8712d-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8712d-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="8712d-115">Library</span></span><br/> | <dl> <span data-ttu-id="8712d-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8712d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8712d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8712d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8712d-118">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="8712d-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




