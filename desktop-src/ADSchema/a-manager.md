---
title: Manager 屬性
description: 包含使用者之管理員的分辨名稱。 管理員的使用者物件包含 directReports 屬性，其中包含所有使用者物件的參考，這些物件的管理員屬性都設為此辨別名稱。
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Manager 屬性 AD 架構
- manager 屬性 AD 架構
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385410"
---
# <a name="manager-attribute"></a><span data-ttu-id="1850f-106">Manager 屬性</span><span class="sxs-lookup"><span data-stu-id="1850f-106">Manager attribute</span></span>

<span data-ttu-id="1850f-107">包含使用者之管理員的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="1850f-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="1850f-108">管理員的使用者物件包含 directReports 屬性，其中包含所有使用者物件的參考，這些物件的管理員屬性都設為此辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="1850f-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="1850f-109">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-109">Entry</span></span> | <span data-ttu-id="1850f-110">值</span><span class="sxs-lookup"><span data-stu-id="1850f-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1850f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1850f-111">CN</span></span>                | <span data-ttu-id="1850f-112">Manager</span><span class="sxs-lookup"><span data-stu-id="1850f-112">Manager</span></span>                                                                     |
| <span data-ttu-id="1850f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="1850f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1850f-114">manager</span><span class="sxs-lookup"><span data-stu-id="1850f-114">manager</span></span>                                                                     |
| <span data-ttu-id="1850f-115">大小</span><span class="sxs-lookup"><span data-stu-id="1850f-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="1850f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="1850f-116">Update Privilege</span></span>  | <span data-ttu-id="1850f-117">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="1850f-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="1850f-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="1850f-118">Update Frequency</span></span>  | <span data-ttu-id="1850f-119">當使用者的記錄建立時，以及每次管理員需要變更時。</span><span class="sxs-lookup"><span data-stu-id="1850f-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="1850f-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-120">Attribute-Id</span></span>      | <span data-ttu-id="1850f-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="1850f-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="1850f-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="1850f-122">System-Id-Guid</span></span>    | <span data-ttu-id="1850f-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1850f-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="1850f-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1850f-124">Syntax</span></span>            | [<span data-ttu-id="1850f-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="1850f-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="1850f-126">實作</span><span class="sxs-lookup"><span data-stu-id="1850f-126">Implementations</span></span>

-   [<span data-ttu-id="1850f-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1850f-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1850f-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1850f-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1850f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1850f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1850f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1850f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1850f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1850f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1850f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1850f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1850f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1850f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1850f-134">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-134">Entry</span></span> | <span data-ttu-id="1850f-135">值</span><span class="sxs-lookup"><span data-stu-id="1850f-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1850f-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-136">Link-Id</span></span>                | <span data-ttu-id="1850f-137">42</span><span class="sxs-lookup"><span data-stu-id="1850f-137">42</span></span>                                                                 |
| <span data-ttu-id="1850f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-138">MAPI-Id</span></span>                | <span data-ttu-id="1850f-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-139">0x8005</span></span>                                                             |
| <span data-ttu-id="1850f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-140">System-Only</span></span>            | <span data-ttu-id="1850f-141">否</span><span class="sxs-lookup"><span data-stu-id="1850f-141">False</span></span>                                                              |
| <span data-ttu-id="1850f-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-143">對</span><span class="sxs-lookup"><span data-stu-id="1850f-143">True</span></span>                                                               |
| <span data-ttu-id="1850f-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-144">Is Indexed</span></span>             | <span data-ttu-id="1850f-145">否</span><span class="sxs-lookup"><span data-stu-id="1850f-145">False</span></span>                                                              |
| <span data-ttu-id="1850f-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-146">In Global Catalog</span></span>      | <span data-ttu-id="1850f-147">對</span><span class="sxs-lookup"><span data-stu-id="1850f-147">True</span></span>                                                               |
| <span data-ttu-id="1850f-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="1850f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="1850f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="1850f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-152">Search-Flags</span></span>           | <span data-ttu-id="1850f-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="1850f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-154">System-Flags</span></span>           | <span data-ttu-id="1850f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="1850f-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-156">Classes used in</span></span>        | [<span data-ttu-id="1850f-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1850f-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1850f-158">Windows Server 2003</span></span>



| <span data-ttu-id="1850f-159">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-159">Entry</span></span> | <span data-ttu-id="1850f-160">值</span><span class="sxs-lookup"><span data-stu-id="1850f-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850f-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-161">Link-Id</span></span>                | <span data-ttu-id="1850f-162">42</span><span class="sxs-lookup"><span data-stu-id="1850f-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="1850f-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-163">MAPI-Id</span></span>                | <span data-ttu-id="1850f-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1850f-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-165">System-Only</span></span>            | <span data-ttu-id="1850f-166">否</span><span class="sxs-lookup"><span data-stu-id="1850f-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-168">對</span><span class="sxs-lookup"><span data-stu-id="1850f-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-169">Is Indexed</span></span>             | <span data-ttu-id="1850f-170">否</span><span class="sxs-lookup"><span data-stu-id="1850f-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-171">In Global Catalog</span></span>      | <span data-ttu-id="1850f-172">對</span><span class="sxs-lookup"><span data-stu-id="1850f-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1850f-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-177">Search-Flags</span></span>           | <span data-ttu-id="1850f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-179">System-Flags</span></span>           | <span data-ttu-id="1850f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-181">Classes used in</span></span>        | [<span data-ttu-id="1850f-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1850f-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1850f-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1850f-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1850f-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1850f-185">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-185">Entry</span></span> | <span data-ttu-id="1850f-186">值</span><span class="sxs-lookup"><span data-stu-id="1850f-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850f-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-187">Link-Id</span></span>                | <span data-ttu-id="1850f-188">42</span><span class="sxs-lookup"><span data-stu-id="1850f-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="1850f-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-189">MAPI-Id</span></span>                | <span data-ttu-id="1850f-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1850f-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-191">System-Only</span></span>            | <span data-ttu-id="1850f-192">否</span><span class="sxs-lookup"><span data-stu-id="1850f-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-193">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-194">對</span><span class="sxs-lookup"><span data-stu-id="1850f-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-195">Is Indexed</span></span>             | <span data-ttu-id="1850f-196">否</span><span class="sxs-lookup"><span data-stu-id="1850f-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-197">In Global Catalog</span></span>      | <span data-ttu-id="1850f-198">對</span><span class="sxs-lookup"><span data-stu-id="1850f-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1850f-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-203">Search-Flags</span></span>           | <span data-ttu-id="1850f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-205">System-Flags</span></span>           | <span data-ttu-id="1850f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-207">Classes used in</span></span>        | [<span data-ttu-id="1850f-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1850f-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1850f-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1850f-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1850f-210">Windows Server 2008</span></span>



| <span data-ttu-id="1850f-211">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-211">Entry</span></span> | <span data-ttu-id="1850f-212">值</span><span class="sxs-lookup"><span data-stu-id="1850f-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850f-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-213">Link-Id</span></span>                | <span data-ttu-id="1850f-214">42</span><span class="sxs-lookup"><span data-stu-id="1850f-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="1850f-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-215">MAPI-Id</span></span>                | <span data-ttu-id="1850f-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1850f-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-217">System-Only</span></span>            | <span data-ttu-id="1850f-218">否</span><span class="sxs-lookup"><span data-stu-id="1850f-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-219">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-220">對</span><span class="sxs-lookup"><span data-stu-id="1850f-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-221">Is Indexed</span></span>             | <span data-ttu-id="1850f-222">否</span><span class="sxs-lookup"><span data-stu-id="1850f-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-223">In Global Catalog</span></span>      | <span data-ttu-id="1850f-224">對</span><span class="sxs-lookup"><span data-stu-id="1850f-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1850f-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-229">Search-Flags</span></span>           | <span data-ttu-id="1850f-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-231">System-Flags</span></span>           | <span data-ttu-id="1850f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-233">Classes used in</span></span>        | [<span data-ttu-id="1850f-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1850f-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1850f-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1850f-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1850f-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1850f-237">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-237">Entry</span></span> | <span data-ttu-id="1850f-238">值</span><span class="sxs-lookup"><span data-stu-id="1850f-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850f-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-239">Link-Id</span></span>                | <span data-ttu-id="1850f-240">42</span><span class="sxs-lookup"><span data-stu-id="1850f-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="1850f-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-241">MAPI-Id</span></span>                | <span data-ttu-id="1850f-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1850f-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-243">System-Only</span></span>            | <span data-ttu-id="1850f-244">否</span><span class="sxs-lookup"><span data-stu-id="1850f-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-245">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-245">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-246">對</span><span class="sxs-lookup"><span data-stu-id="1850f-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-247">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-247">Is Indexed</span></span>             | <span data-ttu-id="1850f-248">否</span><span class="sxs-lookup"><span data-stu-id="1850f-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-249">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-249">In Global Catalog</span></span>      | <span data-ttu-id="1850f-250">對</span><span class="sxs-lookup"><span data-stu-id="1850f-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-251">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-252">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1850f-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-255">Search-Flags</span></span>           | <span data-ttu-id="1850f-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-257">System-Flags</span></span>           | <span data-ttu-id="1850f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-259">Classes used in</span></span>        | [<span data-ttu-id="1850f-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1850f-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1850f-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1850f-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1850f-262">Windows Server 2012</span></span>



| <span data-ttu-id="1850f-263">進入</span><span class="sxs-lookup"><span data-stu-id="1850f-263">Entry</span></span> | <span data-ttu-id="1850f-264">值</span><span class="sxs-lookup"><span data-stu-id="1850f-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1850f-265">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="1850f-265">Link-Id</span></span>                | <span data-ttu-id="1850f-266">42</span><span class="sxs-lookup"><span data-stu-id="1850f-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="1850f-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1850f-267">MAPI-Id</span></span>                | <span data-ttu-id="1850f-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="1850f-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="1850f-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="1850f-269">System-Only</span></span>            | <span data-ttu-id="1850f-270">否</span><span class="sxs-lookup"><span data-stu-id="1850f-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-271">是-單一值</span><span class="sxs-lookup"><span data-stu-id="1850f-271">Is-Single-Valued</span></span>       | <span data-ttu-id="1850f-272">對</span><span class="sxs-lookup"><span data-stu-id="1850f-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-273">已編制索引</span><span class="sxs-lookup"><span data-stu-id="1850f-273">Is Indexed</span></span>             | <span data-ttu-id="1850f-274">否</span><span class="sxs-lookup"><span data-stu-id="1850f-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="1850f-275">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="1850f-275">In Global Catalog</span></span>      | <span data-ttu-id="1850f-276">對</span><span class="sxs-lookup"><span data-stu-id="1850f-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="1850f-277">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="1850f-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="1850f-278">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="1850f-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="1850f-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1850f-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1850f-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="1850f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-281">Search-Flags</span></span>           | <span data-ttu-id="1850f-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1850f-283">System-Flags</span></span>           | <span data-ttu-id="1850f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1850f-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="1850f-285">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="1850f-285">Classes used in</span></span>        | [<span data-ttu-id="1850f-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="1850f-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="1850f-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="1850f-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





