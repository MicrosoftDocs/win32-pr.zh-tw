---
title: Address 屬性
description: 使用者的位址。
ms.assetid: e8dfd384-6617-4a2b-bead-50b5c0a94f8e
ms.tgt_platform: multiple
keywords:
- 位址屬性 AD 架構
- streetAddress 屬性 AD 架構
topic_type:
- apiref
api_name:
- Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 331f431752e35c1a6628a9d2eb0146962230995d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104025550"
---
# <a name="address-attribute"></a><span data-ttu-id="8c814-105">Address 屬性</span><span class="sxs-lookup"><span data-stu-id="8c814-105">Address attribute</span></span>

<span data-ttu-id="8c814-106">使用者的位址。</span><span class="sxs-lookup"><span data-stu-id="8c814-106">The user's address.</span></span>



| <span data-ttu-id="8c814-107">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-107">Entry</span></span> | <span data-ttu-id="8c814-108">值</span><span class="sxs-lookup"><span data-stu-id="8c814-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8c814-109">CN</span><span class="sxs-lookup"><span data-stu-id="8c814-109">CN</span></span>                | <span data-ttu-id="8c814-110">位址</span><span class="sxs-lookup"><span data-stu-id="8c814-110">Address</span></span>                                     |
| <span data-ttu-id="8c814-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8c814-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8c814-112">streetAddress</span><span class="sxs-lookup"><span data-stu-id="8c814-112">streetAddress</span></span>                               |
| <span data-ttu-id="8c814-113">大小</span><span class="sxs-lookup"><span data-stu-id="8c814-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8c814-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="8c814-114">Update Privilege</span></span>  | <span data-ttu-id="8c814-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="8c814-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8c814-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="8c814-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8c814-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-117">Attribute-Id</span></span>      | <span data-ttu-id="8c814-118">1.2.840.113556.1.2.256</span><span class="sxs-lookup"><span data-stu-id="8c814-118">1.2.840.113556.1.2.256</span></span>                      |
| <span data-ttu-id="8c814-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="8c814-119">System-Id-Guid</span></span>    | <span data-ttu-id="8c814-120">f0f8ff84-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="8c814-120">f0f8ff84-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="8c814-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c814-121">Syntax</span></span>            | [<span data-ttu-id="8c814-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8c814-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8c814-123">實作</span><span class="sxs-lookup"><span data-stu-id="8c814-123">Implementations</span></span>

-   [<span data-ttu-id="8c814-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8c814-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8c814-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8c814-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8c814-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8c814-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8c814-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8c814-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8c814-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8c814-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8c814-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8c814-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8c814-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c814-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8c814-131">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-131">Entry</span></span> | <span data-ttu-id="8c814-132">值</span><span class="sxs-lookup"><span data-stu-id="8c814-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-134">MAPI-Id</span></span>                | <span data-ttu-id="8c814-135">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-135">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-136">System-Only</span></span>            | <span data-ttu-id="8c814-137">否</span><span class="sxs-lookup"><span data-stu-id="8c814-137">False</span></span>                                                              |
| <span data-ttu-id="8c814-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-139">對</span><span class="sxs-lookup"><span data-stu-id="8c814-139">True</span></span>                                                               |
| <span data-ttu-id="8c814-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-140">Is Indexed</span></span>             | <span data-ttu-id="8c814-141">否</span><span class="sxs-lookup"><span data-stu-id="8c814-141">False</span></span>                                                              |
| <span data-ttu-id="8c814-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-142">In Global Catalog</span></span>      | <span data-ttu-id="8c814-143">否</span><span class="sxs-lookup"><span data-stu-id="8c814-143">False</span></span>                                                              |
| <span data-ttu-id="8c814-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-146">Range-Lower</span></span>            | <span data-ttu-id="8c814-147">1</span><span class="sxs-lookup"><span data-stu-id="8c814-147">1</span></span>                                                                  |
| <span data-ttu-id="8c814-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-148">Range-Upper</span></span>            | <span data-ttu-id="8c814-149">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-149">1024</span></span>                                                               |
| <span data-ttu-id="8c814-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-150">Search-Flags</span></span>           | <span data-ttu-id="8c814-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-152">System-Flags</span></span>           | <span data-ttu-id="8c814-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-154">Classes used in</span></span>        | [<span data-ttu-id="8c814-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8c814-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c814-156">Windows Server 2003</span></span>



| <span data-ttu-id="8c814-157">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-157">Entry</span></span> | <span data-ttu-id="8c814-158">值</span><span class="sxs-lookup"><span data-stu-id="8c814-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-160">MAPI-Id</span></span>                | <span data-ttu-id="8c814-161">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-161">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-162">System-Only</span></span>            | <span data-ttu-id="8c814-163">否</span><span class="sxs-lookup"><span data-stu-id="8c814-163">False</span></span>                                                              |
| <span data-ttu-id="8c814-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-165">對</span><span class="sxs-lookup"><span data-stu-id="8c814-165">True</span></span>                                                               |
| <span data-ttu-id="8c814-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-166">Is Indexed</span></span>             | <span data-ttu-id="8c814-167">否</span><span class="sxs-lookup"><span data-stu-id="8c814-167">False</span></span>                                                              |
| <span data-ttu-id="8c814-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-168">In Global Catalog</span></span>      | <span data-ttu-id="8c814-169">否</span><span class="sxs-lookup"><span data-stu-id="8c814-169">False</span></span>                                                              |
| <span data-ttu-id="8c814-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-171">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-172">Range-Lower</span></span>            | <span data-ttu-id="8c814-173">1</span><span class="sxs-lookup"><span data-stu-id="8c814-173">1</span></span>                                                                  |
| <span data-ttu-id="8c814-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-174">Range-Upper</span></span>            | <span data-ttu-id="8c814-175">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-175">1024</span></span>                                                               |
| <span data-ttu-id="8c814-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-176">Search-Flags</span></span>           | <span data-ttu-id="8c814-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-177">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-178">System-Flags</span></span>           | <span data-ttu-id="8c814-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-179">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-180">Classes used in</span></span>        | [<span data-ttu-id="8c814-181">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-181">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8c814-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8c814-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8c814-183">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-183">Entry</span></span> | <span data-ttu-id="8c814-184">值</span><span class="sxs-lookup"><span data-stu-id="8c814-184">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-185">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-186">MAPI-Id</span></span>                | <span data-ttu-id="8c814-187">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-187">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-188">System-Only</span></span>            | <span data-ttu-id="8c814-189">否</span><span class="sxs-lookup"><span data-stu-id="8c814-189">False</span></span>                                                              |
| <span data-ttu-id="8c814-190">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-190">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-191">對</span><span class="sxs-lookup"><span data-stu-id="8c814-191">True</span></span>                                                               |
| <span data-ttu-id="8c814-192">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-192">Is Indexed</span></span>             | <span data-ttu-id="8c814-193">否</span><span class="sxs-lookup"><span data-stu-id="8c814-193">False</span></span>                                                              |
| <span data-ttu-id="8c814-194">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-194">In Global Catalog</span></span>      | <span data-ttu-id="8c814-195">否</span><span class="sxs-lookup"><span data-stu-id="8c814-195">False</span></span>                                                              |
| <span data-ttu-id="8c814-196">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-197">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-197">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-198">Range-Lower</span></span>            | <span data-ttu-id="8c814-199">1</span><span class="sxs-lookup"><span data-stu-id="8c814-199">1</span></span>                                                                  |
| <span data-ttu-id="8c814-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-200">Range-Upper</span></span>            | <span data-ttu-id="8c814-201">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-201">1024</span></span>                                                               |
| <span data-ttu-id="8c814-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-202">Search-Flags</span></span>           | <span data-ttu-id="8c814-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-203">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-204">System-Flags</span></span>           | <span data-ttu-id="8c814-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-205">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-206">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-206">Classes used in</span></span>        | [<span data-ttu-id="8c814-207">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-207">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8c814-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c814-208">Windows Server 2008</span></span>



| <span data-ttu-id="8c814-209">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-209">Entry</span></span> | <span data-ttu-id="8c814-210">值</span><span class="sxs-lookup"><span data-stu-id="8c814-210">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-211">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-211">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-212">MAPI-Id</span></span>                | <span data-ttu-id="8c814-213">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-213">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-214">System-Only</span></span>            | <span data-ttu-id="8c814-215">否</span><span class="sxs-lookup"><span data-stu-id="8c814-215">False</span></span>                                                              |
| <span data-ttu-id="8c814-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-216">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-217">對</span><span class="sxs-lookup"><span data-stu-id="8c814-217">True</span></span>                                                               |
| <span data-ttu-id="8c814-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-218">Is Indexed</span></span>             | <span data-ttu-id="8c814-219">否</span><span class="sxs-lookup"><span data-stu-id="8c814-219">False</span></span>                                                              |
| <span data-ttu-id="8c814-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-220">In Global Catalog</span></span>      | <span data-ttu-id="8c814-221">否</span><span class="sxs-lookup"><span data-stu-id="8c814-221">False</span></span>                                                              |
| <span data-ttu-id="8c814-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-223">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-224">Range-Lower</span></span>            | <span data-ttu-id="8c814-225">1</span><span class="sxs-lookup"><span data-stu-id="8c814-225">1</span></span>                                                                  |
| <span data-ttu-id="8c814-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-226">Range-Upper</span></span>            | <span data-ttu-id="8c814-227">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-227">1024</span></span>                                                               |
| <span data-ttu-id="8c814-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-228">Search-Flags</span></span>           | <span data-ttu-id="8c814-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-229">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-230">System-Flags</span></span>           | <span data-ttu-id="8c814-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-231">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-232">Classes used in</span></span>        | [<span data-ttu-id="8c814-233">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-233">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8c814-234">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8c814-234">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8c814-235">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-235">Entry</span></span> | <span data-ttu-id="8c814-236">值</span><span class="sxs-lookup"><span data-stu-id="8c814-236">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-237">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-238">MAPI-Id</span></span>                | <span data-ttu-id="8c814-239">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-239">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-240">System-Only</span></span>            | <span data-ttu-id="8c814-241">否</span><span class="sxs-lookup"><span data-stu-id="8c814-241">False</span></span>                                                              |
| <span data-ttu-id="8c814-242">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-242">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-243">對</span><span class="sxs-lookup"><span data-stu-id="8c814-243">True</span></span>                                                               |
| <span data-ttu-id="8c814-244">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-244">Is Indexed</span></span>             | <span data-ttu-id="8c814-245">否</span><span class="sxs-lookup"><span data-stu-id="8c814-245">False</span></span>                                                              |
| <span data-ttu-id="8c814-246">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-246">In Global Catalog</span></span>      | <span data-ttu-id="8c814-247">否</span><span class="sxs-lookup"><span data-stu-id="8c814-247">False</span></span>                                                              |
| <span data-ttu-id="8c814-248">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-249">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-249">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-250">Range-Lower</span></span>            | <span data-ttu-id="8c814-251">1</span><span class="sxs-lookup"><span data-stu-id="8c814-251">1</span></span>                                                                  |
| <span data-ttu-id="8c814-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-252">Range-Upper</span></span>            | <span data-ttu-id="8c814-253">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-253">1024</span></span>                                                               |
| <span data-ttu-id="8c814-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-254">Search-Flags</span></span>           | <span data-ttu-id="8c814-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-255">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-256">System-Flags</span></span>           | <span data-ttu-id="8c814-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-257">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-258">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-258">Classes used in</span></span>        | [<span data-ttu-id="8c814-259">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-259">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8c814-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c814-260">Windows Server 2012</span></span>



| <span data-ttu-id="8c814-261">進入</span><span class="sxs-lookup"><span data-stu-id="8c814-261">Entry</span></span> | <span data-ttu-id="8c814-262">值</span><span class="sxs-lookup"><span data-stu-id="8c814-262">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8c814-263">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="8c814-263">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8c814-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8c814-264">MAPI-Id</span></span>                | <span data-ttu-id="8c814-265">0x3A29</span><span class="sxs-lookup"><span data-stu-id="8c814-265">0x3A29</span></span>                                                             |
| <span data-ttu-id="8c814-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="8c814-266">System-Only</span></span>            | <span data-ttu-id="8c814-267">否</span><span class="sxs-lookup"><span data-stu-id="8c814-267">False</span></span>                                                              |
| <span data-ttu-id="8c814-268">是-單一值</span><span class="sxs-lookup"><span data-stu-id="8c814-268">Is-Single-Valued</span></span>       | <span data-ttu-id="8c814-269">對</span><span class="sxs-lookup"><span data-stu-id="8c814-269">True</span></span>                                                               |
| <span data-ttu-id="8c814-270">已編制索引</span><span class="sxs-lookup"><span data-stu-id="8c814-270">Is Indexed</span></span>             | <span data-ttu-id="8c814-271">否</span><span class="sxs-lookup"><span data-stu-id="8c814-271">False</span></span>                                                              |
| <span data-ttu-id="8c814-272">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="8c814-272">In Global Catalog</span></span>      | <span data-ttu-id="8c814-273">否</span><span class="sxs-lookup"><span data-stu-id="8c814-273">False</span></span>                                                              |
| <span data-ttu-id="8c814-274">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="8c814-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="8c814-275">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="8c814-275">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8c814-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8c814-276">Range-Lower</span></span>            | <span data-ttu-id="8c814-277">1</span><span class="sxs-lookup"><span data-stu-id="8c814-277">1</span></span>                                                                  |
| <span data-ttu-id="8c814-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8c814-278">Range-Upper</span></span>            | <span data-ttu-id="8c814-279">1024</span><span class="sxs-lookup"><span data-stu-id="8c814-279">1024</span></span>                                                               |
| <span data-ttu-id="8c814-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-280">Search-Flags</span></span>           | <span data-ttu-id="8c814-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c814-281">0x00000000</span></span>                                                         |
| <span data-ttu-id="8c814-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8c814-282">System-Flags</span></span>           | <span data-ttu-id="8c814-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8c814-283">0x00000010</span></span>                                                         |
| <span data-ttu-id="8c814-284">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="8c814-284">Classes used in</span></span>        | [<span data-ttu-id="8c814-285">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="8c814-285">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





