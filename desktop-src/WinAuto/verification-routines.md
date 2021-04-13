---
title: 驗證常式
description: 本節說明 UI 協助工具檢查程式可以執行的驗證常式，以測試應用程式的協助工具實作為測試。
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300987"
---
# <a name="verification-routines"></a><span data-ttu-id="5b3b4-103">驗證常式</span><span class="sxs-lookup"><span data-stu-id="5b3b4-103">Verification Routines</span></span>

<span data-ttu-id="5b3b4-104">本節說明 UI 協助工具檢查程式可以執行的驗證常式，以測試應用程式的協助工具實作為測試。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b3b4-105">類別</span><span class="sxs-lookup"><span data-stu-id="5b3b4-105">Category</span></span></th>
<th><span data-ttu-id="5b3b4-106">常式傳回的值</span><span class="sxs-lookup"><span data-stu-id="5b3b4-106">Routine</span></span></th>
<th><span data-ttu-id="5b3b4-107">Description</span><span class="sxs-lookup"><span data-stu-id="5b3b4-107">Description</span></span></th>
</tr><span data-ttu-id="5b3b4-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>一致性</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-109"><strong>ScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="5b3b4-110">編譯驗證目標中所有可見的元素，並以標準螢幕讀取器向使用者宣告的順序，將這些專案顯示在 ListView 控制項中。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-111"><strong>UiaScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="5b3b4-112">與 <strong>ScreenReader</strong>相同，但適用于 UIA 的執行。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="5b3b4-113"><strong>導覽</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-114"><strong>CheckTreeDepth</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="5b3b4-115">傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認目標的 UI 不太複雜，或無法使用標準鍵盤流覽來存取。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-116"><strong>CheckTabbingUia</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="5b3b4-117">傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認可以使用標準鍵盤流覽，以合理的邏輯方式連線到 UI 中的所有可設定的元素。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="5b3b4-118"><strong>Properties</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-119"><strong>CheckRole</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="5b3b4-120">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 角色，且該控制項具有該角色所需的值。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="5b3b4-122">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 狀態。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-123"><strong>CheckName</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="5b3b4-124">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 MSAA 名稱。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-125"><strong>CheckAccessKeys</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="5b3b4-126">確認指派給驗證目標中專案的存取金鑰在驗證目標內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-127"><strong>CheckBoundingRect</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="5b3b4-128">確認 UI 中的每個可設定焦點專案都有周框，可用來做為點擊測試的目標。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="5b3b4-129"><strong>Tree</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-130"><strong>CheckParentChild</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="5b3b4-131">專案樹狀結構中的父系和子系關聯性一致且可預測。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-132"><strong>CheckOrphanChildren</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="5b3b4-133">確認 UI 中的每個可設定焦點元素都會報告有效的 MSAA 父系。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="5b3b4-134"><strong>UIA 屬性</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-135"><strong>CheckNameUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-136">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 名稱。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-137"><strong>CheckTreeDepthUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-138">傳送索引標籤 (或 Shift + Tab) 個字元做為驗證目標的輸入，以確認 UIA 目標 UI 中的元素時，不太複雜或無法使用標準鍵盤流覽。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-139"><strong>CheckStateUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-140">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 狀態。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-141"><strong>CheckAccessKeysUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-142">確認同輩元素沒有相同的存取和/或快速鍵。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-143"><strong>CheckBoundingRectUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-144">確認 UI 中的每個可設定焦點 UIA 元素都有周框，可用來做為點擊測試的目標。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-145"><strong>CheckControlTypeUIA</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="5b3b4-146">確認 UI 中的每個可設定焦點元素都會報告有效的邏輯 UIA 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="5b3b4-147"><strong>UIA Tree</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-148"><strong>CheckNavigateUia</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="5b3b4-149">確認 UIA TreeWalker 可以流覽元素的子系。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-150"><strong>CheckOrphanChildrenUia</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="5b3b4-151">確認 UI 中的每個可設定焦點元素都會報告有效的 UIA 父系。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-152"><strong>CheckSiblingsUia</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="5b3b4-153">確認同輩元素沒有相同的名稱： ControlType 組，也沒有相同的 AutomationId。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-154">$ {ROWSPAN9} $<strong>ARIA Web 驗證</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-155"><strong>CheckARIARole</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="5b3b4-156">確認所有元素都具有有效的 ARIA 角色。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="5b3b4-157">相關聯的 HTML 標籤和 ARIA 角色是有無效角色標示為錯誤的資訊元素。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-158"><strong>CheckLabel</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="5b3b4-159">確認具有輸入、按鈕、影像按鈕或地標角色的每個元素都有一個標籤。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-160"><strong>CheckRangeControls</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="5b3b4-161">確認具有滑杆或進度列角色的範圍控制項已定義適當的 ARIA 屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-162"><strong>CheckContainerRole</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="5b3b4-163">確認元素（或至少一個子系）已定義 onkeydown/onkeypress。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-164"><strong>CheckLayoutTable</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="5b3b4-165">確認資料表配置具有內含的摘要/th/aria describedby。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-166"><strong>CheckGridStructure</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="5b3b4-167">確認具有方格角色的非資料表專案具有方格>資料列的結構，>gridcell 有相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-168"><strong>CheckDataTable</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="5b3b4-169">確認資料表的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-170"><strong>CheckActiveDescendants</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="5b3b4-171">確認已定義作用中子系的元素屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-172"><strong>CheckElementsWithClickHandler</strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="5b3b4-173">使用按一下處理常式來確認專案的索引標籤索引。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="5b3b4-174"><strong>Web 驗證</strong>$ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="5b3b4-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b3b4-175"><strong>CheckHtml (Web) </strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="5b3b4-176">確認各種 HTML 特性，例如標頭、名稱、框架和標題。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b3b4-177"><strong>CheckName (Web) </strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="5b3b4-178">確認名稱特性，例如長度、無效字元和角色包含。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b3b4-179"><strong>CheckRole (Web) </strong></span><span class="sxs-lookup"><span data-stu-id="5b3b4-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="5b3b4-180">確認不正確角色、應該具有值的角色，以及/或未執行的角色。</span><span class="sxs-lookup"><span data-stu-id="5b3b4-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5b3b4-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b3b4-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b3b4-182">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="5b3b4-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




