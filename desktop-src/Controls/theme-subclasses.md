---
title: 使用主題子類別
description: 代表控制項的主題類別（例如 ComboBox、Edit、ExplorerBar、Rebar、Tab 和 Toolbar）可以子類別化，以提供該特定控制項的主題變化。
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672899"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="65685-103">使用主題子類別</span><span class="sxs-lookup"><span data-stu-id="65685-103">Using Theme Subclasses</span></span>

<span data-ttu-id="65685-104">代表控制項的主題類別（例如 ComboBox、Edit、ExplorerBar、Rebar、Tab 和 Toolbar）可以子類別化，以提供該特定控制項的主題變化。</span><span class="sxs-lookup"><span data-stu-id="65685-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="65685-105">例如， **按鈕** 類別會子類別化，以 `Start::Button` 提供套用至 [ **開始** ] 按鈕之主題的控制權。</span><span class="sxs-lookup"><span data-stu-id="65685-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="65685-106">當您建立子類別（如本主題中所討論的子類別）時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="65685-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="65685-107">因為子類別可能會在後續版本的 Windows 中改變或無法使用，所以您不建議使用它們。</span><span class="sxs-lookup"><span data-stu-id="65685-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="65685-108">使用主題子類別的兩種方式</span><span class="sxs-lookup"><span data-stu-id="65685-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="65685-109">應用程式可以使用下列其中一種方式的子類別化主題：</span><span class="sxs-lookup"><span data-stu-id="65685-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="65685-110">它可以使用 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 函式搭配 `subclass::class` *pszClassList* 參數中的表單字串。</span><span class="sxs-lookup"><span data-stu-id="65685-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="65685-111">它可以使用 *pszSubAppName* 參數中的主題子類別名稱來呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 。</span><span class="sxs-lookup"><span data-stu-id="65685-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="65685-112">使用設定視覺化樣式的主題訊息</span><span class="sxs-lookup"><span data-stu-id="65685-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="65685-113">某些控制項（例如 Rebar 和工具列）提供您可以傳送的特定訊息，指示控制項使用主題子類別。</span><span class="sxs-lookup"><span data-stu-id="65685-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="65685-114">針對這些控制項，在訊息的 *lParam* 參數中提供包含主題子類別名稱之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="65685-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="65685-115">使用一般 [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) 訊息，或使用如下表所示的特定變異。</span><span class="sxs-lookup"><span data-stu-id="65685-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="65685-116">控制</span><span class="sxs-lookup"><span data-stu-id="65685-116">Control</span></span>    | <span data-ttu-id="65685-117">訊息</span><span class="sxs-lookup"><span data-stu-id="65685-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="65685-118">工具提示</span><span class="sxs-lookup"><span data-stu-id="65685-118">Tooltip</span></span>    | [<span data-ttu-id="65685-119">**TTM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="65685-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="65685-120">工具列</span><span class="sxs-lookup"><span data-stu-id="65685-120">Toolbar</span></span>    | [<span data-ttu-id="65685-121">**TB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="65685-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="65685-122">鋼筋</span><span class="sxs-lookup"><span data-stu-id="65685-122">Rebar</span></span>      | [<span data-ttu-id="65685-123">**RB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="65685-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="65685-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="65685-124">ComboBoxEx</span></span> | [<span data-ttu-id="65685-125">**CBEM \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="65685-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="65685-126">下表列出 Windows Vista 定義的一些子類別。</span><span class="sxs-lookup"><span data-stu-id="65685-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65685-127">類別</span><span class="sxs-lookup"><span data-stu-id="65685-127">Class</span></span></th>
<th><span data-ttu-id="65685-128">子</span><span class="sxs-lookup"><span data-stu-id="65685-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65685-129">ComboBox</span><span class="sxs-lookup"><span data-stu-id="65685-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-130">位址</span><span class="sxs-lookup"><span data-stu-id="65685-130">Address</span></span></li>
<li><span data-ttu-id="65685-131">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-131">AddressComposited</span></span></li>
<li><span data-ttu-id="65685-132">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="65685-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="65685-133">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="65685-134">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="65685-134">MaxAddress</span></span></li>
<li><span data-ttu-id="65685-135">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="65685-136">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="65685-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="65685-137">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65685-138">編輯</span><span class="sxs-lookup"><span data-stu-id="65685-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-139">位址</span><span class="sxs-lookup"><span data-stu-id="65685-139">Address</span></span></li>
<li><span data-ttu-id="65685-140">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-140">AddressComposited</span></span></li>
<li><span data-ttu-id="65685-141">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="65685-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="65685-142">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="65685-143">InactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="65685-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="65685-144">InactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="65685-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="65685-145">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="65685-145">MaxAddress</span></span></li>
<li><span data-ttu-id="65685-146">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="65685-147">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="65685-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="65685-148">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="65685-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="65685-149">MaxInactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="65685-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="65685-150">MaxInactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="65685-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="65685-151">MaxSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="65685-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="65685-152">MaxSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="65685-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="65685-153">SearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="65685-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="65685-154">SearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="65685-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65685-155">鋼筋</span><span class="sxs-lookup"><span data-stu-id="65685-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-156">BrowserTabBar</span><span class="sxs-lookup"><span data-stu-id="65685-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="65685-157">InactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="65685-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="65685-158">InactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="65685-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="65685-159">MaxInactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="65685-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="65685-160">MaxInactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="65685-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="65685-161">MaxNavbar</span><span class="sxs-lookup"><span data-stu-id="65685-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="65685-162">MaxNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="65685-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="65685-163">瀏覽列</span><span class="sxs-lookup"><span data-stu-id="65685-163">Navbar</span></span></li>
<li><span data-ttu-id="65685-164">NavbarComposited</span><span class="sxs-lookup"><span data-stu-id="65685-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="65685-165">NavbarNonTopmost</span><span class="sxs-lookup"><span data-stu-id="65685-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65685-166">索引標籤</span><span class="sxs-lookup"><span data-stu-id="65685-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-167">BrowserTab</span><span class="sxs-lookup"><span data-stu-id="65685-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65685-168">工具列</span><span class="sxs-lookup"><span data-stu-id="65685-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-169">Go</span><span class="sxs-lookup"><span data-stu-id="65685-169">Go</span></span></li>
<li><span data-ttu-id="65685-170">GoComposited</span><span class="sxs-lookup"><span data-stu-id="65685-170">GoComposited</span></span></li>
<li><span data-ttu-id="65685-171">InactiveGo</span><span class="sxs-lookup"><span data-stu-id="65685-171">InactiveGo</span></span></li>
<li><span data-ttu-id="65685-172">InactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="65685-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="65685-173">MaxGo</span><span class="sxs-lookup"><span data-stu-id="65685-173">MaxGo</span></span></li>
<li><span data-ttu-id="65685-174">MaxGoComposited</span><span class="sxs-lookup"><span data-stu-id="65685-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="65685-175">MaxInactiveGo</span><span class="sxs-lookup"><span data-stu-id="65685-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="65685-176">MaxInactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="65685-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="65685-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="65685-177">SearchButton</span></span></li>
<li><span data-ttu-id="65685-178">SearchButtonComposited</span><span class="sxs-lookup"><span data-stu-id="65685-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="65685-179">出差</span><span class="sxs-lookup"><span data-stu-id="65685-179">Travel</span></span></li>
<li><span data-ttu-id="65685-180">TravelComposited</span><span class="sxs-lookup"><span data-stu-id="65685-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="65685-181">Internet Explorer 子類別</span><span class="sxs-lookup"><span data-stu-id="65685-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="65685-182">在 Windows Vista 中，即使類別本身不存在，Windows Internet Explorer 和 Windows 檔案總管內部特定類別的子類別也可以使用。</span><span class="sxs-lookup"><span data-stu-id="65685-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="65685-183">下表列出可用的子類別。</span><span class="sxs-lookup"><span data-stu-id="65685-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65685-184">AddressBand</span><span class="sxs-lookup"><span data-stu-id="65685-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-185">AB</span><span class="sxs-lookup"><span data-stu-id="65685-185">AB</span></span></li>
<li><span data-ttu-id="65685-186">ABGreen</span><span class="sxs-lookup"><span data-stu-id="65685-186">ABGreen</span></span></li>
<li><span data-ttu-id="65685-187">ABGreenComposited</span><span class="sxs-lookup"><span data-stu-id="65685-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="65685-188">ABRed</span><span class="sxs-lookup"><span data-stu-id="65685-188">ABRed</span></span></li>
<li><span data-ttu-id="65685-189">ABRedComposited</span><span class="sxs-lookup"><span data-stu-id="65685-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="65685-190">ABYellow</span><span class="sxs-lookup"><span data-stu-id="65685-190">ABYellow</span></span></li>
<li><span data-ttu-id="65685-191">ABYellowComposited</span><span class="sxs-lookup"><span data-stu-id="65685-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65685-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="65685-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="65685-193">InactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="65685-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="65685-194">InactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="65685-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="65685-195">MaxInactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="65685-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="65685-196">MaxInactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="65685-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="65685-197">MaxSearchBox</span><span class="sxs-lookup"><span data-stu-id="65685-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="65685-198">MaxSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="65685-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="65685-199">SearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="65685-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="65685-200">下表顯示這些類別的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="65685-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="65685-201">控制</span><span class="sxs-lookup"><span data-stu-id="65685-201">Control</span></span>     | <span data-ttu-id="65685-202">部分</span><span class="sxs-lookup"><span data-stu-id="65685-202">Part</span></span>         | <span data-ttu-id="65685-203">狀態</span><span class="sxs-lookup"><span data-stu-id="65685-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="65685-204">ADDRESSBAND</span><span class="sxs-lookup"><span data-stu-id="65685-204">ADDRESSBAND</span></span> | <span data-ttu-id="65685-205">ABBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="65685-205">ABBACKGROUND</span></span> | <span data-ttu-id="65685-206">一般 (0x1) 、經常性 (0x2) 、已停用 (0x3) 、焦點 (0x4) </span><span class="sxs-lookup"><span data-stu-id="65685-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="65685-207">搜尋方塊</span><span class="sxs-lookup"><span data-stu-id="65685-207">SEARCHBOX</span></span>   | <span data-ttu-id="65685-208">SBBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="65685-208">SBBACKGROUND</span></span> | <span data-ttu-id="65685-209">一般 (0x1) 、經常性 (0x2) 、已停用 (0x3) 、焦點 (0x4) </span><span class="sxs-lookup"><span data-stu-id="65685-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




