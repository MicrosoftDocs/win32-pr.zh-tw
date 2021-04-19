---
title: Netboot----File-Path 屬性
description: 這個屬性會指定回應用戶端的伺服器。 從 Windows Server 2003 作業系統開始，它可能會指出用戶端取得的 Startrom.com。
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Netboot---File-Path attribute AD Schema
- netbootMachineFilePath 屬性 AD 架構
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973101"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="6cf40-106">Netboot----File-Path 屬性</span><span class="sxs-lookup"><span data-stu-id="6cf40-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="6cf40-107">這個屬性會指定回應用戶端的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6cf40-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="6cf40-108">從 Windows Server 2003 作業系統開始，它可能會指出用戶端取得的 Startrom.com。</span><span class="sxs-lookup"><span data-stu-id="6cf40-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="6cf40-109">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-109">Entry</span></span> | <span data-ttu-id="6cf40-110">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6cf40-111">CN</span><span class="sxs-lookup"><span data-stu-id="6cf40-111">CN</span></span>                | <span data-ttu-id="6cf40-112">Netboot-電腦-檔案-路徑</span><span class="sxs-lookup"><span data-stu-id="6cf40-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="6cf40-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6cf40-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6cf40-114">netbootMachineFilePath</span><span class="sxs-lookup"><span data-stu-id="6cf40-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="6cf40-115">大小</span><span class="sxs-lookup"><span data-stu-id="6cf40-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6cf40-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6cf40-116">Update Privilege</span></span>  | <span data-ttu-id="6cf40-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6cf40-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="6cf40-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6cf40-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6cf40-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-119">Attribute-Id</span></span>      | <span data-ttu-id="6cf40-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="6cf40-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="6cf40-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6cf40-121">System-Id-Guid</span></span>    | <span data-ttu-id="6cf40-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="6cf40-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="6cf40-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cf40-123">Syntax</span></span>            | [<span data-ttu-id="6cf40-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6cf40-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6cf40-125">實作</span><span class="sxs-lookup"><span data-stu-id="6cf40-125">Implementations</span></span>

-   [<span data-ttu-id="6cf40-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6cf40-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6cf40-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6cf40-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6cf40-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6cf40-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6cf40-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6cf40-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6cf40-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6cf40-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6cf40-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6cf40-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6cf40-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6cf40-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6cf40-133">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-133">Entry</span></span> | <span data-ttu-id="6cf40-134">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-137">System-Only</span></span>            | <span data-ttu-id="6cf40-138">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-138">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-140">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-140">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-141">Is Indexed</span></span>             | <span data-ttu-id="6cf40-142">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-142">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-143">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-144">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-144">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-149">Search-Flags</span></span>           | <span data-ttu-id="6cf40-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-151">System-Flags</span></span>           | <span data-ttu-id="6cf40-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-153">Classes used in</span></span>        | [<span data-ttu-id="6cf40-154">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-155">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6cf40-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6cf40-156">Windows Server 2003</span></span>



| <span data-ttu-id="6cf40-157">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-157">Entry</span></span> | <span data-ttu-id="6cf40-158">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-161">System-Only</span></span>            | <span data-ttu-id="6cf40-162">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-162">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-164">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-164">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-165">Is Indexed</span></span>             | <span data-ttu-id="6cf40-166">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-166">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-167">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-168">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-168">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-173">Search-Flags</span></span>           | <span data-ttu-id="6cf40-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-175">System-Flags</span></span>           | <span data-ttu-id="6cf40-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-177">Classes used in</span></span>        | [<span data-ttu-id="6cf40-178">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-179">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6cf40-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6cf40-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6cf40-181">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-181">Entry</span></span> | <span data-ttu-id="6cf40-182">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-185">System-Only</span></span>            | <span data-ttu-id="6cf40-186">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-186">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-188">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-188">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-189">Is Indexed</span></span>             | <span data-ttu-id="6cf40-190">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-190">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-191">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-192">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-192">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-197">Search-Flags</span></span>           | <span data-ttu-id="6cf40-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-199">System-Flags</span></span>           | <span data-ttu-id="6cf40-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-201">Classes used in</span></span>        | [<span data-ttu-id="6cf40-202">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-203">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6cf40-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6cf40-204">Windows Server 2008</span></span>



| <span data-ttu-id="6cf40-205">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-205">Entry</span></span> | <span data-ttu-id="6cf40-206">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-209">System-Only</span></span>            | <span data-ttu-id="6cf40-210">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-210">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-211">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-212">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-212">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-213">Is Indexed</span></span>             | <span data-ttu-id="6cf40-214">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-214">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-215">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-216">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-216">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-221">Search-Flags</span></span>           | <span data-ttu-id="6cf40-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-223">System-Flags</span></span>           | <span data-ttu-id="6cf40-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-225">Classes used in</span></span>        | [<span data-ttu-id="6cf40-226">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-227">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6cf40-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6cf40-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6cf40-229">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-229">Entry</span></span> | <span data-ttu-id="6cf40-230">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-233">System-Only</span></span>            | <span data-ttu-id="6cf40-234">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-234">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-235">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-236">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-236">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-237">Is Indexed</span></span>             | <span data-ttu-id="6cf40-238">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-238">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-239">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-240">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-240">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-245">Search-Flags</span></span>           | <span data-ttu-id="6cf40-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-247">System-Flags</span></span>           | <span data-ttu-id="6cf40-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-249">Classes used in</span></span>        | [<span data-ttu-id="6cf40-250">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-251">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6cf40-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cf40-252">Windows Server 2012</span></span>



| <span data-ttu-id="6cf40-253">進入</span><span class="sxs-lookup"><span data-stu-id="6cf40-253">Entry</span></span> | <span data-ttu-id="6cf40-254">值</span><span class="sxs-lookup"><span data-stu-id="6cf40-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf40-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6cf40-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6cf40-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="6cf40-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="6cf40-257">System-Only</span></span>            | <span data-ttu-id="6cf40-258">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-258">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6cf40-259">Is-Single-Valued</span></span>       | <span data-ttu-id="6cf40-260">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-260">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6cf40-261">Is Indexed</span></span>             | <span data-ttu-id="6cf40-262">否</span><span class="sxs-lookup"><span data-stu-id="6cf40-262">False</span></span>                                                                                                |
| <span data-ttu-id="6cf40-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6cf40-263">In Global Catalog</span></span>      | <span data-ttu-id="6cf40-264">對</span><span class="sxs-lookup"><span data-stu-id="6cf40-264">True</span></span>                                                                                                 |
| <span data-ttu-id="6cf40-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6cf40-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="6cf40-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6cf40-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="6cf40-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6cf40-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6cf40-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="6cf40-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-269">Search-Flags</span></span>           | <span data-ttu-id="6cf40-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cf40-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="6cf40-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6cf40-271">System-Flags</span></span>           | <span data-ttu-id="6cf40-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6cf40-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="6cf40-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6cf40-273">Classes used in</span></span>        | [<span data-ttu-id="6cf40-274">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6cf40-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="6cf40-275">**Intellimirror-SCP**</span><span class="sxs-lookup"><span data-stu-id="6cf40-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





