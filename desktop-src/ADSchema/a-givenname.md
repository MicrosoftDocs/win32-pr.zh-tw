---
title: Given-Name 屬性
description: 包含使用者名字 (名字) 。
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Given-Name 屬性 AD 架構
- givenName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845248"
---
# <a name="given-name-attribute"></a><span data-ttu-id="905c1-105">Given-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="905c1-105">Given-Name attribute</span></span>

<span data-ttu-id="905c1-106">包含使用者名字 (名字) 。</span><span class="sxs-lookup"><span data-stu-id="905c1-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="905c1-107">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-107">Entry</span></span> | <span data-ttu-id="905c1-108">值</span><span class="sxs-lookup"><span data-stu-id="905c1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="905c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="905c1-109">CN</span></span>                | <span data-ttu-id="905c1-110">指定的名稱</span><span class="sxs-lookup"><span data-stu-id="905c1-110">Given-Name</span></span>                                  |
| <span data-ttu-id="905c1-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="905c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="905c1-112">givenName</span><span class="sxs-lookup"><span data-stu-id="905c1-112">givenName</span></span>                                   |
| <span data-ttu-id="905c1-113">大小</span><span class="sxs-lookup"><span data-stu-id="905c1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="905c1-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="905c1-114">Update Privilege</span></span>  | <span data-ttu-id="905c1-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="905c1-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="905c1-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="905c1-116">Update Frequency</span></span>  | <span data-ttu-id="905c1-117">當使用者的記錄建立時。</span><span class="sxs-lookup"><span data-stu-id="905c1-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="905c1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-118">Attribute-Id</span></span>      | <span data-ttu-id="905c1-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="905c1-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="905c1-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="905c1-120">System-Id-Guid</span></span>    | <span data-ttu-id="905c1-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="905c1-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="905c1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="905c1-122">Syntax</span></span>            | [<span data-ttu-id="905c1-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="905c1-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="905c1-124">實作</span><span class="sxs-lookup"><span data-stu-id="905c1-124">Implementations</span></span>

-   [<span data-ttu-id="905c1-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="905c1-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="905c1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="905c1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="905c1-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="905c1-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="905c1-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="905c1-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="905c1-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="905c1-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="905c1-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="905c1-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="905c1-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="905c1-131">Windows 2000 Server</span></span>



| <span data-ttu-id="905c1-132">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-132">Entry</span></span> | <span data-ttu-id="905c1-133">值</span><span class="sxs-lookup"><span data-stu-id="905c1-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="905c1-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="905c1-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-135">MAPI-Id</span></span>                | <span data-ttu-id="905c1-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="905c1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-137">System-Only</span></span>            | <span data-ttu-id="905c1-138">否</span><span class="sxs-lookup"><span data-stu-id="905c1-138">False</span></span>                                                              |
| <span data-ttu-id="905c1-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-140">對</span><span class="sxs-lookup"><span data-stu-id="905c1-140">True</span></span>                                                               |
| <span data-ttu-id="905c1-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-141">Is Indexed</span></span>             | <span data-ttu-id="905c1-142">對</span><span class="sxs-lookup"><span data-stu-id="905c1-142">True</span></span>                                                               |
| <span data-ttu-id="905c1-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-143">In Global Catalog</span></span>      | <span data-ttu-id="905c1-144">對</span><span class="sxs-lookup"><span data-stu-id="905c1-144">True</span></span>                                                               |
| <span data-ttu-id="905c1-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="905c1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-147">Range-Lower</span></span>            | <span data-ttu-id="905c1-148">1</span><span class="sxs-lookup"><span data-stu-id="905c1-148">1</span></span>                                                                  |
| <span data-ttu-id="905c1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-149">Range-Upper</span></span>            | <span data-ttu-id="905c1-150">64</span><span class="sxs-lookup"><span data-stu-id="905c1-150">64</span></span>                                                                 |
| <span data-ttu-id="905c1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-151">Search-Flags</span></span>           | <span data-ttu-id="905c1-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="905c1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-153">System-Flags</span></span>           | <span data-ttu-id="905c1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="905c1-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-155">Classes used in</span></span>        | [<span data-ttu-id="905c1-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="905c1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="905c1-157">Windows Server 2003</span></span>



| <span data-ttu-id="905c1-158">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-158">Entry</span></span> | <span data-ttu-id="905c1-159">值</span><span class="sxs-lookup"><span data-stu-id="905c1-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905c1-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="905c1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-161">MAPI-Id</span></span>                | <span data-ttu-id="905c1-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="905c1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-163">System-Only</span></span>            | <span data-ttu-id="905c1-164">否</span><span class="sxs-lookup"><span data-stu-id="905c1-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="905c1-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-166">對</span><span class="sxs-lookup"><span data-stu-id="905c1-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-167">Is Indexed</span></span>             | <span data-ttu-id="905c1-168">對</span><span class="sxs-lookup"><span data-stu-id="905c1-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-169">In Global Catalog</span></span>      | <span data-ttu-id="905c1-170">對</span><span class="sxs-lookup"><span data-stu-id="905c1-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="905c1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-173">Range-Lower</span></span>            | <span data-ttu-id="905c1-174">1</span><span class="sxs-lookup"><span data-stu-id="905c1-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="905c1-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-175">Range-Upper</span></span>            | <span data-ttu-id="905c1-176">64</span><span class="sxs-lookup"><span data-stu-id="905c1-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="905c1-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-177">Search-Flags</span></span>           | <span data-ttu-id="905c1-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="905c1-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-179">System-Flags</span></span>           | <span data-ttu-id="905c1-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="905c1-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-181">Classes used in</span></span>        | [<span data-ttu-id="905c1-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="905c1-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="905c1-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="905c1-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="905c1-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="905c1-185">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-185">Entry</span></span> | <span data-ttu-id="905c1-186">值</span><span class="sxs-lookup"><span data-stu-id="905c1-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905c1-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="905c1-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-188">MAPI-Id</span></span>                | <span data-ttu-id="905c1-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="905c1-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-190">System-Only</span></span>            | <span data-ttu-id="905c1-191">否</span><span class="sxs-lookup"><span data-stu-id="905c1-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="905c1-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-192">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-193">對</span><span class="sxs-lookup"><span data-stu-id="905c1-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-194">Is Indexed</span></span>             | <span data-ttu-id="905c1-195">對</span><span class="sxs-lookup"><span data-stu-id="905c1-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-196">In Global Catalog</span></span>      | <span data-ttu-id="905c1-197">對</span><span class="sxs-lookup"><span data-stu-id="905c1-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="905c1-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-200">Range-Lower</span></span>            | <span data-ttu-id="905c1-201">1</span><span class="sxs-lookup"><span data-stu-id="905c1-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="905c1-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-202">Range-Upper</span></span>            | <span data-ttu-id="905c1-203">64</span><span class="sxs-lookup"><span data-stu-id="905c1-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="905c1-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-204">Search-Flags</span></span>           | <span data-ttu-id="905c1-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="905c1-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-206">System-Flags</span></span>           | <span data-ttu-id="905c1-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="905c1-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-208">Classes used in</span></span>        | [<span data-ttu-id="905c1-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="905c1-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="905c1-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="905c1-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="905c1-211">Windows Server 2008</span></span>



| <span data-ttu-id="905c1-212">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-212">Entry</span></span> | <span data-ttu-id="905c1-213">值</span><span class="sxs-lookup"><span data-stu-id="905c1-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905c1-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="905c1-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-215">MAPI-Id</span></span>                | <span data-ttu-id="905c1-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="905c1-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-217">System-Only</span></span>            | <span data-ttu-id="905c1-218">否</span><span class="sxs-lookup"><span data-stu-id="905c1-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="905c1-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-219">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-220">對</span><span class="sxs-lookup"><span data-stu-id="905c1-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-221">Is Indexed</span></span>             | <span data-ttu-id="905c1-222">對</span><span class="sxs-lookup"><span data-stu-id="905c1-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-223">In Global Catalog</span></span>      | <span data-ttu-id="905c1-224">對</span><span class="sxs-lookup"><span data-stu-id="905c1-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="905c1-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-227">Range-Lower</span></span>            | <span data-ttu-id="905c1-228">1</span><span class="sxs-lookup"><span data-stu-id="905c1-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="905c1-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-229">Range-Upper</span></span>            | <span data-ttu-id="905c1-230">64</span><span class="sxs-lookup"><span data-stu-id="905c1-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="905c1-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-231">Search-Flags</span></span>           | <span data-ttu-id="905c1-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="905c1-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-233">System-Flags</span></span>           | <span data-ttu-id="905c1-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="905c1-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-235">Classes used in</span></span>        | [<span data-ttu-id="905c1-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="905c1-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="905c1-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="905c1-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="905c1-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="905c1-239">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-239">Entry</span></span> | <span data-ttu-id="905c1-240">值</span><span class="sxs-lookup"><span data-stu-id="905c1-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905c1-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="905c1-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-242">MAPI-Id</span></span>                | <span data-ttu-id="905c1-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="905c1-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-244">System-Only</span></span>            | <span data-ttu-id="905c1-245">否</span><span class="sxs-lookup"><span data-stu-id="905c1-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="905c1-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-246">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-247">對</span><span class="sxs-lookup"><span data-stu-id="905c1-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-248">Is Indexed</span></span>             | <span data-ttu-id="905c1-249">對</span><span class="sxs-lookup"><span data-stu-id="905c1-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-250">In Global Catalog</span></span>      | <span data-ttu-id="905c1-251">對</span><span class="sxs-lookup"><span data-stu-id="905c1-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="905c1-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-254">Range-Lower</span></span>            | <span data-ttu-id="905c1-255">1</span><span class="sxs-lookup"><span data-stu-id="905c1-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="905c1-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-256">Range-Upper</span></span>            | <span data-ttu-id="905c1-257">64</span><span class="sxs-lookup"><span data-stu-id="905c1-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="905c1-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-258">Search-Flags</span></span>           | <span data-ttu-id="905c1-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="905c1-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-260">System-Flags</span></span>           | <span data-ttu-id="905c1-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="905c1-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-262">Classes used in</span></span>        | [<span data-ttu-id="905c1-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="905c1-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="905c1-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="905c1-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="905c1-265">Windows Server 2012</span></span>



| <span data-ttu-id="905c1-266">進入</span><span class="sxs-lookup"><span data-stu-id="905c1-266">Entry</span></span> | <span data-ttu-id="905c1-267">值</span><span class="sxs-lookup"><span data-stu-id="905c1-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905c1-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="905c1-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="905c1-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="905c1-269">MAPI-Id</span></span>                | <span data-ttu-id="905c1-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="905c1-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="905c1-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="905c1-271">System-Only</span></span>            | <span data-ttu-id="905c1-272">否</span><span class="sxs-lookup"><span data-stu-id="905c1-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="905c1-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="905c1-273">Is-Single-Valued</span></span>       | <span data-ttu-id="905c1-274">對</span><span class="sxs-lookup"><span data-stu-id="905c1-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="905c1-275">Is Indexed</span></span>             | <span data-ttu-id="905c1-276">對</span><span class="sxs-lookup"><span data-stu-id="905c1-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="905c1-277">In Global Catalog</span></span>      | <span data-ttu-id="905c1-278">對</span><span class="sxs-lookup"><span data-stu-id="905c1-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="905c1-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="905c1-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="905c1-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="905c1-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="905c1-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="905c1-281">Range-Lower</span></span>            | <span data-ttu-id="905c1-282">1</span><span class="sxs-lookup"><span data-stu-id="905c1-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="905c1-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="905c1-283">Range-Upper</span></span>            | <span data-ttu-id="905c1-284">64</span><span class="sxs-lookup"><span data-stu-id="905c1-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="905c1-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-285">Search-Flags</span></span>           | <span data-ttu-id="905c1-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="905c1-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="905c1-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="905c1-287">System-Flags</span></span>           | <span data-ttu-id="905c1-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="905c1-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="905c1-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="905c1-289">Classes used in</span></span>        | [<span data-ttu-id="905c1-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="905c1-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="905c1-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="905c1-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





