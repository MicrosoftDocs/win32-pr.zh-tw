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
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="e39a5-105">GPC-電腦副檔名-名稱屬性</span><span class="sxs-lookup"><span data-stu-id="e39a5-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="e39a5-106">用於電腦原則的群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="e39a5-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="e39a5-107">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-107">Entry</span></span> | <span data-ttu-id="e39a5-108">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e39a5-109">CN</span><span class="sxs-lookup"><span data-stu-id="e39a5-109">CN</span></span>                | <span data-ttu-id="e39a5-110">GPC-電腦延伸模組名稱</span><span class="sxs-lookup"><span data-stu-id="e39a5-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="e39a5-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e39a5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e39a5-112">gPCMachineExtensionNames</span><span class="sxs-lookup"><span data-stu-id="e39a5-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="e39a5-113">大小</span><span class="sxs-lookup"><span data-stu-id="e39a5-113">Size</span></span>              | <span data-ttu-id="e39a5-114">取決於在此 GPO 中具有原則的用戶端延伸模組數目。</span><span class="sxs-lookup"><span data-stu-id="e39a5-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="e39a5-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e39a5-115">Update Privilege</span></span>  | <span data-ttu-id="e39a5-116">網域或原則管理員。</span><span class="sxs-lookup"><span data-stu-id="e39a5-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="e39a5-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e39a5-117">Update Frequency</span></span>  | <span data-ttu-id="e39a5-118">每次透過 GPE 更新 GPO 時。</span><span class="sxs-lookup"><span data-stu-id="e39a5-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="e39a5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-119">Attribute-Id</span></span>      | <span data-ttu-id="e39a5-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="e39a5-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="e39a5-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e39a5-121">System-Id-Guid</span></span>    | <span data-ttu-id="e39a5-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="e39a5-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="e39a5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e39a5-123">Syntax</span></span>            | [<span data-ttu-id="e39a5-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e39a5-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="e39a5-125">實作</span><span class="sxs-lookup"><span data-stu-id="e39a5-125">Implementations</span></span>

-   [<span data-ttu-id="e39a5-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e39a5-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e39a5-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e39a5-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e39a5-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e39a5-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e39a5-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e39a5-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e39a5-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e39a5-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e39a5-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e39a5-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e39a5-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e39a5-132">Windows 2000 Server</span></span>



| <span data-ttu-id="e39a5-133">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-133">Entry</span></span> | <span data-ttu-id="e39a5-134">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-137">System-Only</span></span>            | <span data-ttu-id="e39a5-138">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-138">False</span></span>                                                               |
| <span data-ttu-id="e39a5-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-139">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-140">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-140">True</span></span>                                                                |
| <span data-ttu-id="e39a5-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-141">Is Indexed</span></span>             | <span data-ttu-id="e39a5-142">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-142">False</span></span>                                                               |
| <span data-ttu-id="e39a5-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-143">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-144">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-144">False</span></span>                                                               |
| <span data-ttu-id="e39a5-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-149">Search-Flags</span></span>           | <span data-ttu-id="e39a5-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-151">System-Flags</span></span>           | <span data-ttu-id="e39a5-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-153">Classes used in</span></span>        | [<span data-ttu-id="e39a5-154">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e39a5-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e39a5-155">Windows Server 2003</span></span>



| <span data-ttu-id="e39a5-156">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-156">Entry</span></span> | <span data-ttu-id="e39a5-157">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-160">System-Only</span></span>            | <span data-ttu-id="e39a5-161">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-161">False</span></span>                                                               |
| <span data-ttu-id="e39a5-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-162">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-163">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-163">True</span></span>                                                                |
| <span data-ttu-id="e39a5-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-164">Is Indexed</span></span>             | <span data-ttu-id="e39a5-165">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-165">False</span></span>                                                               |
| <span data-ttu-id="e39a5-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-166">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-167">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-167">False</span></span>                                                               |
| <span data-ttu-id="e39a5-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-172">Search-Flags</span></span>           | <span data-ttu-id="e39a5-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-174">System-Flags</span></span>           | <span data-ttu-id="e39a5-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-176">Classes used in</span></span>        | [<span data-ttu-id="e39a5-177">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e39a5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e39a5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e39a5-179">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-179">Entry</span></span> | <span data-ttu-id="e39a5-180">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-183">System-Only</span></span>            | <span data-ttu-id="e39a5-184">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-184">False</span></span>                                                               |
| <span data-ttu-id="e39a5-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-186">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-186">True</span></span>                                                                |
| <span data-ttu-id="e39a5-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-187">Is Indexed</span></span>             | <span data-ttu-id="e39a5-188">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-188">False</span></span>                                                               |
| <span data-ttu-id="e39a5-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-189">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-190">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-190">False</span></span>                                                               |
| <span data-ttu-id="e39a5-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-195">Search-Flags</span></span>           | <span data-ttu-id="e39a5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-197">System-Flags</span></span>           | <span data-ttu-id="e39a5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-199">Classes used in</span></span>        | [<span data-ttu-id="e39a5-200">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e39a5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e39a5-201">Windows Server 2008</span></span>



| <span data-ttu-id="e39a5-202">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-202">Entry</span></span> | <span data-ttu-id="e39a5-203">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-206">System-Only</span></span>            | <span data-ttu-id="e39a5-207">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-207">False</span></span>                                                               |
| <span data-ttu-id="e39a5-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-208">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-209">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-209">True</span></span>                                                                |
| <span data-ttu-id="e39a5-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-210">Is Indexed</span></span>             | <span data-ttu-id="e39a5-211">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-211">False</span></span>                                                               |
| <span data-ttu-id="e39a5-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-212">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-213">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-213">False</span></span>                                                               |
| <span data-ttu-id="e39a5-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-218">Search-Flags</span></span>           | <span data-ttu-id="e39a5-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-220">System-Flags</span></span>           | <span data-ttu-id="e39a5-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-222">Classes used in</span></span>        | [<span data-ttu-id="e39a5-223">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e39a5-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e39a5-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e39a5-225">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-225">Entry</span></span> | <span data-ttu-id="e39a5-226">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-229">System-Only</span></span>            | <span data-ttu-id="e39a5-230">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-230">False</span></span>                                                               |
| <span data-ttu-id="e39a5-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-231">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-232">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-232">True</span></span>                                                                |
| <span data-ttu-id="e39a5-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-233">Is Indexed</span></span>             | <span data-ttu-id="e39a5-234">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-234">False</span></span>                                                               |
| <span data-ttu-id="e39a5-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-235">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-236">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-236">False</span></span>                                                               |
| <span data-ttu-id="e39a5-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-241">Search-Flags</span></span>           | <span data-ttu-id="e39a5-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-243">System-Flags</span></span>           | <span data-ttu-id="e39a5-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-245">Classes used in</span></span>        | [<span data-ttu-id="e39a5-246">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e39a5-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e39a5-247">Windows Server 2012</span></span>



| <span data-ttu-id="e39a5-248">進入</span><span class="sxs-lookup"><span data-stu-id="e39a5-248">Entry</span></span> | <span data-ttu-id="e39a5-249">值</span><span class="sxs-lookup"><span data-stu-id="e39a5-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e39a5-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e39a5-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e39a5-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="e39a5-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="e39a5-252">System-Only</span></span>            | <span data-ttu-id="e39a5-253">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-253">False</span></span>                                                               |
| <span data-ttu-id="e39a5-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e39a5-254">Is-Single-Valued</span></span>       | <span data-ttu-id="e39a5-255">對</span><span class="sxs-lookup"><span data-stu-id="e39a5-255">True</span></span>                                                                |
| <span data-ttu-id="e39a5-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e39a5-256">Is Indexed</span></span>             | <span data-ttu-id="e39a5-257">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-257">False</span></span>                                                               |
| <span data-ttu-id="e39a5-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e39a5-258">In Global Catalog</span></span>      | <span data-ttu-id="e39a5-259">否</span><span class="sxs-lookup"><span data-stu-id="e39a5-259">False</span></span>                                                               |
| <span data-ttu-id="e39a5-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e39a5-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="e39a5-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e39a5-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="e39a5-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e39a5-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e39a5-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="e39a5-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-264">Search-Flags</span></span>           | <span data-ttu-id="e39a5-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e39a5-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="e39a5-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e39a5-266">System-Flags</span></span>           | <span data-ttu-id="e39a5-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e39a5-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="e39a5-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e39a5-268">Classes used in</span></span>        | [<span data-ttu-id="e39a5-269">**群組-原則-容器**</span><span class="sxs-lookup"><span data-stu-id="e39a5-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





