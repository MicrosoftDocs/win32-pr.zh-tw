---
title: 已淘汰-複寫-DSA-簽章屬性
description: 追蹤指定 DC 的過去 DS 複寫身分識別。
ms.assetid: 82e8b222-5635-41ad-b2ab-386c9e6aa280
ms.tgt_platform: multiple
keywords:
- 已淘汰-複寫-DSA-簽章屬性 AD 架構
- retiredReplDSASignatures 屬性 AD 架構
topic_type:
- apiref
api_name:
- Retired-Repl-DSA-Signatures
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9a4cb4030a8d3aa24244bc2e7a2702e83686fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385430"
---
# <a name="retired-repl-dsa-signatures-attribute"></a><span data-ttu-id="b0cd9-105">已淘汰-複寫-DSA-簽章屬性</span><span class="sxs-lookup"><span data-stu-id="b0cd9-105">Retired-Repl-DSA-Signatures attribute</span></span>

<span data-ttu-id="b0cd9-106">追蹤指定 DC 的過去 DS 複寫身分識別。</span><span class="sxs-lookup"><span data-stu-id="b0cd9-106">Tracks the past DS replication identities of a given DC.</span></span>



| <span data-ttu-id="b0cd9-107">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-107">Entry</span></span> | <span data-ttu-id="b0cd9-108">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-108">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0cd9-109">CN</span><span class="sxs-lookup"><span data-stu-id="b0cd9-109">CN</span></span>                | <span data-ttu-id="b0cd9-110">已淘汰-複寫-DSA-簽章</span><span class="sxs-lookup"><span data-stu-id="b0cd9-110">Retired-Repl-DSA-Signatures</span></span>                                                         |
| <span data-ttu-id="b0cd9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b0cd9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b0cd9-112">retiredReplDSASignatures</span><span class="sxs-lookup"><span data-stu-id="b0cd9-112">retiredReplDSASignatures</span></span>                                                            |
| <span data-ttu-id="b0cd9-113">大小</span><span class="sxs-lookup"><span data-stu-id="b0cd9-113">Size</span></span>              | <span data-ttu-id="b0cd9-114">長度與從備份還原 DC 的次數成正比。</span><span class="sxs-lookup"><span data-stu-id="b0cd9-114">Length is proportional to the number of times the DC has been restored from backup.</span></span> |
| <span data-ttu-id="b0cd9-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b0cd9-115">Update Privilege</span></span>  | <span data-ttu-id="b0cd9-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b0cd9-116">This value is set by the system.</span></span>                                                    |
| <span data-ttu-id="b0cd9-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b0cd9-117">Update Frequency</span></span>  | \-                                                                                  |
| <span data-ttu-id="b0cd9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-118">Attribute-Id</span></span>      | <span data-ttu-id="b0cd9-119">1.2.840.113556.1.4.673</span><span class="sxs-lookup"><span data-stu-id="b0cd9-119">1.2.840.113556.1.4.673</span></span>                                                              |
| <span data-ttu-id="b0cd9-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b0cd9-120">System-Id-Guid</span></span>    | <span data-ttu-id="b0cd9-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b0cd9-121">7bfdcb7f-4807-11d1-a9c3-0000f80367c1</span></span>                                                |
| <span data-ttu-id="b0cd9-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0cd9-122">Syntax</span></span>            | [<span data-ttu-id="b0cd9-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                               |



## <a name="implementations"></a><span data-ttu-id="b0cd9-124">實作</span><span class="sxs-lookup"><span data-stu-id="b0cd9-124">Implementations</span></span>

-   [<span data-ttu-id="b0cd9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b0cd9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b0cd9-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b0cd9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b0cd9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b0cd9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b0cd9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b0cd9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0cd9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b0cd9-133">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-133">Entry</span></span> | <span data-ttu-id="b0cd9-134">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-134">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-135">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-137">System-Only</span></span>            | <span data-ttu-id="b0cd9-138">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-138">True</span></span>                                     |
| <span data-ttu-id="b0cd9-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-140">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-140">True</span></span>                                     |
| <span data-ttu-id="b0cd9-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-141">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-142">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-142">False</span></span>                                    |
| <span data-ttu-id="b0cd9-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-143">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-144">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-144">False</span></span>                                    |
| <span data-ttu-id="b0cd9-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-147">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-148">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-149">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-150">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-151">System-Flags</span></span>           | <span data-ttu-id="b0cd9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-152">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-153">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-154">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-154">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b0cd9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b0cd9-155">Windows Server 2003</span></span>



| <span data-ttu-id="b0cd9-156">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-156">Entry</span></span> | <span data-ttu-id="b0cd9-157">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-157">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-158">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-159">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-160">System-Only</span></span>            | <span data-ttu-id="b0cd9-161">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-161">True</span></span>                                     |
| <span data-ttu-id="b0cd9-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-163">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-163">True</span></span>                                     |
| <span data-ttu-id="b0cd9-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-164">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-165">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-165">False</span></span>                                    |
| <span data-ttu-id="b0cd9-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-166">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-167">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-167">False</span></span>                                    |
| <span data-ttu-id="b0cd9-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-169">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-170">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-171">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-172">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-173">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-174">System-Flags</span></span>           | <span data-ttu-id="b0cd9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-175">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-176">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-177">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-177">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b0cd9-178">亞當</span><span class="sxs-lookup"><span data-stu-id="b0cd9-178">ADAM</span></span>



| <span data-ttu-id="b0cd9-179">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-179">Entry</span></span> | <span data-ttu-id="b0cd9-180">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-180">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-181">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-182">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-183">System-Only</span></span>            | <span data-ttu-id="b0cd9-184">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-184">True</span></span>                                     |
| <span data-ttu-id="b0cd9-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-186">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-186">True</span></span>                                     |
| <span data-ttu-id="b0cd9-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-187">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-188">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-188">False</span></span>                                    |
| <span data-ttu-id="b0cd9-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-189">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-190">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-190">False</span></span>                                    |
| <span data-ttu-id="b0cd9-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-192">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-193">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-194">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-195">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-196">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-197">System-Flags</span></span>           | <span data-ttu-id="b0cd9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-198">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-199">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b0cd9-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b0cd9-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b0cd9-202">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-202">Entry</span></span> | <span data-ttu-id="b0cd9-203">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-203">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-204">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-205">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-206">System-Only</span></span>            | <span data-ttu-id="b0cd9-207">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-207">True</span></span>                                     |
| <span data-ttu-id="b0cd9-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-209">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-209">True</span></span>                                     |
| <span data-ttu-id="b0cd9-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-210">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-211">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-211">False</span></span>                                    |
| <span data-ttu-id="b0cd9-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-212">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-213">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-213">False</span></span>                                    |
| <span data-ttu-id="b0cd9-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-215">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-216">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-217">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-218">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-219">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-220">System-Flags</span></span>           | <span data-ttu-id="b0cd9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-221">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-222">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-223">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-223">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b0cd9-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0cd9-224">Windows Server 2008</span></span>



| <span data-ttu-id="b0cd9-225">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-225">Entry</span></span> | <span data-ttu-id="b0cd9-226">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-226">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-227">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-228">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-229">System-Only</span></span>            | <span data-ttu-id="b0cd9-230">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-230">True</span></span>                                     |
| <span data-ttu-id="b0cd9-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-232">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-232">True</span></span>                                     |
| <span data-ttu-id="b0cd9-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-233">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-234">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-234">False</span></span>                                    |
| <span data-ttu-id="b0cd9-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-235">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-236">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-236">False</span></span>                                    |
| <span data-ttu-id="b0cd9-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-238">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-239">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-240">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-241">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-242">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-243">System-Flags</span></span>           | <span data-ttu-id="b0cd9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-244">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-245">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-246">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-246">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b0cd9-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0cd9-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b0cd9-248">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-248">Entry</span></span> | <span data-ttu-id="b0cd9-249">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-249">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-250">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-251">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-252">System-Only</span></span>            | <span data-ttu-id="b0cd9-253">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-253">True</span></span>                                     |
| <span data-ttu-id="b0cd9-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-255">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-255">True</span></span>                                     |
| <span data-ttu-id="b0cd9-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-256">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-257">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-257">False</span></span>                                    |
| <span data-ttu-id="b0cd9-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-258">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-259">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-259">False</span></span>                                    |
| <span data-ttu-id="b0cd9-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-261">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-262">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-263">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-264">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-265">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-266">System-Flags</span></span>           | <span data-ttu-id="b0cd9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-267">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-268">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-269">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-269">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b0cd9-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0cd9-270">Windows Server 2012</span></span>



| <span data-ttu-id="b0cd9-271">進入</span><span class="sxs-lookup"><span data-stu-id="b0cd9-271">Entry</span></span> | <span data-ttu-id="b0cd9-272">值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-272">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="b0cd9-273">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b0cd9-273">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b0cd9-274">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="b0cd9-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="b0cd9-275">System-Only</span></span>            | <span data-ttu-id="b0cd9-276">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-276">True</span></span>                                     |
| <span data-ttu-id="b0cd9-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b0cd9-277">Is-Single-Valued</span></span>       | <span data-ttu-id="b0cd9-278">對</span><span class="sxs-lookup"><span data-stu-id="b0cd9-278">True</span></span>                                     |
| <span data-ttu-id="b0cd9-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b0cd9-279">Is Indexed</span></span>             | <span data-ttu-id="b0cd9-280">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-280">False</span></span>                                    |
| <span data-ttu-id="b0cd9-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b0cd9-281">In Global Catalog</span></span>      | <span data-ttu-id="b0cd9-282">否</span><span class="sxs-lookup"><span data-stu-id="b0cd9-282">False</span></span>                                    |
| <span data-ttu-id="b0cd9-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b0cd9-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="b0cd9-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b0cd9-284">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="b0cd9-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b0cd9-285">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b0cd9-286">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="b0cd9-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-287">Search-Flags</span></span>           | <span data-ttu-id="b0cd9-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b0cd9-288">0x00000000</span></span>                               |
| <span data-ttu-id="b0cd9-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b0cd9-289">System-Flags</span></span>           | <span data-ttu-id="b0cd9-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b0cd9-290">0x00000010</span></span>                               |
| <span data-ttu-id="b0cd9-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b0cd9-291">Classes used in</span></span>        | [<span data-ttu-id="b0cd9-292">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="b0cd9-292">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





