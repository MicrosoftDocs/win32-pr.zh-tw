---
title: '其他物件角色和支援的方法 (MSAA UI 元素參考) '
description: 本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443999"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="24cf2-103">其他物件角色和支援的方法 (MSAA UI 元素參考) </span><span class="sxs-lookup"><span data-stu-id="24cf2-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="24cf2-104">本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。</span><span class="sxs-lookup"><span data-stu-id="24cf2-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="24cf2-105">每個物件角色都包含物件角色所支援的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性清單。</span><span class="sxs-lookup"><span data-stu-id="24cf2-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="24cf2-106">雖然其他主題檔支援 UI 元素的 **IAccessible** 方法和屬性，但本主題會列出您可以預期針對特定物件角色支援的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="24cf2-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="24cf2-107">許多可能具有此處所列其中一個角色的 UI 元素，通常會在瀏覽器中看到。</span><span class="sxs-lookup"><span data-stu-id="24cf2-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="24cf2-108">請使用本主題作為指導方針。</span><span class="sxs-lookup"><span data-stu-id="24cf2-108">Use this topic as a guideline.</span></span> <span data-ttu-id="24cf2-109">強烈建議您使用 Microsoft Active Accessibility 工具來確認個別物件角色的預期行為。</span><span class="sxs-lookup"><span data-stu-id="24cf2-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="24cf2-110">下表列出 Oleacc.dll 支援的其他物件角色。</span><span class="sxs-lookup"><span data-stu-id="24cf2-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="24cf2-111">**角色 \_ 系統 \_ 警示**</span><span class="sxs-lookup"><span data-stu-id="24cf2-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="24cf2-112">**角色 \_ 系統 \_ DROPLIST**</span><span class="sxs-lookup"><span data-stu-id="24cf2-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="24cf2-113">**角色 \_ 系統 \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="24cf2-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="24cf2-114">**角色 \_ 系統方程式 \_**</span><span class="sxs-lookup"><span data-stu-id="24cf2-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="24cf2-115">**角色 \_ 系統 \_ 框線**</span><span class="sxs-lookup"><span data-stu-id="24cf2-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="24cf2-116">**角色 \_ 系統 \_ 圖形**</span><span class="sxs-lookup"><span data-stu-id="24cf2-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="24cf2-117">**角色 \_ 系統 \_ BUTTONDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="24cf2-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="24cf2-118">**角色 \_ 系統 \_ HELPBALLOON**</span><span class="sxs-lookup"><span data-stu-id="24cf2-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="24cf2-119">**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="24cf2-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="24cf2-120">**角色 \_ 系統 \_ IPADDRESS**</span><span class="sxs-lookup"><span data-stu-id="24cf2-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="24cf2-121">**角色 \_ 系統 \_ BUTTONMENU**</span><span class="sxs-lookup"><span data-stu-id="24cf2-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="24cf2-122">**角色 \_ 系統 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="24cf2-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="24cf2-123">**角色 \_ 系統 \_ 儲存格**</span><span class="sxs-lookup"><span data-stu-id="24cf2-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="24cf2-124">**角色 \_ 系統 \_ 窗格**</span><span class="sxs-lookup"><span data-stu-id="24cf2-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="24cf2-125">**角色 \_ 系統 \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="24cf2-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="24cf2-126">**角色 \_ 系統資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="24cf2-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="24cf2-127">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="24cf2-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="24cf2-128">**角色 \_ 系統 \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="24cf2-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="24cf2-129">**角色 \_ 系統 \_ 時鐘**</span><span class="sxs-lookup"><span data-stu-id="24cf2-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="24cf2-130">**角色 \_ 系統 \_ 分隔符號**</span><span class="sxs-lookup"><span data-stu-id="24cf2-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="24cf2-131">**角色 \_ 系統資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="24cf2-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="24cf2-132">**角色 \_ 系統 \_ 音效**</span><span class="sxs-lookup"><span data-stu-id="24cf2-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="24cf2-133">**角色 \_ 系統 \_ 圖表**</span><span class="sxs-lookup"><span data-stu-id="24cf2-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="24cf2-134">**角色 \_ 系統 \_ SPLITBUTTON**</span><span class="sxs-lookup"><span data-stu-id="24cf2-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="24cf2-135">**角色 \_ 系統 \_ 撥號**</span><span class="sxs-lookup"><span data-stu-id="24cf2-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="24cf2-136">**角色 \_ 系統 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="24cf2-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="24cf2-137">**角色 \_ 系統 \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="24cf2-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="24cf2-138">**角色 \_ 系統 \_ 空白字元**</span><span class="sxs-lookup"><span data-stu-id="24cf2-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="24cf2-139">角色 \_ 系統 \_ 警示</span><span class="sxs-lookup"><span data-stu-id="24cf2-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="24cf2-140">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 警示**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-141">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-142">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-142">get\_accName</span></span>
-   <span data-ttu-id="24cf2-143">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-143">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-144">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="24cf2-145">角色 \_ 系統 \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="24cf2-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="24cf2-146">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 應用程式**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-147">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-148">accHitTest</span></span>
-   <span data-ttu-id="24cf2-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-149">accLocation</span></span>
-   <span data-ttu-id="24cf2-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-150">accNavigate</span></span>
-   <span data-ttu-id="24cf2-151">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-151">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-152">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-152">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-153">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-153">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-154">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-154">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-155">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-156">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-157">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-157">get\_accName</span></span>
-   <span data-ttu-id="24cf2-158">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-158">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-159">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-159">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-160">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="24cf2-161">角色 \_ 系統 \_ 框線</span><span class="sxs-lookup"><span data-stu-id="24cf2-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="24cf2-162">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 框線**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-163">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-164">accHitTest</span></span>
-   <span data-ttu-id="24cf2-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-165">accLocation</span></span>
-   <span data-ttu-id="24cf2-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-166">accNavigate</span></span>
-   <span data-ttu-id="24cf2-167">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-167">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-168">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="24cf2-169">角色 \_ 系統 \_ BUTTONDROPDOWN</span><span class="sxs-lookup"><span data-stu-id="24cf2-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="24cf2-170">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWN**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-171">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-173">accHitTest</span></span>
-   <span data-ttu-id="24cf2-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-174">accLocation</span></span>
-   <span data-ttu-id="24cf2-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-175">accNavigate</span></span>
-   <span data-ttu-id="24cf2-176">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-176">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-177">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-177">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-178">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-179">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-179">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-180">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-180">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-181">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-182">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-183">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-183">get\_accName</span></span>
-   <span data-ttu-id="24cf2-184">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-184">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-185">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-185">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-186">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="24cf2-187">角色 \_ 系統 \_ BUTTONDROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="24cf2-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="24cf2-188">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-189">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-191">accHitTest</span></span>
-   <span data-ttu-id="24cf2-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-192">accLocation</span></span>
-   <span data-ttu-id="24cf2-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-193">accNavigate</span></span>
-   <span data-ttu-id="24cf2-194">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-194">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-195">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-195">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-196">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-197">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-197">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-198">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-198">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-199">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-200">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-201">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-201">get\_accName</span></span>
-   <span data-ttu-id="24cf2-202">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-202">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-203">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-203">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-204">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="24cf2-205">角色 \_ 系統 \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="24cf2-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="24cf2-206">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONMENU**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-207">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-209">accHitTest</span></span>
-   <span data-ttu-id="24cf2-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-210">accLocation</span></span>
-   <span data-ttu-id="24cf2-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-211">accNavigate</span></span>
-   <span data-ttu-id="24cf2-212">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-213">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-213">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-214">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-214">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-215">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-216">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-217">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-217">get\_accName</span></span>
-   <span data-ttu-id="24cf2-218">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-218">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-219">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-219">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-220">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="24cf2-221">角色 \_ 系統 \_ 儲存格</span><span class="sxs-lookup"><span data-stu-id="24cf2-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="24cf2-222">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 儲存格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-223">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-224">accHitTest</span></span>
-   <span data-ttu-id="24cf2-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-225">accLocation</span></span>
-   <span data-ttu-id="24cf2-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-226">accNavigate</span></span>
-   <span data-ttu-id="24cf2-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-227">accSelect</span></span>
-   <span data-ttu-id="24cf2-228">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-228">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-229">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-229">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-230">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-230">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-231">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-231">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-232">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-233">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-234">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-234">get\_accName</span></span>
-   <span data-ttu-id="24cf2-235">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-235">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-236">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-236">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-237">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-237">get\_accState</span></span>
-   <span data-ttu-id="24cf2-238">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="24cf2-239">角色 \_ 系統 \_ 字元</span><span class="sxs-lookup"><span data-stu-id="24cf2-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="24cf2-240">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 字元**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-241">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-242">accHitTest</span></span>
-   <span data-ttu-id="24cf2-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-243">accLocation</span></span>
-   <span data-ttu-id="24cf2-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-244">accNavigate</span></span>
-   <span data-ttu-id="24cf2-245">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-245">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-246">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-246">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-247">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-248">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-248">get\_accName</span></span>
-   <span data-ttu-id="24cf2-249">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-249">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-250">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-250">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-251">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-251">get\_accState</span></span>
-   <span data-ttu-id="24cf2-252">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="24cf2-253">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="24cf2-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="24cf2-254">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-255">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-256">accHitTest</span></span>
-   <span data-ttu-id="24cf2-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-257">accLocation</span></span>
-   <span data-ttu-id="24cf2-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-258">accNavigate</span></span>
-   <span data-ttu-id="24cf2-259">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-259">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-260">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-260">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-261">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-261">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-262">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-262">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-263">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-264">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-265">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-265">get\_accName</span></span>
-   <span data-ttu-id="24cf2-266">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-266">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-267">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-267">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-268">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="24cf2-269">角色 \_ 系統 \_ 時鐘</span><span class="sxs-lookup"><span data-stu-id="24cf2-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="24cf2-270">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 時鐘**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-271">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-272">accHitTest</span></span>
-   <span data-ttu-id="24cf2-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-273">accLocation</span></span>
-   <span data-ttu-id="24cf2-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-274">accNavigate</span></span>
-   <span data-ttu-id="24cf2-275">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-275">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-276">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-276">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-277">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-278">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-279">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-279">get\_accName</span></span>
-   <span data-ttu-id="24cf2-280">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-280">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-281">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-281">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-282">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-282">get\_accState</span></span>
-   <span data-ttu-id="24cf2-283">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="24cf2-284">角色 \_ 系統資料 \_ 行</span><span class="sxs-lookup"><span data-stu-id="24cf2-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="24cf2-285">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 行**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-286">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-287">accHitTest</span></span>
-   <span data-ttu-id="24cf2-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-288">accLocation</span></span>
-   <span data-ttu-id="24cf2-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-289">accNavigate</span></span>
-   <span data-ttu-id="24cf2-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-290">accSelect</span></span>
-   <span data-ttu-id="24cf2-291">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-291">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-292">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-292">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-293">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-293">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-294">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-294">get\_accName</span></span>
-   <span data-ttu-id="24cf2-295">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-295">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-296">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-296">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-297">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-297">get\_accState</span></span>
-   <span data-ttu-id="24cf2-298">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="24cf2-299">角色 \_ 系統 \_ 圖表</span><span class="sxs-lookup"><span data-stu-id="24cf2-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="24cf2-300">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-301">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-302">accHitTest</span></span>
-   <span data-ttu-id="24cf2-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-303">accLocation</span></span>
-   <span data-ttu-id="24cf2-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-304">accNavigate</span></span>
-   <span data-ttu-id="24cf2-305">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-305">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-306">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-306">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-307">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-307">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-308">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-308">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-309">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-310">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-311">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-311">get\_accName</span></span>
-   <span data-ttu-id="24cf2-312">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-312">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-313">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-313">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-314">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="24cf2-315">角色 \_ 系統 \_ 撥號</span><span class="sxs-lookup"><span data-stu-id="24cf2-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="24cf2-316">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 撥號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-317">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-319">accHitTest</span></span>
-   <span data-ttu-id="24cf2-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-320">accLocation</span></span>
-   <span data-ttu-id="24cf2-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-321">accNavigate</span></span>
-   <span data-ttu-id="24cf2-322">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-323">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-323">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-324">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-324">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-325">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-326">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-327">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-327">get\_accName</span></span>
-   <span data-ttu-id="24cf2-328">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-328">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-329">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-329">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-330">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-330">get\_accState</span></span>
-   <span data-ttu-id="24cf2-331">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="24cf2-332">角色 \_ 系統 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="24cf2-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="24cf2-333">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 檔**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-334">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-335">accHitTest</span></span>
-   <span data-ttu-id="24cf2-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-336">accLocation</span></span>
-   <span data-ttu-id="24cf2-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-337">accNavigate</span></span>
-   <span data-ttu-id="24cf2-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-338">accSelect</span></span>
-   <span data-ttu-id="24cf2-339">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-339">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-340">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-340">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-341">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-341">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-342">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-342">get\_accName</span></span>
-   <span data-ttu-id="24cf2-343">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-343">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-344">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-344">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-345">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="24cf2-346">角色 \_ 系統 \_ DROPLIST</span><span class="sxs-lookup"><span data-stu-id="24cf2-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="24cf2-347">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ DROPLIST**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-348">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-350">accHitTest</span></span>
-   <span data-ttu-id="24cf2-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-351">accLocation</span></span>
-   <span data-ttu-id="24cf2-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-352">accNavigate</span></span>
-   <span data-ttu-id="24cf2-353">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-353">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-354">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-354">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-355">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-356">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-356">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-357">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-357">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-358">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-359">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-360">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-360">get\_accName</span></span>
-   <span data-ttu-id="24cf2-361">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-361">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-362">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-362">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-363">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="24cf2-364">角色 \_ 系統方程式 \_</span><span class="sxs-lookup"><span data-stu-id="24cf2-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="24cf2-365">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_**](object-roles.md)方程式。</span><span class="sxs-lookup"><span data-stu-id="24cf2-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-366">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-367">accHitTest</span></span>
-   <span data-ttu-id="24cf2-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-368">accLocation</span></span>
-   <span data-ttu-id="24cf2-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-369">accNavigate</span></span>
-   <span data-ttu-id="24cf2-370">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-370">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-371">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-371">get\_accName</span></span>
-   <span data-ttu-id="24cf2-372">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-372">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-373">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-373">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-374">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-374">get\_accState</span></span>
-   <span data-ttu-id="24cf2-375">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="24cf2-376">角色 \_ 系統 \_ 圖形</span><span class="sxs-lookup"><span data-stu-id="24cf2-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="24cf2-377">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖形**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-378">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-379">accHitTest</span></span>
-   <span data-ttu-id="24cf2-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-380">accLocation</span></span>
-   <span data-ttu-id="24cf2-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-381">accNavigate</span></span>
-   <span data-ttu-id="24cf2-382">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-382">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-383">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-383">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-384">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-385">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-386">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-386">get\_accName</span></span>
-   <span data-ttu-id="24cf2-387">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-387">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-388">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-388">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-389">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="24cf2-390">角色 \_ 系統 \_ HELPBALLOON</span><span class="sxs-lookup"><span data-stu-id="24cf2-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="24cf2-391">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ HELPBALLOON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-392">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-393">accHitTest</span></span>
-   <span data-ttu-id="24cf2-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-394">accLocation</span></span>
-   <span data-ttu-id="24cf2-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-395">accNavigate</span></span>
-   <span data-ttu-id="24cf2-396">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-396">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-397">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-397">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-398">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-399">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-399">get\_accName</span></span>
-   <span data-ttu-id="24cf2-400">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-400">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-401">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-401">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-402">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-402">get\_accState</span></span>
-   <span data-ttu-id="24cf2-403">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="24cf2-404">角色 \_ 系統 \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="24cf2-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="24cf2-405">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ IPADDRESS**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-406">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-407">accHitTest</span></span>
-   <span data-ttu-id="24cf2-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-408">accLocation</span></span>
-   <span data-ttu-id="24cf2-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-409">accNavigate</span></span>
-   <span data-ttu-id="24cf2-410">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-410">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-411">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-411">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-412">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-412">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-413">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-413">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-414">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-415">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-416">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-416">get\_accName</span></span>
-   <span data-ttu-id="24cf2-417">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-417">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-418">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-418">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-419">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-419">get\_accState</span></span>
-   <span data-ttu-id="24cf2-420">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="24cf2-421">角色 \_ 系統 \_ 連結</span><span class="sxs-lookup"><span data-stu-id="24cf2-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="24cf2-422">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 連結**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-423">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-425">accHitTest</span></span>
-   <span data-ttu-id="24cf2-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-426">accLocation</span></span>
-   <span data-ttu-id="24cf2-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-427">accNavigate</span></span>
-   <span data-ttu-id="24cf2-428">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-428">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-429">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-429">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-430">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-431">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-431">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-432">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-432">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-433">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-434">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-434">get\_accName</span></span>
-   <span data-ttu-id="24cf2-435">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-435">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-436">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-436">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-437">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-437">get\_accState</span></span>
-   <span data-ttu-id="24cf2-438">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="24cf2-439">角色 \_ 系統 \_ 窗格</span><span class="sxs-lookup"><span data-stu-id="24cf2-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="24cf2-440">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 窗格**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-441">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-442">accHitTest</span></span>
-   <span data-ttu-id="24cf2-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-443">accLocation</span></span>
-   <span data-ttu-id="24cf2-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-444">accNavigate</span></span>
-   <span data-ttu-id="24cf2-445">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-445">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-446">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-446">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-447">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-447">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-448">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-448">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-449">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-450">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-451">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-451">get\_accName</span></span>
-   <span data-ttu-id="24cf2-452">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-452">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-453">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-453">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-454">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="24cf2-455">角色 \_ 系統資料 \_ 列</span><span class="sxs-lookup"><span data-stu-id="24cf2-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="24cf2-456">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 列**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-457">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-458">accHitTest</span></span>
-   <span data-ttu-id="24cf2-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-459">accLocation</span></span>
-   <span data-ttu-id="24cf2-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-460">accNavigate</span></span>
-   <span data-ttu-id="24cf2-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-461">accSelect</span></span>
-   <span data-ttu-id="24cf2-462">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-462">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-463">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-463">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-464">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-464">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-465">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-465">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-466">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-466">get\_accName</span></span>
-   <span data-ttu-id="24cf2-467">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-467">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-468">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-468">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-469">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-469">get\_accState</span></span>
-   <span data-ttu-id="24cf2-470">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="24cf2-471">角色 \_ 系統 \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="24cf2-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="24cf2-472">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ ROWHEADER**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-473">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-474">accHitTest</span></span>
-   <span data-ttu-id="24cf2-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-475">accLocation</span></span>
-   <span data-ttu-id="24cf2-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-476">accNavigate</span></span>
-   <span data-ttu-id="24cf2-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-477">accSelect</span></span>
-   <span data-ttu-id="24cf2-478">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-478">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-479">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-479">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-480">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-481">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-481">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-482">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-482">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-483">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-483">get\_accName</span></span>
-   <span data-ttu-id="24cf2-484">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-484">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-485">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-485">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-486">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-486">get\_accState</span></span>
-   <span data-ttu-id="24cf2-487">取得 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="24cf2-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="24cf2-488">角色 \_ 系統 \_ 分隔符號</span><span class="sxs-lookup"><span data-stu-id="24cf2-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="24cf2-489">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 分隔符號**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-490">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-491">accHitTest</span></span>
-   <span data-ttu-id="24cf2-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-492">accLocation</span></span>
-   <span data-ttu-id="24cf2-493">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-493">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-494">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-494">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-495">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-495">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-496">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-496">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-497">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="24cf2-498">角色 \_ 系統 \_ 音效</span><span class="sxs-lookup"><span data-stu-id="24cf2-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="24cf2-499">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 音效**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-500">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-501">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-501">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-502">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-502">get\_accName</span></span>
-   <span data-ttu-id="24cf2-503">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-503">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-504">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="24cf2-505">角色 \_ 系統 \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="24cf2-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="24cf2-506">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-507">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="24cf2-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-509">accHitTest</span></span>
-   <span data-ttu-id="24cf2-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-510">accLocation</span></span>
-   <span data-ttu-id="24cf2-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-511">accNavigate</span></span>
-   <span data-ttu-id="24cf2-512">取得 \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="24cf2-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="24cf2-513">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-513">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-514">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-515">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-516">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-516">get\_accName</span></span>
-   <span data-ttu-id="24cf2-517">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-517">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-518">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-518">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-519">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="24cf2-520">角色 \_ 系統 \_ 資料表</span><span class="sxs-lookup"><span data-stu-id="24cf2-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="24cf2-521">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 資料表**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-522">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="24cf2-523">accHitTest</span></span>
-   <span data-ttu-id="24cf2-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-524">accLocation</span></span>
-   <span data-ttu-id="24cf2-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="24cf2-525">accNavigate</span></span>
-   <span data-ttu-id="24cf2-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-526">accSelect</span></span>
-   <span data-ttu-id="24cf2-527">取得 \_ accChild</span><span class="sxs-lookup"><span data-stu-id="24cf2-527">get\_accChild</span></span>
-   <span data-ttu-id="24cf2-528">取得 \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="24cf2-528">get\_accChildCount</span></span>
-   <span data-ttu-id="24cf2-529">取得 \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="24cf2-529">get\_accDescription</span></span>
-   <span data-ttu-id="24cf2-530">取得 \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="24cf2-530">get\_accFocus</span></span>
-   <span data-ttu-id="24cf2-531">取得 \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="24cf2-531">get\_accHelp</span></span>
-   <span data-ttu-id="24cf2-532">取得 \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="24cf2-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="24cf2-533">取得 \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="24cf2-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="24cf2-534">取得 \_ accName</span><span class="sxs-lookup"><span data-stu-id="24cf2-534">get\_accName</span></span>
-   <span data-ttu-id="24cf2-535">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-535">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-536">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-536">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-537">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="24cf2-538">角色 \_ 系統 \_ 空白字元</span><span class="sxs-lookup"><span data-stu-id="24cf2-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="24cf2-539">如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 空白**](object-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="24cf2-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="24cf2-540">**支援的屬性和方法**</span><span class="sxs-lookup"><span data-stu-id="24cf2-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="24cf2-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="24cf2-541">accLocation</span></span>
-   <span data-ttu-id="24cf2-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="24cf2-542">accSelect</span></span>
-   <span data-ttu-id="24cf2-543">取得 \_ accParent</span><span class="sxs-lookup"><span data-stu-id="24cf2-543">get\_accParent</span></span>
-   <span data-ttu-id="24cf2-544">取得 \_ accRole</span><span class="sxs-lookup"><span data-stu-id="24cf2-544">get\_accRole</span></span>
-   <span data-ttu-id="24cf2-545">取得 \_ accState</span><span class="sxs-lookup"><span data-stu-id="24cf2-545">get\_accState</span></span>

 

 