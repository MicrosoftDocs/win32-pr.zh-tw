---
description: 指出品質是否已變更的旗標。
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'CTransformFilter：： m_bQualityChanged 成員 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979513"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="51420-103">CTransformFilter：： m \_ bQualityChanged 成員</span><span class="sxs-lookup"><span data-stu-id="51420-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="51420-104">指出品質是否已變更的旗標。</span><span class="sxs-lookup"><span data-stu-id="51420-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="51420-105">當篩選器第一次卸載範例時，它會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員，並將此旗標設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="51420-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="51420-106">除非篩選器停止並重新啟動，否則它不會再次傳送此事件，即使在此情況下，仍會繼續卸載範例。</span><span class="sxs-lookup"><span data-stu-id="51420-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="51420-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="51420-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="51420-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="51420-108">Requirements</span></span>



| <span data-ttu-id="51420-109">需求</span><span class="sxs-lookup"><span data-stu-id="51420-109">Requirement</span></span> | <span data-ttu-id="51420-110">值</span><span class="sxs-lookup"><span data-stu-id="51420-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51420-111">標頭</span><span class="sxs-lookup"><span data-stu-id="51420-111">Header</span></span><br/>  | <dl> <span data-ttu-id="51420-112"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="51420-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51420-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="51420-113">Library</span></span><br/> | <dl> <span data-ttu-id="51420-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="51420-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51420-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51420-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51420-116">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="51420-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




