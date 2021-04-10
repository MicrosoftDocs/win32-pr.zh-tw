---
title: GPC-電腦副檔名-名稱屬性
description: 用於電腦原則的群組原則物件。
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- GPC-電腦延伸模組名稱屬性 AD 架構
- gPCMachineExtensionNames 屬性 AD 架構
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935461"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="826f9-105">GPC-電腦副檔名-名稱屬性</span><span class="sxs-lookup"><span data-stu-id="826f9-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="826f9-106">用於電腦原則的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="826f9-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="826f9-107">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-107">Entry</span></span> | <span data-ttu-id="826f9-108">值</span><span class="sxs-lookup"><span data-stu-id="826f9-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="826f9-109">CN</span><span class="sxs-lookup"><span data-stu-id="826f9-109">CN</span></span>                | <span data-ttu-id="826f9-110">GPC-電腦延伸模組名稱</span><span class="sxs-lookup"><span data-stu-id="826f9-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="826f9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="826f9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="826f9-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="826f9-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="826f9-113">大小</span><span class="sxs-lookup"><span data-stu-id="826f9-113">Size</span></span>              | <span data-ttu-id="826f9-114">取決於在此 GPO 中具有原則的用戶端延伸模組數目。</span><span class="sxs-lookup"><span data-stu-id="826f9-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="826f9-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="826f9-115">Update Privilege</span></span>  | <span data-ttu-id="826f9-116">網域或原則管理員。</span><span class="sxs-lookup"><span data-stu-id="826f9-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="826f9-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="826f9-117">Update Frequency</span></span>  | <span data-ttu-id="826f9-118">每次透過 GPE 更新 GPO 時。</span><span class="sxs-lookup"><span data-stu-id="826f9-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="826f9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-119">Attribute-Id</span></span>      | <span data-ttu-id="826f9-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="826f9-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="826f9-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="826f9-121">System-Id-Guid</span></span>    | <span data-ttu-id="826f9-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="826f9-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="826f9-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="826f9-123">Syntax</span></span>            | [<span data-ttu-id="826f9-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="826f9-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="826f9-125">實作</span><span class="sxs-lookup"><span data-stu-id="826f9-125">Implementations</span></span>

-   [<span data-ttu-id="826f9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="826f9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="826f9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="826f9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="826f9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="826f9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="826f9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="826f9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="826f9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="826f9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="826f9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="826f9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="826f9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="826f9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="826f9-133">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-133">Entry</span></span> | <span data-ttu-id="826f9-134">值</span><span class="sxs-lookup"><span data-stu-id="826f9-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-137">System-Only</span></span>            | <span data-ttu-id="826f9-138">否</span><span class="sxs-lookup"><span data-stu-id="826f9-138">False</span></span>                                                               |
| <span data-ttu-id="826f9-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-140">對</span><span class="sxs-lookup"><span data-stu-id="826f9-140">True</span></span>                                                                |
| <span data-ttu-id="826f9-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-141">Is Indexed</span></span>             | <span data-ttu-id="826f9-142">否</span><span class="sxs-lookup"><span data-stu-id="826f9-142">False</span></span>                                                               |
| <span data-ttu-id="826f9-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-143">In Global Catalog</span></span>      | <span data-ttu-id="826f9-144">否</span><span class="sxs-lookup"><span data-stu-id="826f9-144">False</span></span>                                                               |
| <span data-ttu-id="826f9-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-149">Search-Flags</span></span>           | <span data-ttu-id="826f9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-151">System-Flags</span></span>           | <span data-ttu-id="826f9-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-153">Classes used in</span></span>        | [<span data-ttu-id="826f9-154">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="826f9-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="826f9-155">Windows Server 2003</span></span>



| <span data-ttu-id="826f9-156">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-156">Entry</span></span> | <span data-ttu-id="826f9-157">值</span><span class="sxs-lookup"><span data-stu-id="826f9-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-160">System-Only</span></span>            | <span data-ttu-id="826f9-161">否</span><span class="sxs-lookup"><span data-stu-id="826f9-161">False</span></span>                                                               |
| <span data-ttu-id="826f9-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-162">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-163">對</span><span class="sxs-lookup"><span data-stu-id="826f9-163">True</span></span>                                                                |
| <span data-ttu-id="826f9-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-164">Is Indexed</span></span>             | <span data-ttu-id="826f9-165">否</span><span class="sxs-lookup"><span data-stu-id="826f9-165">False</span></span>                                                               |
| <span data-ttu-id="826f9-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-166">In Global Catalog</span></span>      | <span data-ttu-id="826f9-167">否</span><span class="sxs-lookup"><span data-stu-id="826f9-167">False</span></span>                                                               |
| <span data-ttu-id="826f9-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-172">Search-Flags</span></span>           | <span data-ttu-id="826f9-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-174">System-Flags</span></span>           | <span data-ttu-id="826f9-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-176">Classes used in</span></span>        | [<span data-ttu-id="826f9-177">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="826f9-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="826f9-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="826f9-179">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-179">Entry</span></span> | <span data-ttu-id="826f9-180">值</span><span class="sxs-lookup"><span data-stu-id="826f9-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-183">System-Only</span></span>            | <span data-ttu-id="826f9-184">否</span><span class="sxs-lookup"><span data-stu-id="826f9-184">False</span></span>                                                               |
| <span data-ttu-id="826f9-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-185">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-186">對</span><span class="sxs-lookup"><span data-stu-id="826f9-186">True</span></span>                                                                |
| <span data-ttu-id="826f9-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-187">Is Indexed</span></span>             | <span data-ttu-id="826f9-188">否</span><span class="sxs-lookup"><span data-stu-id="826f9-188">False</span></span>                                                               |
| <span data-ttu-id="826f9-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-189">In Global Catalog</span></span>      | <span data-ttu-id="826f9-190">否</span><span class="sxs-lookup"><span data-stu-id="826f9-190">False</span></span>                                                               |
| <span data-ttu-id="826f9-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-195">Search-Flags</span></span>           | <span data-ttu-id="826f9-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-197">System-Flags</span></span>           | <span data-ttu-id="826f9-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-199">Classes used in</span></span>        | [<span data-ttu-id="826f9-200">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="826f9-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="826f9-201">Windows Server 2008</span></span>



| <span data-ttu-id="826f9-202">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-202">Entry</span></span> | <span data-ttu-id="826f9-203">值</span><span class="sxs-lookup"><span data-stu-id="826f9-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-206">System-Only</span></span>            | <span data-ttu-id="826f9-207">否</span><span class="sxs-lookup"><span data-stu-id="826f9-207">False</span></span>                                                               |
| <span data-ttu-id="826f9-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-208">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-209">對</span><span class="sxs-lookup"><span data-stu-id="826f9-209">True</span></span>                                                                |
| <span data-ttu-id="826f9-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-210">Is Indexed</span></span>             | <span data-ttu-id="826f9-211">否</span><span class="sxs-lookup"><span data-stu-id="826f9-211">False</span></span>                                                               |
| <span data-ttu-id="826f9-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-212">In Global Catalog</span></span>      | <span data-ttu-id="826f9-213">否</span><span class="sxs-lookup"><span data-stu-id="826f9-213">False</span></span>                                                               |
| <span data-ttu-id="826f9-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-218">Search-Flags</span></span>           | <span data-ttu-id="826f9-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-220">System-Flags</span></span>           | <span data-ttu-id="826f9-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-222">Classes used in</span></span>        | [<span data-ttu-id="826f9-223">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="826f9-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="826f9-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="826f9-225">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-225">Entry</span></span> | <span data-ttu-id="826f9-226">值</span><span class="sxs-lookup"><span data-stu-id="826f9-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-229">System-Only</span></span>            | <span data-ttu-id="826f9-230">否</span><span class="sxs-lookup"><span data-stu-id="826f9-230">False</span></span>                                                               |
| <span data-ttu-id="826f9-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-231">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-232">對</span><span class="sxs-lookup"><span data-stu-id="826f9-232">True</span></span>                                                                |
| <span data-ttu-id="826f9-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-233">Is Indexed</span></span>             | <span data-ttu-id="826f9-234">否</span><span class="sxs-lookup"><span data-stu-id="826f9-234">False</span></span>                                                               |
| <span data-ttu-id="826f9-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-235">In Global Catalog</span></span>      | <span data-ttu-id="826f9-236">否</span><span class="sxs-lookup"><span data-stu-id="826f9-236">False</span></span>                                                               |
| <span data-ttu-id="826f9-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-241">Search-Flags</span></span>           | <span data-ttu-id="826f9-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-243">System-Flags</span></span>           | <span data-ttu-id="826f9-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-245">Classes used in</span></span>        | [<span data-ttu-id="826f9-246">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="826f9-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="826f9-247">Windows Server 2012</span></span>



| <span data-ttu-id="826f9-248">進入</span><span class="sxs-lookup"><span data-stu-id="826f9-248">Entry</span></span> | <span data-ttu-id="826f9-249">值</span><span class="sxs-lookup"><span data-stu-id="826f9-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="826f9-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="826f9-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="826f9-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="826f9-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="826f9-252">System-Only</span></span>            | <span data-ttu-id="826f9-253">否</span><span class="sxs-lookup"><span data-stu-id="826f9-253">False</span></span>                                                               |
| <span data-ttu-id="826f9-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="826f9-254">Is-Single-Valued</span></span>       | <span data-ttu-id="826f9-255">對</span><span class="sxs-lookup"><span data-stu-id="826f9-255">True</span></span>                                                                |
| <span data-ttu-id="826f9-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="826f9-256">Is Indexed</span></span>             | <span data-ttu-id="826f9-257">否</span><span class="sxs-lookup"><span data-stu-id="826f9-257">False</span></span>                                                               |
| <span data-ttu-id="826f9-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="826f9-258">In Global Catalog</span></span>      | <span data-ttu-id="826f9-259">否</span><span class="sxs-lookup"><span data-stu-id="826f9-259">False</span></span>                                                               |
| <span data-ttu-id="826f9-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="826f9-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="826f9-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="826f9-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="826f9-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="826f9-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="826f9-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="826f9-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-264">Search-Flags</span></span>           | <span data-ttu-id="826f9-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="826f9-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="826f9-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="826f9-266">System-Flags</span></span>           | <span data-ttu-id="826f9-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="826f9-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="826f9-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="826f9-268">Classes used in</span></span>        | [<span data-ttu-id="826f9-269">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="826f9-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





