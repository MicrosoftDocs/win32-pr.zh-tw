---
description: 表示樣本抵達轉譯器的延遲時間（以參考時間單位為單位）。 語法。
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'CVideoTransformFilter：： m_itrLate 成員 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992997"
---
# <a name="cvideotransformfilterm_itrlate-member"></a><span data-ttu-id="4884e-104">CVideoTransformFilter：： m \_ itrLate 成員</span><span class="sxs-lookup"><span data-stu-id="4884e-104">CVideoTransformFilter::m\_itrLate member</span></span>

<span data-ttu-id="4884e-105">表示樣本抵達轉譯器的延遲時間（以參考時間單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="4884e-105">Indicates how late the samples are arriving at the renderer, in reference time units.</span></span> <span data-ttu-id="4884e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4884e-106">Syntax</span></span>

## <a name="syntax"></a><span data-ttu-id="4884e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4884e-107">Syntax</span></span>


```C++
int m_itrLate;
```



## <a name="remarks"></a><span data-ttu-id="4884e-108">備註</span><span class="sxs-lookup"><span data-stu-id="4884e-108">Remarks</span></span>

<span data-ttu-id="4884e-109">當篩選從下游收到品質訊息時，它會將延遲值儲存在此變數中。</span><span class="sxs-lookup"><span data-stu-id="4884e-109">When the filter receives a quality message from downstream, it stores the lateness value in this variable.</span></span> <span data-ttu-id="4884e-110">當篩選器卸載框架時，它會藉由減去每個畫面格的持續時間來更新此值。</span><span class="sxs-lookup"><span data-stu-id="4884e-110">As the filter drops frames, it updates this value by subtracting the duration of each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4884e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4884e-111">Requirements</span></span>



| <span data-ttu-id="4884e-112">需求</span><span class="sxs-lookup"><span data-stu-id="4884e-112">Requirement</span></span> | <span data-ttu-id="4884e-113">值</span><span class="sxs-lookup"><span data-stu-id="4884e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4884e-114">標頭</span><span class="sxs-lookup"><span data-stu-id="4884e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4884e-115"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4884e-115"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4884e-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="4884e-116">Library</span></span><br/> | <dl> <span data-ttu-id="4884e-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4884e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4884e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4884e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4884e-119">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4884e-119">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




