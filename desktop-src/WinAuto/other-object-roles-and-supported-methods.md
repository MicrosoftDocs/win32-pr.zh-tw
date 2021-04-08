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
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="38f98-103">其他物件角色和支援的方法 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="38f98-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="38f98-104">本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。</span><span class="sxs-lookup"><span data-stu-id="38f98-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="38f98-105">每個物件角色都包含物件角色所支援的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性清單。</span><span class="sxs-lookup"><span data-stu-id="38f98-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="38f98-106">雖然其他主題檔支援 UI 元素的 **IAccessible** 方法和屬性，但本主題會列出您可以預期針對特定物件角色支援的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="38f98-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="38f98-107">許多可能具有此處所列其中一個角色的 UI 元素，通常會在瀏覽器中看到。</span><span class="sxs-lookup"><span data-stu-id="38f98-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="38f98-108">請使用本主題作為指導方針。</span><span class="sxs-lookup"><span data-stu-id="38f98-108">Use this topic as a guideline.</span></span> <span data-ttu-id="38f98-109">強烈建議您使用 Microsoft Active Accessibility 工具來確認個別物件角色的預期行為。</span><span class="sxs-lookup"><span data-stu-id="38f98-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="38f98-110">下表列出 Oleacc.dll 支援的其他物件角色。</span><span class="sxs-lookup"><span data-stu-id="38f98-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="38f98-111">**角色 \_ 系統 \_ 警示**</span><span class="sxs-lookup"><span data-stu-id="38f98-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="38f98-112">**角色 \_ 系統 \_ DROPLIST**</span><span class="sxs-lookup"><span data-stu-id="38f98-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="38f98-113">**角色 \_ 系統 \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="38f98-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="38f98-114">**角色 \_ 系統方程式 \_**</span><span class="sxs-lookup"><span data-stu-id="38f98-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="38f98-115">**角色 \_ 系統 \_ 框線**</span><span class="sxs-lookup"><span data-stu-id="38f98-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="38f98-116">**角色 \_ 系統 \_ 圖形**</span><span class="sxs-lookup"><span data-stu-id="38f98-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="38f98-117">**角色 \_ 系統 \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="38f98-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="38f98-118">**角色 \_ 系統 \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="38f98-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="38f98-119">**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="38f98-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="38f98-120">**角色 \_ 系統 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="38f98-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="38f98-121">**角色 \_ 系統 \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="38f98-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="38f98-122">**角色 \_ 系統 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="38f98-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="38f98-123">**角色 \_ 系統 \_ 儲存格**</span><span class="sxs-lookup"><span data-stu-id="38f98-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="38f98-124">**角色 \_ 系統 \_ 窗格**</span><span class="sxs-lookup"><span data-stu-id="38f98-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="38f98-125">**角色 \_ 系統 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="38f98-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="38f98-126">**角色 \_ 系統資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="38f98-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="38f98-127">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="38f98-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="38f98-128">**角色 \_ 系統 \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="38f98-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="38f98-129">**角色 \_ 系統 \_ 時鐘**</span><span class="sxs-lookup"><span data-stu-id="38f98-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="38f98-130">**角色 \_ 系統 \_ 分隔符號**</span><span class="sxs-lookup"><span data-stu-id="38f98-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="38f98-131">**角色 \_ 系統資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="38f98-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="38f98-132">**角色 \_ 系統 \_ 音效**</span><span class="sxs-lookup"><span data-stu-id="38f98-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="38f98-133">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="38f98-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="38f98-134">**角色 \_ 系統 \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="38f98-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="38f98-135">**角色 \_ 系統 \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="38f98-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="38f98-136">**角色 \_ 系統 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="38f98-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="38f98-137">**角色 \_ 系統 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="38f98-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="38f98-138">**角色 \_ 系統 \_ 空白字元**</span><span class="sxs-lookup"><span data-stu-id="38f98-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="38f98-139">角色 \_ 系統 \_ 警示</span><span class="sxs-lookup"><span data-stu-id="38f98-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="38f98-140">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 警示**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="38f98-141">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-142">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-142">get\_accName</span></span>
-   <span data-ttu-id="38f98-143">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-143">get\_accRole</span></span>
-   <span data-ttu-id="38f98-144">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="38f98-145">角色 \_ 系統 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="38f98-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="38f98-146">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 應用程式**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="38f98-147">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-148">accHitTest</span></span>
-   <span data-ttu-id="38f98-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-149">accLocation</span></span>
-   <span data-ttu-id="38f98-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-150">accNavigate</span></span>
-   <span data-ttu-id="38f98-151">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-151">get\_accChild</span></span>
-   <span data-ttu-id="38f98-152">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-152">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-153">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-153">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-154">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-154">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-155">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-156">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-157">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-157">get\_accName</span></span>
-   <span data-ttu-id="38f98-158">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-158">get\_accParent</span></span>
-   <span data-ttu-id="38f98-159">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-159">get\_accRole</span></span>
-   <span data-ttu-id="38f98-160">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="38f98-161">角色 \_ 系統 \_ 框線</span><span class="sxs-lookup"><span data-stu-id="38f98-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="38f98-162">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 框線**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="38f98-163">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-164">accHitTest</span></span>
-   <span data-ttu-id="38f98-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-165">accLocation</span></span>
-   <span data-ttu-id="38f98-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-166">accNavigate</span></span>
-   <span data-ttu-id="38f98-167">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-167">get\_accRole</span></span>
-   <span data-ttu-id="38f98-168">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="38f98-169">角色 \_ 系統 \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="38f98-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="38f98-170">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWN**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="38f98-171">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-173">accHitTest</span></span>
-   <span data-ttu-id="38f98-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-174">accLocation</span></span>
-   <span data-ttu-id="38f98-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-175">accNavigate</span></span>
-   <span data-ttu-id="38f98-176">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-176">get\_accChild</span></span>
-   <span data-ttu-id="38f98-177">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-177">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-178">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-179">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-179">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-180">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-180">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-181">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-182">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-183">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-183">get\_accName</span></span>
-   <span data-ttu-id="38f98-184">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-184">get\_accParent</span></span>
-   <span data-ttu-id="38f98-185">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-185">get\_accRole</span></span>
-   <span data-ttu-id="38f98-186">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="38f98-187">角色 \_ 系統 \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="38f98-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="38f98-188">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="38f98-189">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-191">accHitTest</span></span>
-   <span data-ttu-id="38f98-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-192">accLocation</span></span>
-   <span data-ttu-id="38f98-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-193">accNavigate</span></span>
-   <span data-ttu-id="38f98-194">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-194">get\_accChild</span></span>
-   <span data-ttu-id="38f98-195">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-195">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-196">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-197">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-197">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-198">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-198">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-199">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-200">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-201">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-201">get\_accName</span></span>
-   <span data-ttu-id="38f98-202">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-202">get\_accParent</span></span>
-   <span data-ttu-id="38f98-203">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-203">get\_accRole</span></span>
-   <span data-ttu-id="38f98-204">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="38f98-205">角色 \_ 系統 \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="38f98-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="38f98-206">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONMENU**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="38f98-207">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-209">accHitTest</span></span>
-   <span data-ttu-id="38f98-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-210">accLocation</span></span>
-   <span data-ttu-id="38f98-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-211">accNavigate</span></span>
-   <span data-ttu-id="38f98-212">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-213">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-213">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-214">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-214">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-215">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-216">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-217">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-217">get\_accName</span></span>
-   <span data-ttu-id="38f98-218">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-218">get\_accParent</span></span>
-   <span data-ttu-id="38f98-219">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-219">get\_accRole</span></span>
-   <span data-ttu-id="38f98-220">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="38f98-221">角色 \_ 系統 \_ 儲存格</span><span class="sxs-lookup"><span data-stu-id="38f98-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="38f98-222">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 儲存格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="38f98-223">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-224">accHitTest</span></span>
-   <span data-ttu-id="38f98-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-225">accLocation</span></span>
-   <span data-ttu-id="38f98-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-226">accNavigate</span></span>
-   <span data-ttu-id="38f98-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-227">accSelect</span></span>
-   <span data-ttu-id="38f98-228">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-228">get\_accChild</span></span>
-   <span data-ttu-id="38f98-229">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-229">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-230">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-230">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-231">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-231">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-232">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-233">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-234">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-234">get\_accName</span></span>
-   <span data-ttu-id="38f98-235">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-235">get\_accParent</span></span>
-   <span data-ttu-id="38f98-236">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-236">get\_accRole</span></span>
-   <span data-ttu-id="38f98-237">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-237">get\_accState</span></span>
-   <span data-ttu-id="38f98-238">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="38f98-239">角色 \_ 系統 \_ 字元</span><span class="sxs-lookup"><span data-stu-id="38f98-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="38f98-240">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 字元**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="38f98-241">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-242">accHitTest</span></span>
-   <span data-ttu-id="38f98-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-243">accLocation</span></span>
-   <span data-ttu-id="38f98-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-244">accNavigate</span></span>
-   <span data-ttu-id="38f98-245">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-245">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-246">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-246">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-247">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-248">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-248">get\_accName</span></span>
-   <span data-ttu-id="38f98-249">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-249">get\_accParent</span></span>
-   <span data-ttu-id="38f98-250">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-250">get\_accRole</span></span>
-   <span data-ttu-id="38f98-251">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-251">get\_accState</span></span>
-   <span data-ttu-id="38f98-252">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="38f98-253">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="38f98-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="38f98-254">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="38f98-255">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-256">accHitTest</span></span>
-   <span data-ttu-id="38f98-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-257">accLocation</span></span>
-   <span data-ttu-id="38f98-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-258">accNavigate</span></span>
-   <span data-ttu-id="38f98-259">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-259">get\_accChild</span></span>
-   <span data-ttu-id="38f98-260">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-260">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-261">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-261">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-262">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-262">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-263">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-264">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-265">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-265">get\_accName</span></span>
-   <span data-ttu-id="38f98-266">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-266">get\_accParent</span></span>
-   <span data-ttu-id="38f98-267">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-267">get\_accRole</span></span>
-   <span data-ttu-id="38f98-268">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="38f98-269">角色 \_ 系統 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="38f98-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="38f98-270">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 時鐘**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="38f98-271">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-272">accHitTest</span></span>
-   <span data-ttu-id="38f98-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-273">accLocation</span></span>
-   <span data-ttu-id="38f98-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-274">accNavigate</span></span>
-   <span data-ttu-id="38f98-275">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-275">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-276">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-276">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-277">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-278">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-279">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-279">get\_accName</span></span>
-   <span data-ttu-id="38f98-280">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-280">get\_accParent</span></span>
-   <span data-ttu-id="38f98-281">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-281">get\_accRole</span></span>
-   <span data-ttu-id="38f98-282">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-282">get\_accState</span></span>
-   <span data-ttu-id="38f98-283">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="38f98-284">角色 \_ 系統資料 \_ 行</span><span class="sxs-lookup"><span data-stu-id="38f98-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="38f98-285">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 行**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="38f98-286">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-287">accHitTest</span></span>
-   <span data-ttu-id="38f98-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-288">accLocation</span></span>
-   <span data-ttu-id="38f98-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-289">accNavigate</span></span>
-   <span data-ttu-id="38f98-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-290">accSelect</span></span>
-   <span data-ttu-id="38f98-291">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-291">get\_accChild</span></span>
-   <span data-ttu-id="38f98-292">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-292">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-293">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-293">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-294">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-294">get\_accName</span></span>
-   <span data-ttu-id="38f98-295">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-295">get\_accParent</span></span>
-   <span data-ttu-id="38f98-296">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-296">get\_accRole</span></span>
-   <span data-ttu-id="38f98-297">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-297">get\_accState</span></span>
-   <span data-ttu-id="38f98-298">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="38f98-299">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="38f98-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="38f98-300">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="38f98-301">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-302">accHitTest</span></span>
-   <span data-ttu-id="38f98-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-303">accLocation</span></span>
-   <span data-ttu-id="38f98-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-304">accNavigate</span></span>
-   <span data-ttu-id="38f98-305">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-305">get\_accChild</span></span>
-   <span data-ttu-id="38f98-306">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-306">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-307">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-307">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-308">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-308">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-309">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-310">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-311">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-311">get\_accName</span></span>
-   <span data-ttu-id="38f98-312">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-312">get\_accParent</span></span>
-   <span data-ttu-id="38f98-313">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-313">get\_accRole</span></span>
-   <span data-ttu-id="38f98-314">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="38f98-315">角色 \_ 系統 \_ 撥號</span><span class="sxs-lookup"><span data-stu-id="38f98-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="38f98-316">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 撥號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="38f98-317">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-319">accHitTest</span></span>
-   <span data-ttu-id="38f98-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-320">accLocation</span></span>
-   <span data-ttu-id="38f98-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-321">accNavigate</span></span>
-   <span data-ttu-id="38f98-322">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-323">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-323">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-324">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-324">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-325">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-326">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-327">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-327">get\_accName</span></span>
-   <span data-ttu-id="38f98-328">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-328">get\_accParent</span></span>
-   <span data-ttu-id="38f98-329">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-329">get\_accRole</span></span>
-   <span data-ttu-id="38f98-330">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-330">get\_accState</span></span>
-   <span data-ttu-id="38f98-331">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="38f98-332">角色 \_ 系統 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="38f98-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="38f98-333">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 檔**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="38f98-334">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-335">accHitTest</span></span>
-   <span data-ttu-id="38f98-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-336">accLocation</span></span>
-   <span data-ttu-id="38f98-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-337">accNavigate</span></span>
-   <span data-ttu-id="38f98-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-338">accSelect</span></span>
-   <span data-ttu-id="38f98-339">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-339">get\_accChild</span></span>
-   <span data-ttu-id="38f98-340">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-340">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-341">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-341">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-342">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-342">get\_accName</span></span>
-   <span data-ttu-id="38f98-343">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-343">get\_accParent</span></span>
-   <span data-ttu-id="38f98-344">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-344">get\_accRole</span></span>
-   <span data-ttu-id="38f98-345">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="38f98-346">角色 \_ 系統 \_ DROPLIST</span><span class="sxs-lookup"><span data-stu-id="38f98-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="38f98-347">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ DROPLIST**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="38f98-348">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-350">accHitTest</span></span>
-   <span data-ttu-id="38f98-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-351">accLocation</span></span>
-   <span data-ttu-id="38f98-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-352">accNavigate</span></span>
-   <span data-ttu-id="38f98-353">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-353">get\_accChild</span></span>
-   <span data-ttu-id="38f98-354">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-354">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-355">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-356">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-356">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-357">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-357">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-358">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-359">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-360">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-360">get\_accName</span></span>
-   <span data-ttu-id="38f98-361">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-361">get\_accParent</span></span>
-   <span data-ttu-id="38f98-362">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-362">get\_accRole</span></span>
-   <span data-ttu-id="38f98-363">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="38f98-364">角色 \_ 系統方程式 \_</span><span class="sxs-lookup"><span data-stu-id="38f98-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="38f98-365">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_**](object-roles.md)方程式。</span><span class="sxs-lookup"><span data-stu-id="38f98-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="38f98-366">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-367">accHitTest</span></span>
-   <span data-ttu-id="38f98-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-368">accLocation</span></span>
-   <span data-ttu-id="38f98-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-369">accNavigate</span></span>
-   <span data-ttu-id="38f98-370">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-370">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-371">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-371">get\_accName</span></span>
-   <span data-ttu-id="38f98-372">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-372">get\_accParent</span></span>
-   <span data-ttu-id="38f98-373">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-373">get\_accRole</span></span>
-   <span data-ttu-id="38f98-374">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-374">get\_accState</span></span>
-   <span data-ttu-id="38f98-375">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="38f98-376">角色 \_ 系統 \_ 圖形</span><span class="sxs-lookup"><span data-stu-id="38f98-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="38f98-377">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖形**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="38f98-378">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-379">accHitTest</span></span>
-   <span data-ttu-id="38f98-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-380">accLocation</span></span>
-   <span data-ttu-id="38f98-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-381">accNavigate</span></span>
-   <span data-ttu-id="38f98-382">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-382">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-383">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-383">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-384">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-385">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-386">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-386">get\_accName</span></span>
-   <span data-ttu-id="38f98-387">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-387">get\_accParent</span></span>
-   <span data-ttu-id="38f98-388">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-388">get\_accRole</span></span>
-   <span data-ttu-id="38f98-389">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="38f98-390">角色 \_ 系統 \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="38f98-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="38f98-391">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ HELPBALLOON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="38f98-392">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-393">accHitTest</span></span>
-   <span data-ttu-id="38f98-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-394">accLocation</span></span>
-   <span data-ttu-id="38f98-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-395">accNavigate</span></span>
-   <span data-ttu-id="38f98-396">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-396">get\_accChild</span></span>
-   <span data-ttu-id="38f98-397">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-397">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-398">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-399">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-399">get\_accName</span></span>
-   <span data-ttu-id="38f98-400">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-400">get\_accParent</span></span>
-   <span data-ttu-id="38f98-401">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-401">get\_accRole</span></span>
-   <span data-ttu-id="38f98-402">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-402">get\_accState</span></span>
-   <span data-ttu-id="38f98-403">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="38f98-404">角色 \_ 系統 \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="38f98-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="38f98-405">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ IPADDRESS**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="38f98-406">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-407">accHitTest</span></span>
-   <span data-ttu-id="38f98-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-408">accLocation</span></span>
-   <span data-ttu-id="38f98-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-409">accNavigate</span></span>
-   <span data-ttu-id="38f98-410">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-410">get\_accChild</span></span>
-   <span data-ttu-id="38f98-411">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-411">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-412">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-412">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-413">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-413">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-414">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-415">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-416">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-416">get\_accName</span></span>
-   <span data-ttu-id="38f98-417">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-417">get\_accParent</span></span>
-   <span data-ttu-id="38f98-418">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-418">get\_accRole</span></span>
-   <span data-ttu-id="38f98-419">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-419">get\_accState</span></span>
-   <span data-ttu-id="38f98-420">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="38f98-421">角色 \_ 系統 \_ 連結</span><span class="sxs-lookup"><span data-stu-id="38f98-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="38f98-422">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 連結**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="38f98-423">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-425">accHitTest</span></span>
-   <span data-ttu-id="38f98-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-426">accLocation</span></span>
-   <span data-ttu-id="38f98-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-427">accNavigate</span></span>
-   <span data-ttu-id="38f98-428">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-428">get\_accChild</span></span>
-   <span data-ttu-id="38f98-429">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-429">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-430">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-431">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-431">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-432">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-432">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-433">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-434">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-434">get\_accName</span></span>
-   <span data-ttu-id="38f98-435">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-435">get\_accParent</span></span>
-   <span data-ttu-id="38f98-436">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-436">get\_accRole</span></span>
-   <span data-ttu-id="38f98-437">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-437">get\_accState</span></span>
-   <span data-ttu-id="38f98-438">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="38f98-439">角色 \_ 系統 \_ 窗格</span><span class="sxs-lookup"><span data-stu-id="38f98-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="38f98-440">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 窗格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="38f98-441">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-442">accHitTest</span></span>
-   <span data-ttu-id="38f98-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-443">accLocation</span></span>
-   <span data-ttu-id="38f98-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-444">accNavigate</span></span>
-   <span data-ttu-id="38f98-445">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-445">get\_accChild</span></span>
-   <span data-ttu-id="38f98-446">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-446">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-447">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-447">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-448">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-448">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-449">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-450">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-451">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-451">get\_accName</span></span>
-   <span data-ttu-id="38f98-452">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-452">get\_accParent</span></span>
-   <span data-ttu-id="38f98-453">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-453">get\_accRole</span></span>
-   <span data-ttu-id="38f98-454">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="38f98-455">角色 \_ 系統資料 \_ 列</span><span class="sxs-lookup"><span data-stu-id="38f98-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="38f98-456">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 列**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="38f98-457">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-458">accHitTest</span></span>
-   <span data-ttu-id="38f98-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-459">accLocation</span></span>
-   <span data-ttu-id="38f98-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-460">accNavigate</span></span>
-   <span data-ttu-id="38f98-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-461">accSelect</span></span>
-   <span data-ttu-id="38f98-462">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-462">get\_accChild</span></span>
-   <span data-ttu-id="38f98-463">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-463">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-464">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-464">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-465">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-465">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-466">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-466">get\_accName</span></span>
-   <span data-ttu-id="38f98-467">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-467">get\_accParent</span></span>
-   <span data-ttu-id="38f98-468">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-468">get\_accRole</span></span>
-   <span data-ttu-id="38f98-469">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-469">get\_accState</span></span>
-   <span data-ttu-id="38f98-470">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="38f98-471">角色 \_ 系統 \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="38f98-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="38f98-472">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ ROWHEADER**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="38f98-473">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-474">accHitTest</span></span>
-   <span data-ttu-id="38f98-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-475">accLocation</span></span>
-   <span data-ttu-id="38f98-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-476">accNavigate</span></span>
-   <span data-ttu-id="38f98-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-477">accSelect</span></span>
-   <span data-ttu-id="38f98-478">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-478">get\_accChild</span></span>
-   <span data-ttu-id="38f98-479">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-479">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-480">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-481">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-481">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-482">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-482">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-483">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-483">get\_accName</span></span>
-   <span data-ttu-id="38f98-484">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-484">get\_accParent</span></span>
-   <span data-ttu-id="38f98-485">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-485">get\_accRole</span></span>
-   <span data-ttu-id="38f98-486">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-486">get\_accState</span></span>
-   <span data-ttu-id="38f98-487">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="38f98-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="38f98-488">角色 \_ 系統 \_ 分隔符號</span><span class="sxs-lookup"><span data-stu-id="38f98-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="38f98-489">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 分隔符號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="38f98-490">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-491">accHitTest</span></span>
-   <span data-ttu-id="38f98-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-492">accLocation</span></span>
-   <span data-ttu-id="38f98-493">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-493">get\_accChild</span></span>
-   <span data-ttu-id="38f98-494">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-494">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-495">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-495">get\_accParent</span></span>
-   <span data-ttu-id="38f98-496">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-496">get\_accRole</span></span>
-   <span data-ttu-id="38f98-497">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="38f98-498">角色 \_ 系統 \_ 音效</span><span class="sxs-lookup"><span data-stu-id="38f98-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="38f98-499">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 音效**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="38f98-500">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-501">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-501">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-502">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-502">get\_accName</span></span>
-   <span data-ttu-id="38f98-503">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-503">get\_accRole</span></span>
-   <span data-ttu-id="38f98-504">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="38f98-505">角色 \_ 系統 \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="38f98-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="38f98-506">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="38f98-507">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="38f98-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-509">accHitTest</span></span>
-   <span data-ttu-id="38f98-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-510">accLocation</span></span>
-   <span data-ttu-id="38f98-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-511">accNavigate</span></span>
-   <span data-ttu-id="38f98-512">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="38f98-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="38f98-513">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-513">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-514">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-515">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-516">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-516">get\_accName</span></span>
-   <span data-ttu-id="38f98-517">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-517">get\_accParent</span></span>
-   <span data-ttu-id="38f98-518">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-518">get\_accRole</span></span>
-   <span data-ttu-id="38f98-519">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="38f98-520">角色 \_ 系統 \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="38f98-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="38f98-521">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 資料表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="38f98-522">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="38f98-523">accHitTest</span></span>
-   <span data-ttu-id="38f98-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-524">accLocation</span></span>
-   <span data-ttu-id="38f98-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="38f98-525">accNavigate</span></span>
-   <span data-ttu-id="38f98-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-526">accSelect</span></span>
-   <span data-ttu-id="38f98-527">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="38f98-527">get\_accChild</span></span>
-   <span data-ttu-id="38f98-528">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="38f98-528">get\_accChildCount</span></span>
-   <span data-ttu-id="38f98-529">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="38f98-529">get\_accDescription</span></span>
-   <span data-ttu-id="38f98-530">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="38f98-530">get\_accFocus</span></span>
-   <span data-ttu-id="38f98-531">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="38f98-531">get\_accHelp</span></span>
-   <span data-ttu-id="38f98-532">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="38f98-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="38f98-533">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="38f98-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="38f98-534">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="38f98-534">get\_accName</span></span>
-   <span data-ttu-id="38f98-535">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-535">get\_accParent</span></span>
-   <span data-ttu-id="38f98-536">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-536">get\_accRole</span></span>
-   <span data-ttu-id="38f98-537">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="38f98-538">角色 \_ 系統 \_ 空白字元</span><span class="sxs-lookup"><span data-stu-id="38f98-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="38f98-539">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 空白**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="38f98-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="38f98-540">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="38f98-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="38f98-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="38f98-541">accLocation</span></span>
-   <span data-ttu-id="38f98-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="38f98-542">accSelect</span></span>
-   <span data-ttu-id="38f98-543">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="38f98-543">get\_accParent</span></span>
-   <span data-ttu-id="38f98-544">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="38f98-544">get\_accRole</span></span>
-   <span data-ttu-id="38f98-545">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="38f98-545">get\_accState</span></span>

 

 