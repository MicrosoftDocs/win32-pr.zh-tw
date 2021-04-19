---
description: 停止時間。 根據預設，值會設定為非常大的數位。 衍生的類別可以重設其函式中的值，或初始化篩選時的值。
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'CSourceSeeking：： m_rtStop 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981309"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="1e0fd-105">CSourceSeeking：： m \_ rtStop 成員</span><span class="sxs-lookup"><span data-stu-id="1e0fd-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="1e0fd-106">停止時間。</span><span class="sxs-lookup"><span data-stu-id="1e0fd-106">Stop time.</span></span> <span data-ttu-id="1e0fd-107">根據預設，值會設定為非常大的數位。</span><span class="sxs-lookup"><span data-stu-id="1e0fd-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="1e0fd-108">衍生的類別可以重設其函式中的值，或初始化篩選時的值。</span><span class="sxs-lookup"><span data-stu-id="1e0fd-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e0fd-109">語法</span><span class="sxs-lookup"><span data-stu-id="1e0fd-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="1e0fd-110">備註</span><span class="sxs-lookup"><span data-stu-id="1e0fd-110">Remarks</span></span>

<span data-ttu-id="1e0fd-111">存取此變數之前，請先保留 **m \_ pLock** 重要區段。</span><span class="sxs-lookup"><span data-stu-id="1e0fd-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e0fd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e0fd-112">Requirements</span></span>



| <span data-ttu-id="1e0fd-113">需求</span><span class="sxs-lookup"><span data-stu-id="1e0fd-113">Requirement</span></span> | <span data-ttu-id="1e0fd-114">值</span><span class="sxs-lookup"><span data-stu-id="1e0fd-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0fd-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1e0fd-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1e0fd-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1e0fd-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e0fd-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e0fd-117">Library</span></span><br/> | <dl> <span data-ttu-id="1e0fd-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1e0fd-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0fd-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e0fd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0fd-120">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="1e0fd-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




