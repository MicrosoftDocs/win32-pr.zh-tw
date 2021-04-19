---
title: Other-Mailbox 屬性
description: 在表單中包含其他的其他郵寄地址，例如 CCMAIL BruceKeever。
ms.assetid: c7e49fbc-fb3a-487e-835b-ad2c1481425a
ms.tgt_platform: multiple
keywords:
- Other-Mailbox 屬性 AD 架構
- otherMailbox 屬性 AD 架構
topic_type:
- apiref
api_name:
- Other-Mailbox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d02bb4031da8938fc38bf25562918204089db08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971905"
---
# <a name="other-mailbox-attribute"></a><span data-ttu-id="bff14-105">Other-Mailbox 屬性</span><span class="sxs-lookup"><span data-stu-id="bff14-105">Other-Mailbox attribute</span></span>

<span data-ttu-id="bff14-106">在表單中包含其他其他郵寄地址，例如 CCMAIL： BruceKeever。</span><span class="sxs-lookup"><span data-stu-id="bff14-106">Contains other additional mail addresses in a form such as CCMAIL: BruceKeever.</span></span>



| <span data-ttu-id="bff14-107">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-107">Entry</span></span> | <span data-ttu-id="bff14-108">值</span><span class="sxs-lookup"><span data-stu-id="bff14-108">Value</span></span> |
|-------------------|----------------------------------------------------------|
| <span data-ttu-id="bff14-109">CN</span><span class="sxs-lookup"><span data-stu-id="bff14-109">CN</span></span>                | <span data-ttu-id="bff14-110">Other-Mailbox</span><span class="sxs-lookup"><span data-stu-id="bff14-110">Other-Mailbox</span></span>                                            |
| <span data-ttu-id="bff14-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bff14-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bff14-112">otherMailbox</span><span class="sxs-lookup"><span data-stu-id="bff14-112">otherMailbox</span></span>                                             |
| <span data-ttu-id="bff14-113">大小</span><span class="sxs-lookup"><span data-stu-id="bff14-113">Size</span></span>              | \-                                                       |
| <span data-ttu-id="bff14-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bff14-114">Update Privilege</span></span>  | <span data-ttu-id="bff14-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="bff14-115">Domain administrator</span></span>                                     |
| <span data-ttu-id="bff14-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bff14-116">Update Frequency</span></span>  | <span data-ttu-id="bff14-117">每次使用者發出額外的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="bff14-117">Each time the user is issued an additional mail address.</span></span> |
| <span data-ttu-id="bff14-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-118">Attribute-Id</span></span>      | <span data-ttu-id="bff14-119">1.2.840.113556.1.4.651</span><span class="sxs-lookup"><span data-stu-id="bff14-119">1.2.840.113556.1.4.651</span></span>                                   |
| <span data-ttu-id="bff14-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bff14-120">System-Id-Guid</span></span>    | <span data-ttu-id="bff14-121">0296c123-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="bff14-121">0296c123-40da-11d1-a9c0-0000f80367c1</span></span>                     |
| <span data-ttu-id="bff14-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="bff14-122">Syntax</span></span>            | [<span data-ttu-id="bff14-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bff14-123">**String(Unicode)**</span></span>](s-string-unicode.md)              |



## <a name="implementations"></a><span data-ttu-id="bff14-124">實作</span><span class="sxs-lookup"><span data-stu-id="bff14-124">Implementations</span></span>

-   [<span data-ttu-id="bff14-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bff14-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bff14-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bff14-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bff14-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bff14-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bff14-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bff14-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bff14-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bff14-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bff14-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bff14-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bff14-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bff14-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bff14-132">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-132">Entry</span></span> | <span data-ttu-id="bff14-133">值</span><span class="sxs-lookup"><span data-stu-id="bff14-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-136">System-Only</span></span>            | <span data-ttu-id="bff14-137">否</span><span class="sxs-lookup"><span data-stu-id="bff14-137">False</span></span>                                                              |
| <span data-ttu-id="bff14-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-138">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-139">否</span><span class="sxs-lookup"><span data-stu-id="bff14-139">False</span></span>                                                              |
| <span data-ttu-id="bff14-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-140">Is Indexed</span></span>             | <span data-ttu-id="bff14-141">否</span><span class="sxs-lookup"><span data-stu-id="bff14-141">False</span></span>                                                              |
| <span data-ttu-id="bff14-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-142">In Global Catalog</span></span>      | <span data-ttu-id="bff14-143">否</span><span class="sxs-lookup"><span data-stu-id="bff14-143">False</span></span>                                                              |
| <span data-ttu-id="bff14-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-146">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-147">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-148">Search-Flags</span></span>           | <span data-ttu-id="bff14-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-149">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-150">System-Flags</span></span>           | <span data-ttu-id="bff14-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-152">Classes used in</span></span>        | [<span data-ttu-id="bff14-153">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-153">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bff14-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bff14-154">Windows Server 2003</span></span>



| <span data-ttu-id="bff14-155">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-155">Entry</span></span> | <span data-ttu-id="bff14-156">值</span><span class="sxs-lookup"><span data-stu-id="bff14-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-157">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-158">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-159">System-Only</span></span>            | <span data-ttu-id="bff14-160">否</span><span class="sxs-lookup"><span data-stu-id="bff14-160">False</span></span>                                                              |
| <span data-ttu-id="bff14-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-161">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-162">否</span><span class="sxs-lookup"><span data-stu-id="bff14-162">False</span></span>                                                              |
| <span data-ttu-id="bff14-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-163">Is Indexed</span></span>             | <span data-ttu-id="bff14-164">否</span><span class="sxs-lookup"><span data-stu-id="bff14-164">False</span></span>                                                              |
| <span data-ttu-id="bff14-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-165">In Global Catalog</span></span>      | <span data-ttu-id="bff14-166">否</span><span class="sxs-lookup"><span data-stu-id="bff14-166">False</span></span>                                                              |
| <span data-ttu-id="bff14-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-168">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-169">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-170">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-171">Search-Flags</span></span>           | <span data-ttu-id="bff14-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-172">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-173">System-Flags</span></span>           | <span data-ttu-id="bff14-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-175">Classes used in</span></span>        | [<span data-ttu-id="bff14-176">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-176">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bff14-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bff14-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bff14-178">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-178">Entry</span></span> | <span data-ttu-id="bff14-179">值</span><span class="sxs-lookup"><span data-stu-id="bff14-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-180">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-181">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-182">System-Only</span></span>            | <span data-ttu-id="bff14-183">否</span><span class="sxs-lookup"><span data-stu-id="bff14-183">False</span></span>                                                              |
| <span data-ttu-id="bff14-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-184">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-185">否</span><span class="sxs-lookup"><span data-stu-id="bff14-185">False</span></span>                                                              |
| <span data-ttu-id="bff14-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-186">Is Indexed</span></span>             | <span data-ttu-id="bff14-187">否</span><span class="sxs-lookup"><span data-stu-id="bff14-187">False</span></span>                                                              |
| <span data-ttu-id="bff14-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-188">In Global Catalog</span></span>      | <span data-ttu-id="bff14-189">否</span><span class="sxs-lookup"><span data-stu-id="bff14-189">False</span></span>                                                              |
| <span data-ttu-id="bff14-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-191">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-192">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-193">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-194">Search-Flags</span></span>           | <span data-ttu-id="bff14-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-195">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-196">System-Flags</span></span>           | <span data-ttu-id="bff14-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-198">Classes used in</span></span>        | [<span data-ttu-id="bff14-199">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-199">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bff14-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bff14-200">Windows Server 2008</span></span>



| <span data-ttu-id="bff14-201">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-201">Entry</span></span> | <span data-ttu-id="bff14-202">值</span><span class="sxs-lookup"><span data-stu-id="bff14-202">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-203">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-204">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-205">System-Only</span></span>            | <span data-ttu-id="bff14-206">否</span><span class="sxs-lookup"><span data-stu-id="bff14-206">False</span></span>                                                              |
| <span data-ttu-id="bff14-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-207">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-208">否</span><span class="sxs-lookup"><span data-stu-id="bff14-208">False</span></span>                                                              |
| <span data-ttu-id="bff14-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-209">Is Indexed</span></span>             | <span data-ttu-id="bff14-210">否</span><span class="sxs-lookup"><span data-stu-id="bff14-210">False</span></span>                                                              |
| <span data-ttu-id="bff14-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-211">In Global Catalog</span></span>      | <span data-ttu-id="bff14-212">否</span><span class="sxs-lookup"><span data-stu-id="bff14-212">False</span></span>                                                              |
| <span data-ttu-id="bff14-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-214">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-215">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-216">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-217">Search-Flags</span></span>           | <span data-ttu-id="bff14-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-218">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-219">System-Flags</span></span>           | <span data-ttu-id="bff14-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-221">Classes used in</span></span>        | [<span data-ttu-id="bff14-222">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-222">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bff14-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bff14-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bff14-224">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-224">Entry</span></span> | <span data-ttu-id="bff14-225">值</span><span class="sxs-lookup"><span data-stu-id="bff14-225">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-226">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-227">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-228">System-Only</span></span>            | <span data-ttu-id="bff14-229">否</span><span class="sxs-lookup"><span data-stu-id="bff14-229">False</span></span>                                                              |
| <span data-ttu-id="bff14-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-230">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-231">否</span><span class="sxs-lookup"><span data-stu-id="bff14-231">False</span></span>                                                              |
| <span data-ttu-id="bff14-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-232">Is Indexed</span></span>             | <span data-ttu-id="bff14-233">否</span><span class="sxs-lookup"><span data-stu-id="bff14-233">False</span></span>                                                              |
| <span data-ttu-id="bff14-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-234">In Global Catalog</span></span>      | <span data-ttu-id="bff14-235">否</span><span class="sxs-lookup"><span data-stu-id="bff14-235">False</span></span>                                                              |
| <span data-ttu-id="bff14-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-237">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-238">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-239">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-240">Search-Flags</span></span>           | <span data-ttu-id="bff14-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-241">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-242">System-Flags</span></span>           | <span data-ttu-id="bff14-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-244">Classes used in</span></span>        | [<span data-ttu-id="bff14-245">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-245">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bff14-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bff14-246">Windows Server 2012</span></span>



| <span data-ttu-id="bff14-247">進入</span><span class="sxs-lookup"><span data-stu-id="bff14-247">Entry</span></span> | <span data-ttu-id="bff14-248">值</span><span class="sxs-lookup"><span data-stu-id="bff14-248">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="bff14-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bff14-249">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bff14-250">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="bff14-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="bff14-251">System-Only</span></span>            | <span data-ttu-id="bff14-252">否</span><span class="sxs-lookup"><span data-stu-id="bff14-252">False</span></span>                                                              |
| <span data-ttu-id="bff14-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bff14-253">Is-Single-Valued</span></span>       | <span data-ttu-id="bff14-254">否</span><span class="sxs-lookup"><span data-stu-id="bff14-254">False</span></span>                                                              |
| <span data-ttu-id="bff14-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bff14-255">Is Indexed</span></span>             | <span data-ttu-id="bff14-256">否</span><span class="sxs-lookup"><span data-stu-id="bff14-256">False</span></span>                                                              |
| <span data-ttu-id="bff14-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bff14-257">In Global Catalog</span></span>      | <span data-ttu-id="bff14-258">否</span><span class="sxs-lookup"><span data-stu-id="bff14-258">False</span></span>                                                              |
| <span data-ttu-id="bff14-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bff14-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="bff14-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bff14-260">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="bff14-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bff14-261">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bff14-262">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="bff14-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-263">Search-Flags</span></span>           | <span data-ttu-id="bff14-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-264">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bff14-265">System-Flags</span></span>           | <span data-ttu-id="bff14-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bff14-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="bff14-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bff14-267">Classes used in</span></span>        | [<span data-ttu-id="bff14-268">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="bff14-268">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





