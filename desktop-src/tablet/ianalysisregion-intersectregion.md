---
description: 將 IAnalysisRegion 的區域限制為其與指定 IAnalysisRegion 的交集所建立的區域。
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion：： IntersectRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972054"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="6a223-103">IAnalysisRegion：： IntersectRegion 方法</span><span class="sxs-lookup"><span data-stu-id="6a223-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="6a223-104">將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其與指定 **IAnalysisRegion** 的交集所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="6a223-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a223-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a223-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="6a223-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a223-107">*pRegionToIntersect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a223-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a223-108">要與之交集的 [**IAnalysisRegion**](ianalysisregion.md) 。</span><span class="sxs-lookup"><span data-stu-id="6a223-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a223-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a223-109">Return value</span></span>

<span data-ttu-id="6a223-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6a223-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a223-111">備註</span><span class="sxs-lookup"><span data-stu-id="6a223-111">Remarks</span></span>

<span data-ttu-id="6a223-112">如果兩個區域不相交，則新區域是空的。</span><span class="sxs-lookup"><span data-stu-id="6a223-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a223-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a223-113">Requirements</span></span>



| <span data-ttu-id="6a223-114">需求</span><span class="sxs-lookup"><span data-stu-id="6a223-114">Requirement</span></span> | <span data-ttu-id="6a223-115">值</span><span class="sxs-lookup"><span data-stu-id="6a223-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a223-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a223-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a223-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a223-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a223-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a223-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a223-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6a223-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6a223-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6a223-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a223-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6a223-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6a223-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6a223-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a223-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a223-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6a223-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a223-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a223-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="6a223-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="6a223-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="6a223-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="6a223-127">**IAnalysisRegion：： ExcludeRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="6a223-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="6a223-128">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="6a223-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="6a223-129">**IAnalysisRegion：： UnionRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="6a223-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="6a223-130">**IAnalysisRegion：： UnionRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="6a223-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="6a223-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="6a223-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




