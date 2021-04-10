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
# <a name="ms-ds-security-group-extra-classes-attribute"></a><span data-ttu-id="5dcc5-105">ms-DS-安全性群組-額外類別屬性</span><span class="sxs-lookup"><span data-stu-id="5dcc5-105">ms-DS-Security-Group-Extra-Classes attribute</span></span>

<span data-ttu-id="5dcc5-106">可透過 Active Directory 消費者和電腦嵌入式管理單元新增至安全性群組之非標準類別的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="5dcc5-106">The common names of the nonstandard classes that can be added to a security group through the Active Directory Users and Computers snap-in.</span></span>



| <span data-ttu-id="5dcc5-107">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-107">Entry</span></span> | <span data-ttu-id="5dcc5-108">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5dcc5-109">CN</span><span class="sxs-lookup"><span data-stu-id="5dcc5-109">CN</span></span>                | <span data-ttu-id="5dcc5-110">ms-DS-安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-110">ms-DS-Security-Group-Extra-Classes</span></span>          |
| <span data-ttu-id="5dcc5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5dcc5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5dcc5-112">安全性群組-額外類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-112">msDS-Security-Group-Extra-Classes</span></span>           |
| <span data-ttu-id="5dcc5-113">大小</span><span class="sxs-lookup"><span data-stu-id="5dcc5-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5dcc5-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="5dcc5-114">Update Privilege</span></span>  | <span data-ttu-id="5dcc5-115">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="5dcc5-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="5dcc5-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="5dcc5-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5dcc5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-117">Attribute-Id</span></span>      | <span data-ttu-id="5dcc5-118">1.2.840.113556.1.4.1688</span><span class="sxs-lookup"><span data-stu-id="5dcc5-118">1.2.840.113556.1.4.1688</span></span>                     |
| <span data-ttu-id="5dcc5-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="5dcc5-119">System-Id-Guid</span></span>    | <span data-ttu-id="5dcc5-120">4f146ae8-a4fe-4801-a731-f51848a4f4e4</span><span class="sxs-lookup"><span data-stu-id="5dcc5-120">4f146ae8-a4fe-4801-a731-f51848a4f4e4</span></span>        |
| <span data-ttu-id="5dcc5-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dcc5-121">Syntax</span></span>            | [<span data-ttu-id="5dcc5-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5dcc5-123">實作</span><span class="sxs-lookup"><span data-stu-id="5dcc5-123">Implementations</span></span>

-   [<span data-ttu-id="5dcc5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5dcc5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5dcc5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5dcc5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5dcc5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5dcc5-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5dcc5-129">Windows Server 2003</span></span>



| <span data-ttu-id="5dcc5-130">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-130">Entry</span></span> | <span data-ttu-id="5dcc5-131">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5dcc5-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5dcc5-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dcc5-134">System-Only</span></span>            | <span data-ttu-id="5dcc5-135">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-135">False</span></span>                                               |
| <span data-ttu-id="5dcc5-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5dcc5-137">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-137">False</span></span>                                               |
| <span data-ttu-id="5dcc5-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5dcc5-138">Is Indexed</span></span>             | <span data-ttu-id="5dcc5-139">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-139">False</span></span>                                               |
| <span data-ttu-id="5dcc5-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5dcc5-140">In Global Catalog</span></span>      | <span data-ttu-id="5dcc5-141">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-141">False</span></span>                                               |
| <span data-ttu-id="5dcc5-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5dcc5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dcc5-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5dcc5-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5dcc5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dcc5-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dcc5-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-146">Search-Flags</span></span>           | <span data-ttu-id="5dcc5-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dcc5-147">0x00000000</span></span>                                          |
| <span data-ttu-id="5dcc5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-148">System-Flags</span></span>           | <span data-ttu-id="5dcc5-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dcc5-149">0x00000010</span></span>                                          |
| <span data-ttu-id="5dcc5-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-150">Classes used in</span></span>        | [<span data-ttu-id="5dcc5-151">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-151">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5dcc5-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5dcc5-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5dcc5-153">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-153">Entry</span></span> | <span data-ttu-id="5dcc5-154">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5dcc5-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5dcc5-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dcc5-157">System-Only</span></span>            | <span data-ttu-id="5dcc5-158">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-158">False</span></span>                                               |
| <span data-ttu-id="5dcc5-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5dcc5-160">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-160">False</span></span>                                               |
| <span data-ttu-id="5dcc5-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5dcc5-161">Is Indexed</span></span>             | <span data-ttu-id="5dcc5-162">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-162">False</span></span>                                               |
| <span data-ttu-id="5dcc5-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5dcc5-163">In Global Catalog</span></span>      | <span data-ttu-id="5dcc5-164">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-164">False</span></span>                                               |
| <span data-ttu-id="5dcc5-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5dcc5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dcc5-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5dcc5-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5dcc5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dcc5-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dcc5-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-169">Search-Flags</span></span>           | <span data-ttu-id="5dcc5-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dcc5-170">0x00000000</span></span>                                          |
| <span data-ttu-id="5dcc5-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-171">System-Flags</span></span>           | <span data-ttu-id="5dcc5-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dcc5-172">0x00000010</span></span>                                          |
| <span data-ttu-id="5dcc5-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-173">Classes used in</span></span>        | [<span data-ttu-id="5dcc5-174">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-174">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5dcc5-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dcc5-175">Windows Server 2008</span></span>



| <span data-ttu-id="5dcc5-176">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-176">Entry</span></span> | <span data-ttu-id="5dcc5-177">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5dcc5-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5dcc5-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dcc5-180">System-Only</span></span>            | <span data-ttu-id="5dcc5-181">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-181">False</span></span>                                               |
| <span data-ttu-id="5dcc5-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5dcc5-183">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-183">False</span></span>                                               |
| <span data-ttu-id="5dcc5-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5dcc5-184">Is Indexed</span></span>             | <span data-ttu-id="5dcc5-185">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-185">False</span></span>                                               |
| <span data-ttu-id="5dcc5-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5dcc5-186">In Global Catalog</span></span>      | <span data-ttu-id="5dcc5-187">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-187">False</span></span>                                               |
| <span data-ttu-id="5dcc5-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5dcc5-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dcc5-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5dcc5-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5dcc5-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dcc5-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dcc5-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-192">Search-Flags</span></span>           | <span data-ttu-id="5dcc5-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dcc5-193">0x00000000</span></span>                                          |
| <span data-ttu-id="5dcc5-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-194">System-Flags</span></span>           | <span data-ttu-id="5dcc5-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dcc5-195">0x00000010</span></span>                                          |
| <span data-ttu-id="5dcc5-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-196">Classes used in</span></span>        | [<span data-ttu-id="5dcc5-197">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-197">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5dcc5-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5dcc5-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5dcc5-199">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-199">Entry</span></span> | <span data-ttu-id="5dcc5-200">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5dcc5-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5dcc5-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dcc5-203">System-Only</span></span>            | <span data-ttu-id="5dcc5-204">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-204">False</span></span>                                               |
| <span data-ttu-id="5dcc5-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5dcc5-206">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-206">False</span></span>                                               |
| <span data-ttu-id="5dcc5-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5dcc5-207">Is Indexed</span></span>             | <span data-ttu-id="5dcc5-208">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-208">False</span></span>                                               |
| <span data-ttu-id="5dcc5-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5dcc5-209">In Global Catalog</span></span>      | <span data-ttu-id="5dcc5-210">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-210">False</span></span>                                               |
| <span data-ttu-id="5dcc5-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5dcc5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dcc5-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5dcc5-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5dcc5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dcc5-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dcc5-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-215">Search-Flags</span></span>           | <span data-ttu-id="5dcc5-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dcc5-216">0x00000000</span></span>                                          |
| <span data-ttu-id="5dcc5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-217">System-Flags</span></span>           | <span data-ttu-id="5dcc5-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dcc5-218">0x00000010</span></span>                                          |
| <span data-ttu-id="5dcc5-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-219">Classes used in</span></span>        | [<span data-ttu-id="5dcc5-220">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-220">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5dcc5-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5dcc5-221">Windows Server 2012</span></span>



| <span data-ttu-id="5dcc5-222">進入</span><span class="sxs-lookup"><span data-stu-id="5dcc5-222">Entry</span></span> | <span data-ttu-id="5dcc5-223">值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="5dcc5-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="5dcc5-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dcc5-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="5dcc5-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dcc5-226">System-Only</span></span>            | <span data-ttu-id="5dcc5-227">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-227">False</span></span>                                               |
| <span data-ttu-id="5dcc5-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="5dcc5-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5dcc5-229">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-229">False</span></span>                                               |
| <span data-ttu-id="5dcc5-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="5dcc5-230">Is Indexed</span></span>             | <span data-ttu-id="5dcc5-231">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-231">False</span></span>                                               |
| <span data-ttu-id="5dcc5-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="5dcc5-232">In Global Catalog</span></span>      | <span data-ttu-id="5dcc5-233">否</span><span class="sxs-lookup"><span data-stu-id="5dcc5-233">False</span></span>                                               |
| <span data-ttu-id="5dcc5-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="5dcc5-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dcc5-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="5dcc5-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="5dcc5-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dcc5-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dcc5-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="5dcc5-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-238">Search-Flags</span></span>           | <span data-ttu-id="5dcc5-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dcc5-239">0x00000000</span></span>                                          |
| <span data-ttu-id="5dcc5-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dcc5-240">System-Flags</span></span>           | <span data-ttu-id="5dcc5-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dcc5-241">0x00000010</span></span>                                          |
| <span data-ttu-id="5dcc5-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="5dcc5-242">Classes used in</span></span>        | [<span data-ttu-id="5dcc5-243">**DS-UI-設定**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-243">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5dcc5-244">備註</span><span class="sxs-lookup"><span data-stu-id="5dcc5-244">Remarks</span></span>

<span data-ttu-id="5dcc5-245">下列清單會識別可透過 Active Directory 消費者和電腦嵌入式管理單元新增至群組的標準類別。</span><span class="sxs-lookup"><span data-stu-id="5dcc5-245">The following list identifies the standard classes that can be added to a group through the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="5dcc5-246">**Group**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-246">**Group**</span></span>](c-group.md)
-   [<span data-ttu-id="5dcc5-247">**User**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-247">**User**</span></span>](c-user.md)
-   [<span data-ttu-id="5dcc5-248">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-248">**inetOrgPerson**</span></span>](c-inetorgperson.md)
-   [<span data-ttu-id="5dcc5-249">**Contact**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-249">**Contact**</span></span>](c-contact.md)
-   [<span data-ttu-id="5dcc5-250">**電腦**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-250">**Computer**</span></span>](c-computer.md)

## <a name="see-also"></a><span data-ttu-id="5dcc5-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dcc5-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dcc5-252">**ms DS-非安全性群組-額外類別**</span><span class="sxs-lookup"><span data-stu-id="5dcc5-252">**ms-DS-Non-Security-Group-Extra-Classes**</span></span>](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





