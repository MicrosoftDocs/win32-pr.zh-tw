---
description: 從 Windows XP，主控台支援主控台專案的分類。 註冊的專案會出現在一或多個類別中。 無法建立新的類別。
title: 指派主控台分類
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972076"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="90ecc-105">指派主控台分類</span><span class="sxs-lookup"><span data-stu-id="90ecc-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="90ecc-106">從 Windows XP，主控台支援主控台專案的分類。</span><span class="sxs-lookup"><span data-stu-id="90ecc-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="90ecc-107">註冊的專案會出現在一或多個類別中。</span><span class="sxs-lookup"><span data-stu-id="90ecc-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="90ecc-108">無法建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="90ecc-108">New categories cannot be created.</span></span>

<span data-ttu-id="90ecc-109">若要在一或多個類別中註冊主控台專案，請視需要在[註冊主控台專案](registering-control-panel-items.md)的[可執行檔主控台專案註冊](registering-control-panel-items.md)或[DLL 主控台專案註冊](registering-control-panel-items.md)區段中，加入值。</span><span class="sxs-lookup"><span data-stu-id="90ecc-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90ecc-110">類別目錄識別碼</span><span class="sxs-lookup"><span data-stu-id="90ecc-110">Category ID</span></span></th>
<th><span data-ttu-id="90ecc-111"> (Windows 7) 的類別名稱</span><span class="sxs-lookup"><span data-stu-id="90ecc-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="90ecc-112">Windows Vista)  (的類別名稱</span><span class="sxs-lookup"><span data-stu-id="90ecc-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="90ecc-113"> (Windows XP) 的類別名稱</span><span class="sxs-lookup"><span data-stu-id="90ecc-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90ecc-114">0</span><span class="sxs-lookup"><span data-stu-id="90ecc-114">0</span></span></td>
<td><span data-ttu-id="90ecc-115">&quot;所有主控台專案&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="90ecc-116">&quot;其他選項&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-117">未指定類別目錄識別碼的任何主控台專案都會出現在此分類中。</span><span class="sxs-lookup"><span data-stu-id="90ecc-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="90ecc-118">&quot;其他主控台選項&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-119">未指定類別目錄識別碼的任何主控台專案都會出現在此分類中。</span><span class="sxs-lookup"><span data-stu-id="90ecc-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-120">1</span><span class="sxs-lookup"><span data-stu-id="90ecc-120">1</span></span></td>
<td><span data-ttu-id="90ecc-121">&quot;[外觀與個人化]&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="90ecc-122">&quot;[外觀與個人化]&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="90ecc-123">&quot;外觀和主題&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90ecc-124">2</span><span class="sxs-lookup"><span data-stu-id="90ecc-124">2</span></span></td>
<td><span data-ttu-id="90ecc-125">&quot;硬體和音效&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="90ecc-126">&quot;硬體和音效&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="90ecc-127">&quot;印表機和其他硬體&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-128">3</span><span class="sxs-lookup"><span data-stu-id="90ecc-128">3</span></span></td>
<td><span data-ttu-id="90ecc-129">&quot;[網路和網際網路]&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="90ecc-130">&quot;[網路和網際網路]&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="90ecc-131">&quot;網路和網際網路連接&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90ecc-132">4</span><span class="sxs-lookup"><span data-stu-id="90ecc-132">4</span></span></td>
<td><span data-ttu-id="90ecc-133">不再使用。</span><span class="sxs-lookup"><span data-stu-id="90ecc-133">No longer used.</span></span> <span data-ttu-id="90ecc-134">只要將本身新增至類別4的任何專案，就會出現在類別 2 (硬體和音效) 。</span><span class="sxs-lookup"><span data-stu-id="90ecc-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="90ecc-135">不再使用。</span><span class="sxs-lookup"><span data-stu-id="90ecc-135">No longer used.</span></span> <span data-ttu-id="90ecc-136">只要將本身新增至類別4的任何專案，就會出現在類別 2 (硬體和音效) 。</span><span class="sxs-lookup"><span data-stu-id="90ecc-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="90ecc-137">&quot;聲音、語音和音訊裝置&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-138">5</span><span class="sxs-lookup"><span data-stu-id="90ecc-138">5</span></span></td>
<td><span data-ttu-id="90ecc-139">&quot;系統和安全性&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="90ecc-140">&quot;系統及維護&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="90ecc-141">&quot;效能與維護&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90ecc-142">6</span><span class="sxs-lookup"><span data-stu-id="90ecc-142">6</span></span></td>
<td><span data-ttu-id="90ecc-143">&quot;時鐘、語言和區域&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="90ecc-144">&quot;時鐘、語言和區域&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="90ecc-145">&quot;日期、時間、語言和地區選項&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-146">7</span><span class="sxs-lookup"><span data-stu-id="90ecc-146">7</span></span></td>
<td><span data-ttu-id="90ecc-147">&quot;輕鬆存取&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="90ecc-148">&quot;輕鬆存取&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="90ecc-149">&quot;協助工具選項&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90ecc-150">8</span><span class="sxs-lookup"><span data-stu-id="90ecc-150">8</span></span></td>
<td><span data-ttu-id="90ecc-151">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="90ecc-152">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="90ecc-153">&quot;新增或移除程式&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-154">9</span><span class="sxs-lookup"><span data-stu-id="90ecc-154">9</span></span></td>
<td><span data-ttu-id="90ecc-155">&quot;使用者帳戶&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-156">若未連線至網域，這稱為 &quot; 使用者帳戶和家庭安全 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="90ecc-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="90ecc-157">&quot;使用者帳戶&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-158">若未連線至網域，這稱為 &quot; 使用者帳戶和家庭安全 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="90ecc-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="90ecc-159">&quot;使用者帳戶&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90ecc-160">10</span><span class="sxs-lookup"><span data-stu-id="90ecc-160">10</span></span></td>
<td><span data-ttu-id="90ecc-161">不再使用。</span><span class="sxs-lookup"><span data-stu-id="90ecc-161">No longer used.</span></span> <span data-ttu-id="90ecc-162">在此類別中註冊的專案會出現在 [類別 5 (系統和安全性) ] 中。</span><span class="sxs-lookup"><span data-stu-id="90ecc-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="90ecc-163">&quot;安全性&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="90ecc-164">&quot;資訊安全中心&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-165">僅適用于 Windows XP Service Pack 2 (SP2) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="90ecc-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90ecc-166">11</span><span class="sxs-lookup"><span data-stu-id="90ecc-166">11</span></span></td>
<td><span data-ttu-id="90ecc-167">不再使用。</span><span class="sxs-lookup"><span data-stu-id="90ecc-167">No longer used.</span></span> <span data-ttu-id="90ecc-168">在此類別中註冊的專案會顯示在類別 0 (所有主控台專案) 。</span><span class="sxs-lookup"><span data-stu-id="90ecc-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="90ecc-169">&quot;行動電腦&quot;</span><span class="sxs-lookup"><span data-stu-id="90ecc-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90ecc-170">此類別只會顯示在行動電腦上。</span><span class="sxs-lookup"><span data-stu-id="90ecc-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="90ecc-171">未使用。</span><span class="sxs-lookup"><span data-stu-id="90ecc-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="90ecc-172">在 Windows XP 中，[ **新增或移除程式** ] 和 [ **使用者帳戶** ] 類別的運作方式與主控台中其他類別的運作方式稍有不同。</span><span class="sxs-lookup"><span data-stu-id="90ecc-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="90ecc-173">當一或多個專案新增至這兩個類別的其中一個時，主控台中的相關聯連結會開啟 [類別目錄] 頁面。</span><span class="sxs-lookup"><span data-stu-id="90ecc-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="90ecc-174">註冊的專案會出現在頁面的下半部的 [或挑選主控台圖示] 標題下方。</span><span class="sxs-lookup"><span data-stu-id="90ecc-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="90ecc-175">如果未針對其中一個類別註冊任何專案，主控台中的相關連結會直接叫用該類別的標準 Windows 專案。</span><span class="sxs-lookup"><span data-stu-id="90ecc-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="90ecc-176">在 Windows Vista 和更新版本中，[ **程式** ] 類別和 [ **使用者帳戶** ] 類別沒有此屬性。</span><span class="sxs-lookup"><span data-stu-id="90ecc-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="90ecc-177">只有在 Windows XP SP2 中提供的「 **安全性中心** 」類別也有點非標準。</span><span class="sxs-lookup"><span data-stu-id="90ecc-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="90ecc-178">按一下此類別會在新視窗中開啟 [ **安全性中心** ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="90ecc-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="90ecc-179">針對「 **安全性中心** 」註冊的專案會出現在該頁面下半部的 [ **管理安全性設定：**] 標題下方。</span><span class="sxs-lookup"><span data-stu-id="90ecc-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="90ecc-180">按一下圖示會開啟主控台專案。</span><span class="sxs-lookup"><span data-stu-id="90ecc-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90ecc-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="90ecc-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ecc-182">主控台專案</span><span class="sxs-lookup"><span data-stu-id="90ecc-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="90ecc-183">使用者體驗指南</span><span class="sxs-lookup"><span data-stu-id="90ecc-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="90ecc-184">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="90ecc-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="90ecc-185">使用 CPLApplet</span><span class="sxs-lookup"><span data-stu-id="90ecc-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="90ecc-186">主控台訊息處理</span><span class="sxs-lookup"><span data-stu-id="90ecc-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="90ecc-187">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="90ecc-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="90ecc-188">擴充系統主控台專案</span><span class="sxs-lookup"><span data-stu-id="90ecc-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="90ecc-189">建立主控台專案的可搜尋工作連結</span><span class="sxs-lookup"><span data-stu-id="90ecc-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="90ecc-190">在 Windows Vista 下存取安全模式下的主控台</span><span class="sxs-lookup"><span data-stu-id="90ecc-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




