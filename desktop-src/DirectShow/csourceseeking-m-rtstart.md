---
description: 開始時間。 依預設，此值設定為零。
ms.assetid: bafa69c3-ead0-4409-abbf-4e8cc325e5f9
title: 'CSourceSeeking：： m_rtStart 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStart
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc7bf18f23177095328c1faee8dd8da28e830b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999303"
---
# <a name="csourceseekingm_rtstart-member"></a><span data-ttu-id="7cbbb-104">CSourceSeeking：： m \_ rtStart 成員</span><span class="sxs-lookup"><span data-stu-id="7cbbb-104">CSourceSeeking::m\_rtStart member</span></span>

<span data-ttu-id="7cbbb-105">開始時間。</span><span class="sxs-lookup"><span data-stu-id="7cbbb-105">Start time.</span></span> <span data-ttu-id="7cbbb-106">依預設，此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="7cbbb-106">By default, the value is set to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbbb-107">語法</span><span class="sxs-lookup"><span data-stu-id="7cbbb-107">Syntax</span></span>


```C++
CRefTime m_rtStart;
```



## <a name="remarks"></a><span data-ttu-id="7cbbb-108">備註</span><span class="sxs-lookup"><span data-stu-id="7cbbb-108">Remarks</span></span>

<span data-ttu-id="7cbbb-109">存取此變數之前，請先保留 **m \_ pLock** 重要區段。</span><span class="sxs-lookup"><span data-stu-id="7cbbb-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbbb-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cbbb-110">Requirements</span></span>



| <span data-ttu-id="7cbbb-111">需求</span><span class="sxs-lookup"><span data-stu-id="7cbbb-111">Requirement</span></span> | <span data-ttu-id="7cbbb-112">值</span><span class="sxs-lookup"><span data-stu-id="7cbbb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbbb-113">標頭</span><span class="sxs-lookup"><span data-stu-id="7cbbb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7cbbb-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7cbbb-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7cbbb-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="7cbbb-115">Library</span></span><br/> | <dl> <span data-ttu-id="7cbbb-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7cbbb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cbbb-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cbbb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbbb-118">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="7cbbb-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




