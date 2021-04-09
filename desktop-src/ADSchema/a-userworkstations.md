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
# <a name="user-workstations-attribute"></a><span data-ttu-id="61177-105">User-Workstations 屬性</span><span class="sxs-lookup"><span data-stu-id="61177-105">User-Workstations attribute</span></span>

<span data-ttu-id="61177-106">包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。</span><span class="sxs-lookup"><span data-stu-id="61177-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="61177-107">每個 NetBIOS 名稱會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="61177-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="61177-108">多個名稱應以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="61177-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="61177-109">此使用者屬性不應再使用。</span><span class="sxs-lookup"><span data-stu-id="61177-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="61177-110">若要管理哪些帳戶可以登入哪些工作站，建議使用「允許本機登入」和「拒絕本機登入」或「允許登入遠端桌面服務」和「拒絕透過遠端桌面服務登入」。</span><span class="sxs-lookup"><span data-stu-id="61177-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="61177-111">進入</span><span class="sxs-lookup"><span data-stu-id="61177-111">Entry</span></span> | <span data-ttu-id="61177-112">值</span><span class="sxs-lookup"><span data-stu-id="61177-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="61177-113">CN</span><span class="sxs-lookup"><span data-stu-id="61177-113">CN</span></span>                | <span data-ttu-id="61177-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="61177-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="61177-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="61177-115">Ldap-Display-Name</span></span> | <span data-ttu-id="61177-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="61177-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="61177-117">大小</span><span class="sxs-lookup"><span data-stu-id="61177-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="61177-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="61177-118">Update Privilege</span></span>  | <span data-ttu-id="61177-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="61177-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="61177-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="61177-120">Update Frequency</span></span>  | <span data-ttu-id="61177-121">當使用者的記錄建立時，以及每次使用者的登入許可權需要變更時。</span><span class="sxs-lookup"><span data-stu-id="61177-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="61177-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61177-122">Attribute-Id</span></span>      | <span data-ttu-id="61177-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="61177-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="61177-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="61177-124">System-Id-Guid</span></span>    | <span data-ttu-id="61177-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="61177-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="61177-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="61177-126">Syntax</span></span>            | [<span data-ttu-id="61177-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="61177-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="61177-128">實作</span><span class="sxs-lookup"><span data-stu-id="61177-128">Implementations</span></span>

-   [<span data-ttu-id="61177-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61177-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61177-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61177-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61177-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61177-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61177-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61177-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61177-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61177-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61177-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61177-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61177-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61177-135">Windows 2000 Server</span></span>



| <span data-ttu-id="61177-136">進入</span><span class="sxs-lookup"><span data-stu-id="61177-136">Entry</span></span> | <span data-ttu-id="61177-137">值</span><span class="sxs-lookup"><span data-stu-id="61177-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-140">System-Only</span></span>            | <span data-ttu-id="61177-141">否</span><span class="sxs-lookup"><span data-stu-id="61177-141">False</span></span>                             |
| <span data-ttu-id="61177-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-142">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-143">對</span><span class="sxs-lookup"><span data-stu-id="61177-143">True</span></span>                              |
| <span data-ttu-id="61177-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-144">Is Indexed</span></span>             | <span data-ttu-id="61177-145">否</span><span class="sxs-lookup"><span data-stu-id="61177-145">False</span></span>                             |
| <span data-ttu-id="61177-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-146">In Global Catalog</span></span>      | <span data-ttu-id="61177-147">否</span><span class="sxs-lookup"><span data-stu-id="61177-147">False</span></span>                             |
| <span data-ttu-id="61177-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-150">Range-Lower</span></span>            | <span data-ttu-id="61177-151">0</span><span class="sxs-lookup"><span data-stu-id="61177-151">0</span></span>                                 |
| <span data-ttu-id="61177-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-152">Range-Upper</span></span>            | <span data-ttu-id="61177-153">1024</span><span class="sxs-lookup"><span data-stu-id="61177-153">1024</span></span>                              |
| <span data-ttu-id="61177-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-154">Search-Flags</span></span>           | <span data-ttu-id="61177-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-155">0x00000010</span></span>                        |
| <span data-ttu-id="61177-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-156">System-Flags</span></span>           | <span data-ttu-id="61177-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-157">0x00000010</span></span>                        |
| <span data-ttu-id="61177-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-158">Classes used in</span></span>        | [<span data-ttu-id="61177-159">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61177-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61177-160">Windows Server 2003</span></span>



| <span data-ttu-id="61177-161">進入</span><span class="sxs-lookup"><span data-stu-id="61177-161">Entry</span></span> | <span data-ttu-id="61177-162">值</span><span class="sxs-lookup"><span data-stu-id="61177-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-165">System-Only</span></span>            | <span data-ttu-id="61177-166">否</span><span class="sxs-lookup"><span data-stu-id="61177-166">False</span></span>                             |
| <span data-ttu-id="61177-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-167">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-168">對</span><span class="sxs-lookup"><span data-stu-id="61177-168">True</span></span>                              |
| <span data-ttu-id="61177-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-169">Is Indexed</span></span>             | <span data-ttu-id="61177-170">否</span><span class="sxs-lookup"><span data-stu-id="61177-170">False</span></span>                             |
| <span data-ttu-id="61177-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-171">In Global Catalog</span></span>      | <span data-ttu-id="61177-172">否</span><span class="sxs-lookup"><span data-stu-id="61177-172">False</span></span>                             |
| <span data-ttu-id="61177-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-175">Range-Lower</span></span>            | <span data-ttu-id="61177-176">0</span><span class="sxs-lookup"><span data-stu-id="61177-176">0</span></span>                                 |
| <span data-ttu-id="61177-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-177">Range-Upper</span></span>            | <span data-ttu-id="61177-178">1024</span><span class="sxs-lookup"><span data-stu-id="61177-178">1024</span></span>                              |
| <span data-ttu-id="61177-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-179">Search-Flags</span></span>           | <span data-ttu-id="61177-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-180">0x00000010</span></span>                        |
| <span data-ttu-id="61177-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-181">System-Flags</span></span>           | <span data-ttu-id="61177-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-182">0x00000010</span></span>                        |
| <span data-ttu-id="61177-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-183">Classes used in</span></span>        | [<span data-ttu-id="61177-184">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61177-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61177-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61177-186">進入</span><span class="sxs-lookup"><span data-stu-id="61177-186">Entry</span></span> | <span data-ttu-id="61177-187">值</span><span class="sxs-lookup"><span data-stu-id="61177-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-190">System-Only</span></span>            | <span data-ttu-id="61177-191">否</span><span class="sxs-lookup"><span data-stu-id="61177-191">False</span></span>                             |
| <span data-ttu-id="61177-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-192">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-193">對</span><span class="sxs-lookup"><span data-stu-id="61177-193">True</span></span>                              |
| <span data-ttu-id="61177-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-194">Is Indexed</span></span>             | <span data-ttu-id="61177-195">否</span><span class="sxs-lookup"><span data-stu-id="61177-195">False</span></span>                             |
| <span data-ttu-id="61177-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-196">In Global Catalog</span></span>      | <span data-ttu-id="61177-197">否</span><span class="sxs-lookup"><span data-stu-id="61177-197">False</span></span>                             |
| <span data-ttu-id="61177-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-200">Range-Lower</span></span>            | <span data-ttu-id="61177-201">0</span><span class="sxs-lookup"><span data-stu-id="61177-201">0</span></span>                                 |
| <span data-ttu-id="61177-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-202">Range-Upper</span></span>            | <span data-ttu-id="61177-203">1024</span><span class="sxs-lookup"><span data-stu-id="61177-203">1024</span></span>                              |
| <span data-ttu-id="61177-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-204">Search-Flags</span></span>           | <span data-ttu-id="61177-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-205">0x00000010</span></span>                        |
| <span data-ttu-id="61177-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-206">System-Flags</span></span>           | <span data-ttu-id="61177-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-207">0x00000010</span></span>                        |
| <span data-ttu-id="61177-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-208">Classes used in</span></span>        | [<span data-ttu-id="61177-209">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61177-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61177-210">Windows Server 2008</span></span>



| <span data-ttu-id="61177-211">進入</span><span class="sxs-lookup"><span data-stu-id="61177-211">Entry</span></span> | <span data-ttu-id="61177-212">值</span><span class="sxs-lookup"><span data-stu-id="61177-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-215">System-Only</span></span>            | <span data-ttu-id="61177-216">否</span><span class="sxs-lookup"><span data-stu-id="61177-216">False</span></span>                             |
| <span data-ttu-id="61177-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-217">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-218">對</span><span class="sxs-lookup"><span data-stu-id="61177-218">True</span></span>                              |
| <span data-ttu-id="61177-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-219">Is Indexed</span></span>             | <span data-ttu-id="61177-220">否</span><span class="sxs-lookup"><span data-stu-id="61177-220">False</span></span>                             |
| <span data-ttu-id="61177-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-221">In Global Catalog</span></span>      | <span data-ttu-id="61177-222">否</span><span class="sxs-lookup"><span data-stu-id="61177-222">False</span></span>                             |
| <span data-ttu-id="61177-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-225">Range-Lower</span></span>            | <span data-ttu-id="61177-226">0</span><span class="sxs-lookup"><span data-stu-id="61177-226">0</span></span>                                 |
| <span data-ttu-id="61177-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-227">Range-Upper</span></span>            | <span data-ttu-id="61177-228">1024</span><span class="sxs-lookup"><span data-stu-id="61177-228">1024</span></span>                              |
| <span data-ttu-id="61177-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-229">Search-Flags</span></span>           | <span data-ttu-id="61177-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-230">0x00000010</span></span>                        |
| <span data-ttu-id="61177-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-231">System-Flags</span></span>           | <span data-ttu-id="61177-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-232">0x00000010</span></span>                        |
| <span data-ttu-id="61177-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-233">Classes used in</span></span>        | [<span data-ttu-id="61177-234">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61177-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61177-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61177-236">進入</span><span class="sxs-lookup"><span data-stu-id="61177-236">Entry</span></span> | <span data-ttu-id="61177-237">值</span><span class="sxs-lookup"><span data-stu-id="61177-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-240">System-Only</span></span>            | <span data-ttu-id="61177-241">否</span><span class="sxs-lookup"><span data-stu-id="61177-241">False</span></span>                             |
| <span data-ttu-id="61177-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-242">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-243">對</span><span class="sxs-lookup"><span data-stu-id="61177-243">True</span></span>                              |
| <span data-ttu-id="61177-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-244">Is Indexed</span></span>             | <span data-ttu-id="61177-245">否</span><span class="sxs-lookup"><span data-stu-id="61177-245">False</span></span>                             |
| <span data-ttu-id="61177-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-246">In Global Catalog</span></span>      | <span data-ttu-id="61177-247">否</span><span class="sxs-lookup"><span data-stu-id="61177-247">False</span></span>                             |
| <span data-ttu-id="61177-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-250">Range-Lower</span></span>            | <span data-ttu-id="61177-251">0</span><span class="sxs-lookup"><span data-stu-id="61177-251">0</span></span>                                 |
| <span data-ttu-id="61177-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-252">Range-Upper</span></span>            | <span data-ttu-id="61177-253">1024</span><span class="sxs-lookup"><span data-stu-id="61177-253">1024</span></span>                              |
| <span data-ttu-id="61177-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-254">Search-Flags</span></span>           | <span data-ttu-id="61177-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-255">0x00000010</span></span>                        |
| <span data-ttu-id="61177-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-256">System-Flags</span></span>           | <span data-ttu-id="61177-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-257">0x00000010</span></span>                        |
| <span data-ttu-id="61177-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-258">Classes used in</span></span>        | [<span data-ttu-id="61177-259">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61177-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61177-260">Windows Server 2012</span></span>



| <span data-ttu-id="61177-261">進入</span><span class="sxs-lookup"><span data-stu-id="61177-261">Entry</span></span> | <span data-ttu-id="61177-262">值</span><span class="sxs-lookup"><span data-stu-id="61177-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="61177-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="61177-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61177-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="61177-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="61177-265">System-Only</span></span>            | <span data-ttu-id="61177-266">否</span><span class="sxs-lookup"><span data-stu-id="61177-266">False</span></span>                             |
| <span data-ttu-id="61177-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="61177-267">Is-Single-Valued</span></span>       | <span data-ttu-id="61177-268">對</span><span class="sxs-lookup"><span data-stu-id="61177-268">True</span></span>                              |
| <span data-ttu-id="61177-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="61177-269">Is Indexed</span></span>             | <span data-ttu-id="61177-270">否</span><span class="sxs-lookup"><span data-stu-id="61177-270">False</span></span>                             |
| <span data-ttu-id="61177-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="61177-271">In Global Catalog</span></span>      | <span data-ttu-id="61177-272">否</span><span class="sxs-lookup"><span data-stu-id="61177-272">False</span></span>                             |
| <span data-ttu-id="61177-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="61177-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="61177-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="61177-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="61177-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61177-275">Range-Lower</span></span>            | <span data-ttu-id="61177-276">0</span><span class="sxs-lookup"><span data-stu-id="61177-276">0</span></span>                                 |
| <span data-ttu-id="61177-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61177-277">Range-Upper</span></span>            | <span data-ttu-id="61177-278">1024</span><span class="sxs-lookup"><span data-stu-id="61177-278">1024</span></span>                              |
| <span data-ttu-id="61177-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-279">Search-Flags</span></span>           | <span data-ttu-id="61177-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-280">0x00000010</span></span>                        |
| <span data-ttu-id="61177-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61177-281">System-Flags</span></span>           | <span data-ttu-id="61177-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61177-282">0x00000010</span></span>                        |
| <span data-ttu-id="61177-283">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="61177-283">Classes used in</span></span>        | [<span data-ttu-id="61177-284">**User**</span><span class="sxs-lookup"><span data-stu-id="61177-284">**User**</span></span>](c-user.md)<br/> |



 

 





