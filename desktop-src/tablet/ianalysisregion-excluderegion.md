---
description: 將 IAnalysisRegion 的區域限制為其區域中未與指定 IAnalysisRegion 相交的部分。
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion：： ExcludeRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511700"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="918b5-103">IAnalysisRegion：： ExcludeRegion 方法</span><span class="sxs-lookup"><span data-stu-id="918b5-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="918b5-104">將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其區域中未與指定 **IAnalysisRegion** 相交的部分。</span><span class="sxs-lookup"><span data-stu-id="918b5-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="918b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="918b5-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="918b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="918b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="918b5-107">*pRegionToExclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="918b5-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="918b5-108">要從此 **IAnalysisRegion** 排除的 [**IAnalysisRegion**](ianalysisregion.md) 。</span><span class="sxs-lookup"><span data-stu-id="918b5-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="918b5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="918b5-109">Return value</span></span>

<span data-ttu-id="918b5-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="918b5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="918b5-111">備註</span><span class="sxs-lookup"><span data-stu-id="918b5-111">Remarks</span></span>

<span data-ttu-id="918b5-112">如果這兩個區域不相交，此 [**IAnalysisRegion**](ianalysisregion.md) 就不會變更。</span><span class="sxs-lookup"><span data-stu-id="918b5-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="918b5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="918b5-113">Requirements</span></span>



| <span data-ttu-id="918b5-114">需求</span><span class="sxs-lookup"><span data-stu-id="918b5-114">Requirement</span></span> | <span data-ttu-id="918b5-115">值</span><span class="sxs-lookup"><span data-stu-id="918b5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="918b5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="918b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="918b5-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="918b5-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="918b5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="918b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="918b5-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="918b5-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="918b5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="918b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="918b5-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="918b5-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="918b5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="918b5-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="918b5-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="918b5-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="918b5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="918b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="918b5-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="918b5-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="918b5-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="918b5-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="918b5-127">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="918b5-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="918b5-128">**IAnalysisRegion：： IntersectRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="918b5-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="918b5-129">**IAnalysisRegion：： UnionRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="918b5-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="918b5-130">**IAnalysisRegion：： UnionRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="918b5-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="918b5-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="918b5-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




