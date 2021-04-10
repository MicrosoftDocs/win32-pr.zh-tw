---
description: 公開代表檔區域之區域的方法和屬性。
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: 'IAnalysisRegion 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690607"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="11f21-103">IAnalysisRegion 介面</span><span class="sxs-lookup"><span data-stu-id="11f21-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="11f21-104">公開代表檔區域之區域的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="11f21-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="11f21-105">成員</span><span class="sxs-lookup"><span data-stu-id="11f21-105">Members</span></span>

<span data-ttu-id="11f21-106">**IAnalysisRegion** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="11f21-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="11f21-107">**IAnalysisRegion** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11f21-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="11f21-108">方法</span><span class="sxs-lookup"><span data-stu-id="11f21-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11f21-109">方法</span><span class="sxs-lookup"><span data-stu-id="11f21-109">Methods</span></span>

<span data-ttu-id="11f21-110">**IAnalysisRegion** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="11f21-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="11f21-111">方法</span><span class="sxs-lookup"><span data-stu-id="11f21-111">Method</span></span>                                                           | <span data-ttu-id="11f21-112">描述</span><span class="sxs-lookup"><span data-stu-id="11f21-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11f21-113">**克隆**</span><span class="sxs-lookup"><span data-stu-id="11f21-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="11f21-114">建立 **IAnalysisRegion** 的複本。</span><span class="sxs-lookup"><span data-stu-id="11f21-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="11f21-115">**ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="11f21-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="11f21-116">將 **IAnalysisRegion** 的區域限制為其區域中未與指定的矩形相交的部分。</span><span class="sxs-lookup"><span data-stu-id="11f21-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="11f21-117">**ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="11f21-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="11f21-118">將 **IAnalysisRegion** 的區域限制為其區域中未與指定 **IAnalysisRegion** 相交的部分。</span><span class="sxs-lookup"><span data-stu-id="11f21-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="11f21-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="11f21-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="11f21-120">抓取 **IAnalysisRegion** 的周框。</span><span class="sxs-lookup"><span data-stu-id="11f21-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="11f21-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="11f21-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="11f21-122">捕獲定義 **IAnalysisRegion** 區域的矩形陣列。</span><span class="sxs-lookup"><span data-stu-id="11f21-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="11f21-123">**IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="11f21-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="11f21-124">將這個 **IAnalysisRegion** 的區域限制為其與指定矩形的交集所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="11f21-125">**IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="11f21-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="11f21-126">將 **IAnalysisRegion** 的區域限制為其與指定 **IAnalysisRegion** 的交集所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="11f21-127">**IntersectsWith**</span><span class="sxs-lookup"><span data-stu-id="11f21-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="11f21-128">判斷 **IAnalysisRegion** 的區域是否與指定的矩形相交。</span><span class="sxs-lookup"><span data-stu-id="11f21-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="11f21-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="11f21-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="11f21-130">抓取值，指出 **IAnalysisRegion** 是否代表空白區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="11f21-131">**IsInfinite**</span><span class="sxs-lookup"><span data-stu-id="11f21-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="11f21-132">抓取值，指出 **IAnalysisRegion** 是否代表無限區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="11f21-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="11f21-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="11f21-134">減少 **IAnalysisRegion** 以代表空白區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="11f21-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="11f21-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="11f21-136">展開 **IAnalysisRegion** 以代表無限區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="11f21-137">**UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="11f21-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="11f21-138">將這個 **IAnalysisRegion** 的區域展開至其聯集所建立的區域（具有指定的矩形）。</span><span class="sxs-lookup"><span data-stu-id="11f21-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="11f21-139">**UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="11f21-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="11f21-140">將這個 **IAnalysisRegion** 的區域展開至具有指定 **IAnalysisRegion** 的聯集所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="11f21-141">備註</span><span class="sxs-lookup"><span data-stu-id="11f21-141">Remarks</span></span>

<span data-ttu-id="11f21-142">此介面代表從矩形區域所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="11f21-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="11f21-143">[**IInkAnalyzer**](iinkanalyzer.md)會在其接收筆觸資料的座標空間內，傳回或解讀區域的座標。</span><span class="sxs-lookup"><span data-stu-id="11f21-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="11f21-144">若要取得目前的 **IAnalysisRegion** 範圍，請使用 [**IAnalysisRegion：： GetBounds 方法**](ianalysisregion-getbounds.md) 或 [**IAnalysisRegion：： GetRegionScans 方法**](ianalysisregion-getregionscans.md)。</span><span class="sxs-lookup"><span data-stu-id="11f21-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="11f21-145">若要修改現有 **IAnalysisRegion** 的區域，請使用下列方法。</span><span class="sxs-lookup"><span data-stu-id="11f21-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="11f21-146">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="11f21-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="11f21-147">**IAnalysisRegion：： ExcludeRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="11f21-148">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="11f21-149">**IAnalysisRegion：： IntersectRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="11f21-150">**IAnalysisRegion：： MakeEmpty 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="11f21-151">**IAnalysisRegion：： MakeInfinite 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="11f21-152">**IAnalysisRegion：： UnionRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="11f21-153">**IAnalysisRegion：： UnionRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="11f21-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="11f21-154">這個介面相當於 .NET Framework 中的 AnalysisCore. AnalysisRegionBase 類別。</span><span class="sxs-lookup"><span data-stu-id="11f21-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f21-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="11f21-155">Requirements</span></span>



| <span data-ttu-id="11f21-156">需求</span><span class="sxs-lookup"><span data-stu-id="11f21-156">Requirement</span></span> | <span data-ttu-id="11f21-157">值</span><span class="sxs-lookup"><span data-stu-id="11f21-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f21-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11f21-158">Minimum supported client</span></span><br/> | <span data-ttu-id="11f21-159">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11f21-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11f21-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11f21-160">Minimum supported server</span></span><br/> | <span data-ttu-id="11f21-161">都不支援</span><span class="sxs-lookup"><span data-stu-id="11f21-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="11f21-162">標頭</span><span class="sxs-lookup"><span data-stu-id="11f21-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f21-163"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="11f21-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11f21-164">DLL</span><span class="sxs-lookup"><span data-stu-id="11f21-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f21-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f21-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="11f21-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11f21-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f21-167">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="11f21-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="11f21-168">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="11f21-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

