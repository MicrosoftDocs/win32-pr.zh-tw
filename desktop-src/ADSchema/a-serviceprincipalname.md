---
title: 服務主體名稱屬性
description: 用來在這部電腦上與服務實例進行相互驗證的主體名稱清單。
ms.assetid: 0ad1694f-0d6f-4350-a088-fdf3ef798c46
ms.tgt_platform: multiple
keywords:
- 服務主體名稱屬性 AD 架構
- servicePrincipalName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Service-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861f160d2c9b71d2c9914c7ff9c2ea0ee43c8528
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106968402"
---
# <a name="service-principal-name-attribute"></a><span data-ttu-id="666be-105">服務主體名稱屬性</span><span class="sxs-lookup"><span data-stu-id="666be-105">Service-Principal-Name attribute</span></span>

<span data-ttu-id="666be-106">用來在這部電腦上與服務實例進行相互驗證的主體名稱清單。</span><span class="sxs-lookup"><span data-stu-id="666be-106">List of principal names used for mutual authentication with an instance of a service on this computer.</span></span>



| <span data-ttu-id="666be-107">進入</span><span class="sxs-lookup"><span data-stu-id="666be-107">Entry</span></span> | <span data-ttu-id="666be-108">值</span><span class="sxs-lookup"><span data-stu-id="666be-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="666be-109">CN</span><span class="sxs-lookup"><span data-stu-id="666be-109">CN</span></span>                | <span data-ttu-id="666be-110">服務主體名稱</span><span class="sxs-lookup"><span data-stu-id="666be-110">Service-Principal-Name</span></span>                      |
| <span data-ttu-id="666be-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="666be-111">Ldap-Display-Name</span></span> | <span data-ttu-id="666be-112">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="666be-112">servicePrincipalName</span></span>                        |
| <span data-ttu-id="666be-113">大小</span><span class="sxs-lookup"><span data-stu-id="666be-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="666be-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="666be-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="666be-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="666be-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="666be-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="666be-116">Attribute-Id</span></span>      | <span data-ttu-id="666be-117">1.2.840.113556.1.4.771</span><span class="sxs-lookup"><span data-stu-id="666be-117">1.2.840.113556.1.4.771</span></span>                      |
| <span data-ttu-id="666be-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="666be-118">System-Id-Guid</span></span>    | <span data-ttu-id="666be-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="666be-119">f3a64788-5306-11d1-a9c5-0000f80367c1</span></span>        |
| <span data-ttu-id="666be-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="666be-120">Syntax</span></span>            | [<span data-ttu-id="666be-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="666be-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="666be-122">實作</span><span class="sxs-lookup"><span data-stu-id="666be-122">Implementations</span></span>

-   [<span data-ttu-id="666be-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="666be-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="666be-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="666be-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="666be-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="666be-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="666be-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="666be-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="666be-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="666be-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="666be-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="666be-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="666be-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="666be-129">Windows 2000 Server</span></span>



| <span data-ttu-id="666be-130">進入</span><span class="sxs-lookup"><span data-stu-id="666be-130">Entry</span></span> | <span data-ttu-id="666be-131">值</span><span class="sxs-lookup"><span data-stu-id="666be-131">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-132">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-133">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-134">System-Only</span></span>            | <span data-ttu-id="666be-135">否</span><span class="sxs-lookup"><span data-stu-id="666be-135">False</span></span>                             |
| <span data-ttu-id="666be-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-136">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-137">否</span><span class="sxs-lookup"><span data-stu-id="666be-137">False</span></span>                             |
| <span data-ttu-id="666be-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-138">Is Indexed</span></span>             | <span data-ttu-id="666be-139">對</span><span class="sxs-lookup"><span data-stu-id="666be-139">True</span></span>                              |
| <span data-ttu-id="666be-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-140">In Global Catalog</span></span>      | <span data-ttu-id="666be-141">對</span><span class="sxs-lookup"><span data-stu-id="666be-141">True</span></span>                              |
| <span data-ttu-id="666be-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-143">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-144">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-145">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-146">Search-Flags</span></span>           | <span data-ttu-id="666be-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-147">0x00000001</span></span>                        |
| <span data-ttu-id="666be-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-148">System-Flags</span></span>           | <span data-ttu-id="666be-149">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-149">0x00000012</span></span>                        |
| <span data-ttu-id="666be-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-150">Classes used in</span></span>        | [<span data-ttu-id="666be-151">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="666be-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="666be-152">Windows Server 2003</span></span>



| <span data-ttu-id="666be-153">進入</span><span class="sxs-lookup"><span data-stu-id="666be-153">Entry</span></span> | <span data-ttu-id="666be-154">值</span><span class="sxs-lookup"><span data-stu-id="666be-154">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-155">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-157">System-Only</span></span>            | <span data-ttu-id="666be-158">否</span><span class="sxs-lookup"><span data-stu-id="666be-158">False</span></span>                             |
| <span data-ttu-id="666be-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-159">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-160">否</span><span class="sxs-lookup"><span data-stu-id="666be-160">False</span></span>                             |
| <span data-ttu-id="666be-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-161">Is Indexed</span></span>             | <span data-ttu-id="666be-162">對</span><span class="sxs-lookup"><span data-stu-id="666be-162">True</span></span>                              |
| <span data-ttu-id="666be-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-163">In Global Catalog</span></span>      | <span data-ttu-id="666be-164">對</span><span class="sxs-lookup"><span data-stu-id="666be-164">True</span></span>                              |
| <span data-ttu-id="666be-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-169">Search-Flags</span></span>           | <span data-ttu-id="666be-170">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-170">0x00000001</span></span>                        |
| <span data-ttu-id="666be-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-171">System-Flags</span></span>           | <span data-ttu-id="666be-172">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-172">0x00000012</span></span>                        |
| <span data-ttu-id="666be-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-173">Classes used in</span></span>        | [<span data-ttu-id="666be-174">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="666be-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="666be-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="666be-176">進入</span><span class="sxs-lookup"><span data-stu-id="666be-176">Entry</span></span> | <span data-ttu-id="666be-177">值</span><span class="sxs-lookup"><span data-stu-id="666be-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-178">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-179">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-180">System-Only</span></span>            | <span data-ttu-id="666be-181">否</span><span class="sxs-lookup"><span data-stu-id="666be-181">False</span></span>                             |
| <span data-ttu-id="666be-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-182">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-183">否</span><span class="sxs-lookup"><span data-stu-id="666be-183">False</span></span>                             |
| <span data-ttu-id="666be-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-184">Is Indexed</span></span>             | <span data-ttu-id="666be-185">對</span><span class="sxs-lookup"><span data-stu-id="666be-185">True</span></span>                              |
| <span data-ttu-id="666be-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-186">In Global Catalog</span></span>      | <span data-ttu-id="666be-187">對</span><span class="sxs-lookup"><span data-stu-id="666be-187">True</span></span>                              |
| <span data-ttu-id="666be-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-189">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-190">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-191">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-192">Search-Flags</span></span>           | <span data-ttu-id="666be-193">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-193">0x00000001</span></span>                        |
| <span data-ttu-id="666be-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-194">System-Flags</span></span>           | <span data-ttu-id="666be-195">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-195">0x00000012</span></span>                        |
| <span data-ttu-id="666be-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-196">Classes used in</span></span>        | [<span data-ttu-id="666be-197">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-197">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="666be-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="666be-198">Windows Server 2008</span></span>



| <span data-ttu-id="666be-199">進入</span><span class="sxs-lookup"><span data-stu-id="666be-199">Entry</span></span> | <span data-ttu-id="666be-200">值</span><span class="sxs-lookup"><span data-stu-id="666be-200">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-201">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-202">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-203">System-Only</span></span>            | <span data-ttu-id="666be-204">否</span><span class="sxs-lookup"><span data-stu-id="666be-204">False</span></span>                             |
| <span data-ttu-id="666be-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-205">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-206">否</span><span class="sxs-lookup"><span data-stu-id="666be-206">False</span></span>                             |
| <span data-ttu-id="666be-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-207">Is Indexed</span></span>             | <span data-ttu-id="666be-208">對</span><span class="sxs-lookup"><span data-stu-id="666be-208">True</span></span>                              |
| <span data-ttu-id="666be-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-209">In Global Catalog</span></span>      | <span data-ttu-id="666be-210">對</span><span class="sxs-lookup"><span data-stu-id="666be-210">True</span></span>                              |
| <span data-ttu-id="666be-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-212">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-213">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-214">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-215">Search-Flags</span></span>           | <span data-ttu-id="666be-216">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-216">0x00000001</span></span>                        |
| <span data-ttu-id="666be-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-217">System-Flags</span></span>           | <span data-ttu-id="666be-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-218">0x00000012</span></span>                        |
| <span data-ttu-id="666be-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-219">Classes used in</span></span>        | [<span data-ttu-id="666be-220">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-220">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="666be-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="666be-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="666be-222">進入</span><span class="sxs-lookup"><span data-stu-id="666be-222">Entry</span></span> | <span data-ttu-id="666be-223">值</span><span class="sxs-lookup"><span data-stu-id="666be-223">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-224">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-225">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-226">System-Only</span></span>            | <span data-ttu-id="666be-227">否</span><span class="sxs-lookup"><span data-stu-id="666be-227">False</span></span>                             |
| <span data-ttu-id="666be-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-228">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-229">否</span><span class="sxs-lookup"><span data-stu-id="666be-229">False</span></span>                             |
| <span data-ttu-id="666be-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-230">Is Indexed</span></span>             | <span data-ttu-id="666be-231">對</span><span class="sxs-lookup"><span data-stu-id="666be-231">True</span></span>                              |
| <span data-ttu-id="666be-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-232">In Global Catalog</span></span>      | <span data-ttu-id="666be-233">對</span><span class="sxs-lookup"><span data-stu-id="666be-233">True</span></span>                              |
| <span data-ttu-id="666be-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-235">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-236">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-237">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-238">Search-Flags</span></span>           | <span data-ttu-id="666be-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-239">0x00000001</span></span>                        |
| <span data-ttu-id="666be-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-240">System-Flags</span></span>           | <span data-ttu-id="666be-241">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-241">0x00000012</span></span>                        |
| <span data-ttu-id="666be-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-242">Classes used in</span></span>        | [<span data-ttu-id="666be-243">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-243">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="666be-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="666be-244">Windows Server 2012</span></span>



| <span data-ttu-id="666be-245">進入</span><span class="sxs-lookup"><span data-stu-id="666be-245">Entry</span></span> | <span data-ttu-id="666be-246">值</span><span class="sxs-lookup"><span data-stu-id="666be-246">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="666be-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="666be-247">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="666be-248">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="666be-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="666be-249">System-Only</span></span>            | <span data-ttu-id="666be-250">否</span><span class="sxs-lookup"><span data-stu-id="666be-250">False</span></span>                             |
| <span data-ttu-id="666be-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="666be-251">Is-Single-Valued</span></span>       | <span data-ttu-id="666be-252">否</span><span class="sxs-lookup"><span data-stu-id="666be-252">False</span></span>                             |
| <span data-ttu-id="666be-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="666be-253">Is Indexed</span></span>             | <span data-ttu-id="666be-254">對</span><span class="sxs-lookup"><span data-stu-id="666be-254">True</span></span>                              |
| <span data-ttu-id="666be-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="666be-255">In Global Catalog</span></span>      | <span data-ttu-id="666be-256">對</span><span class="sxs-lookup"><span data-stu-id="666be-256">True</span></span>                              |
| <span data-ttu-id="666be-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="666be-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="666be-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="666be-258">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="666be-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="666be-259">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="666be-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="666be-260">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="666be-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-261">Search-Flags</span></span>           | <span data-ttu-id="666be-262">0x00000001</span><span class="sxs-lookup"><span data-stu-id="666be-262">0x00000001</span></span>                        |
| <span data-ttu-id="666be-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="666be-263">System-Flags</span></span>           | <span data-ttu-id="666be-264">0x00000012</span><span class="sxs-lookup"><span data-stu-id="666be-264">0x00000012</span></span>                        |
| <span data-ttu-id="666be-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="666be-265">Classes used in</span></span>        | [<span data-ttu-id="666be-266">**User**</span><span class="sxs-lookup"><span data-stu-id="666be-266">**User**</span></span>](c-user.md)<br/> |



 

 





