---
title: 驗證記錄訊息
description: 本節說明 UI 協助工具檢查程式 (AccChecker) 的驗證記錄訊息。
ms.assetid: 27BA13D8-162B-4604-A048-2C8D49060FA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4d0d9afd30307c77ebebb1039ba2f2e0817884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965579"
---
# <a name="verification-log-messages"></a><span data-ttu-id="8618c-103">驗證記錄訊息</span><span class="sxs-lookup"><span data-stu-id="8618c-103">Verification Log Messages</span></span>

<span data-ttu-id="8618c-104">本節說明 UI 協助工具檢查程式 (AccChecker) 的驗證記錄訊息。</span><span class="sxs-lookup"><span data-stu-id="8618c-104">This section describes the verification log messages for UI Accessibility Checker (AccChecker).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8618c-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="8618c-105">In this section</span></span>

-   [<span data-ttu-id="8618c-106">AccessibleObjectFromPointReturnedNullIAccessible</span><span class="sxs-lookup"><span data-stu-id="8618c-106">AccessibleObjectFromPointReturnedNullIAccessible</span></span>](accessibleobjectfrompointreturnednulliaccessible.md)
-   [<span data-ttu-id="8618c-107">AccessibleObjectFromPointReturnedNot \_ S \_ 沒問題</span><span class="sxs-lookup"><span data-stu-id="8618c-107">AccessibleObjectFromPointReturnedNot\_S\_OK</span></span>](accessibleobjectfrompointreturnednot-s-ok.md)
-   [<span data-ttu-id="8618c-108">AccessibleObjectFromPointReturnedNullChildId</span><span class="sxs-lookup"><span data-stu-id="8618c-108">AccessibleObjectFromPointReturnedNullChildId</span></span>](accessibleobjectfrompointreturnednullchildid.md)
-   [<span data-ttu-id="8618c-109">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="8618c-109">AccNameContainsInvalidString</span></span>](accnamecontainsinvalidstring.md)
-   [<span data-ttu-id="8618c-110">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="8618c-110">AccNameLengthTooLong</span></span>](accnamelengthtoolong.md)
-   [<span data-ttu-id="8618c-111">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="8618c-111">AccNameShouldNotContainRole</span></span>](accnameshouldnotcontainrole.md)
-   [<span data-ttu-id="8618c-112">AccNavigate \_ ReturnedElementWithIncorrectParent</span><span class="sxs-lookup"><span data-stu-id="8618c-112">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>](accnavigate-returnedelementwithincorrectparent.md)
-   [<span data-ttu-id="8618c-113">AppearsToNotSupportTabbing</span><span class="sxs-lookup"><span data-stu-id="8618c-113">AppearsToNotSupportTabbing</span></span>](appearstonotsupporttabbing.md)
-   [<span data-ttu-id="8618c-114">ARIA 容器 Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-114">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
-   [<span data-ttu-id="8618c-115">ARIA 容器角色鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-115">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
-   [<span data-ttu-id="8618c-116">沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-116">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
-   [<span data-ttu-id="8618c-117">沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-117">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
-   [<span data-ttu-id="8618c-118">ARIA 容器角色錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-118">ARIA Container Role Error</span></span>](aria-container-role.md)
-   [<span data-ttu-id="8618c-119">ARIA 資料表錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-119">ARIA Data Table Error</span></span>](aria-table-name-and-header.md)
-   [<span data-ttu-id="8618c-120">ARIA 資料表格警告</span><span class="sxs-lookup"><span data-stu-id="8618c-120">ARIA Data Table Warning</span></span>](aria-data-table-description.md)
-   [<span data-ttu-id="8618c-121">ARIA 方格結構錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-121">ARIA Grid Structure Error</span></span>](aria-grid-structure.md)
-   [<span data-ttu-id="8618c-122">ARIA 標籤錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-122">ARIA Label Error</span></span>](aria-label.md)
-   [<span data-ttu-id="8618c-123">ARIA 展示表錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-123">ARIA Presentation Table Error</span></span>](aria-layout-table.md)
-   [<span data-ttu-id="8618c-124">缺少 ARIA 範圍控制項屬性</span><span class="sxs-lookup"><span data-stu-id="8618c-124">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
-   [<span data-ttu-id="8618c-125">ARIA 範圍控制項屬性不相容</span><span class="sxs-lookup"><span data-stu-id="8618c-125">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
-   [<span data-ttu-id="8618c-126">ARIA 角色錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-126">ARIA Role Error</span></span>](aria-role-invalid.md)
-   [<span data-ttu-id="8618c-127">具有事件處理常式之元素的 ARIA 角色錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-127">ARIA Role Error for elements with event handlers</span></span>](aria-role-missing.md)
-   [<span data-ttu-id="8618c-128">ARIA Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="8618c-128">ARIA Tabindex Error</span></span>](aria-click-tabindex.md)
-   [<span data-ttu-id="8618c-129">BoundingRectIsIncorrect</span><span class="sxs-lookup"><span data-stu-id="8618c-129">BoundingRectIsIncorrect</span></span>](boundingrectisincorrect.md)
-   [<span data-ttu-id="8618c-130">BoundingRectNotHitTestable</span><span class="sxs-lookup"><span data-stu-id="8618c-130">BoundingRectNotHitTestable</span></span>](boundingrectnothittestable.md)
-   [<span data-ttu-id="8618c-131">CheckTreeDepth</span><span class="sxs-lookup"><span data-stu-id="8618c-131">CheckTreeDepth</span></span>](checktreedepth.md)
-   [<span data-ttu-id="8618c-132">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="8618c-132">ControlShouldHaveValue</span></span>](controlshouldhavevalue.md)
-   [<span data-ttu-id="8618c-133">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="8618c-133">ControlTypeNoExpectedPatternsSupported</span></span>](controltypenoexpectedpatternssupported.md)
-   [<span data-ttu-id="8618c-134">ControlTypeRequiredPatternNotSupported</span><span class="sxs-lookup"><span data-stu-id="8618c-134">ControlTypeRequiredPatternNotSupported</span></span>](controltyperequiredpatternnotsupported.md)
-   [<span data-ttu-id="8618c-135">CustomControlTypeWithoutLocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="8618c-135">CustomControlTypeWithoutLocalizedControlType</span></span>](customcontroltypewithoutlocalizedcontroltype.md)
-   [<span data-ttu-id="8618c-136">DragPattern/DragDropPattern 元素需要名稱</span><span class="sxs-lookup"><span data-stu-id="8618c-136">DragPattern/DragDropPattern elements requires Name</span></span>](dragpattern-dragdroppattern-elements-requires-name-.md)
-   [<span data-ttu-id="8618c-137">DragPattern/DragDropPattern 元素需要有效的 DropEffect</span><span class="sxs-lookup"><span data-stu-id="8618c-137">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>](dragpattern-dragdroppattern-elements-requires-valid-dropeffect.md)
-   [<span data-ttu-id="8618c-138">DuplicateAccessKey</span><span class="sxs-lookup"><span data-stu-id="8618c-138">DuplicateAccessKey</span></span>](duplicateaccesskey.md)
-   [<span data-ttu-id="8618c-139">DuplicateSiblingIDs</span><span class="sxs-lookup"><span data-stu-id="8618c-139">DuplicateSiblingIDs</span></span>](duplicatesiblingids.md)
-   [<span data-ttu-id="8618c-140">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="8618c-140">DuplicateSiblingNames</span></span>](duplicatesiblingnames.md)
-   [<span data-ttu-id="8618c-141">ElementFromPointReturnedNull</span><span class="sxs-lookup"><span data-stu-id="8618c-141">ElementFromPointReturnedNull</span></span>](elementfrompointreturnednull.md)
-   [<span data-ttu-id="8618c-142">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="8618c-142">ElementHasNoName</span></span>](elementhasnoname.md)
-   [<span data-ttu-id="8618c-143">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="8618c-143">ElementIsChildOfParentMulipleTimes</span></span>](elementischildofparentmulipletimes.md)
-   [<span data-ttu-id="8618c-144">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="8618c-144">ElementIsNotChildOfElementsParent</span></span>](elementisnotchildofelementsparent.md)
-   [<span data-ttu-id="8618c-145">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="8618c-145">ElementIsOrphaned</span></span>](elementisorphaned.md)
-   [<span data-ttu-id="8618c-146">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="8618c-146">ElementsChildHasDifferentParent</span></span>](elementschildhasdifferentparent.md)
-   [<span data-ttu-id="8618c-147">ElementShouldBeOffScreen</span><span class="sxs-lookup"><span data-stu-id="8618c-147">ElementShouldBeOffScreen</span></span>](elementshouldbeoffscreen.md)
-   [<span data-ttu-id="8618c-148">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="8618c-148">FirstChildLastChildMismatch</span></span>](firstchildlastchildmismatch.md)
-   [<span data-ttu-id="8618c-149">GatheringElement</span><span class="sxs-lookup"><span data-stu-id="8618c-149">GatheringElement</span></span>](gatheringelement.md)
-   [<span data-ttu-id="8618c-150">InconsistentState, InconsistentProperties</span><span class="sxs-lookup"><span data-stu-id="8618c-150">InconsistentState, InconsistentProperties</span></span>](inconsistentstate--inconsistentproperties.md)
-   [<span data-ttu-id="8618c-151">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="8618c-151">IncorrectRoundTrip</span></span>](incorrectroundtrip.md)
-   [<span data-ttu-id="8618c-152">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="8618c-152">InvalidRole</span></span>](invalidrole.md)
-   [<span data-ttu-id="8618c-153">MemberNotImplememented</span><span class="sxs-lookup"><span data-stu-id="8618c-153">MemberNotImplememented</span></span>](membernotimplememented.md)
-   [<span data-ttu-id="8618c-154">MethodExceptionOccured</span><span class="sxs-lookup"><span data-stu-id="8618c-154">MethodExceptionOccured</span></span>](methodexceptionoccured.md)
-   [<span data-ttu-id="8618c-155">MethodReturnedUnexpectedHResult</span><span class="sxs-lookup"><span data-stu-id="8618c-155">MethodReturnedUnexpectedHResult</span></span>](methodreturnedunexpectedhresult.md)
-   [<span data-ttu-id="8618c-156">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="8618c-156">MissingItemInTabOrder</span></span>](missingitemintaborder.md)
-   [<span data-ttu-id="8618c-157">NullParent</span><span class="sxs-lookup"><span data-stu-id="8618c-157">NullParent</span></span>](nullparent.md)
-   [<span data-ttu-id="8618c-158">StartingTab</span><span class="sxs-lookup"><span data-stu-id="8618c-158">StartingTab</span></span>](startingtab.md)
-   [<span data-ttu-id="8618c-159">TabbedBackwardTo</span><span class="sxs-lookup"><span data-stu-id="8618c-159">TabbedBackwardTo</span></span>](tabbedbackwardto.md)
-   [<span data-ttu-id="8618c-160">TabbedForwardTo</span><span class="sxs-lookup"><span data-stu-id="8618c-160">TabbedForwardTo</span></span>](tabbedforwardto.md)
-   [<span data-ttu-id="8618c-161">TabbedToInfo</span><span class="sxs-lookup"><span data-stu-id="8618c-161">TabbedToInfo</span></span>](tabbedtoinfo.md)
-   [<span data-ttu-id="8618c-162">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="8618c-162">TabbedToUnknownElement</span></span>](tabbedtounknownelement.md)
-   [<span data-ttu-id="8618c-163">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="8618c-163">TabbingNotCyclic</span></span>](tabbingnotcyclic.md)
-   [<span data-ttu-id="8618c-164">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="8618c-164">TabbingNotSymmetric</span></span>](tabbingnotsymmetric.md)
-   [<span data-ttu-id="8618c-165">TabOrderInQuestion</span><span class="sxs-lookup"><span data-stu-id="8618c-165">TabOrderInQuestion</span></span>](taborderinquestion.md)
-   [<span data-ttu-id="8618c-166">TooManyChildren</span><span class="sxs-lookup"><span data-stu-id="8618c-166">TooManyChildren</span></span>](toomanychildren.md)
-   [<span data-ttu-id="8618c-167">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="8618c-167">TreeMightBeCyclic</span></span>](treemightbecyclic.md)
-   [<span data-ttu-id="8618c-168">TreeTooDeep</span><span class="sxs-lookup"><span data-stu-id="8618c-168">TreeTooDeep</span></span>](treetoodeep.md)
-   [<span data-ttu-id="8618c-169">UiaDuplicateAccessKey</span><span class="sxs-lookup"><span data-stu-id="8618c-169">UiaDuplicateAccessKey</span></span>](uiaduplicateaccesskey.md)
-   [<span data-ttu-id="8618c-170">UiaElementDoesNotParentToRoot</span><span class="sxs-lookup"><span data-stu-id="8618c-170">UiaElementDoesNotParentToRoot</span></span>](uiaelementdoesnotparenttoroot.md)
-   [<span data-ttu-id="8618c-171">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="8618c-171">UiaElementIsOrphaned</span></span>](uiaelementisorphaned.md)
-   [<span data-ttu-id="8618c-172">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="8618c-172">UiaNameLengthTooLong</span></span>](uianamelengthtoolong.md)
-   [<span data-ttu-id="8618c-173">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="8618c-173">UiaNameShouldNotContainControlType</span></span>](uianameshouldnotcontaincontroltype.md)
-   [<span data-ttu-id="8618c-174">UnexpectedTestError</span><span class="sxs-lookup"><span data-stu-id="8618c-174">UnexpectedTestError</span></span>](unexpectedtesterror.md)
-   [<span data-ttu-id="8618c-175">VariantNotInt (CheckRole) </span><span class="sxs-lookup"><span data-stu-id="8618c-175">VariantNotInt (CheckRole)</span></span>](variantnotint.md)
-   [<span data-ttu-id="8618c-176">VariantNotInt (CheckState) </span><span class="sxs-lookup"><span data-stu-id="8618c-176">VariantNotInt (CheckState)</span></span>](variantnotint--checkstate-.md)

## <a name="related-topics"></a><span data-ttu-id="8618c-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="8618c-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8618c-178">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="8618c-178">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




