---
description: 資料流程的持續時間。 根據預設，值會設定為 CSourceSeeking：： m \_ rtStop 成員變數的值。
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'CSourceSeeking：： m_rtDuration 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995785"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="a0bc9-104">CSourceSeeking：： m \_ rtDuration 成員</span><span class="sxs-lookup"><span data-stu-id="a0bc9-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="a0bc9-105">資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="a0bc9-105">Duration of the stream.</span></span> <span data-ttu-id="a0bc9-106">根據預設，值會設定為 [**CSourceSeeking：： m \_ rtStop**](csourceseeking-m-rtstop.md) 成員變數的值。</span><span class="sxs-lookup"><span data-stu-id="a0bc9-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bc9-107">語法</span><span class="sxs-lookup"><span data-stu-id="a0bc9-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="a0bc9-108">備註</span><span class="sxs-lookup"><span data-stu-id="a0bc9-108">Remarks</span></span>

<span data-ttu-id="a0bc9-109">存取此變數之前，請先保留 **m \_ pLock** 重要區段。</span><span class="sxs-lookup"><span data-stu-id="a0bc9-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0bc9-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0bc9-110">Requirements</span></span>



| <span data-ttu-id="a0bc9-111">需求</span><span class="sxs-lookup"><span data-stu-id="a0bc9-111">Requirement</span></span> | <span data-ttu-id="a0bc9-112">值</span><span class="sxs-lookup"><span data-stu-id="a0bc9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bc9-113">標頭</span><span class="sxs-lookup"><span data-stu-id="a0bc9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a0bc9-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a0bc9-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0bc9-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="a0bc9-115">Library</span></span><br/> | <dl> <span data-ttu-id="a0bc9-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a0bc9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bc9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0bc9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bc9-118">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="a0bc9-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




