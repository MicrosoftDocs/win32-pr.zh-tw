---
title: '其他物件角色和支援的方法 (MSAA UI 元素參考) '
description: 本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682789"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="02030-103">其他物件角色和支援的方法 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="02030-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="02030-104">本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。</span><span class="sxs-lookup"><span data-stu-id="02030-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="02030-105">每個物件角色都包含物件角色所支援的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性清單。</span><span class="sxs-lookup"><span data-stu-id="02030-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="02030-106">雖然其他主題檔支援 UI 元素的 **IAccessible** 方法和屬性，但本主題會列出您可以預期針對特定物件角色支援的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="02030-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="02030-107">許多可能具有此處所列其中一個角色的 UI 元素，通常會在瀏覽器中看到。</span><span class="sxs-lookup"><span data-stu-id="02030-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="02030-108">請使用本主題作為指導方針。</span><span class="sxs-lookup"><span data-stu-id="02030-108">Use this topic as a guideline.</span></span> <span data-ttu-id="02030-109">強烈建議您使用 Microsoft Active Accessibility 工具來確認個別物件角色的預期行為。</span><span class="sxs-lookup"><span data-stu-id="02030-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="02030-110">下表列出 Oleacc.dll 支援的其他物件角色。</span><span class="sxs-lookup"><span data-stu-id="02030-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="02030-111">**角色 \_ 系統 \_ 警示**</span><span class="sxs-lookup"><span data-stu-id="02030-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="02030-112">**角色 \_ 系統 \_ DROPLIST**</span><span class="sxs-lookup"><span data-stu-id="02030-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="02030-113">**角色 \_ 系統 \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="02030-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="02030-114">**角色 \_ 系統方程式 \_**</span><span class="sxs-lookup"><span data-stu-id="02030-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="02030-115">**角色 \_ 系統 \_ 框線**</span><span class="sxs-lookup"><span data-stu-id="02030-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="02030-116">**角色 \_ 系統 \_ 圖形**</span><span class="sxs-lookup"><span data-stu-id="02030-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="02030-117">**角色 \_ 系統 \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="02030-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="02030-118">**角色 \_ 系統 \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="02030-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="02030-119">**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="02030-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="02030-120">**角色 \_ 系統 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="02030-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="02030-121">**角色 \_ 系統 \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="02030-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="02030-122">**角色 \_ 系統 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="02030-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="02030-123">**角色 \_ 系統 \_ 儲存格**</span><span class="sxs-lookup"><span data-stu-id="02030-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="02030-124">**角色 \_ 系統 \_ 窗格**</span><span class="sxs-lookup"><span data-stu-id="02030-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="02030-125">**角色 \_ 系統 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="02030-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="02030-126">**角色 \_ 系統資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="02030-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="02030-127">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="02030-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="02030-128">**角色 \_ 系統 \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="02030-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="02030-129">**角色 \_ 系統 \_ 時鐘**</span><span class="sxs-lookup"><span data-stu-id="02030-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="02030-130">**角色 \_ 系統 \_ 分隔符號**</span><span class="sxs-lookup"><span data-stu-id="02030-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="02030-131">**角色 \_ 系統資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="02030-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="02030-132">**角色 \_ 系統 \_ 音效**</span><span class="sxs-lookup"><span data-stu-id="02030-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="02030-133">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="02030-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="02030-134">**角色 \_ 系統 \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="02030-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="02030-135">**角色 \_ 系統 \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="02030-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="02030-136">**角色 \_ 系統 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="02030-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="02030-137">**角色 \_ 系統 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="02030-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="02030-138">**角色 \_ 系統 \_ 空白字元**</span><span class="sxs-lookup"><span data-stu-id="02030-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="02030-139">角色 \_ 系統 \_ 警示</span><span class="sxs-lookup"><span data-stu-id="02030-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="02030-140">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 警示**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="02030-141">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-142">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-142">get\_accName</span></span>
-   <span data-ttu-id="02030-143">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-143">get\_accRole</span></span>
-   <span data-ttu-id="02030-144">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="02030-145">角色 \_ 系統 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="02030-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="02030-146">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 應用程式**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="02030-147">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-148">accHitTest</span></span>
-   <span data-ttu-id="02030-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-149">accLocation</span></span>
-   <span data-ttu-id="02030-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-150">accNavigate</span></span>
-   <span data-ttu-id="02030-151">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-151">get\_accChild</span></span>
-   <span data-ttu-id="02030-152">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-152">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-153">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-153">get\_accFocus</span></span>
-   <span data-ttu-id="02030-154">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-154">get\_accHelp</span></span>
-   <span data-ttu-id="02030-155">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-156">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-157">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-157">get\_accName</span></span>
-   <span data-ttu-id="02030-158">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-158">get\_accParent</span></span>
-   <span data-ttu-id="02030-159">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-159">get\_accRole</span></span>
-   <span data-ttu-id="02030-160">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="02030-161">角色 \_ 系統 \_ 框線</span><span class="sxs-lookup"><span data-stu-id="02030-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="02030-162">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 框線**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="02030-163">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-164">accHitTest</span></span>
-   <span data-ttu-id="02030-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-165">accLocation</span></span>
-   <span data-ttu-id="02030-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-166">accNavigate</span></span>
-   <span data-ttu-id="02030-167">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-167">get\_accRole</span></span>
-   <span data-ttu-id="02030-168">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="02030-169">角色 \_ 系統 \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="02030-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="02030-170">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWN**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="02030-171">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-173">accHitTest</span></span>
-   <span data-ttu-id="02030-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-174">accLocation</span></span>
-   <span data-ttu-id="02030-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-175">accNavigate</span></span>
-   <span data-ttu-id="02030-176">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-176">get\_accChild</span></span>
-   <span data-ttu-id="02030-177">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-177">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-178">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-179">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-179">get\_accFocus</span></span>
-   <span data-ttu-id="02030-180">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-180">get\_accHelp</span></span>
-   <span data-ttu-id="02030-181">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-182">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-183">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-183">get\_accName</span></span>
-   <span data-ttu-id="02030-184">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-184">get\_accParent</span></span>
-   <span data-ttu-id="02030-185">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-185">get\_accRole</span></span>
-   <span data-ttu-id="02030-186">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="02030-187">角色 \_ 系統 \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="02030-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="02030-188">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="02030-189">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-191">accHitTest</span></span>
-   <span data-ttu-id="02030-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-192">accLocation</span></span>
-   <span data-ttu-id="02030-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-193">accNavigate</span></span>
-   <span data-ttu-id="02030-194">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-194">get\_accChild</span></span>
-   <span data-ttu-id="02030-195">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-195">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-196">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-197">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-197">get\_accFocus</span></span>
-   <span data-ttu-id="02030-198">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-198">get\_accHelp</span></span>
-   <span data-ttu-id="02030-199">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-200">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-201">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-201">get\_accName</span></span>
-   <span data-ttu-id="02030-202">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-202">get\_accParent</span></span>
-   <span data-ttu-id="02030-203">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-203">get\_accRole</span></span>
-   <span data-ttu-id="02030-204">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="02030-205">角色 \_ 系統 \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="02030-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="02030-206">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONMENU**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="02030-207">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-209">accHitTest</span></span>
-   <span data-ttu-id="02030-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-210">accLocation</span></span>
-   <span data-ttu-id="02030-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-211">accNavigate</span></span>
-   <span data-ttu-id="02030-212">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-213">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-213">get\_accFocus</span></span>
-   <span data-ttu-id="02030-214">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-214">get\_accHelp</span></span>
-   <span data-ttu-id="02030-215">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-216">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-217">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-217">get\_accName</span></span>
-   <span data-ttu-id="02030-218">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-218">get\_accParent</span></span>
-   <span data-ttu-id="02030-219">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-219">get\_accRole</span></span>
-   <span data-ttu-id="02030-220">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="02030-221">角色 \_ 系統 \_ 儲存格</span><span class="sxs-lookup"><span data-stu-id="02030-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="02030-222">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 儲存格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="02030-223">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-224">accHitTest</span></span>
-   <span data-ttu-id="02030-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-225">accLocation</span></span>
-   <span data-ttu-id="02030-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-226">accNavigate</span></span>
-   <span data-ttu-id="02030-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-227">accSelect</span></span>
-   <span data-ttu-id="02030-228">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-228">get\_accChild</span></span>
-   <span data-ttu-id="02030-229">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-229">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-230">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-230">get\_accFocus</span></span>
-   <span data-ttu-id="02030-231">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-231">get\_accHelp</span></span>
-   <span data-ttu-id="02030-232">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-233">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-234">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-234">get\_accName</span></span>
-   <span data-ttu-id="02030-235">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-235">get\_accParent</span></span>
-   <span data-ttu-id="02030-236">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-236">get\_accRole</span></span>
-   <span data-ttu-id="02030-237">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-237">get\_accState</span></span>
-   <span data-ttu-id="02030-238">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="02030-239">角色 \_ 系統 \_ 字元</span><span class="sxs-lookup"><span data-stu-id="02030-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="02030-240">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 字元**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="02030-241">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-242">accHitTest</span></span>
-   <span data-ttu-id="02030-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-243">accLocation</span></span>
-   <span data-ttu-id="02030-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-244">accNavigate</span></span>
-   <span data-ttu-id="02030-245">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-245">get\_accDescription</span></span>
-   <span data-ttu-id="02030-246">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-246">get\_accFocus</span></span>
-   <span data-ttu-id="02030-247">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-248">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-248">get\_accName</span></span>
-   <span data-ttu-id="02030-249">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-249">get\_accParent</span></span>
-   <span data-ttu-id="02030-250">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-250">get\_accRole</span></span>
-   <span data-ttu-id="02030-251">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-251">get\_accState</span></span>
-   <span data-ttu-id="02030-252">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="02030-253">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="02030-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="02030-254">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="02030-255">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-256">accHitTest</span></span>
-   <span data-ttu-id="02030-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-257">accLocation</span></span>
-   <span data-ttu-id="02030-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-258">accNavigate</span></span>
-   <span data-ttu-id="02030-259">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-259">get\_accChild</span></span>
-   <span data-ttu-id="02030-260">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-260">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-261">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-261">get\_accFocus</span></span>
-   <span data-ttu-id="02030-262">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-262">get\_accHelp</span></span>
-   <span data-ttu-id="02030-263">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-264">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-265">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-265">get\_accName</span></span>
-   <span data-ttu-id="02030-266">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-266">get\_accParent</span></span>
-   <span data-ttu-id="02030-267">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-267">get\_accRole</span></span>
-   <span data-ttu-id="02030-268">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="02030-269">角色 \_ 系統 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="02030-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="02030-270">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 時鐘**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="02030-271">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-272">accHitTest</span></span>
-   <span data-ttu-id="02030-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-273">accLocation</span></span>
-   <span data-ttu-id="02030-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-274">accNavigate</span></span>
-   <span data-ttu-id="02030-275">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-275">get\_accFocus</span></span>
-   <span data-ttu-id="02030-276">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-276">get\_accHelp</span></span>
-   <span data-ttu-id="02030-277">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-278">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-279">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-279">get\_accName</span></span>
-   <span data-ttu-id="02030-280">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-280">get\_accParent</span></span>
-   <span data-ttu-id="02030-281">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-281">get\_accRole</span></span>
-   <span data-ttu-id="02030-282">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-282">get\_accState</span></span>
-   <span data-ttu-id="02030-283">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="02030-284">角色 \_ 系統資料 \_ 行</span><span class="sxs-lookup"><span data-stu-id="02030-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="02030-285">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 行**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="02030-286">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-287">accHitTest</span></span>
-   <span data-ttu-id="02030-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-288">accLocation</span></span>
-   <span data-ttu-id="02030-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-289">accNavigate</span></span>
-   <span data-ttu-id="02030-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-290">accSelect</span></span>
-   <span data-ttu-id="02030-291">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-291">get\_accChild</span></span>
-   <span data-ttu-id="02030-292">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-292">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-293">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-293">get\_accFocus</span></span>
-   <span data-ttu-id="02030-294">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-294">get\_accName</span></span>
-   <span data-ttu-id="02030-295">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-295">get\_accParent</span></span>
-   <span data-ttu-id="02030-296">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-296">get\_accRole</span></span>
-   <span data-ttu-id="02030-297">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-297">get\_accState</span></span>
-   <span data-ttu-id="02030-298">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="02030-299">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="02030-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="02030-300">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="02030-301">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-302">accHitTest</span></span>
-   <span data-ttu-id="02030-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-303">accLocation</span></span>
-   <span data-ttu-id="02030-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-304">accNavigate</span></span>
-   <span data-ttu-id="02030-305">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-305">get\_accChild</span></span>
-   <span data-ttu-id="02030-306">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-306">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-307">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-307">get\_accFocus</span></span>
-   <span data-ttu-id="02030-308">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-308">get\_accHelp</span></span>
-   <span data-ttu-id="02030-309">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-310">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-311">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-311">get\_accName</span></span>
-   <span data-ttu-id="02030-312">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-312">get\_accParent</span></span>
-   <span data-ttu-id="02030-313">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-313">get\_accRole</span></span>
-   <span data-ttu-id="02030-314">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="02030-315">角色 \_ 系統 \_ 撥號</span><span class="sxs-lookup"><span data-stu-id="02030-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="02030-316">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 撥號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="02030-317">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-319">accHitTest</span></span>
-   <span data-ttu-id="02030-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-320">accLocation</span></span>
-   <span data-ttu-id="02030-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-321">accNavigate</span></span>
-   <span data-ttu-id="02030-322">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-323">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-323">get\_accFocus</span></span>
-   <span data-ttu-id="02030-324">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-324">get\_accHelp</span></span>
-   <span data-ttu-id="02030-325">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-326">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-327">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-327">get\_accName</span></span>
-   <span data-ttu-id="02030-328">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-328">get\_accParent</span></span>
-   <span data-ttu-id="02030-329">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-329">get\_accRole</span></span>
-   <span data-ttu-id="02030-330">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-330">get\_accState</span></span>
-   <span data-ttu-id="02030-331">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="02030-332">角色 \_ 系統 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="02030-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="02030-333">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 檔**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="02030-334">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-335">accHitTest</span></span>
-   <span data-ttu-id="02030-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-336">accLocation</span></span>
-   <span data-ttu-id="02030-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-337">accNavigate</span></span>
-   <span data-ttu-id="02030-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-338">accSelect</span></span>
-   <span data-ttu-id="02030-339">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-339">get\_accChild</span></span>
-   <span data-ttu-id="02030-340">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-340">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-341">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-341">get\_accFocus</span></span>
-   <span data-ttu-id="02030-342">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-342">get\_accName</span></span>
-   <span data-ttu-id="02030-343">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-343">get\_accParent</span></span>
-   <span data-ttu-id="02030-344">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-344">get\_accRole</span></span>
-   <span data-ttu-id="02030-345">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="02030-346">角色 \_ 系統 \_ DROPLIST</span><span class="sxs-lookup"><span data-stu-id="02030-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="02030-347">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ DROPLIST**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="02030-348">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-350">accHitTest</span></span>
-   <span data-ttu-id="02030-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-351">accLocation</span></span>
-   <span data-ttu-id="02030-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-352">accNavigate</span></span>
-   <span data-ttu-id="02030-353">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-353">get\_accChild</span></span>
-   <span data-ttu-id="02030-354">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-354">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-355">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-356">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-356">get\_accFocus</span></span>
-   <span data-ttu-id="02030-357">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-357">get\_accHelp</span></span>
-   <span data-ttu-id="02030-358">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-359">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-360">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-360">get\_accName</span></span>
-   <span data-ttu-id="02030-361">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-361">get\_accParent</span></span>
-   <span data-ttu-id="02030-362">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-362">get\_accRole</span></span>
-   <span data-ttu-id="02030-363">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="02030-364">角色 \_ 系統方程式 \_</span><span class="sxs-lookup"><span data-stu-id="02030-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="02030-365">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_**](object-roles.md)方程式。</span><span class="sxs-lookup"><span data-stu-id="02030-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="02030-366">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-367">accHitTest</span></span>
-   <span data-ttu-id="02030-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-368">accLocation</span></span>
-   <span data-ttu-id="02030-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-369">accNavigate</span></span>
-   <span data-ttu-id="02030-370">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-370">get\_accFocus</span></span>
-   <span data-ttu-id="02030-371">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-371">get\_accName</span></span>
-   <span data-ttu-id="02030-372">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-372">get\_accParent</span></span>
-   <span data-ttu-id="02030-373">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-373">get\_accRole</span></span>
-   <span data-ttu-id="02030-374">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-374">get\_accState</span></span>
-   <span data-ttu-id="02030-375">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="02030-376">角色 \_ 系統 \_ 圖形</span><span class="sxs-lookup"><span data-stu-id="02030-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="02030-377">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖形**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="02030-378">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-379">accHitTest</span></span>
-   <span data-ttu-id="02030-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-380">accLocation</span></span>
-   <span data-ttu-id="02030-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-381">accNavigate</span></span>
-   <span data-ttu-id="02030-382">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-382">get\_accFocus</span></span>
-   <span data-ttu-id="02030-383">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-383">get\_accHelp</span></span>
-   <span data-ttu-id="02030-384">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-385">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-386">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-386">get\_accName</span></span>
-   <span data-ttu-id="02030-387">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-387">get\_accParent</span></span>
-   <span data-ttu-id="02030-388">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-388">get\_accRole</span></span>
-   <span data-ttu-id="02030-389">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="02030-390">角色 \_ 系統 \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="02030-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="02030-391">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ HELPBALLOON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="02030-392">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-393">accHitTest</span></span>
-   <span data-ttu-id="02030-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-394">accLocation</span></span>
-   <span data-ttu-id="02030-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-395">accNavigate</span></span>
-   <span data-ttu-id="02030-396">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-396">get\_accChild</span></span>
-   <span data-ttu-id="02030-397">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-397">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-398">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-399">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-399">get\_accName</span></span>
-   <span data-ttu-id="02030-400">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-400">get\_accParent</span></span>
-   <span data-ttu-id="02030-401">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-401">get\_accRole</span></span>
-   <span data-ttu-id="02030-402">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-402">get\_accState</span></span>
-   <span data-ttu-id="02030-403">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="02030-404">角色 \_ 系統 \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="02030-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="02030-405">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ IPADDRESS**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="02030-406">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-407">accHitTest</span></span>
-   <span data-ttu-id="02030-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-408">accLocation</span></span>
-   <span data-ttu-id="02030-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-409">accNavigate</span></span>
-   <span data-ttu-id="02030-410">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-410">get\_accChild</span></span>
-   <span data-ttu-id="02030-411">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-411">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-412">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-412">get\_accFocus</span></span>
-   <span data-ttu-id="02030-413">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-413">get\_accHelp</span></span>
-   <span data-ttu-id="02030-414">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-415">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-416">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-416">get\_accName</span></span>
-   <span data-ttu-id="02030-417">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-417">get\_accParent</span></span>
-   <span data-ttu-id="02030-418">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-418">get\_accRole</span></span>
-   <span data-ttu-id="02030-419">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-419">get\_accState</span></span>
-   <span data-ttu-id="02030-420">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="02030-421">角色 \_ 系統 \_ 連結</span><span class="sxs-lookup"><span data-stu-id="02030-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="02030-422">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 連結**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="02030-423">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-425">accHitTest</span></span>
-   <span data-ttu-id="02030-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-426">accLocation</span></span>
-   <span data-ttu-id="02030-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-427">accNavigate</span></span>
-   <span data-ttu-id="02030-428">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-428">get\_accChild</span></span>
-   <span data-ttu-id="02030-429">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-429">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-430">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-431">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-431">get\_accDescription</span></span>
-   <span data-ttu-id="02030-432">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-432">get\_accFocus</span></span>
-   <span data-ttu-id="02030-433">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-434">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-434">get\_accName</span></span>
-   <span data-ttu-id="02030-435">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-435">get\_accParent</span></span>
-   <span data-ttu-id="02030-436">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-436">get\_accRole</span></span>
-   <span data-ttu-id="02030-437">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-437">get\_accState</span></span>
-   <span data-ttu-id="02030-438">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="02030-439">角色 \_ 系統 \_ 窗格</span><span class="sxs-lookup"><span data-stu-id="02030-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="02030-440">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 窗格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="02030-441">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-442">accHitTest</span></span>
-   <span data-ttu-id="02030-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-443">accLocation</span></span>
-   <span data-ttu-id="02030-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-444">accNavigate</span></span>
-   <span data-ttu-id="02030-445">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-445">get\_accChild</span></span>
-   <span data-ttu-id="02030-446">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-446">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-447">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-447">get\_accFocus</span></span>
-   <span data-ttu-id="02030-448">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-448">get\_accHelp</span></span>
-   <span data-ttu-id="02030-449">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-450">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-451">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-451">get\_accName</span></span>
-   <span data-ttu-id="02030-452">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-452">get\_accParent</span></span>
-   <span data-ttu-id="02030-453">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-453">get\_accRole</span></span>
-   <span data-ttu-id="02030-454">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="02030-455">角色 \_ 系統資料 \_ 列</span><span class="sxs-lookup"><span data-stu-id="02030-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="02030-456">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 列**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="02030-457">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-458">accHitTest</span></span>
-   <span data-ttu-id="02030-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-459">accLocation</span></span>
-   <span data-ttu-id="02030-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-460">accNavigate</span></span>
-   <span data-ttu-id="02030-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-461">accSelect</span></span>
-   <span data-ttu-id="02030-462">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-462">get\_accChild</span></span>
-   <span data-ttu-id="02030-463">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-463">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-464">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-464">get\_accDescription</span></span>
-   <span data-ttu-id="02030-465">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-465">get\_accFocus</span></span>
-   <span data-ttu-id="02030-466">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-466">get\_accName</span></span>
-   <span data-ttu-id="02030-467">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-467">get\_accParent</span></span>
-   <span data-ttu-id="02030-468">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-468">get\_accRole</span></span>
-   <span data-ttu-id="02030-469">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-469">get\_accState</span></span>
-   <span data-ttu-id="02030-470">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="02030-471">角色 \_ 系統 \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="02030-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="02030-472">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ ROWHEADER**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="02030-473">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-474">accHitTest</span></span>
-   <span data-ttu-id="02030-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-475">accLocation</span></span>
-   <span data-ttu-id="02030-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-476">accNavigate</span></span>
-   <span data-ttu-id="02030-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-477">accSelect</span></span>
-   <span data-ttu-id="02030-478">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-478">get\_accChild</span></span>
-   <span data-ttu-id="02030-479">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-479">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-480">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-481">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-481">get\_accDescription</span></span>
-   <span data-ttu-id="02030-482">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-482">get\_accFocus</span></span>
-   <span data-ttu-id="02030-483">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-483">get\_accName</span></span>
-   <span data-ttu-id="02030-484">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-484">get\_accParent</span></span>
-   <span data-ttu-id="02030-485">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-485">get\_accRole</span></span>
-   <span data-ttu-id="02030-486">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-486">get\_accState</span></span>
-   <span data-ttu-id="02030-487">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="02030-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="02030-488">角色 \_ 系統 \_ 分隔符號</span><span class="sxs-lookup"><span data-stu-id="02030-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="02030-489">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 分隔符號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="02030-490">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-491">accHitTest</span></span>
-   <span data-ttu-id="02030-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-492">accLocation</span></span>
-   <span data-ttu-id="02030-493">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-493">get\_accChild</span></span>
-   <span data-ttu-id="02030-494">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-494">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-495">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-495">get\_accParent</span></span>
-   <span data-ttu-id="02030-496">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-496">get\_accRole</span></span>
-   <span data-ttu-id="02030-497">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="02030-498">角色 \_ 系統 \_ 音效</span><span class="sxs-lookup"><span data-stu-id="02030-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="02030-499">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 音效**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="02030-500">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-501">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-501">get\_accDescription</span></span>
-   <span data-ttu-id="02030-502">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-502">get\_accName</span></span>
-   <span data-ttu-id="02030-503">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-503">get\_accRole</span></span>
-   <span data-ttu-id="02030-504">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="02030-505">角色 \_ 系統 \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="02030-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="02030-506">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="02030-507">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="02030-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-509">accHitTest</span></span>
-   <span data-ttu-id="02030-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-510">accLocation</span></span>
-   <span data-ttu-id="02030-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-511">accNavigate</span></span>
-   <span data-ttu-id="02030-512">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="02030-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="02030-513">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-513">get\_accHelp</span></span>
-   <span data-ttu-id="02030-514">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-515">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-516">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-516">get\_accName</span></span>
-   <span data-ttu-id="02030-517">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-517">get\_accParent</span></span>
-   <span data-ttu-id="02030-518">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-518">get\_accRole</span></span>
-   <span data-ttu-id="02030-519">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="02030-520">角色 \_ 系統 \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="02030-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="02030-521">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 資料表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="02030-522">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="02030-523">accHitTest</span></span>
-   <span data-ttu-id="02030-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-524">accLocation</span></span>
-   <span data-ttu-id="02030-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="02030-525">accNavigate</span></span>
-   <span data-ttu-id="02030-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-526">accSelect</span></span>
-   <span data-ttu-id="02030-527">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="02030-527">get\_accChild</span></span>
-   <span data-ttu-id="02030-528">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="02030-528">get\_accChildCount</span></span>
-   <span data-ttu-id="02030-529">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="02030-529">get\_accDescription</span></span>
-   <span data-ttu-id="02030-530">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="02030-530">get\_accFocus</span></span>
-   <span data-ttu-id="02030-531">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="02030-531">get\_accHelp</span></span>
-   <span data-ttu-id="02030-532">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="02030-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="02030-533">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="02030-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="02030-534">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="02030-534">get\_accName</span></span>
-   <span data-ttu-id="02030-535">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-535">get\_accParent</span></span>
-   <span data-ttu-id="02030-536">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-536">get\_accRole</span></span>
-   <span data-ttu-id="02030-537">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="02030-538">角色 \_ 系統 \_ 空白字元</span><span class="sxs-lookup"><span data-stu-id="02030-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="02030-539">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 空白**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="02030-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="02030-540">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="02030-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="02030-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="02030-541">accLocation</span></span>
-   <span data-ttu-id="02030-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="02030-542">accSelect</span></span>
-   <span data-ttu-id="02030-543">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="02030-543">get\_accParent</span></span>
-   <span data-ttu-id="02030-544">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="02030-544">get\_accRole</span></span>
-   <span data-ttu-id="02030-545">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="02030-545">get\_accState</span></span>

 

 