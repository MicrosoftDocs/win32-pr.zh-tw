---
title: ms-DS-安全性群組-額外類別屬性
description: 可透過 Active Directory 消費者和電腦嵌入式管理單元新增至安全性群組之非標準類別的一般名稱。
ms.assetid: 3808cb03-3d54-46ca-bad8-23120ed2ca07
ms.tgt_platform: multiple
keywords:
- ms-DS-安全性群組-額外類別的屬性 AD 架構
- 安全性群組-額外類別的屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3860cc80c669eaad30262cce63aff6dca3a2a8f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108121"
---
# <a name="ms-ds-security-group-extra-classes-attribute"></a><span data-ttu-id="43e06-105">ms-DS-安全性群組-額外類別屬性</span><span class="sxs-lookup"><span data-stu-id="43e06-105">ms-DS-Security-Group-Extra-Classes attribute</span></span>

<span data-ttu-id="43e06-106">可透過 Active Directory 消費者和電腦嵌入式管理單元新增至安全性群組之非標準類別的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="43e06-106">The common names of the nonstandard classes that can be added to a security group through the Active Directory Users and Computers snap-in.</span></span>



| <span data-ttu-id="43e06-107">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-107">Entry</span></span> | <span data-ttu-id="43e06-108">值</span><span class="sxs-lookup"><span data-stu-id="43e06-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="43e06-109">CN</span><span class="sxs-lookup"><span data-stu-id="43e06-109">CN</span></span>                | <span data-ttu-id="43e06-110">ms-DS-安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="43e06-110">ms-DS-Security-Group-Extra-Classes</span></span>          |
| <span data-ttu-id="43e06-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="43e06-111">Ldap-Display-Name</span></span> | <span data-ttu-id="43e06-112">安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="43e06-112">msDS-Security-Group-Extra-Classes</span></span>           |
| <span data-ttu-id="43e06-113">大小</span><span class="sxs-lookup"><span data-stu-id="43e06-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="43e06-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="43e06-114">Update Privilege</span></span>  | <span data-ttu-id="43e06-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="43e06-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="43e06-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="43e06-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="43e06-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-117">Attribute-Id</span></span>      | <span data-ttu-id="43e06-118">1.2.840.113556.1.4.1688</span><span class="sxs-lookup"><span data-stu-id="43e06-118">1.2.840.113556.1.4.1688</span></span>                     |
| <span data-ttu-id="43e06-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="43e06-119">System-Id-Guid</span></span>    | <span data-ttu-id="43e06-120">4f146ae8-a4fe-4801-a731-f51848a4f4e4</span><span class="sxs-lookup"><span data-stu-id="43e06-120">4f146ae8-a4fe-4801-a731-f51848a4f4e4</span></span>        |
| <span data-ttu-id="43e06-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="43e06-121">Syntax</span></span>            | [<span data-ttu-id="43e06-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="43e06-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="43e06-123">實作</span><span class="sxs-lookup"><span data-stu-id="43e06-123">Implementations</span></span>

-   [<span data-ttu-id="43e06-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="43e06-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="43e06-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="43e06-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="43e06-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="43e06-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="43e06-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="43e06-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="43e06-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="43e06-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="43e06-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43e06-129">Windows Server 2003</span></span>



| <span data-ttu-id="43e06-130">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-130">Entry</span></span> | <span data-ttu-id="43e06-131">值</span><span class="sxs-lookup"><span data-stu-id="43e06-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="43e06-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43e06-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="43e06-134">System-Only</span></span>            | <span data-ttu-id="43e06-135">否</span><span class="sxs-lookup"><span data-stu-id="43e06-135">False</span></span>                                               |
| <span data-ttu-id="43e06-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43e06-136">Is-Single-Valued</span></span>       | <span data-ttu-id="43e06-137">否</span><span class="sxs-lookup"><span data-stu-id="43e06-137">False</span></span>                                               |
| <span data-ttu-id="43e06-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43e06-138">Is Indexed</span></span>             | <span data-ttu-id="43e06-139">否</span><span class="sxs-lookup"><span data-stu-id="43e06-139">False</span></span>                                               |
| <span data-ttu-id="43e06-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43e06-140">In Global Catalog</span></span>      | <span data-ttu-id="43e06-141">否</span><span class="sxs-lookup"><span data-stu-id="43e06-141">False</span></span>                                               |
| <span data-ttu-id="43e06-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43e06-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="43e06-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43e06-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="43e06-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43e06-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43e06-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-146">Search-Flags</span></span>           | <span data-ttu-id="43e06-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43e06-147">0x00000000</span></span>                                          |
| <span data-ttu-id="43e06-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-148">System-Flags</span></span>           | <span data-ttu-id="43e06-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43e06-149">0x00000010</span></span>                                          |
| <span data-ttu-id="43e06-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43e06-150">Classes used in</span></span>        | [<span data-ttu-id="43e06-151">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="43e06-151">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="43e06-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="43e06-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="43e06-153">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-153">Entry</span></span> | <span data-ttu-id="43e06-154">值</span><span class="sxs-lookup"><span data-stu-id="43e06-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="43e06-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43e06-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="43e06-157">System-Only</span></span>            | <span data-ttu-id="43e06-158">否</span><span class="sxs-lookup"><span data-stu-id="43e06-158">False</span></span>                                               |
| <span data-ttu-id="43e06-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43e06-159">Is-Single-Valued</span></span>       | <span data-ttu-id="43e06-160">否</span><span class="sxs-lookup"><span data-stu-id="43e06-160">False</span></span>                                               |
| <span data-ttu-id="43e06-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43e06-161">Is Indexed</span></span>             | <span data-ttu-id="43e06-162">否</span><span class="sxs-lookup"><span data-stu-id="43e06-162">False</span></span>                                               |
| <span data-ttu-id="43e06-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43e06-163">In Global Catalog</span></span>      | <span data-ttu-id="43e06-164">否</span><span class="sxs-lookup"><span data-stu-id="43e06-164">False</span></span>                                               |
| <span data-ttu-id="43e06-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43e06-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="43e06-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43e06-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="43e06-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43e06-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43e06-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-169">Search-Flags</span></span>           | <span data-ttu-id="43e06-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43e06-170">0x00000000</span></span>                                          |
| <span data-ttu-id="43e06-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-171">System-Flags</span></span>           | <span data-ttu-id="43e06-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43e06-172">0x00000010</span></span>                                          |
| <span data-ttu-id="43e06-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43e06-173">Classes used in</span></span>        | [<span data-ttu-id="43e06-174">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="43e06-174">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="43e06-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43e06-175">Windows Server 2008</span></span>



| <span data-ttu-id="43e06-176">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-176">Entry</span></span> | <span data-ttu-id="43e06-177">值</span><span class="sxs-lookup"><span data-stu-id="43e06-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="43e06-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43e06-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="43e06-180">System-Only</span></span>            | <span data-ttu-id="43e06-181">否</span><span class="sxs-lookup"><span data-stu-id="43e06-181">False</span></span>                                               |
| <span data-ttu-id="43e06-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43e06-182">Is-Single-Valued</span></span>       | <span data-ttu-id="43e06-183">否</span><span class="sxs-lookup"><span data-stu-id="43e06-183">False</span></span>                                               |
| <span data-ttu-id="43e06-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43e06-184">Is Indexed</span></span>             | <span data-ttu-id="43e06-185">否</span><span class="sxs-lookup"><span data-stu-id="43e06-185">False</span></span>                                               |
| <span data-ttu-id="43e06-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43e06-186">In Global Catalog</span></span>      | <span data-ttu-id="43e06-187">否</span><span class="sxs-lookup"><span data-stu-id="43e06-187">False</span></span>                                               |
| <span data-ttu-id="43e06-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43e06-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="43e06-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43e06-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="43e06-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43e06-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43e06-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-192">Search-Flags</span></span>           | <span data-ttu-id="43e06-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43e06-193">0x00000000</span></span>                                          |
| <span data-ttu-id="43e06-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-194">System-Flags</span></span>           | <span data-ttu-id="43e06-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43e06-195">0x00000010</span></span>                                          |
| <span data-ttu-id="43e06-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43e06-196">Classes used in</span></span>        | [<span data-ttu-id="43e06-197">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="43e06-197">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="43e06-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="43e06-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="43e06-199">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-199">Entry</span></span> | <span data-ttu-id="43e06-200">值</span><span class="sxs-lookup"><span data-stu-id="43e06-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="43e06-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43e06-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="43e06-203">System-Only</span></span>            | <span data-ttu-id="43e06-204">否</span><span class="sxs-lookup"><span data-stu-id="43e06-204">False</span></span>                                               |
| <span data-ttu-id="43e06-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43e06-205">Is-Single-Valued</span></span>       | <span data-ttu-id="43e06-206">否</span><span class="sxs-lookup"><span data-stu-id="43e06-206">False</span></span>                                               |
| <span data-ttu-id="43e06-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43e06-207">Is Indexed</span></span>             | <span data-ttu-id="43e06-208">否</span><span class="sxs-lookup"><span data-stu-id="43e06-208">False</span></span>                                               |
| <span data-ttu-id="43e06-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43e06-209">In Global Catalog</span></span>      | <span data-ttu-id="43e06-210">否</span><span class="sxs-lookup"><span data-stu-id="43e06-210">False</span></span>                                               |
| <span data-ttu-id="43e06-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43e06-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="43e06-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43e06-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="43e06-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43e06-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43e06-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-215">Search-Flags</span></span>           | <span data-ttu-id="43e06-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43e06-216">0x00000000</span></span>                                          |
| <span data-ttu-id="43e06-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-217">System-Flags</span></span>           | <span data-ttu-id="43e06-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43e06-218">0x00000010</span></span>                                          |
| <span data-ttu-id="43e06-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43e06-219">Classes used in</span></span>        | [<span data-ttu-id="43e06-220">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="43e06-220">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="43e06-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="43e06-221">Windows Server 2012</span></span>



| <span data-ttu-id="43e06-222">進入</span><span class="sxs-lookup"><span data-stu-id="43e06-222">Entry</span></span> | <span data-ttu-id="43e06-223">值</span><span class="sxs-lookup"><span data-stu-id="43e06-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="43e06-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="43e06-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="43e06-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="43e06-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="43e06-226">System-Only</span></span>            | <span data-ttu-id="43e06-227">否</span><span class="sxs-lookup"><span data-stu-id="43e06-227">False</span></span>                                               |
| <span data-ttu-id="43e06-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="43e06-228">Is-Single-Valued</span></span>       | <span data-ttu-id="43e06-229">否</span><span class="sxs-lookup"><span data-stu-id="43e06-229">False</span></span>                                               |
| <span data-ttu-id="43e06-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="43e06-230">Is Indexed</span></span>             | <span data-ttu-id="43e06-231">否</span><span class="sxs-lookup"><span data-stu-id="43e06-231">False</span></span>                                               |
| <span data-ttu-id="43e06-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="43e06-232">In Global Catalog</span></span>      | <span data-ttu-id="43e06-233">否</span><span class="sxs-lookup"><span data-stu-id="43e06-233">False</span></span>                                               |
| <span data-ttu-id="43e06-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="43e06-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="43e06-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="43e06-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="43e06-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="43e06-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="43e06-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="43e06-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-238">Search-Flags</span></span>           | <span data-ttu-id="43e06-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43e06-239">0x00000000</span></span>                                          |
| <span data-ttu-id="43e06-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="43e06-240">System-Flags</span></span>           | <span data-ttu-id="43e06-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43e06-241">0x00000010</span></span>                                          |
| <span data-ttu-id="43e06-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="43e06-242">Classes used in</span></span>        | [<span data-ttu-id="43e06-243">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="43e06-243">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="43e06-244">備註</span><span class="sxs-lookup"><span data-stu-id="43e06-244">Remarks</span></span>

<span data-ttu-id="43e06-245">下列清單會識別可透過 Active Directory 消費者和電腦嵌入式管理單元新增至群組的標準類別。</span><span class="sxs-lookup"><span data-stu-id="43e06-245">The following list identifies the standard classes that can be added to a group through the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="43e06-246">**Group**</span><span class="sxs-lookup"><span data-stu-id="43e06-246">**Group**</span></span>](c-group.md)
-   [<span data-ttu-id="43e06-247">**User**</span><span class="sxs-lookup"><span data-stu-id="43e06-247">**User**</span></span>](c-user.md)
-   [<span data-ttu-id="43e06-248">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="43e06-248">**inetOrgPerson**</span></span>](c-inetorgperson.md)
-   [<span data-ttu-id="43e06-249">**Contact**</span><span class="sxs-lookup"><span data-stu-id="43e06-249">**Contact**</span></span>](c-contact.md)
-   [<span data-ttu-id="43e06-250">**電腦**</span><span class="sxs-lookup"><span data-stu-id="43e06-250">**Computer**</span></span>](c-computer.md)

## <a name="see-also"></a><span data-ttu-id="43e06-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43e06-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e06-252">**ms DS-非安全性群組-額外類別**</span><span class="sxs-lookup"><span data-stu-id="43e06-252">**ms-DS-Non-Security-Group-Extra-Classes**</span></span>](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





