---
description: 將這個 IAnalysisRegion 的區域展開至其聯集所建立的區域（具有指定的矩形）。
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion：： UnionRectangle 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971417"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="0341b-103">IAnalysisRegion：： UnionRectangle 方法</span><span class="sxs-lookup"><span data-stu-id="0341b-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="0341b-104">將這個 [**IAnalysisRegion**](ianalysisregion.md) 的區域展開至其聯集所建立的區域（具有指定的矩形）。</span><span class="sxs-lookup"><span data-stu-id="0341b-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0341b-105">語法</span><span class="sxs-lookup"><span data-stu-id="0341b-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="0341b-106">參數</span><span class="sxs-lookup"><span data-stu-id="0341b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0341b-107">*pRectangle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0341b-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0341b-108">要結合的矩形指標，以筆墨的空格座標表示。</span><span class="sxs-lookup"><span data-stu-id="0341b-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0341b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0341b-109">Return value</span></span>

<span data-ttu-id="0341b-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="0341b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0341b-111">備註</span><span class="sxs-lookup"><span data-stu-id="0341b-111">Remarks</span></span>

<span data-ttu-id="0341b-112">矩形座標以 HIMETRIC 單位表示。</span><span class="sxs-lookup"><span data-stu-id="0341b-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="0341b-113">如果任一區域都是無限的，則新區域也是無限的。</span><span class="sxs-lookup"><span data-stu-id="0341b-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="0341b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0341b-114">Requirements</span></span>



| <span data-ttu-id="0341b-115">需求</span><span class="sxs-lookup"><span data-stu-id="0341b-115">Requirement</span></span> | <span data-ttu-id="0341b-116">值</span><span class="sxs-lookup"><span data-stu-id="0341b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0341b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0341b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0341b-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0341b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0341b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0341b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0341b-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="0341b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0341b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0341b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0341b-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="0341b-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0341b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0341b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0341b-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0341b-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0341b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0341b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0341b-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="0341b-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="0341b-127">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="0341b-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="0341b-128">**IAnalysisRegion：： ExcludeRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="0341b-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="0341b-129">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="0341b-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="0341b-130">**IAnalysisRegion：： IntersectRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="0341b-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="0341b-131">**IAnalysisRegion：： UnionRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="0341b-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="0341b-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="0341b-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




