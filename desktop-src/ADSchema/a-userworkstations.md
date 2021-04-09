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
# <a name="user-workstations-attribute"></a><span data-ttu-id="75a79-105">User-Workstations 屬性</span><span class="sxs-lookup"><span data-stu-id="75a79-105">User-Workstations attribute</span></span>

<span data-ttu-id="75a79-106">包含執行 Windows NT 工作站或 Windows 2000 Professional 的電腦之 NetBIOS 或 DNS 名稱，使用者可從中登入。</span><span class="sxs-lookup"><span data-stu-id="75a79-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="75a79-107">每個 NetBIOS 名稱會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="75a79-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="75a79-108">多個名稱應以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="75a79-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="75a79-109">此使用者屬性不應再使用。</span><span class="sxs-lookup"><span data-stu-id="75a79-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="75a79-110">若要管理哪些帳戶可以登入哪些工作站，建議使用「允許本機登入」和「拒絕本機登入」或「允許登入遠端桌面服務」和「拒絕透過遠端桌面服務登入」。</span><span class="sxs-lookup"><span data-stu-id="75a79-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="75a79-111">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-111">Entry</span></span> | <span data-ttu-id="75a79-112">值</span><span class="sxs-lookup"><span data-stu-id="75a79-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a79-113">CN</span><span class="sxs-lookup"><span data-stu-id="75a79-113">CN</span></span>                | <span data-ttu-id="75a79-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="75a79-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="75a79-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="75a79-115">Ldap-Display-Name</span></span> | <span data-ttu-id="75a79-116">userWorkstations</span><span class="sxs-lookup"><span data-stu-id="75a79-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="75a79-117">大小</span><span class="sxs-lookup"><span data-stu-id="75a79-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="75a79-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="75a79-118">Update Privilege</span></span>  | <span data-ttu-id="75a79-119">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="75a79-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="75a79-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="75a79-120">Update Frequency</span></span>  | <span data-ttu-id="75a79-121">當使用者的記錄建立時，以及每次使用者的登入許可權需要變更時。</span><span class="sxs-lookup"><span data-stu-id="75a79-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="75a79-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-122">Attribute-Id</span></span>      | <span data-ttu-id="75a79-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="75a79-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="75a79-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="75a79-124">System-Id-Guid</span></span>    | <span data-ttu-id="75a79-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="75a79-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="75a79-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="75a79-126">Syntax</span></span>            | [<span data-ttu-id="75a79-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="75a79-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="75a79-128">實作</span><span class="sxs-lookup"><span data-stu-id="75a79-128">Implementations</span></span>

-   [<span data-ttu-id="75a79-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75a79-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75a79-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75a79-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75a79-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75a79-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75a79-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75a79-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75a79-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75a79-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75a79-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75a79-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75a79-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75a79-135">Windows 2000 Server</span></span>



| <span data-ttu-id="75a79-136">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-136">Entry</span></span> | <span data-ttu-id="75a79-137">值</span><span class="sxs-lookup"><span data-stu-id="75a79-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-140">System-Only</span></span>            | <span data-ttu-id="75a79-141">否</span><span class="sxs-lookup"><span data-stu-id="75a79-141">False</span></span>                             |
| <span data-ttu-id="75a79-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-142">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-143">對</span><span class="sxs-lookup"><span data-stu-id="75a79-143">True</span></span>                              |
| <span data-ttu-id="75a79-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-144">Is Indexed</span></span>             | <span data-ttu-id="75a79-145">否</span><span class="sxs-lookup"><span data-stu-id="75a79-145">False</span></span>                             |
| <span data-ttu-id="75a79-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-146">In Global Catalog</span></span>      | <span data-ttu-id="75a79-147">否</span><span class="sxs-lookup"><span data-stu-id="75a79-147">False</span></span>                             |
| <span data-ttu-id="75a79-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-150">Range-Lower</span></span>            | <span data-ttu-id="75a79-151">0</span><span class="sxs-lookup"><span data-stu-id="75a79-151">0</span></span>                                 |
| <span data-ttu-id="75a79-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-152">Range-Upper</span></span>            | <span data-ttu-id="75a79-153">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-153">1024</span></span>                              |
| <span data-ttu-id="75a79-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-154">Search-Flags</span></span>           | <span data-ttu-id="75a79-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-155">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-156">System-Flags</span></span>           | <span data-ttu-id="75a79-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-157">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-158">Classes used in</span></span>        | [<span data-ttu-id="75a79-159">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75a79-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75a79-160">Windows Server 2003</span></span>



| <span data-ttu-id="75a79-161">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-161">Entry</span></span> | <span data-ttu-id="75a79-162">值</span><span class="sxs-lookup"><span data-stu-id="75a79-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-165">System-Only</span></span>            | <span data-ttu-id="75a79-166">否</span><span class="sxs-lookup"><span data-stu-id="75a79-166">False</span></span>                             |
| <span data-ttu-id="75a79-167">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-167">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-168">對</span><span class="sxs-lookup"><span data-stu-id="75a79-168">True</span></span>                              |
| <span data-ttu-id="75a79-169">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-169">Is Indexed</span></span>             | <span data-ttu-id="75a79-170">否</span><span class="sxs-lookup"><span data-stu-id="75a79-170">False</span></span>                             |
| <span data-ttu-id="75a79-171">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-171">In Global Catalog</span></span>      | <span data-ttu-id="75a79-172">否</span><span class="sxs-lookup"><span data-stu-id="75a79-172">False</span></span>                             |
| <span data-ttu-id="75a79-173">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-174">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-175">Range-Lower</span></span>            | <span data-ttu-id="75a79-176">0</span><span class="sxs-lookup"><span data-stu-id="75a79-176">0</span></span>                                 |
| <span data-ttu-id="75a79-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-177">Range-Upper</span></span>            | <span data-ttu-id="75a79-178">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-178">1024</span></span>                              |
| <span data-ttu-id="75a79-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-179">Search-Flags</span></span>           | <span data-ttu-id="75a79-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-180">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-181">System-Flags</span></span>           | <span data-ttu-id="75a79-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-182">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-183">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-183">Classes used in</span></span>        | [<span data-ttu-id="75a79-184">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75a79-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75a79-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75a79-186">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-186">Entry</span></span> | <span data-ttu-id="75a79-187">值</span><span class="sxs-lookup"><span data-stu-id="75a79-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-188">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-190">System-Only</span></span>            | <span data-ttu-id="75a79-191">否</span><span class="sxs-lookup"><span data-stu-id="75a79-191">False</span></span>                             |
| <span data-ttu-id="75a79-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-192">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-193">對</span><span class="sxs-lookup"><span data-stu-id="75a79-193">True</span></span>                              |
| <span data-ttu-id="75a79-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-194">Is Indexed</span></span>             | <span data-ttu-id="75a79-195">否</span><span class="sxs-lookup"><span data-stu-id="75a79-195">False</span></span>                             |
| <span data-ttu-id="75a79-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-196">In Global Catalog</span></span>      | <span data-ttu-id="75a79-197">否</span><span class="sxs-lookup"><span data-stu-id="75a79-197">False</span></span>                             |
| <span data-ttu-id="75a79-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-200">Range-Lower</span></span>            | <span data-ttu-id="75a79-201">0</span><span class="sxs-lookup"><span data-stu-id="75a79-201">0</span></span>                                 |
| <span data-ttu-id="75a79-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-202">Range-Upper</span></span>            | <span data-ttu-id="75a79-203">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-203">1024</span></span>                              |
| <span data-ttu-id="75a79-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-204">Search-Flags</span></span>           | <span data-ttu-id="75a79-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-205">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-206">System-Flags</span></span>           | <span data-ttu-id="75a79-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-207">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-208">Classes used in</span></span>        | [<span data-ttu-id="75a79-209">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75a79-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75a79-210">Windows Server 2008</span></span>



| <span data-ttu-id="75a79-211">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-211">Entry</span></span> | <span data-ttu-id="75a79-212">值</span><span class="sxs-lookup"><span data-stu-id="75a79-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-213">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-215">System-Only</span></span>            | <span data-ttu-id="75a79-216">否</span><span class="sxs-lookup"><span data-stu-id="75a79-216">False</span></span>                             |
| <span data-ttu-id="75a79-217">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-217">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-218">對</span><span class="sxs-lookup"><span data-stu-id="75a79-218">True</span></span>                              |
| <span data-ttu-id="75a79-219">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-219">Is Indexed</span></span>             | <span data-ttu-id="75a79-220">否</span><span class="sxs-lookup"><span data-stu-id="75a79-220">False</span></span>                             |
| <span data-ttu-id="75a79-221">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-221">In Global Catalog</span></span>      | <span data-ttu-id="75a79-222">否</span><span class="sxs-lookup"><span data-stu-id="75a79-222">False</span></span>                             |
| <span data-ttu-id="75a79-223">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-224">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-225">Range-Lower</span></span>            | <span data-ttu-id="75a79-226">0</span><span class="sxs-lookup"><span data-stu-id="75a79-226">0</span></span>                                 |
| <span data-ttu-id="75a79-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-227">Range-Upper</span></span>            | <span data-ttu-id="75a79-228">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-228">1024</span></span>                              |
| <span data-ttu-id="75a79-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-229">Search-Flags</span></span>           | <span data-ttu-id="75a79-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-230">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-231">System-Flags</span></span>           | <span data-ttu-id="75a79-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-232">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-233">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-233">Classes used in</span></span>        | [<span data-ttu-id="75a79-234">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75a79-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75a79-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75a79-236">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-236">Entry</span></span> | <span data-ttu-id="75a79-237">值</span><span class="sxs-lookup"><span data-stu-id="75a79-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-238">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-240">System-Only</span></span>            | <span data-ttu-id="75a79-241">否</span><span class="sxs-lookup"><span data-stu-id="75a79-241">False</span></span>                             |
| <span data-ttu-id="75a79-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-242">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-243">對</span><span class="sxs-lookup"><span data-stu-id="75a79-243">True</span></span>                              |
| <span data-ttu-id="75a79-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-244">Is Indexed</span></span>             | <span data-ttu-id="75a79-245">否</span><span class="sxs-lookup"><span data-stu-id="75a79-245">False</span></span>                             |
| <span data-ttu-id="75a79-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-246">In Global Catalog</span></span>      | <span data-ttu-id="75a79-247">否</span><span class="sxs-lookup"><span data-stu-id="75a79-247">False</span></span>                             |
| <span data-ttu-id="75a79-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-250">Range-Lower</span></span>            | <span data-ttu-id="75a79-251">0</span><span class="sxs-lookup"><span data-stu-id="75a79-251">0</span></span>                                 |
| <span data-ttu-id="75a79-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-252">Range-Upper</span></span>            | <span data-ttu-id="75a79-253">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-253">1024</span></span>                              |
| <span data-ttu-id="75a79-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-254">Search-Flags</span></span>           | <span data-ttu-id="75a79-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-255">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-256">System-Flags</span></span>           | <span data-ttu-id="75a79-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-257">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-258">Classes used in</span></span>        | [<span data-ttu-id="75a79-259">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75a79-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75a79-260">Windows Server 2012</span></span>



| <span data-ttu-id="75a79-261">進入</span><span class="sxs-lookup"><span data-stu-id="75a79-261">Entry</span></span> | <span data-ttu-id="75a79-262">值</span><span class="sxs-lookup"><span data-stu-id="75a79-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="75a79-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75a79-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75a79-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="75a79-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="75a79-265">System-Only</span></span>            | <span data-ttu-id="75a79-266">否</span><span class="sxs-lookup"><span data-stu-id="75a79-266">False</span></span>                             |
| <span data-ttu-id="75a79-267">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75a79-267">Is-Single-Valued</span></span>       | <span data-ttu-id="75a79-268">對</span><span class="sxs-lookup"><span data-stu-id="75a79-268">True</span></span>                              |
| <span data-ttu-id="75a79-269">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75a79-269">Is Indexed</span></span>             | <span data-ttu-id="75a79-270">否</span><span class="sxs-lookup"><span data-stu-id="75a79-270">False</span></span>                             |
| <span data-ttu-id="75a79-271">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75a79-271">In Global Catalog</span></span>      | <span data-ttu-id="75a79-272">否</span><span class="sxs-lookup"><span data-stu-id="75a79-272">False</span></span>                             |
| <span data-ttu-id="75a79-273">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75a79-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="75a79-274">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75a79-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="75a79-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75a79-275">Range-Lower</span></span>            | <span data-ttu-id="75a79-276">0</span><span class="sxs-lookup"><span data-stu-id="75a79-276">0</span></span>                                 |
| <span data-ttu-id="75a79-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75a79-277">Range-Upper</span></span>            | <span data-ttu-id="75a79-278">1024</span><span class="sxs-lookup"><span data-stu-id="75a79-278">1024</span></span>                              |
| <span data-ttu-id="75a79-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-279">Search-Flags</span></span>           | <span data-ttu-id="75a79-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-280">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75a79-281">System-Flags</span></span>           | <span data-ttu-id="75a79-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75a79-282">0x00000010</span></span>                        |
| <span data-ttu-id="75a79-283">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75a79-283">Classes used in</span></span>        | [<span data-ttu-id="75a79-284">**User**</span><span class="sxs-lookup"><span data-stu-id="75a79-284">**User**</span></span>](c-user.md)<br/> |



 

 





