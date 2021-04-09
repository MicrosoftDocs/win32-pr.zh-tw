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
# <a name="given-name-attribute"></a><span data-ttu-id="6a477-105">Given-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="6a477-105">Given-Name attribute</span></span>

<span data-ttu-id="6a477-106">包含使用者名字 (名字) 。</span><span class="sxs-lookup"><span data-stu-id="6a477-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="6a477-107">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-107">Entry</span></span> | <span data-ttu-id="6a477-108">值</span><span class="sxs-lookup"><span data-stu-id="6a477-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6a477-109">CN</span><span class="sxs-lookup"><span data-stu-id="6a477-109">CN</span></span>                | <span data-ttu-id="6a477-110">指定的名稱</span><span class="sxs-lookup"><span data-stu-id="6a477-110">Given-Name</span></span>                                  |
| <span data-ttu-id="6a477-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6a477-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6a477-112">givenName</span><span class="sxs-lookup"><span data-stu-id="6a477-112">givenName</span></span>                                   |
| <span data-ttu-id="6a477-113">大小</span><span class="sxs-lookup"><span data-stu-id="6a477-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="6a477-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6a477-114">Update Privilege</span></span>  | <span data-ttu-id="6a477-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="6a477-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="6a477-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6a477-116">Update Frequency</span></span>  | <span data-ttu-id="6a477-117">當使用者的記錄建立時。</span><span class="sxs-lookup"><span data-stu-id="6a477-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="6a477-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-118">Attribute-Id</span></span>      | <span data-ttu-id="6a477-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="6a477-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="6a477-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6a477-120">System-Id-Guid</span></span>    | <span data-ttu-id="6a477-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="6a477-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="6a477-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a477-122">Syntax</span></span>            | [<span data-ttu-id="6a477-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6a477-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6a477-124">實作</span><span class="sxs-lookup"><span data-stu-id="6a477-124">Implementations</span></span>

-   [<span data-ttu-id="6a477-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6a477-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6a477-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6a477-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6a477-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6a477-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6a477-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6a477-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6a477-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6a477-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6a477-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6a477-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6a477-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a477-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6a477-132">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-132">Entry</span></span> | <span data-ttu-id="6a477-133">值</span><span class="sxs-lookup"><span data-stu-id="6a477-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6a477-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6a477-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-135">MAPI-Id</span></span>                | <span data-ttu-id="6a477-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="6a477-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-137">System-Only</span></span>            | <span data-ttu-id="6a477-138">否</span><span class="sxs-lookup"><span data-stu-id="6a477-138">False</span></span>                                                              |
| <span data-ttu-id="6a477-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-140">對</span><span class="sxs-lookup"><span data-stu-id="6a477-140">True</span></span>                                                               |
| <span data-ttu-id="6a477-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-141">Is Indexed</span></span>             | <span data-ttu-id="6a477-142">對</span><span class="sxs-lookup"><span data-stu-id="6a477-142">True</span></span>                                                               |
| <span data-ttu-id="6a477-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-143">In Global Catalog</span></span>      | <span data-ttu-id="6a477-144">對</span><span class="sxs-lookup"><span data-stu-id="6a477-144">True</span></span>                                                               |
| <span data-ttu-id="6a477-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6a477-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-147">Range-Lower</span></span>            | <span data-ttu-id="6a477-148">1</span><span class="sxs-lookup"><span data-stu-id="6a477-148">1</span></span>                                                                  |
| <span data-ttu-id="6a477-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-149">Range-Upper</span></span>            | <span data-ttu-id="6a477-150">64</span><span class="sxs-lookup"><span data-stu-id="6a477-150">64</span></span>                                                                 |
| <span data-ttu-id="6a477-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-151">Search-Flags</span></span>           | <span data-ttu-id="6a477-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="6a477-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-153">System-Flags</span></span>           | <span data-ttu-id="6a477-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="6a477-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-155">Classes used in</span></span>        | [<span data-ttu-id="6a477-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6a477-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a477-157">Windows Server 2003</span></span>



| <span data-ttu-id="6a477-158">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-158">Entry</span></span> | <span data-ttu-id="6a477-159">值</span><span class="sxs-lookup"><span data-stu-id="6a477-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a477-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="6a477-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-161">MAPI-Id</span></span>                | <span data-ttu-id="6a477-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="6a477-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-163">System-Only</span></span>            | <span data-ttu-id="6a477-164">否</span><span class="sxs-lookup"><span data-stu-id="6a477-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="6a477-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-165">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-166">對</span><span class="sxs-lookup"><span data-stu-id="6a477-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-167">Is Indexed</span></span>             | <span data-ttu-id="6a477-168">對</span><span class="sxs-lookup"><span data-stu-id="6a477-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-169">In Global Catalog</span></span>      | <span data-ttu-id="6a477-170">對</span><span class="sxs-lookup"><span data-stu-id="6a477-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="6a477-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-173">Range-Lower</span></span>            | <span data-ttu-id="6a477-174">1</span><span class="sxs-lookup"><span data-stu-id="6a477-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="6a477-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-175">Range-Upper</span></span>            | <span data-ttu-id="6a477-176">64</span><span class="sxs-lookup"><span data-stu-id="6a477-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="6a477-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-177">Search-Flags</span></span>           | <span data-ttu-id="6a477-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="6a477-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-179">System-Flags</span></span>           | <span data-ttu-id="6a477-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="6a477-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-181">Classes used in</span></span>        | [<span data-ttu-id="6a477-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="6a477-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="6a477-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6a477-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6a477-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6a477-185">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-185">Entry</span></span> | <span data-ttu-id="6a477-186">值</span><span class="sxs-lookup"><span data-stu-id="6a477-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a477-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="6a477-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-188">MAPI-Id</span></span>                | <span data-ttu-id="6a477-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="6a477-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-190">System-Only</span></span>            | <span data-ttu-id="6a477-191">否</span><span class="sxs-lookup"><span data-stu-id="6a477-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="6a477-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-192">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-193">對</span><span class="sxs-lookup"><span data-stu-id="6a477-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-194">Is Indexed</span></span>             | <span data-ttu-id="6a477-195">對</span><span class="sxs-lookup"><span data-stu-id="6a477-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-196">In Global Catalog</span></span>      | <span data-ttu-id="6a477-197">對</span><span class="sxs-lookup"><span data-stu-id="6a477-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="6a477-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-200">Range-Lower</span></span>            | <span data-ttu-id="6a477-201">1</span><span class="sxs-lookup"><span data-stu-id="6a477-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="6a477-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-202">Range-Upper</span></span>            | <span data-ttu-id="6a477-203">64</span><span class="sxs-lookup"><span data-stu-id="6a477-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="6a477-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-204">Search-Flags</span></span>           | <span data-ttu-id="6a477-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="6a477-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-206">System-Flags</span></span>           | <span data-ttu-id="6a477-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="6a477-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-208">Classes used in</span></span>        | [<span data-ttu-id="6a477-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="6a477-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="6a477-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6a477-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a477-211">Windows Server 2008</span></span>



| <span data-ttu-id="6a477-212">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-212">Entry</span></span> | <span data-ttu-id="6a477-213">值</span><span class="sxs-lookup"><span data-stu-id="6a477-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a477-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="6a477-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-215">MAPI-Id</span></span>                | <span data-ttu-id="6a477-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="6a477-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-217">System-Only</span></span>            | <span data-ttu-id="6a477-218">否</span><span class="sxs-lookup"><span data-stu-id="6a477-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="6a477-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-219">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-220">對</span><span class="sxs-lookup"><span data-stu-id="6a477-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-221">Is Indexed</span></span>             | <span data-ttu-id="6a477-222">對</span><span class="sxs-lookup"><span data-stu-id="6a477-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-223">In Global Catalog</span></span>      | <span data-ttu-id="6a477-224">對</span><span class="sxs-lookup"><span data-stu-id="6a477-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="6a477-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-227">Range-Lower</span></span>            | <span data-ttu-id="6a477-228">1</span><span class="sxs-lookup"><span data-stu-id="6a477-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="6a477-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-229">Range-Upper</span></span>            | <span data-ttu-id="6a477-230">64</span><span class="sxs-lookup"><span data-stu-id="6a477-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="6a477-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-231">Search-Flags</span></span>           | <span data-ttu-id="6a477-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="6a477-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-233">System-Flags</span></span>           | <span data-ttu-id="6a477-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="6a477-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-235">Classes used in</span></span>        | [<span data-ttu-id="6a477-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="6a477-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="6a477-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6a477-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a477-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6a477-239">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-239">Entry</span></span> | <span data-ttu-id="6a477-240">值</span><span class="sxs-lookup"><span data-stu-id="6a477-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a477-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="6a477-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-242">MAPI-Id</span></span>                | <span data-ttu-id="6a477-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="6a477-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-244">System-Only</span></span>            | <span data-ttu-id="6a477-245">否</span><span class="sxs-lookup"><span data-stu-id="6a477-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="6a477-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-246">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-247">對</span><span class="sxs-lookup"><span data-stu-id="6a477-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-248">Is Indexed</span></span>             | <span data-ttu-id="6a477-249">對</span><span class="sxs-lookup"><span data-stu-id="6a477-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-250">In Global Catalog</span></span>      | <span data-ttu-id="6a477-251">對</span><span class="sxs-lookup"><span data-stu-id="6a477-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="6a477-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-254">Range-Lower</span></span>            | <span data-ttu-id="6a477-255">1</span><span class="sxs-lookup"><span data-stu-id="6a477-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="6a477-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-256">Range-Upper</span></span>            | <span data-ttu-id="6a477-257">64</span><span class="sxs-lookup"><span data-stu-id="6a477-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="6a477-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-258">Search-Flags</span></span>           | <span data-ttu-id="6a477-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="6a477-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-260">System-Flags</span></span>           | <span data-ttu-id="6a477-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="6a477-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-262">Classes used in</span></span>        | [<span data-ttu-id="6a477-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="6a477-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="6a477-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6a477-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a477-265">Windows Server 2012</span></span>



| <span data-ttu-id="6a477-266">進入</span><span class="sxs-lookup"><span data-stu-id="6a477-266">Entry</span></span> | <span data-ttu-id="6a477-267">值</span><span class="sxs-lookup"><span data-stu-id="6a477-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a477-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6a477-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="6a477-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6a477-269">MAPI-Id</span></span>                | <span data-ttu-id="6a477-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="6a477-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="6a477-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="6a477-271">System-Only</span></span>            | <span data-ttu-id="6a477-272">否</span><span class="sxs-lookup"><span data-stu-id="6a477-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="6a477-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6a477-273">Is-Single-Valued</span></span>       | <span data-ttu-id="6a477-274">對</span><span class="sxs-lookup"><span data-stu-id="6a477-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6a477-275">Is Indexed</span></span>             | <span data-ttu-id="6a477-276">對</span><span class="sxs-lookup"><span data-stu-id="6a477-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6a477-277">In Global Catalog</span></span>      | <span data-ttu-id="6a477-278">對</span><span class="sxs-lookup"><span data-stu-id="6a477-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="6a477-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6a477-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="6a477-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6a477-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="6a477-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6a477-281">Range-Lower</span></span>            | <span data-ttu-id="6a477-282">1</span><span class="sxs-lookup"><span data-stu-id="6a477-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="6a477-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6a477-283">Range-Upper</span></span>            | <span data-ttu-id="6a477-284">64</span><span class="sxs-lookup"><span data-stu-id="6a477-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="6a477-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-285">Search-Flags</span></span>           | <span data-ttu-id="6a477-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="6a477-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="6a477-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6a477-287">System-Flags</span></span>           | <span data-ttu-id="6a477-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6a477-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="6a477-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6a477-289">Classes used in</span></span>        | [<span data-ttu-id="6a477-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="6a477-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="6a477-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6a477-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





