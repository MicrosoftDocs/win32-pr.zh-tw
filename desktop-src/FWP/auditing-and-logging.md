---
title: 稽核
description: Windows 篩選平台 (WFP) 提供防火牆和 IPsec 相關事件的審核。
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "103933781"
---
# <a name="auditing"></a><span data-ttu-id="6509e-103">稽核</span><span class="sxs-lookup"><span data-stu-id="6509e-103">Auditing</span></span>

<span data-ttu-id="6509e-104">Windows 篩選平台 (WFP) 提供防火牆和 IPsec 相關事件的審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="6509e-105">這些事件會儲存在系統安全性記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="6509e-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="6509e-106">已審核的事件如下所示。</span><span class="sxs-lookup"><span data-stu-id="6509e-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6509e-107">審核分類</span><span class="sxs-lookup"><span data-stu-id="6509e-107">Auditing category</span></span></th>
<th><span data-ttu-id="6509e-108">稽核子類別</span><span class="sxs-lookup"><span data-stu-id="6509e-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="6509e-109">已審核的事件</span><span class="sxs-lookup"><span data-stu-id="6509e-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6509e-110">原則變更</span><span class="sxs-lookup"><span data-stu-id="6509e-110">Policy Change</span></span><br/> <span data-ttu-id="6509e-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-112">篩選平臺原則變更</span><span class="sxs-lookup"><span data-stu-id="6509e-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="6509e-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="6509e-114">數位代表事件檢視器 (eventvwr.exe) 所顯示的事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6509e-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="6509e-115">新增和移除 WFP 物件：</span><span class="sxs-lookup"><span data-stu-id="6509e-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-116">5440已新增持續性標注</span><span class="sxs-lookup"><span data-stu-id="6509e-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="6509e-117">5441已新增開機時間或持續性篩選</span><span class="sxs-lookup"><span data-stu-id="6509e-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="6509e-118">5442持續性提供者已新增</span><span class="sxs-lookup"><span data-stu-id="6509e-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="6509e-119">已新增5443持續性提供者內容</span><span class="sxs-lookup"><span data-stu-id="6509e-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="6509e-120">5444已新增持續性子層</span><span class="sxs-lookup"><span data-stu-id="6509e-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="6509e-121">5446已新增或移除執行時間標注</span><span class="sxs-lookup"><span data-stu-id="6509e-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="6509e-122">5447已新增或移除執行時間篩選</span><span class="sxs-lookup"><span data-stu-id="6509e-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="6509e-123">5448已新增或移除執行時間提供者</span><span class="sxs-lookup"><span data-stu-id="6509e-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="6509e-124">5449已新增或移除執行時間提供者內容</span><span class="sxs-lookup"><span data-stu-id="6509e-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="6509e-125">5450已新增或移除的執行時間子圖層</span><span class="sxs-lookup"><span data-stu-id="6509e-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6509e-126">物件存取</span><span class="sxs-lookup"><span data-stu-id="6509e-126">Object Access</span></span><br/> <span data-ttu-id="6509e-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-128">篩選平臺封包捨棄</span><span class="sxs-lookup"><span data-stu-id="6509e-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="6509e-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-130">由 WFP 捨棄的封包：</span><span class="sxs-lookup"><span data-stu-id="6509e-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-131">5152封包已捨棄</span><span class="sxs-lookup"><span data-stu-id="6509e-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="6509e-132">5153封包被否決</span><span class="sxs-lookup"><span data-stu-id="6509e-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6509e-133">物件存取</span><span class="sxs-lookup"><span data-stu-id="6509e-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="6509e-134">篩選平臺連接</span><span class="sxs-lookup"><span data-stu-id="6509e-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="6509e-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-136">允許和封鎖的連接：</span><span class="sxs-lookup"><span data-stu-id="6509e-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-137">允許5154接聽</span><span class="sxs-lookup"><span data-stu-id="6509e-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="6509e-138">5155接聽封鎖</span><span class="sxs-lookup"><span data-stu-id="6509e-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="6509e-139">允許的5156連接</span><span class="sxs-lookup"><span data-stu-id="6509e-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="6509e-140">5157連接已封鎖</span><span class="sxs-lookup"><span data-stu-id="6509e-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="6509e-141">5158允許系結</span><span class="sxs-lookup"><span data-stu-id="6509e-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="6509e-142">5159系結已封鎖</span><span class="sxs-lookup"><span data-stu-id="6509e-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="6509e-143">允許的連接不一定會審核相關篩選的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6509e-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="6509e-144">除非使用下列篩選準則的子集，否則 TCP 的 FilterID 會是0： UserID、AppID、Protocol、Remote Port。</span><span class="sxs-lookup"><span data-stu-id="6509e-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6509e-145">物件存取</span><span class="sxs-lookup"><span data-stu-id="6509e-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="6509e-146">其他物件存取事件</span><span class="sxs-lookup"><span data-stu-id="6509e-146">Other Object Access Events</span></span><br/> <span data-ttu-id="6509e-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="6509e-148">此子類別可進行許多審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-148">This subcategory enables many audits.</span></span> <span data-ttu-id="6509e-149">以下列出 WFP 特定的審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="6509e-150">拒絕服務防護狀態：</span><span class="sxs-lookup"><span data-stu-id="6509e-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-151">5148 WFP DoS 預防模式已啟動</span><span class="sxs-lookup"><span data-stu-id="6509e-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="6509e-152">5149 WFP DoS 防護模式已停止</span><span class="sxs-lookup"><span data-stu-id="6509e-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6509e-153">登入/登出</span><span class="sxs-lookup"><span data-stu-id="6509e-153">Logon/Logoff</span></span><br/> <span data-ttu-id="6509e-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-155">IPsec 主要模式</span><span class="sxs-lookup"><span data-stu-id="6509e-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="6509e-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-157">IKE 和 AuthIP 主要模式協商：</span><span class="sxs-lookup"><span data-stu-id="6509e-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-158">4650，已建立4651安全性關聯</span><span class="sxs-lookup"><span data-stu-id="6509e-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="6509e-159">4652，4653協商失敗</span><span class="sxs-lookup"><span data-stu-id="6509e-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="6509e-160">4655安全性關聯已結束</span><span class="sxs-lookup"><span data-stu-id="6509e-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6509e-161">登入/登出</span><span class="sxs-lookup"><span data-stu-id="6509e-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="6509e-162">IPsec 快速模式</span><span class="sxs-lookup"><span data-stu-id="6509e-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="6509e-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-164">IKE 和 AuthIP 快速模式協商：</span><span class="sxs-lookup"><span data-stu-id="6509e-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-165">已建立5451安全性關聯</span><span class="sxs-lookup"><span data-stu-id="6509e-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="6509e-166">5452安全性關聯已結束</span><span class="sxs-lookup"><span data-stu-id="6509e-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="6509e-167">4654協商失敗</span><span class="sxs-lookup"><span data-stu-id="6509e-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6509e-168">登入/登出</span><span class="sxs-lookup"><span data-stu-id="6509e-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="6509e-169">IPsec 延伸模式</span><span class="sxs-lookup"><span data-stu-id="6509e-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="6509e-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-171">AuthIP 延伸模式的協商：</span><span class="sxs-lookup"><span data-stu-id="6509e-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-172">4978不正確協商封包</span><span class="sxs-lookup"><span data-stu-id="6509e-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="6509e-173">已建立4979、4980、4981、4982安全性關聯</span><span class="sxs-lookup"><span data-stu-id="6509e-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="6509e-174">4983，4984協商失敗</span><span class="sxs-lookup"><span data-stu-id="6509e-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6509e-175">系統</span><span class="sxs-lookup"><span data-stu-id="6509e-175">System</span></span><br/> <span data-ttu-id="6509e-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-177">IPsec 驅動程式</span><span class="sxs-lookup"><span data-stu-id="6509e-177">IPsec Driver</span></span><br/> <span data-ttu-id="6509e-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6509e-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6509e-179">IPsec 驅動程式丟棄的封包：</span><span class="sxs-lookup"><span data-stu-id="6509e-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="6509e-180">4963已卸載輸入純文字封包</span><span class="sxs-lookup"><span data-stu-id="6509e-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6509e-181">預設會停用 WFP 的審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="6509e-182">您可以透過群組原則物件編輯器 MMC 嵌入式管理單元、[本機安全性原則] MMC 嵌入式管理單元或 auditpol.exe 命令，針對每個類別啟用審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="6509e-183">例如，若要啟用原則變更事件的審核，您可能會：</span><span class="sxs-lookup"><span data-stu-id="6509e-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="6509e-184">使用群組原則物件編輯器</span><span class="sxs-lookup"><span data-stu-id="6509e-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="6509e-185">執行 **gpedit.msc**。</span><span class="sxs-lookup"><span data-stu-id="6509e-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="6509e-186">展開 [本機電腦原則]。</span><span class="sxs-lookup"><span data-stu-id="6509e-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="6509e-187">展開 [電腦設定]。</span><span class="sxs-lookup"><span data-stu-id="6509e-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="6509e-188">展開 \[Windows 設定\]。</span><span class="sxs-lookup"><span data-stu-id="6509e-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="6509e-189">展開 [安全性設定]。</span><span class="sxs-lookup"><span data-stu-id="6509e-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="6509e-190">展開 [本機原則]。</span><span class="sxs-lookup"><span data-stu-id="6509e-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="6509e-191">按一下 [稽核原則]。</span><span class="sxs-lookup"><span data-stu-id="6509e-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="6509e-192">按兩下 [稽核原則變更]，以啟動 [屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6509e-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="6509e-193">檢查 [成功] 和 [失敗] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="6509e-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="6509e-194">使用本機安全性原則</span><span class="sxs-lookup"><span data-stu-id="6509e-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="6509e-195">執行 **secpol.msc services.msc**。</span><span class="sxs-lookup"><span data-stu-id="6509e-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="6509e-196">展開 [本機原則]。</span><span class="sxs-lookup"><span data-stu-id="6509e-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="6509e-197">按一下 [稽核原則]。</span><span class="sxs-lookup"><span data-stu-id="6509e-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="6509e-198">按兩下 [稽核原則變更]，以啟動 [屬性] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6509e-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="6509e-199">檢查 [成功] 和 [失敗] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="6509e-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="6509e-200">使用 auditpol.exe 命令</span><span class="sxs-lookup"><span data-stu-id="6509e-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="6509e-201">**auditpol/set/category：「原則變更」/success： enable/failure： enable**</span><span class="sxs-lookup"><span data-stu-id="6509e-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="6509e-202">只能透過 auditpol.exe 命令以個別子類別為基礎來啟用審核。</span><span class="sxs-lookup"><span data-stu-id="6509e-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="6509e-203">審核分類和子類別目錄名稱已當地語系化。</span><span class="sxs-lookup"><span data-stu-id="6509e-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="6509e-204">為了避免針對審核腳本進行當地語系化，可能會使用對應的 Guid 來取代名稱。</span><span class="sxs-lookup"><span data-stu-id="6509e-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="6509e-205">例如，若要啟用篩選平臺原則變更事件的審核，您可以使用下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="6509e-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="6509e-206">**auditpol/set/subcategory：「篩選平臺原則變更」/success： enable/failure： enable**</span><span class="sxs-lookup"><span data-stu-id="6509e-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="6509e-207">**auditpol/set/subcategory： "{0CCE9233-69AE-11D9-BED3-505054503030}"/success： enable/failure： enable**</span><span class="sxs-lookup"><span data-stu-id="6509e-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="6509e-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="6509e-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6509e-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="6509e-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="6509e-210">[事件記錄檔](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6509e-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6509e-211">群組原則</span><span class="sxs-lookup"><span data-stu-id="6509e-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

