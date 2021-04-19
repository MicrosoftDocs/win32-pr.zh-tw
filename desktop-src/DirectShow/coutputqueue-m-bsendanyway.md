---
description: 覆寫批次處理的旗標。 將此旗標設定為 TRUE 會覆寫 COutputQueue：： m \_ bBatchExact 旗標，並傳遞所有暫止的範例。
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'COutputQueue：： m_bSendAnyway 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990537"
---
# <a name="coutputqueuem_bsendanyway-member"></a><span data-ttu-id="a149c-104">COutputQueue：： m \_ bSendAnyway 成員</span><span class="sxs-lookup"><span data-stu-id="a149c-104">COutputQueue::m\_bSendAnyway member</span></span>

<span data-ttu-id="a149c-105">覆寫批次處理的旗標。</span><span class="sxs-lookup"><span data-stu-id="a149c-105">Flag to override batch processing.</span></span> <span data-ttu-id="a149c-106">將此旗標設定為 **TRUE** 會覆寫 [**COutputQueue：： m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) 旗標，並傳遞所有暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="a149c-106">Setting this flag to **TRUE** overrides the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) flag and delivers all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="a149c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a149c-107">Syntax</span></span>


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a><span data-ttu-id="a149c-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="a149c-108">Requirements</span></span>



| <span data-ttu-id="a149c-109">需求</span><span class="sxs-lookup"><span data-stu-id="a149c-109">Requirement</span></span> | <span data-ttu-id="a149c-110">值</span><span class="sxs-lookup"><span data-stu-id="a149c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a149c-111">標頭</span><span class="sxs-lookup"><span data-stu-id="a149c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a149c-112"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a149c-112"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a149c-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="a149c-113">Library</span></span><br/> | <dl> <span data-ttu-id="a149c-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a149c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a149c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a149c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a149c-116">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="a149c-116">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




