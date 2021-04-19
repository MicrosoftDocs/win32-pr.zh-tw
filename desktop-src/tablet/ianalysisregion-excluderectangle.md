---
description: 將 IAnalysisRegion 的區域限制為其區域中未與指定的矩形相交的部分。
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion：： ExcludeRectangle 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972430"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="98ba5-103">IAnalysisRegion：： ExcludeRectangle 方法</span><span class="sxs-lookup"><span data-stu-id="98ba5-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="98ba5-104">將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其區域中未與指定的矩形相交的部分。</span><span class="sxs-lookup"><span data-stu-id="98ba5-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ba5-105">語法</span><span class="sxs-lookup"><span data-stu-id="98ba5-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="98ba5-106">參數</span><span class="sxs-lookup"><span data-stu-id="98ba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ba5-107">*pExcludingRectangle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98ba5-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98ba5-108">要從此 [**IAnalysisRegion**](ianalysisregion.md)中排除的矩形。</span><span class="sxs-lookup"><span data-stu-id="98ba5-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ba5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="98ba5-109">Return value</span></span>

<span data-ttu-id="98ba5-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="98ba5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98ba5-111">備註</span><span class="sxs-lookup"><span data-stu-id="98ba5-111">Remarks</span></span>

<span data-ttu-id="98ba5-112">矩形座標以 HIMETRIC 單位表示。</span><span class="sxs-lookup"><span data-stu-id="98ba5-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="98ba5-113">如果這兩個區域不相交， [**IAnalysisRegion**](ianalysisregion.md) 就不會變更。</span><span class="sxs-lookup"><span data-stu-id="98ba5-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ba5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="98ba5-114">Requirements</span></span>



| <span data-ttu-id="98ba5-115">需求</span><span class="sxs-lookup"><span data-stu-id="98ba5-115">Requirement</span></span> | <span data-ttu-id="98ba5-116">值</span><span class="sxs-lookup"><span data-stu-id="98ba5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ba5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98ba5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98ba5-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98ba5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98ba5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98ba5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98ba5-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="98ba5-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="98ba5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="98ba5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ba5-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="98ba5-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98ba5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="98ba5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ba5-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ba5-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="98ba5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98ba5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ba5-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="98ba5-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="98ba5-127">**IAnalysisRegion：： ExcludeRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="98ba5-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="98ba5-128">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="98ba5-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="98ba5-129">**IAnalysisRegion：： IntersectRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="98ba5-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="98ba5-130">**IAnalysisRegion：： UnionRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="98ba5-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="98ba5-131">**IAnalysisRegion：： UnionRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="98ba5-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="98ba5-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="98ba5-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




