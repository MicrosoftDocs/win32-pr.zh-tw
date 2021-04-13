---
title: MSMQ-使用者 Sid 屬性
description: 已遷移使用者的 SID。
ms.assetid: 2bc658b7-987e-464e-9bf9-d4c7fd8a0df8
ms.tgt_platform: multiple
keywords:
- MSMQ-使用者 Sid 屬性 AD 架構
- mSMQUserSid 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-User-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dce18d3ad7c153b7484c2f5a815f73005baf2b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509690"
---
# <a name="msmq-user-sid-attribute"></a><span data-ttu-id="bd286-105">MSMQ-使用者 Sid 屬性</span><span class="sxs-lookup"><span data-stu-id="bd286-105">MSMQ-User-Sid attribute</span></span>

<span data-ttu-id="bd286-106">已遷移使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="bd286-106">The migrated user's SID.</span></span>



| <span data-ttu-id="bd286-107">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-107">Entry</span></span> | <span data-ttu-id="bd286-108">值</span><span class="sxs-lookup"><span data-stu-id="bd286-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bd286-109">CN</span><span class="sxs-lookup"><span data-stu-id="bd286-109">CN</span></span>                | <span data-ttu-id="bd286-110">MSMQ-使用者 Sid</span><span class="sxs-lookup"><span data-stu-id="bd286-110">MSMQ-User-Sid</span></span>                                         |
| <span data-ttu-id="bd286-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bd286-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bd286-112">mSMQUserSid</span><span class="sxs-lookup"><span data-stu-id="bd286-112">mSMQUserSid</span></span>                                           |
| <span data-ttu-id="bd286-113">大小</span><span class="sxs-lookup"><span data-stu-id="bd286-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bd286-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bd286-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bd286-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bd286-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="bd286-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-116">Attribute-Id</span></span>      | <span data-ttu-id="bd286-117">1.2.840.113556.1.4.1337</span><span class="sxs-lookup"><span data-stu-id="bd286-117">1.2.840.113556.1.4.1337</span></span>                               |
| <span data-ttu-id="bd286-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bd286-118">System-Id-Guid</span></span>    | <span data-ttu-id="bd286-119">c58aae32-56f9-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="bd286-119">c58aae32-56f9-11d2-90d0-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="bd286-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd286-120">Syntax</span></span>            | [<span data-ttu-id="bd286-121">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="bd286-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bd286-122">實作</span><span class="sxs-lookup"><span data-stu-id="bd286-122">Implementations</span></span>

-   [<span data-ttu-id="bd286-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bd286-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bd286-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bd286-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bd286-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bd286-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bd286-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bd286-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bd286-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bd286-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bd286-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bd286-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bd286-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd286-129">Windows 2000 Server</span></span>



| <span data-ttu-id="bd286-130">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-130">Entry</span></span> | <span data-ttu-id="bd286-131">值</span><span class="sxs-lookup"><span data-stu-id="bd286-131">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-132">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-133">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-134">System-Only</span></span>            | <span data-ttu-id="bd286-135">對</span><span class="sxs-lookup"><span data-stu-id="bd286-135">True</span></span>                                                        |
| <span data-ttu-id="bd286-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-136">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-137">對</span><span class="sxs-lookup"><span data-stu-id="bd286-137">True</span></span>                                                        |
| <span data-ttu-id="bd286-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-138">Is Indexed</span></span>             | <span data-ttu-id="bd286-139">否</span><span class="sxs-lookup"><span data-stu-id="bd286-139">False</span></span>                                                       |
| <span data-ttu-id="bd286-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-140">In Global Catalog</span></span>      | <span data-ttu-id="bd286-141">對</span><span class="sxs-lookup"><span data-stu-id="bd286-141">True</span></span>                                                        |
| <span data-ttu-id="bd286-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-143">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-144">Range-Lower</span></span>            | <span data-ttu-id="bd286-145">0</span><span class="sxs-lookup"><span data-stu-id="bd286-145">0</span></span>                                                           |
| <span data-ttu-id="bd286-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-146">Range-Upper</span></span>            | <span data-ttu-id="bd286-147">128</span><span class="sxs-lookup"><span data-stu-id="bd286-147">128</span></span>                                                         |
| <span data-ttu-id="bd286-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-148">Search-Flags</span></span>           | <span data-ttu-id="bd286-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-150">System-Flags</span></span>           | <span data-ttu-id="bd286-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bd286-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="bd286-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-152">Classes used in</span></span>        | [<span data-ttu-id="bd286-153">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bd286-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bd286-154">Windows Server 2003</span></span>



| <span data-ttu-id="bd286-155">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-155">Entry</span></span> | <span data-ttu-id="bd286-156">值</span><span class="sxs-lookup"><span data-stu-id="bd286-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-159">System-Only</span></span>            | <span data-ttu-id="bd286-160">對</span><span class="sxs-lookup"><span data-stu-id="bd286-160">True</span></span>                                                        |
| <span data-ttu-id="bd286-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-162">對</span><span class="sxs-lookup"><span data-stu-id="bd286-162">True</span></span>                                                        |
| <span data-ttu-id="bd286-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-163">Is Indexed</span></span>             | <span data-ttu-id="bd286-164">否</span><span class="sxs-lookup"><span data-stu-id="bd286-164">False</span></span>                                                       |
| <span data-ttu-id="bd286-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-165">In Global Catalog</span></span>      | <span data-ttu-id="bd286-166">對</span><span class="sxs-lookup"><span data-stu-id="bd286-166">True</span></span>                                                        |
| <span data-ttu-id="bd286-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-169">Range-Lower</span></span>            | <span data-ttu-id="bd286-170">0</span><span class="sxs-lookup"><span data-stu-id="bd286-170">0</span></span>                                                           |
| <span data-ttu-id="bd286-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-171">Range-Upper</span></span>            | <span data-ttu-id="bd286-172">128</span><span class="sxs-lookup"><span data-stu-id="bd286-172">128</span></span>                                                         |
| <span data-ttu-id="bd286-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-173">Search-Flags</span></span>           | <span data-ttu-id="bd286-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-174">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-175">System-Flags</span></span>           | <span data-ttu-id="bd286-176">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bd286-176">0x00000012</span></span>                                                  |
| <span data-ttu-id="bd286-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-177">Classes used in</span></span>        | [<span data-ttu-id="bd286-178">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-178">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bd286-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bd286-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bd286-180">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-180">Entry</span></span> | <span data-ttu-id="bd286-181">值</span><span class="sxs-lookup"><span data-stu-id="bd286-181">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-182">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-183">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-184">System-Only</span></span>            | <span data-ttu-id="bd286-185">對</span><span class="sxs-lookup"><span data-stu-id="bd286-185">True</span></span>                                                        |
| <span data-ttu-id="bd286-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-186">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-187">對</span><span class="sxs-lookup"><span data-stu-id="bd286-187">True</span></span>                                                        |
| <span data-ttu-id="bd286-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-188">Is Indexed</span></span>             | <span data-ttu-id="bd286-189">否</span><span class="sxs-lookup"><span data-stu-id="bd286-189">False</span></span>                                                       |
| <span data-ttu-id="bd286-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-190">In Global Catalog</span></span>      | <span data-ttu-id="bd286-191">對</span><span class="sxs-lookup"><span data-stu-id="bd286-191">True</span></span>                                                        |
| <span data-ttu-id="bd286-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-193">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-194">Range-Lower</span></span>            | <span data-ttu-id="bd286-195">0</span><span class="sxs-lookup"><span data-stu-id="bd286-195">0</span></span>                                                           |
| <span data-ttu-id="bd286-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-196">Range-Upper</span></span>            | <span data-ttu-id="bd286-197">128</span><span class="sxs-lookup"><span data-stu-id="bd286-197">128</span></span>                                                         |
| <span data-ttu-id="bd286-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-198">Search-Flags</span></span>           | <span data-ttu-id="bd286-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-199">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-200">System-Flags</span></span>           | <span data-ttu-id="bd286-201">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bd286-201">0x00000012</span></span>                                                  |
| <span data-ttu-id="bd286-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-202">Classes used in</span></span>        | [<span data-ttu-id="bd286-203">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-203">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bd286-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd286-204">Windows Server 2008</span></span>



| <span data-ttu-id="bd286-205">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-205">Entry</span></span> | <span data-ttu-id="bd286-206">值</span><span class="sxs-lookup"><span data-stu-id="bd286-206">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-207">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-208">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-209">System-Only</span></span>            | <span data-ttu-id="bd286-210">對</span><span class="sxs-lookup"><span data-stu-id="bd286-210">True</span></span>                                                        |
| <span data-ttu-id="bd286-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-211">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-212">對</span><span class="sxs-lookup"><span data-stu-id="bd286-212">True</span></span>                                                        |
| <span data-ttu-id="bd286-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-213">Is Indexed</span></span>             | <span data-ttu-id="bd286-214">否</span><span class="sxs-lookup"><span data-stu-id="bd286-214">False</span></span>                                                       |
| <span data-ttu-id="bd286-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-215">In Global Catalog</span></span>      | <span data-ttu-id="bd286-216">對</span><span class="sxs-lookup"><span data-stu-id="bd286-216">True</span></span>                                                        |
| <span data-ttu-id="bd286-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-218">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-219">Range-Lower</span></span>            | <span data-ttu-id="bd286-220">0</span><span class="sxs-lookup"><span data-stu-id="bd286-220">0</span></span>                                                           |
| <span data-ttu-id="bd286-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-221">Range-Upper</span></span>            | <span data-ttu-id="bd286-222">128</span><span class="sxs-lookup"><span data-stu-id="bd286-222">128</span></span>                                                         |
| <span data-ttu-id="bd286-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-223">Search-Flags</span></span>           | <span data-ttu-id="bd286-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-224">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-225">System-Flags</span></span>           | <span data-ttu-id="bd286-226">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bd286-226">0x00000012</span></span>                                                  |
| <span data-ttu-id="bd286-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-227">Classes used in</span></span>        | [<span data-ttu-id="bd286-228">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bd286-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bd286-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bd286-230">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-230">Entry</span></span> | <span data-ttu-id="bd286-231">值</span><span class="sxs-lookup"><span data-stu-id="bd286-231">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-232">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-233">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-234">System-Only</span></span>            | <span data-ttu-id="bd286-235">對</span><span class="sxs-lookup"><span data-stu-id="bd286-235">True</span></span>                                                        |
| <span data-ttu-id="bd286-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-236">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-237">對</span><span class="sxs-lookup"><span data-stu-id="bd286-237">True</span></span>                                                        |
| <span data-ttu-id="bd286-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-238">Is Indexed</span></span>             | <span data-ttu-id="bd286-239">否</span><span class="sxs-lookup"><span data-stu-id="bd286-239">False</span></span>                                                       |
| <span data-ttu-id="bd286-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-240">In Global Catalog</span></span>      | <span data-ttu-id="bd286-241">對</span><span class="sxs-lookup"><span data-stu-id="bd286-241">True</span></span>                                                        |
| <span data-ttu-id="bd286-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-243">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-244">Range-Lower</span></span>            | <span data-ttu-id="bd286-245">0</span><span class="sxs-lookup"><span data-stu-id="bd286-245">0</span></span>                                                           |
| <span data-ttu-id="bd286-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-246">Range-Upper</span></span>            | <span data-ttu-id="bd286-247">128</span><span class="sxs-lookup"><span data-stu-id="bd286-247">128</span></span>                                                         |
| <span data-ttu-id="bd286-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-248">Search-Flags</span></span>           | <span data-ttu-id="bd286-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-249">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-250">System-Flags</span></span>           | <span data-ttu-id="bd286-251">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bd286-251">0x00000012</span></span>                                                  |
| <span data-ttu-id="bd286-252">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-252">Classes used in</span></span>        | [<span data-ttu-id="bd286-253">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-253">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bd286-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bd286-254">Windows Server 2012</span></span>



| <span data-ttu-id="bd286-255">進入</span><span class="sxs-lookup"><span data-stu-id="bd286-255">Entry</span></span> | <span data-ttu-id="bd286-256">值</span><span class="sxs-lookup"><span data-stu-id="bd286-256">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="bd286-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bd286-257">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bd286-258">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="bd286-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="bd286-259">System-Only</span></span>            | <span data-ttu-id="bd286-260">對</span><span class="sxs-lookup"><span data-stu-id="bd286-260">True</span></span>                                                        |
| <span data-ttu-id="bd286-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bd286-261">Is-Single-Valued</span></span>       | <span data-ttu-id="bd286-262">對</span><span class="sxs-lookup"><span data-stu-id="bd286-262">True</span></span>                                                        |
| <span data-ttu-id="bd286-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bd286-263">Is Indexed</span></span>             | <span data-ttu-id="bd286-264">否</span><span class="sxs-lookup"><span data-stu-id="bd286-264">False</span></span>                                                       |
| <span data-ttu-id="bd286-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bd286-265">In Global Catalog</span></span>      | <span data-ttu-id="bd286-266">對</span><span class="sxs-lookup"><span data-stu-id="bd286-266">True</span></span>                                                        |
| <span data-ttu-id="bd286-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bd286-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="bd286-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bd286-268">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="bd286-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bd286-269">Range-Lower</span></span>            | <span data-ttu-id="bd286-270">0</span><span class="sxs-lookup"><span data-stu-id="bd286-270">0</span></span>                                                           |
| <span data-ttu-id="bd286-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bd286-271">Range-Upper</span></span>            | <span data-ttu-id="bd286-272">128</span><span class="sxs-lookup"><span data-stu-id="bd286-272">128</span></span>                                                         |
| <span data-ttu-id="bd286-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-273">Search-Flags</span></span>           | <span data-ttu-id="bd286-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bd286-274">0x00000000</span></span>                                                  |
| <span data-ttu-id="bd286-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bd286-275">System-Flags</span></span>           | <span data-ttu-id="bd286-276">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bd286-276">0x00000012</span></span>                                                  |
| <span data-ttu-id="bd286-277">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bd286-277">Classes used in</span></span>        | [<span data-ttu-id="bd286-278">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="bd286-278">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> |



 

 





