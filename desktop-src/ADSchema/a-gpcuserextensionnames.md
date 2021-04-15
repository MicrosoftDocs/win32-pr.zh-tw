---
title: GPC-使用者-Extension-Names 屬性
description: 用於使用者原則的群組原則物件。
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- GPC-使用者-Extension-Names 屬性 AD 架構
- gPCUserExtensionNames 屬性 AD 架構
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467182"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="e6aa9-105">GPC-使用者-Extension-Names 屬性</span><span class="sxs-lookup"><span data-stu-id="e6aa9-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="e6aa9-106">用於使用者原則的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="e6aa9-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="e6aa9-107">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-107">Entry</span></span> | <span data-ttu-id="e6aa9-108">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-109">CN</span><span class="sxs-lookup"><span data-stu-id="e6aa9-109">CN</span></span>                | <span data-ttu-id="e6aa9-110">GPC-使用者延伸-名稱</span><span class="sxs-lookup"><span data-stu-id="e6aa9-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="e6aa9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e6aa9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e6aa9-112">gPCUserExtensionNames</span><span class="sxs-lookup"><span data-stu-id="e6aa9-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="e6aa9-113">大小</span><span class="sxs-lookup"><span data-stu-id="e6aa9-113">Size</span></span>              | <span data-ttu-id="e6aa9-114">取決於在此 GPO 中具有原則的用戶端延伸模組數目。</span><span class="sxs-lookup"><span data-stu-id="e6aa9-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="e6aa9-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e6aa9-115">Update Privilege</span></span>  | <span data-ttu-id="e6aa9-116">網域或原則管理員。</span><span class="sxs-lookup"><span data-stu-id="e6aa9-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="e6aa9-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e6aa9-117">Update Frequency</span></span>  | <span data-ttu-id="e6aa9-118">每次透過 GPE 更新 GPO 時。</span><span class="sxs-lookup"><span data-stu-id="e6aa9-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="e6aa9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-119">Attribute-Id</span></span>      | <span data-ttu-id="e6aa9-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="e6aa9-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="e6aa9-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e6aa9-121">System-Id-Guid</span></span>    | <span data-ttu-id="e6aa9-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e6aa9-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="e6aa9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6aa9-123">Syntax</span></span>            | [<span data-ttu-id="e6aa9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="e6aa9-125">實作</span><span class="sxs-lookup"><span data-stu-id="e6aa9-125">Implementations</span></span>

-   [<span data-ttu-id="e6aa9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e6aa9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e6aa9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e6aa9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e6aa9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e6aa9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e6aa9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e6aa9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e6aa9-133">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-133">Entry</span></span> | <span data-ttu-id="e6aa9-134">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-137">System-Only</span></span>            | <span data-ttu-id="e6aa9-138">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-138">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-140">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-140">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-141">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-142">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-142">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-143">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-144">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-144">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-149">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-151">System-Flags</span></span>           | <span data-ttu-id="e6aa9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-153">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-154">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e6aa9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6aa9-155">Windows Server 2003</span></span>



| <span data-ttu-id="e6aa9-156">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-156">Entry</span></span> | <span data-ttu-id="e6aa9-157">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-160">System-Only</span></span>            | <span data-ttu-id="e6aa9-161">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-161">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-163">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-163">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-164">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-165">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-165">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-166">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-167">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-167">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-172">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-174">System-Flags</span></span>           | <span data-ttu-id="e6aa9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-176">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-177">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e6aa9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e6aa9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e6aa9-179">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-179">Entry</span></span> | <span data-ttu-id="e6aa9-180">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-183">System-Only</span></span>            | <span data-ttu-id="e6aa9-184">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-184">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-186">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-186">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-187">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-188">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-188">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-189">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-190">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-190">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-195">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-197">System-Flags</span></span>           | <span data-ttu-id="e6aa9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-199">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-200">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e6aa9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6aa9-201">Windows Server 2008</span></span>



| <span data-ttu-id="e6aa9-202">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-202">Entry</span></span> | <span data-ttu-id="e6aa9-203">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-206">System-Only</span></span>            | <span data-ttu-id="e6aa9-207">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-207">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-209">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-209">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-210">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-211">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-211">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-212">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-213">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-213">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-218">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-220">System-Flags</span></span>           | <span data-ttu-id="e6aa9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-222">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-223">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e6aa9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e6aa9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e6aa9-225">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-225">Entry</span></span> | <span data-ttu-id="e6aa9-226">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-229">System-Only</span></span>            | <span data-ttu-id="e6aa9-230">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-230">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-232">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-232">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-233">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-234">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-234">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-235">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-236">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-236">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-241">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-243">System-Flags</span></span>           | <span data-ttu-id="e6aa9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-245">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-246">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e6aa9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6aa9-247">Windows Server 2012</span></span>



| <span data-ttu-id="e6aa9-248">進入</span><span class="sxs-lookup"><span data-stu-id="e6aa9-248">Entry</span></span> | <span data-ttu-id="e6aa9-249">值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e6aa9-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e6aa9-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e6aa9-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e6aa9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e6aa9-252">System-Only</span></span>            | <span data-ttu-id="e6aa9-253">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-253">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e6aa9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e6aa9-255">對</span><span class="sxs-lookup"><span data-stu-id="e6aa9-255">True</span></span>                                                                |
| <span data-ttu-id="e6aa9-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e6aa9-256">Is Indexed</span></span>             | <span data-ttu-id="e6aa9-257">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-257">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e6aa9-258">In Global Catalog</span></span>      | <span data-ttu-id="e6aa9-259">否</span><span class="sxs-lookup"><span data-stu-id="e6aa9-259">False</span></span>                                                               |
| <span data-ttu-id="e6aa9-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e6aa9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e6aa9-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e6aa9-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e6aa9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e6aa9-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e6aa9-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e6aa9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-264">Search-Flags</span></span>           | <span data-ttu-id="e6aa9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e6aa9-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="e6aa9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e6aa9-266">System-Flags</span></span>           | <span data-ttu-id="e6aa9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e6aa9-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="e6aa9-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e6aa9-268">Classes used in</span></span>        | [<span data-ttu-id="e6aa9-269">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e6aa9-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





