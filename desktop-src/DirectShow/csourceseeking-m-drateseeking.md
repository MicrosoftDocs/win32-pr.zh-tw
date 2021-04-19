---
description: 播放速率。 依預設，此值會設定為1.0。
ms.assetid: 835ddbe8-2017-4a4a-8f10-b3f33a8215a7
title: 'CSourceSeeking：： m_dRateSeeking 成員 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dRateSeeking
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1055a420316868db6374798c0295339dd74ac172
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987182"
---
# <a name="csourceseekingm_drateseeking-member"></a><span data-ttu-id="55f8c-104">CSourceSeeking：： m \_ dRateSeeking 成員</span><span class="sxs-lookup"><span data-stu-id="55f8c-104">CSourceSeeking::m\_dRateSeeking member</span></span>

<span data-ttu-id="55f8c-105">播放速率。</span><span class="sxs-lookup"><span data-stu-id="55f8c-105">Playback rate.</span></span> <span data-ttu-id="55f8c-106">依預設，此值會設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="55f8c-106">By default, the value is set to 1.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f8c-107">語法</span><span class="sxs-lookup"><span data-stu-id="55f8c-107">Syntax</span></span>


```C++
double m_dRateSeeking;
```



## <a name="remarks"></a><span data-ttu-id="55f8c-108">備註</span><span class="sxs-lookup"><span data-stu-id="55f8c-108">Remarks</span></span>

<span data-ttu-id="55f8c-109">存取此變數之前，請先保留 **m \_ pLock** 重要區段。</span><span class="sxs-lookup"><span data-stu-id="55f8c-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f8c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="55f8c-110">Requirements</span></span>



| <span data-ttu-id="55f8c-111">需求</span><span class="sxs-lookup"><span data-stu-id="55f8c-111">Requirement</span></span> | <span data-ttu-id="55f8c-112">值</span><span class="sxs-lookup"><span data-stu-id="55f8c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f8c-113">標頭</span><span class="sxs-lookup"><span data-stu-id="55f8c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="55f8c-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55f8c-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55f8c-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="55f8c-115">Library</span></span><br/> | <dl> <span data-ttu-id="55f8c-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="55f8c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f8c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55f8c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f8c-118">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="55f8c-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




