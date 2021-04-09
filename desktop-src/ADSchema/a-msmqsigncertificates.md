---
title: MSMQ 簽署憑證屬性
description: 此屬性包含許多憑證。 使用者可以產生每台電腦的憑證。 我們也會針對每個憑證保留摘要。
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- MSMQ-簽署憑證屬性 AD 架構
- mSMQSignCertificates 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845080"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="2b455-107">MSMQ 簽署憑證屬性</span><span class="sxs-lookup"><span data-stu-id="2b455-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="2b455-108">此屬性包含許多憑證。</span><span class="sxs-lookup"><span data-stu-id="2b455-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="2b455-109">使用者可以產生每台電腦的憑證。</span><span class="sxs-lookup"><span data-stu-id="2b455-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="2b455-110">我們也會針對每個憑證保留摘要。</span><span class="sxs-lookup"><span data-stu-id="2b455-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="2b455-111">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-111">Entry</span></span> | <span data-ttu-id="2b455-112">值</span><span class="sxs-lookup"><span data-stu-id="2b455-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-113">CN</span><span class="sxs-lookup"><span data-stu-id="2b455-113">CN</span></span>                | <span data-ttu-id="2b455-114">MSMQ-簽署憑證</span><span class="sxs-lookup"><span data-stu-id="2b455-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="2b455-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2b455-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2b455-116">mSMQSignCertificates</span><span class="sxs-lookup"><span data-stu-id="2b455-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="2b455-117">大小</span><span class="sxs-lookup"><span data-stu-id="2b455-117">Size</span></span>              | <span data-ttu-id="2b455-118">屬性類型是 BLOB、大小不受限制，且資料會以我們自己的格式保存。</span><span class="sxs-lookup"><span data-stu-id="2b455-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="2b455-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="2b455-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="2b455-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="2b455-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="2b455-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-121">Attribute-Id</span></span>      | <span data-ttu-id="2b455-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="2b455-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="2b455-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="2b455-123">System-Id-Guid</span></span>    | <span data-ttu-id="2b455-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2b455-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="2b455-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b455-125">Syntax</span></span>            | [<span data-ttu-id="2b455-126">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="2b455-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="2b455-127">實作</span><span class="sxs-lookup"><span data-stu-id="2b455-127">Implementations</span></span>

-   [<span data-ttu-id="2b455-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b455-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b455-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b455-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b455-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b455-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b455-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b455-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b455-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b455-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b455-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b455-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b455-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b455-134">Windows 2000 Server</span></span>



| <span data-ttu-id="2b455-135">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-135">Entry</span></span> | <span data-ttu-id="2b455-136">值</span><span class="sxs-lookup"><span data-stu-id="2b455-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-139">System-Only</span></span>            | <span data-ttu-id="2b455-140">否</span><span class="sxs-lookup"><span data-stu-id="2b455-140">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-142">對</span><span class="sxs-lookup"><span data-stu-id="2b455-142">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-143">Is Indexed</span></span>             | <span data-ttu-id="2b455-144">否</span><span class="sxs-lookup"><span data-stu-id="2b455-144">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-145">In Global Catalog</span></span>      | <span data-ttu-id="2b455-146">對</span><span class="sxs-lookup"><span data-stu-id="2b455-146">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-151">Search-Flags</span></span>           | <span data-ttu-id="2b455-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-153">System-Flags</span></span>           | <span data-ttu-id="2b455-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-155">Classes used in</span></span>        | [<span data-ttu-id="2b455-156">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-157">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b455-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b455-158">Windows Server 2003</span></span>



| <span data-ttu-id="2b455-159">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-159">Entry</span></span> | <span data-ttu-id="2b455-160">值</span><span class="sxs-lookup"><span data-stu-id="2b455-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-163">System-Only</span></span>            | <span data-ttu-id="2b455-164">否</span><span class="sxs-lookup"><span data-stu-id="2b455-164">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-166">對</span><span class="sxs-lookup"><span data-stu-id="2b455-166">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-167">Is Indexed</span></span>             | <span data-ttu-id="2b455-168">否</span><span class="sxs-lookup"><span data-stu-id="2b455-168">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-169">In Global Catalog</span></span>      | <span data-ttu-id="2b455-170">對</span><span class="sxs-lookup"><span data-stu-id="2b455-170">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-175">Search-Flags</span></span>           | <span data-ttu-id="2b455-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-177">System-Flags</span></span>           | <span data-ttu-id="2b455-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-179">Classes used in</span></span>        | [<span data-ttu-id="2b455-180">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-181">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b455-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b455-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b455-183">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-183">Entry</span></span> | <span data-ttu-id="2b455-184">值</span><span class="sxs-lookup"><span data-stu-id="2b455-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-187">System-Only</span></span>            | <span data-ttu-id="2b455-188">否</span><span class="sxs-lookup"><span data-stu-id="2b455-188">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-190">對</span><span class="sxs-lookup"><span data-stu-id="2b455-190">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-191">Is Indexed</span></span>             | <span data-ttu-id="2b455-192">否</span><span class="sxs-lookup"><span data-stu-id="2b455-192">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-193">In Global Catalog</span></span>      | <span data-ttu-id="2b455-194">對</span><span class="sxs-lookup"><span data-stu-id="2b455-194">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-199">Search-Flags</span></span>           | <span data-ttu-id="2b455-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-201">System-Flags</span></span>           | <span data-ttu-id="2b455-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-203">Classes used in</span></span>        | [<span data-ttu-id="2b455-204">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-205">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b455-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b455-206">Windows Server 2008</span></span>



| <span data-ttu-id="2b455-207">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-207">Entry</span></span> | <span data-ttu-id="2b455-208">值</span><span class="sxs-lookup"><span data-stu-id="2b455-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-209">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-211">System-Only</span></span>            | <span data-ttu-id="2b455-212">否</span><span class="sxs-lookup"><span data-stu-id="2b455-212">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-213">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-214">對</span><span class="sxs-lookup"><span data-stu-id="2b455-214">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-215">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-215">Is Indexed</span></span>             | <span data-ttu-id="2b455-216">否</span><span class="sxs-lookup"><span data-stu-id="2b455-216">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-217">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-217">In Global Catalog</span></span>      | <span data-ttu-id="2b455-218">對</span><span class="sxs-lookup"><span data-stu-id="2b455-218">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-219">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-220">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-223">Search-Flags</span></span>           | <span data-ttu-id="2b455-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-225">System-Flags</span></span>           | <span data-ttu-id="2b455-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-227">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-227">Classes used in</span></span>        | [<span data-ttu-id="2b455-228">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-229">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b455-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b455-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b455-231">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-231">Entry</span></span> | <span data-ttu-id="2b455-232">值</span><span class="sxs-lookup"><span data-stu-id="2b455-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-233">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-235">System-Only</span></span>            | <span data-ttu-id="2b455-236">否</span><span class="sxs-lookup"><span data-stu-id="2b455-236">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-237">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-238">對</span><span class="sxs-lookup"><span data-stu-id="2b455-238">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-239">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-239">Is Indexed</span></span>             | <span data-ttu-id="2b455-240">否</span><span class="sxs-lookup"><span data-stu-id="2b455-240">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-241">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-241">In Global Catalog</span></span>      | <span data-ttu-id="2b455-242">對</span><span class="sxs-lookup"><span data-stu-id="2b455-242">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-243">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-244">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-247">Search-Flags</span></span>           | <span data-ttu-id="2b455-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-249">System-Flags</span></span>           | <span data-ttu-id="2b455-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-251">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-251">Classes used in</span></span>        | [<span data-ttu-id="2b455-252">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-253">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b455-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b455-254">Windows Server 2012</span></span>



| <span data-ttu-id="2b455-255">進入</span><span class="sxs-lookup"><span data-stu-id="2b455-255">Entry</span></span> | <span data-ttu-id="2b455-256">值</span><span class="sxs-lookup"><span data-stu-id="2b455-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b455-257">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="2b455-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b455-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="2b455-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b455-259">System-Only</span></span>            | <span data-ttu-id="2b455-260">否</span><span class="sxs-lookup"><span data-stu-id="2b455-260">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-261">是-單一值</span><span class="sxs-lookup"><span data-stu-id="2b455-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2b455-262">對</span><span class="sxs-lookup"><span data-stu-id="2b455-262">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-263">已編制索引</span><span class="sxs-lookup"><span data-stu-id="2b455-263">Is Indexed</span></span>             | <span data-ttu-id="2b455-264">否</span><span class="sxs-lookup"><span data-stu-id="2b455-264">False</span></span>                                                                                         |
| <span data-ttu-id="2b455-265">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="2b455-265">In Global Catalog</span></span>      | <span data-ttu-id="2b455-266">對</span><span class="sxs-lookup"><span data-stu-id="2b455-266">True</span></span>                                                                                          |
| <span data-ttu-id="2b455-267">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="2b455-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b455-268">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="2b455-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="2b455-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b455-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b455-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="2b455-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-271">Search-Flags</span></span>           | <span data-ttu-id="2b455-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b455-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="2b455-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b455-273">System-Flags</span></span>           | <span data-ttu-id="2b455-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b455-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="2b455-275">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="2b455-275">Classes used in</span></span>        | [<span data-ttu-id="2b455-276">**MSMQ 遷移-使用者**</span><span class="sxs-lookup"><span data-stu-id="2b455-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="2b455-277">**User**</span><span class="sxs-lookup"><span data-stu-id="2b455-277">**User**</span></span>](c-user.md)<br/> |



 

 





