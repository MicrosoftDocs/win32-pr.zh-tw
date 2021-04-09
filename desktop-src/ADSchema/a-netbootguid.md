---
title: Netboot-GUID 屬性
description: 無磁片開機：電腦的機載 GUID。 對應于電腦的網路介面卡 MAC 位址。
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Netboot-GUID 屬性 AD 架構
- netbootGUID 屬性 AD 架構
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845387"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="12844-106">Netboot-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="12844-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="12844-107">無磁片開機：電腦的機載 GUID。</span><span class="sxs-lookup"><span data-stu-id="12844-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="12844-108">對應于電腦的網路介面卡 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="12844-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="12844-109">進入</span><span class="sxs-lookup"><span data-stu-id="12844-109">Entry</span></span> | <span data-ttu-id="12844-110">值</span><span class="sxs-lookup"><span data-stu-id="12844-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="12844-111">CN</span><span class="sxs-lookup"><span data-stu-id="12844-111">CN</span></span>                | <span data-ttu-id="12844-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="12844-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="12844-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="12844-113">Ldap-Display-Name</span></span> | <span data-ttu-id="12844-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="12844-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="12844-115">大小</span><span class="sxs-lookup"><span data-stu-id="12844-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="12844-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="12844-116">Update Privilege</span></span>  | <span data-ttu-id="12844-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="12844-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="12844-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="12844-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="12844-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="12844-119">Attribute-Id</span></span>      | <span data-ttu-id="12844-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="12844-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="12844-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="12844-121">System-Id-Guid</span></span>    | <span data-ttu-id="12844-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="12844-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="12844-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="12844-123">Syntax</span></span>            | [<span data-ttu-id="12844-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="12844-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="12844-125">實作</span><span class="sxs-lookup"><span data-stu-id="12844-125">Implementations</span></span>

-   [<span data-ttu-id="12844-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="12844-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="12844-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="12844-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="12844-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="12844-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="12844-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="12844-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="12844-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="12844-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="12844-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="12844-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="12844-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12844-132">Windows 2000 Server</span></span>



| <span data-ttu-id="12844-133">進入</span><span class="sxs-lookup"><span data-stu-id="12844-133">Entry</span></span> | <span data-ttu-id="12844-134">值</span><span class="sxs-lookup"><span data-stu-id="12844-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-137">System-Only</span></span>            | <span data-ttu-id="12844-138">否</span><span class="sxs-lookup"><span data-stu-id="12844-138">False</span></span>                                     |
| <span data-ttu-id="12844-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-139">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-140">對</span><span class="sxs-lookup"><span data-stu-id="12844-140">True</span></span>                                      |
| <span data-ttu-id="12844-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-141">Is Indexed</span></span>             | <span data-ttu-id="12844-142">對</span><span class="sxs-lookup"><span data-stu-id="12844-142">True</span></span>                                      |
| <span data-ttu-id="12844-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-143">In Global Catalog</span></span>      | <span data-ttu-id="12844-144">對</span><span class="sxs-lookup"><span data-stu-id="12844-144">True</span></span>                                      |
| <span data-ttu-id="12844-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-147">Range-Lower</span></span>            | <span data-ttu-id="12844-148">16</span><span class="sxs-lookup"><span data-stu-id="12844-148">16</span></span>                                        |
| <span data-ttu-id="12844-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-149">Range-Upper</span></span>            | <span data-ttu-id="12844-150">16</span><span class="sxs-lookup"><span data-stu-id="12844-150">16</span></span>                                        |
| <span data-ttu-id="12844-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-151">Search-Flags</span></span>           | <span data-ttu-id="12844-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-152">0x00000001</span></span>                                |
| <span data-ttu-id="12844-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-153">System-Flags</span></span>           | <span data-ttu-id="12844-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-154">0x00000010</span></span>                                |
| <span data-ttu-id="12844-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-155">Classes used in</span></span>        | [<span data-ttu-id="12844-156">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="12844-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="12844-157">Windows Server 2003</span></span>



| <span data-ttu-id="12844-158">進入</span><span class="sxs-lookup"><span data-stu-id="12844-158">Entry</span></span> | <span data-ttu-id="12844-159">值</span><span class="sxs-lookup"><span data-stu-id="12844-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-162">System-Only</span></span>            | <span data-ttu-id="12844-163">否</span><span class="sxs-lookup"><span data-stu-id="12844-163">False</span></span>                                     |
| <span data-ttu-id="12844-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-164">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-165">對</span><span class="sxs-lookup"><span data-stu-id="12844-165">True</span></span>                                      |
| <span data-ttu-id="12844-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-166">Is Indexed</span></span>             | <span data-ttu-id="12844-167">對</span><span class="sxs-lookup"><span data-stu-id="12844-167">True</span></span>                                      |
| <span data-ttu-id="12844-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-168">In Global Catalog</span></span>      | <span data-ttu-id="12844-169">對</span><span class="sxs-lookup"><span data-stu-id="12844-169">True</span></span>                                      |
| <span data-ttu-id="12844-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-172">Range-Lower</span></span>            | <span data-ttu-id="12844-173">16</span><span class="sxs-lookup"><span data-stu-id="12844-173">16</span></span>                                        |
| <span data-ttu-id="12844-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-174">Range-Upper</span></span>            | <span data-ttu-id="12844-175">16</span><span class="sxs-lookup"><span data-stu-id="12844-175">16</span></span>                                        |
| <span data-ttu-id="12844-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-176">Search-Flags</span></span>           | <span data-ttu-id="12844-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-177">0x00000001</span></span>                                |
| <span data-ttu-id="12844-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-178">System-Flags</span></span>           | <span data-ttu-id="12844-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-179">0x00000010</span></span>                                |
| <span data-ttu-id="12844-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-180">Classes used in</span></span>        | [<span data-ttu-id="12844-181">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="12844-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="12844-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="12844-183">進入</span><span class="sxs-lookup"><span data-stu-id="12844-183">Entry</span></span> | <span data-ttu-id="12844-184">值</span><span class="sxs-lookup"><span data-stu-id="12844-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-187">System-Only</span></span>            | <span data-ttu-id="12844-188">否</span><span class="sxs-lookup"><span data-stu-id="12844-188">False</span></span>                                     |
| <span data-ttu-id="12844-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-189">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-190">對</span><span class="sxs-lookup"><span data-stu-id="12844-190">True</span></span>                                      |
| <span data-ttu-id="12844-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-191">Is Indexed</span></span>             | <span data-ttu-id="12844-192">對</span><span class="sxs-lookup"><span data-stu-id="12844-192">True</span></span>                                      |
| <span data-ttu-id="12844-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-193">In Global Catalog</span></span>      | <span data-ttu-id="12844-194">對</span><span class="sxs-lookup"><span data-stu-id="12844-194">True</span></span>                                      |
| <span data-ttu-id="12844-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-197">Range-Lower</span></span>            | <span data-ttu-id="12844-198">16</span><span class="sxs-lookup"><span data-stu-id="12844-198">16</span></span>                                        |
| <span data-ttu-id="12844-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-199">Range-Upper</span></span>            | <span data-ttu-id="12844-200">16</span><span class="sxs-lookup"><span data-stu-id="12844-200">16</span></span>                                        |
| <span data-ttu-id="12844-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-201">Search-Flags</span></span>           | <span data-ttu-id="12844-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-202">0x00000001</span></span>                                |
| <span data-ttu-id="12844-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-203">System-Flags</span></span>           | <span data-ttu-id="12844-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-204">0x00000010</span></span>                                |
| <span data-ttu-id="12844-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-205">Classes used in</span></span>        | [<span data-ttu-id="12844-206">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="12844-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12844-207">Windows Server 2008</span></span>



| <span data-ttu-id="12844-208">進入</span><span class="sxs-lookup"><span data-stu-id="12844-208">Entry</span></span> | <span data-ttu-id="12844-209">值</span><span class="sxs-lookup"><span data-stu-id="12844-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-212">System-Only</span></span>            | <span data-ttu-id="12844-213">否</span><span class="sxs-lookup"><span data-stu-id="12844-213">False</span></span>                                     |
| <span data-ttu-id="12844-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-214">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-215">對</span><span class="sxs-lookup"><span data-stu-id="12844-215">True</span></span>                                      |
| <span data-ttu-id="12844-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-216">Is Indexed</span></span>             | <span data-ttu-id="12844-217">對</span><span class="sxs-lookup"><span data-stu-id="12844-217">True</span></span>                                      |
| <span data-ttu-id="12844-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-218">In Global Catalog</span></span>      | <span data-ttu-id="12844-219">對</span><span class="sxs-lookup"><span data-stu-id="12844-219">True</span></span>                                      |
| <span data-ttu-id="12844-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-222">Range-Lower</span></span>            | <span data-ttu-id="12844-223">16</span><span class="sxs-lookup"><span data-stu-id="12844-223">16</span></span>                                        |
| <span data-ttu-id="12844-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-224">Range-Upper</span></span>            | <span data-ttu-id="12844-225">16</span><span class="sxs-lookup"><span data-stu-id="12844-225">16</span></span>                                        |
| <span data-ttu-id="12844-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-226">Search-Flags</span></span>           | <span data-ttu-id="12844-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-227">0x00000001</span></span>                                |
| <span data-ttu-id="12844-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-228">System-Flags</span></span>           | <span data-ttu-id="12844-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-229">0x00000010</span></span>                                |
| <span data-ttu-id="12844-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-230">Classes used in</span></span>        | [<span data-ttu-id="12844-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="12844-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="12844-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="12844-233">進入</span><span class="sxs-lookup"><span data-stu-id="12844-233">Entry</span></span> | <span data-ttu-id="12844-234">值</span><span class="sxs-lookup"><span data-stu-id="12844-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-237">System-Only</span></span>            | <span data-ttu-id="12844-238">否</span><span class="sxs-lookup"><span data-stu-id="12844-238">False</span></span>                                     |
| <span data-ttu-id="12844-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-239">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-240">對</span><span class="sxs-lookup"><span data-stu-id="12844-240">True</span></span>                                      |
| <span data-ttu-id="12844-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-241">Is Indexed</span></span>             | <span data-ttu-id="12844-242">對</span><span class="sxs-lookup"><span data-stu-id="12844-242">True</span></span>                                      |
| <span data-ttu-id="12844-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-243">In Global Catalog</span></span>      | <span data-ttu-id="12844-244">對</span><span class="sxs-lookup"><span data-stu-id="12844-244">True</span></span>                                      |
| <span data-ttu-id="12844-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-247">Range-Lower</span></span>            | <span data-ttu-id="12844-248">16</span><span class="sxs-lookup"><span data-stu-id="12844-248">16</span></span>                                        |
| <span data-ttu-id="12844-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-249">Range-Upper</span></span>            | <span data-ttu-id="12844-250">16</span><span class="sxs-lookup"><span data-stu-id="12844-250">16</span></span>                                        |
| <span data-ttu-id="12844-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-251">Search-Flags</span></span>           | <span data-ttu-id="12844-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-252">0x00000001</span></span>                                |
| <span data-ttu-id="12844-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-253">System-Flags</span></span>           | <span data-ttu-id="12844-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-254">0x00000010</span></span>                                |
| <span data-ttu-id="12844-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-255">Classes used in</span></span>        | [<span data-ttu-id="12844-256">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="12844-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12844-257">Windows Server 2012</span></span>



| <span data-ttu-id="12844-258">進入</span><span class="sxs-lookup"><span data-stu-id="12844-258">Entry</span></span> | <span data-ttu-id="12844-259">值</span><span class="sxs-lookup"><span data-stu-id="12844-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="12844-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="12844-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="12844-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="12844-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="12844-262">System-Only</span></span>            | <span data-ttu-id="12844-263">否</span><span class="sxs-lookup"><span data-stu-id="12844-263">False</span></span>                                     |
| <span data-ttu-id="12844-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="12844-264">Is-Single-Valued</span></span>       | <span data-ttu-id="12844-265">對</span><span class="sxs-lookup"><span data-stu-id="12844-265">True</span></span>                                      |
| <span data-ttu-id="12844-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="12844-266">Is Indexed</span></span>             | <span data-ttu-id="12844-267">對</span><span class="sxs-lookup"><span data-stu-id="12844-267">True</span></span>                                      |
| <span data-ttu-id="12844-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="12844-268">In Global Catalog</span></span>      | <span data-ttu-id="12844-269">對</span><span class="sxs-lookup"><span data-stu-id="12844-269">True</span></span>                                      |
| <span data-ttu-id="12844-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="12844-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="12844-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="12844-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="12844-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="12844-272">Range-Lower</span></span>            | <span data-ttu-id="12844-273">16</span><span class="sxs-lookup"><span data-stu-id="12844-273">16</span></span>                                        |
| <span data-ttu-id="12844-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="12844-274">Range-Upper</span></span>            | <span data-ttu-id="12844-275">16</span><span class="sxs-lookup"><span data-stu-id="12844-275">16</span></span>                                        |
| <span data-ttu-id="12844-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-276">Search-Flags</span></span>           | <span data-ttu-id="12844-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12844-277">0x00000001</span></span>                                |
| <span data-ttu-id="12844-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="12844-278">System-Flags</span></span>           | <span data-ttu-id="12844-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12844-279">0x00000010</span></span>                                |
| <span data-ttu-id="12844-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="12844-280">Classes used in</span></span>        | [<span data-ttu-id="12844-281">**電腦**</span><span class="sxs-lookup"><span data-stu-id="12844-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





