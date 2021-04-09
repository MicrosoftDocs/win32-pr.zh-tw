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
# <a name="given-name-attribute"></a><span data-ttu-id="4c502-105">Given-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="4c502-105">Given-Name attribute</span></span>

<span data-ttu-id="4c502-106">包含使用者名字 (名字) 。</span><span class="sxs-lookup"><span data-stu-id="4c502-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="4c502-107">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-107">Entry</span></span> | <span data-ttu-id="4c502-108">值</span><span class="sxs-lookup"><span data-stu-id="4c502-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4c502-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c502-109">CN</span></span>                | <span data-ttu-id="4c502-110">指定的名稱</span><span class="sxs-lookup"><span data-stu-id="4c502-110">Given-Name</span></span>                                  |
| <span data-ttu-id="4c502-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4c502-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c502-112">givenName</span><span class="sxs-lookup"><span data-stu-id="4c502-112">givenName</span></span>                                   |
| <span data-ttu-id="4c502-113">大小</span><span class="sxs-lookup"><span data-stu-id="4c502-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4c502-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="4c502-114">Update Privilege</span></span>  | <span data-ttu-id="4c502-115">網域系統管理員或帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="4c502-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="4c502-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="4c502-116">Update Frequency</span></span>  | <span data-ttu-id="4c502-117">當使用者的記錄建立時。</span><span class="sxs-lookup"><span data-stu-id="4c502-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="4c502-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-118">Attribute-Id</span></span>      | <span data-ttu-id="4c502-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="4c502-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="4c502-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="4c502-120">System-Id-Guid</span></span>    | <span data-ttu-id="4c502-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="4c502-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="4c502-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c502-122">Syntax</span></span>            | [<span data-ttu-id="4c502-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="4c502-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4c502-124">實作</span><span class="sxs-lookup"><span data-stu-id="4c502-124">Implementations</span></span>

-   [<span data-ttu-id="4c502-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4c502-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4c502-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c502-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c502-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c502-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c502-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c502-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c502-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c502-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c502-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c502-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4c502-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c502-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4c502-132">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-132">Entry</span></span> | <span data-ttu-id="4c502-133">值</span><span class="sxs-lookup"><span data-stu-id="4c502-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4c502-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="4c502-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-135">MAPI-Id</span></span>                | <span data-ttu-id="4c502-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="4c502-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-137">System-Only</span></span>            | <span data-ttu-id="4c502-138">否</span><span class="sxs-lookup"><span data-stu-id="4c502-138">False</span></span>                                                              |
| <span data-ttu-id="4c502-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-140">對</span><span class="sxs-lookup"><span data-stu-id="4c502-140">True</span></span>                                                               |
| <span data-ttu-id="4c502-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-141">Is Indexed</span></span>             | <span data-ttu-id="4c502-142">對</span><span class="sxs-lookup"><span data-stu-id="4c502-142">True</span></span>                                                               |
| <span data-ttu-id="4c502-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-143">In Global Catalog</span></span>      | <span data-ttu-id="4c502-144">對</span><span class="sxs-lookup"><span data-stu-id="4c502-144">True</span></span>                                                               |
| <span data-ttu-id="4c502-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="4c502-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-147">Range-Lower</span></span>            | <span data-ttu-id="4c502-148">1</span><span class="sxs-lookup"><span data-stu-id="4c502-148">1</span></span>                                                                  |
| <span data-ttu-id="4c502-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-149">Range-Upper</span></span>            | <span data-ttu-id="4c502-150">64</span><span class="sxs-lookup"><span data-stu-id="4c502-150">64</span></span>                                                                 |
| <span data-ttu-id="4c502-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-151">Search-Flags</span></span>           | <span data-ttu-id="4c502-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="4c502-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-153">System-Flags</span></span>           | <span data-ttu-id="4c502-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="4c502-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-155">Classes used in</span></span>        | [<span data-ttu-id="4c502-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4c502-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c502-157">Windows Server 2003</span></span>



| <span data-ttu-id="4c502-158">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-158">Entry</span></span> | <span data-ttu-id="4c502-159">值</span><span class="sxs-lookup"><span data-stu-id="4c502-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c502-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="4c502-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-161">MAPI-Id</span></span>                | <span data-ttu-id="4c502-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="4c502-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-163">System-Only</span></span>            | <span data-ttu-id="4c502-164">否</span><span class="sxs-lookup"><span data-stu-id="4c502-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="4c502-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-166">對</span><span class="sxs-lookup"><span data-stu-id="4c502-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-167">Is Indexed</span></span>             | <span data-ttu-id="4c502-168">對</span><span class="sxs-lookup"><span data-stu-id="4c502-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-169">In Global Catalog</span></span>      | <span data-ttu-id="4c502-170">對</span><span class="sxs-lookup"><span data-stu-id="4c502-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="4c502-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-173">Range-Lower</span></span>            | <span data-ttu-id="4c502-174">1</span><span class="sxs-lookup"><span data-stu-id="4c502-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="4c502-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-175">Range-Upper</span></span>            | <span data-ttu-id="4c502-176">64</span><span class="sxs-lookup"><span data-stu-id="4c502-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="4c502-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-177">Search-Flags</span></span>           | <span data-ttu-id="4c502-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="4c502-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-179">System-Flags</span></span>           | <span data-ttu-id="4c502-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="4c502-181">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-181">Classes used in</span></span>        | [<span data-ttu-id="4c502-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4c502-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="4c502-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c502-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c502-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c502-185">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-185">Entry</span></span> | <span data-ttu-id="4c502-186">值</span><span class="sxs-lookup"><span data-stu-id="4c502-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c502-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="4c502-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-188">MAPI-Id</span></span>                | <span data-ttu-id="4c502-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="4c502-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-190">System-Only</span></span>            | <span data-ttu-id="4c502-191">否</span><span class="sxs-lookup"><span data-stu-id="4c502-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="4c502-192">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-192">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-193">對</span><span class="sxs-lookup"><span data-stu-id="4c502-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-194">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-194">Is Indexed</span></span>             | <span data-ttu-id="4c502-195">對</span><span class="sxs-lookup"><span data-stu-id="4c502-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-196">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-196">In Global Catalog</span></span>      | <span data-ttu-id="4c502-197">對</span><span class="sxs-lookup"><span data-stu-id="4c502-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-198">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-199">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="4c502-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-200">Range-Lower</span></span>            | <span data-ttu-id="4c502-201">1</span><span class="sxs-lookup"><span data-stu-id="4c502-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="4c502-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-202">Range-Upper</span></span>            | <span data-ttu-id="4c502-203">64</span><span class="sxs-lookup"><span data-stu-id="4c502-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="4c502-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-204">Search-Flags</span></span>           | <span data-ttu-id="4c502-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="4c502-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-206">System-Flags</span></span>           | <span data-ttu-id="4c502-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="4c502-208">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-208">Classes used in</span></span>        | [<span data-ttu-id="4c502-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4c502-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="4c502-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c502-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c502-211">Windows Server 2008</span></span>



| <span data-ttu-id="4c502-212">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-212">Entry</span></span> | <span data-ttu-id="4c502-213">值</span><span class="sxs-lookup"><span data-stu-id="4c502-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c502-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="4c502-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-215">MAPI-Id</span></span>                | <span data-ttu-id="4c502-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="4c502-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-217">System-Only</span></span>            | <span data-ttu-id="4c502-218">否</span><span class="sxs-lookup"><span data-stu-id="4c502-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="4c502-219">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-219">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-220">對</span><span class="sxs-lookup"><span data-stu-id="4c502-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-221">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-221">Is Indexed</span></span>             | <span data-ttu-id="4c502-222">對</span><span class="sxs-lookup"><span data-stu-id="4c502-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-223">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-223">In Global Catalog</span></span>      | <span data-ttu-id="4c502-224">對</span><span class="sxs-lookup"><span data-stu-id="4c502-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-225">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-226">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="4c502-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-227">Range-Lower</span></span>            | <span data-ttu-id="4c502-228">1</span><span class="sxs-lookup"><span data-stu-id="4c502-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="4c502-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-229">Range-Upper</span></span>            | <span data-ttu-id="4c502-230">64</span><span class="sxs-lookup"><span data-stu-id="4c502-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="4c502-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-231">Search-Flags</span></span>           | <span data-ttu-id="4c502-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="4c502-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-233">System-Flags</span></span>           | <span data-ttu-id="4c502-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="4c502-235">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-235">Classes used in</span></span>        | [<span data-ttu-id="4c502-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4c502-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="4c502-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c502-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c502-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c502-239">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-239">Entry</span></span> | <span data-ttu-id="4c502-240">值</span><span class="sxs-lookup"><span data-stu-id="4c502-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c502-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="4c502-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-242">MAPI-Id</span></span>                | <span data-ttu-id="4c502-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="4c502-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-244">System-Only</span></span>            | <span data-ttu-id="4c502-245">否</span><span class="sxs-lookup"><span data-stu-id="4c502-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="4c502-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-246">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-247">對</span><span class="sxs-lookup"><span data-stu-id="4c502-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-248">Is Indexed</span></span>             | <span data-ttu-id="4c502-249">對</span><span class="sxs-lookup"><span data-stu-id="4c502-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-250">In Global Catalog</span></span>      | <span data-ttu-id="4c502-251">對</span><span class="sxs-lookup"><span data-stu-id="4c502-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="4c502-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-254">Range-Lower</span></span>            | <span data-ttu-id="4c502-255">1</span><span class="sxs-lookup"><span data-stu-id="4c502-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="4c502-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-256">Range-Upper</span></span>            | <span data-ttu-id="4c502-257">64</span><span class="sxs-lookup"><span data-stu-id="4c502-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="4c502-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-258">Search-Flags</span></span>           | <span data-ttu-id="4c502-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="4c502-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-260">System-Flags</span></span>           | <span data-ttu-id="4c502-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="4c502-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-262">Classes used in</span></span>        | [<span data-ttu-id="4c502-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4c502-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="4c502-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c502-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c502-265">Windows Server 2012</span></span>



| <span data-ttu-id="4c502-266">進入</span><span class="sxs-lookup"><span data-stu-id="4c502-266">Entry</span></span> | <span data-ttu-id="4c502-267">值</span><span class="sxs-lookup"><span data-stu-id="4c502-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c502-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="4c502-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="4c502-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c502-269">MAPI-Id</span></span>                | <span data-ttu-id="4c502-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="4c502-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="4c502-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c502-271">System-Only</span></span>            | <span data-ttu-id="4c502-272">否</span><span class="sxs-lookup"><span data-stu-id="4c502-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="4c502-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="4c502-273">Is-Single-Valued</span></span>       | <span data-ttu-id="4c502-274">對</span><span class="sxs-lookup"><span data-stu-id="4c502-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="4c502-275">Is Indexed</span></span>             | <span data-ttu-id="4c502-276">對</span><span class="sxs-lookup"><span data-stu-id="4c502-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="4c502-277">In Global Catalog</span></span>      | <span data-ttu-id="4c502-278">對</span><span class="sxs-lookup"><span data-stu-id="4c502-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="4c502-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="4c502-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c502-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="4c502-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="4c502-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c502-281">Range-Lower</span></span>            | <span data-ttu-id="4c502-282">1</span><span class="sxs-lookup"><span data-stu-id="4c502-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="4c502-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c502-283">Range-Upper</span></span>            | <span data-ttu-id="4c502-284">64</span><span class="sxs-lookup"><span data-stu-id="4c502-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="4c502-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-285">Search-Flags</span></span>           | <span data-ttu-id="4c502-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c502-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="4c502-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c502-287">System-Flags</span></span>           | <span data-ttu-id="4c502-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c502-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="4c502-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="4c502-289">Classes used in</span></span>        | [<span data-ttu-id="4c502-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="4c502-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="4c502-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="4c502-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





