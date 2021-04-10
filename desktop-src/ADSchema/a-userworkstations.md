---
title: User-Workstations 屬性
description: 包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- User-Workstations 屬性 AD 架構
- userWorkstations 屬性 AD 架構
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844891"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="89427-105">User-Workstations 屬性</span><span class="sxs-lookup"><span data-stu-id="89427-105">User-Workstations attribute</span></span>

<span data-ttu-id="89427-106">包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。</span><span class="sxs-lookup"><span data-stu-id="89427-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="89427-107">每個 NetBIOS 名稱會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="89427-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="89427-108">多個名稱應以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="89427-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="89427-109">此使用者屬性不應再使用。</span><span class="sxs-lookup"><span data-stu-id="89427-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="89427-110">若要管理哪些帳戶可以登入哪些工作站，建議使用「允許本機登入」和「拒絕本機登入」或「允許登入遠端桌面服務」和「拒絕透過遠端桌面服務登入」。</span><span class="sxs-lookup"><span data-stu-id="89427-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="89427-111">進入</span><span class="sxs-lookup"><span data-stu-id="89427-111">Entry</span></span> | <span data-ttu-id="89427-112">值</span><span class="sxs-lookup"><span data-stu-id="89427-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="89427-113">CN</span><span class="sxs-lookup"><span data-stu-id="89427-113">CN</span></span>                | <span data-ttu-id="89427-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="89427-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="89427-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="89427-115">Ldap-Display-Name</span></span> | <span data-ttu-id="89427-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="89427-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="89427-117">大小</span><span class="sxs-lookup"><span data-stu-id="89427-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="89427-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="89427-118">Update Privilege</span></span>  | <span data-ttu-id="89427-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="89427-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="89427-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="89427-120">Update Frequency</span></span>  | <span data-ttu-id="89427-121">當使用者的記錄建立時，以及每次使用者的登入許可權需要變更時。</span><span class="sxs-lookup"><span data-stu-id="89427-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="89427-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="89427-122">Attribute-Id</span></span>      | <span data-ttu-id="89427-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="89427-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="89427-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="89427-124">System-Id-Guid</span></span>    | <span data-ttu-id="89427-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="89427-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="89427-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="89427-126">Syntax</span></span>            | [<span data-ttu-id="89427-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="89427-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="89427-128">實作</span><span class="sxs-lookup"><span data-stu-id="89427-128">Implementations</span></span>

-   [<span data-ttu-id="89427-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="89427-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="89427-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="89427-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="89427-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="89427-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="89427-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="89427-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="89427-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="89427-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="89427-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="89427-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="89427-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89427-135">Windows 2000 Server</span></span>



| <span data-ttu-id="89427-136">進入</span><span class="sxs-lookup"><span data-stu-id="89427-136">Entry</span></span> | <span data-ttu-id="89427-137">值</span><span class="sxs-lookup"><span data-stu-id="89427-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-140">System-Only</span></span>            | <span data-ttu-id="89427-141">否</span><span class="sxs-lookup"><span data-stu-id="89427-141">False</span></span>                             |
| <span data-ttu-id="89427-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-142">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-143">對</span><span class="sxs-lookup"><span data-stu-id="89427-143">True</span></span>                              |
| <span data-ttu-id="89427-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-144">Is Indexed</span></span>             | <span data-ttu-id="89427-145">否</span><span class="sxs-lookup"><span data-stu-id="89427-145">False</span></span>                             |
| <span data-ttu-id="89427-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-146">In Global Catalog</span></span>      | <span data-ttu-id="89427-147">否</span><span class="sxs-lookup"><span data-stu-id="89427-147">False</span></span>                             |
| <span data-ttu-id="89427-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-150">Range-Lower</span></span>            | <span data-ttu-id="89427-151">0</span><span class="sxs-lookup"><span data-stu-id="89427-151">0</span></span>                                 |
| <span data-ttu-id="89427-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-152">Range-Upper</span></span>            | <span data-ttu-id="89427-153">1024</span><span class="sxs-lookup"><span data-stu-id="89427-153">1024</span></span>                              |
| <span data-ttu-id="89427-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-154">Search-Flags</span></span>           | <span data-ttu-id="89427-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-155">0x00000010</span></span>                        |
| <span data-ttu-id="89427-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-156">System-Flags</span></span>           | <span data-ttu-id="89427-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-157">0x00000010</span></span>                        |
| <span data-ttu-id="89427-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-158">Classes used in</span></span>        | [<span data-ttu-id="89427-159">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="89427-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89427-160">Windows Server 2003</span></span>



| <span data-ttu-id="89427-161">進入</span><span class="sxs-lookup"><span data-stu-id="89427-161">Entry</span></span> | <span data-ttu-id="89427-162">值</span><span class="sxs-lookup"><span data-stu-id="89427-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-165">System-Only</span></span>            | <span data-ttu-id="89427-166">否</span><span class="sxs-lookup"><span data-stu-id="89427-166">False</span></span>                             |
| <span data-ttu-id="89427-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-167">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-168">對</span><span class="sxs-lookup"><span data-stu-id="89427-168">True</span></span>                              |
| <span data-ttu-id="89427-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-169">Is Indexed</span></span>             | <span data-ttu-id="89427-170">否</span><span class="sxs-lookup"><span data-stu-id="89427-170">False</span></span>                             |
| <span data-ttu-id="89427-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-171">In Global Catalog</span></span>      | <span data-ttu-id="89427-172">否</span><span class="sxs-lookup"><span data-stu-id="89427-172">False</span></span>                             |
| <span data-ttu-id="89427-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-175">Range-Lower</span></span>            | <span data-ttu-id="89427-176">0</span><span class="sxs-lookup"><span data-stu-id="89427-176">0</span></span>                                 |
| <span data-ttu-id="89427-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-177">Range-Upper</span></span>            | <span data-ttu-id="89427-178">1024</span><span class="sxs-lookup"><span data-stu-id="89427-178">1024</span></span>                              |
| <span data-ttu-id="89427-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-179">Search-Flags</span></span>           | <span data-ttu-id="89427-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-180">0x00000010</span></span>                        |
| <span data-ttu-id="89427-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-181">System-Flags</span></span>           | <span data-ttu-id="89427-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-182">0x00000010</span></span>                        |
| <span data-ttu-id="89427-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-183">Classes used in</span></span>        | [<span data-ttu-id="89427-184">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="89427-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="89427-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="89427-186">進入</span><span class="sxs-lookup"><span data-stu-id="89427-186">Entry</span></span> | <span data-ttu-id="89427-187">值</span><span class="sxs-lookup"><span data-stu-id="89427-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-190">System-Only</span></span>            | <span data-ttu-id="89427-191">否</span><span class="sxs-lookup"><span data-stu-id="89427-191">False</span></span>                             |
| <span data-ttu-id="89427-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-192">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-193">對</span><span class="sxs-lookup"><span data-stu-id="89427-193">True</span></span>                              |
| <span data-ttu-id="89427-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-194">Is Indexed</span></span>             | <span data-ttu-id="89427-195">否</span><span class="sxs-lookup"><span data-stu-id="89427-195">False</span></span>                             |
| <span data-ttu-id="89427-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-196">In Global Catalog</span></span>      | <span data-ttu-id="89427-197">否</span><span class="sxs-lookup"><span data-stu-id="89427-197">False</span></span>                             |
| <span data-ttu-id="89427-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-200">Range-Lower</span></span>            | <span data-ttu-id="89427-201">0</span><span class="sxs-lookup"><span data-stu-id="89427-201">0</span></span>                                 |
| <span data-ttu-id="89427-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-202">Range-Upper</span></span>            | <span data-ttu-id="89427-203">1024</span><span class="sxs-lookup"><span data-stu-id="89427-203">1024</span></span>                              |
| <span data-ttu-id="89427-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-204">Search-Flags</span></span>           | <span data-ttu-id="89427-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-205">0x00000010</span></span>                        |
| <span data-ttu-id="89427-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-206">System-Flags</span></span>           | <span data-ttu-id="89427-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-207">0x00000010</span></span>                        |
| <span data-ttu-id="89427-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-208">Classes used in</span></span>        | [<span data-ttu-id="89427-209">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="89427-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89427-210">Windows Server 2008</span></span>



| <span data-ttu-id="89427-211">進入</span><span class="sxs-lookup"><span data-stu-id="89427-211">Entry</span></span> | <span data-ttu-id="89427-212">值</span><span class="sxs-lookup"><span data-stu-id="89427-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-215">System-Only</span></span>            | <span data-ttu-id="89427-216">否</span><span class="sxs-lookup"><span data-stu-id="89427-216">False</span></span>                             |
| <span data-ttu-id="89427-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-217">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-218">對</span><span class="sxs-lookup"><span data-stu-id="89427-218">True</span></span>                              |
| <span data-ttu-id="89427-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-219">Is Indexed</span></span>             | <span data-ttu-id="89427-220">否</span><span class="sxs-lookup"><span data-stu-id="89427-220">False</span></span>                             |
| <span data-ttu-id="89427-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-221">In Global Catalog</span></span>      | <span data-ttu-id="89427-222">否</span><span class="sxs-lookup"><span data-stu-id="89427-222">False</span></span>                             |
| <span data-ttu-id="89427-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-225">Range-Lower</span></span>            | <span data-ttu-id="89427-226">0</span><span class="sxs-lookup"><span data-stu-id="89427-226">0</span></span>                                 |
| <span data-ttu-id="89427-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-227">Range-Upper</span></span>            | <span data-ttu-id="89427-228">1024</span><span class="sxs-lookup"><span data-stu-id="89427-228">1024</span></span>                              |
| <span data-ttu-id="89427-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-229">Search-Flags</span></span>           | <span data-ttu-id="89427-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-230">0x00000010</span></span>                        |
| <span data-ttu-id="89427-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-231">System-Flags</span></span>           | <span data-ttu-id="89427-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-232">0x00000010</span></span>                        |
| <span data-ttu-id="89427-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-233">Classes used in</span></span>        | [<span data-ttu-id="89427-234">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="89427-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89427-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="89427-236">進入</span><span class="sxs-lookup"><span data-stu-id="89427-236">Entry</span></span> | <span data-ttu-id="89427-237">值</span><span class="sxs-lookup"><span data-stu-id="89427-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-240">System-Only</span></span>            | <span data-ttu-id="89427-241">否</span><span class="sxs-lookup"><span data-stu-id="89427-241">False</span></span>                             |
| <span data-ttu-id="89427-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-242">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-243">對</span><span class="sxs-lookup"><span data-stu-id="89427-243">True</span></span>                              |
| <span data-ttu-id="89427-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-244">Is Indexed</span></span>             | <span data-ttu-id="89427-245">否</span><span class="sxs-lookup"><span data-stu-id="89427-245">False</span></span>                             |
| <span data-ttu-id="89427-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-246">In Global Catalog</span></span>      | <span data-ttu-id="89427-247">否</span><span class="sxs-lookup"><span data-stu-id="89427-247">False</span></span>                             |
| <span data-ttu-id="89427-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-250">Range-Lower</span></span>            | <span data-ttu-id="89427-251">0</span><span class="sxs-lookup"><span data-stu-id="89427-251">0</span></span>                                 |
| <span data-ttu-id="89427-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-252">Range-Upper</span></span>            | <span data-ttu-id="89427-253">1024</span><span class="sxs-lookup"><span data-stu-id="89427-253">1024</span></span>                              |
| <span data-ttu-id="89427-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-254">Search-Flags</span></span>           | <span data-ttu-id="89427-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-255">0x00000010</span></span>                        |
| <span data-ttu-id="89427-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-256">System-Flags</span></span>           | <span data-ttu-id="89427-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-257">0x00000010</span></span>                        |
| <span data-ttu-id="89427-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-258">Classes used in</span></span>        | [<span data-ttu-id="89427-259">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="89427-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89427-260">Windows Server 2012</span></span>



| <span data-ttu-id="89427-261">進入</span><span class="sxs-lookup"><span data-stu-id="89427-261">Entry</span></span> | <span data-ttu-id="89427-262">值</span><span class="sxs-lookup"><span data-stu-id="89427-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="89427-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="89427-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="89427-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="89427-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="89427-265">System-Only</span></span>            | <span data-ttu-id="89427-266">否</span><span class="sxs-lookup"><span data-stu-id="89427-266">False</span></span>                             |
| <span data-ttu-id="89427-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="89427-267">Is-Single-Valued</span></span>       | <span data-ttu-id="89427-268">對</span><span class="sxs-lookup"><span data-stu-id="89427-268">True</span></span>                              |
| <span data-ttu-id="89427-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="89427-269">Is Indexed</span></span>             | <span data-ttu-id="89427-270">否</span><span class="sxs-lookup"><span data-stu-id="89427-270">False</span></span>                             |
| <span data-ttu-id="89427-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="89427-271">In Global Catalog</span></span>      | <span data-ttu-id="89427-272">否</span><span class="sxs-lookup"><span data-stu-id="89427-272">False</span></span>                             |
| <span data-ttu-id="89427-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="89427-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="89427-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="89427-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="89427-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="89427-275">Range-Lower</span></span>            | <span data-ttu-id="89427-276">0</span><span class="sxs-lookup"><span data-stu-id="89427-276">0</span></span>                                 |
| <span data-ttu-id="89427-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="89427-277">Range-Upper</span></span>            | <span data-ttu-id="89427-278">1024</span><span class="sxs-lookup"><span data-stu-id="89427-278">1024</span></span>                              |
| <span data-ttu-id="89427-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-279">Search-Flags</span></span>           | <span data-ttu-id="89427-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-280">0x00000010</span></span>                        |
| <span data-ttu-id="89427-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="89427-281">System-Flags</span></span>           | <span data-ttu-id="89427-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89427-282">0x00000010</span></span>                        |
| <span data-ttu-id="89427-283">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="89427-283">Classes used in</span></span>        | [<span data-ttu-id="89427-284">**User**</span><span class="sxs-lookup"><span data-stu-id="89427-284">**User**</span></span>](c-user.md)<br/> |



 

 





