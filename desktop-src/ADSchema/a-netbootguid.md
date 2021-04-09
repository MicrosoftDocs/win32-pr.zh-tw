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
# <a name="netboot-guid-attribute"></a><span data-ttu-id="78df4-106">Netboot-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="78df4-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="78df4-107">無磁片開機：電腦的機載 GUID。</span><span class="sxs-lookup"><span data-stu-id="78df4-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="78df4-108">對應于電腦的網路介面卡 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="78df4-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="78df4-109">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-109">Entry</span></span> | <span data-ttu-id="78df4-110">值</span><span class="sxs-lookup"><span data-stu-id="78df4-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="78df4-111">CN</span><span class="sxs-lookup"><span data-stu-id="78df4-111">CN</span></span>                | <span data-ttu-id="78df4-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="78df4-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="78df4-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="78df4-113">Ldap-Display-Name</span></span> | <span data-ttu-id="78df4-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="78df4-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="78df4-115">大小</span><span class="sxs-lookup"><span data-stu-id="78df4-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="78df4-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="78df4-116">Update Privilege</span></span>  | <span data-ttu-id="78df4-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="78df4-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="78df4-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="78df4-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="78df4-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-119">Attribute-Id</span></span>      | <span data-ttu-id="78df4-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="78df4-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="78df4-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="78df4-121">System-Id-Guid</span></span>    | <span data-ttu-id="78df4-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="78df4-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="78df4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="78df4-123">Syntax</span></span>            | [<span data-ttu-id="78df4-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="78df4-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="78df4-125">實作</span><span class="sxs-lookup"><span data-stu-id="78df4-125">Implementations</span></span>

-   [<span data-ttu-id="78df4-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="78df4-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="78df4-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="78df4-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="78df4-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="78df4-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="78df4-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="78df4-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="78df4-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="78df4-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="78df4-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="78df4-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="78df4-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78df4-132">Windows 2000 Server</span></span>



| <span data-ttu-id="78df4-133">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-133">Entry</span></span> | <span data-ttu-id="78df4-134">值</span><span class="sxs-lookup"><span data-stu-id="78df4-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-137">System-Only</span></span>            | <span data-ttu-id="78df4-138">否</span><span class="sxs-lookup"><span data-stu-id="78df4-138">False</span></span>                                     |
| <span data-ttu-id="78df4-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-139">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-140">對</span><span class="sxs-lookup"><span data-stu-id="78df4-140">True</span></span>                                      |
| <span data-ttu-id="78df4-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-141">Is Indexed</span></span>             | <span data-ttu-id="78df4-142">對</span><span class="sxs-lookup"><span data-stu-id="78df4-142">True</span></span>                                      |
| <span data-ttu-id="78df4-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-143">In Global Catalog</span></span>      | <span data-ttu-id="78df4-144">對</span><span class="sxs-lookup"><span data-stu-id="78df4-144">True</span></span>                                      |
| <span data-ttu-id="78df4-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-147">Range-Lower</span></span>            | <span data-ttu-id="78df4-148">16</span><span class="sxs-lookup"><span data-stu-id="78df4-148">16</span></span>                                        |
| <span data-ttu-id="78df4-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-149">Range-Upper</span></span>            | <span data-ttu-id="78df4-150">16</span><span class="sxs-lookup"><span data-stu-id="78df4-150">16</span></span>                                        |
| <span data-ttu-id="78df4-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-151">Search-Flags</span></span>           | <span data-ttu-id="78df4-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-152">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-153">System-Flags</span></span>           | <span data-ttu-id="78df4-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-154">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-155">Classes used in</span></span>        | [<span data-ttu-id="78df4-156">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="78df4-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="78df4-157">Windows Server 2003</span></span>



| <span data-ttu-id="78df4-158">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-158">Entry</span></span> | <span data-ttu-id="78df4-159">值</span><span class="sxs-lookup"><span data-stu-id="78df4-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-162">System-Only</span></span>            | <span data-ttu-id="78df4-163">否</span><span class="sxs-lookup"><span data-stu-id="78df4-163">False</span></span>                                     |
| <span data-ttu-id="78df4-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-164">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-165">對</span><span class="sxs-lookup"><span data-stu-id="78df4-165">True</span></span>                                      |
| <span data-ttu-id="78df4-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-166">Is Indexed</span></span>             | <span data-ttu-id="78df4-167">對</span><span class="sxs-lookup"><span data-stu-id="78df4-167">True</span></span>                                      |
| <span data-ttu-id="78df4-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-168">In Global Catalog</span></span>      | <span data-ttu-id="78df4-169">對</span><span class="sxs-lookup"><span data-stu-id="78df4-169">True</span></span>                                      |
| <span data-ttu-id="78df4-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-172">Range-Lower</span></span>            | <span data-ttu-id="78df4-173">16</span><span class="sxs-lookup"><span data-stu-id="78df4-173">16</span></span>                                        |
| <span data-ttu-id="78df4-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-174">Range-Upper</span></span>            | <span data-ttu-id="78df4-175">16</span><span class="sxs-lookup"><span data-stu-id="78df4-175">16</span></span>                                        |
| <span data-ttu-id="78df4-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-176">Search-Flags</span></span>           | <span data-ttu-id="78df4-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-177">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-178">System-Flags</span></span>           | <span data-ttu-id="78df4-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-179">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-180">Classes used in</span></span>        | [<span data-ttu-id="78df4-181">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="78df4-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="78df4-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="78df4-183">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-183">Entry</span></span> | <span data-ttu-id="78df4-184">值</span><span class="sxs-lookup"><span data-stu-id="78df4-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-187">System-Only</span></span>            | <span data-ttu-id="78df4-188">否</span><span class="sxs-lookup"><span data-stu-id="78df4-188">False</span></span>                                     |
| <span data-ttu-id="78df4-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-189">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-190">對</span><span class="sxs-lookup"><span data-stu-id="78df4-190">True</span></span>                                      |
| <span data-ttu-id="78df4-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-191">Is Indexed</span></span>             | <span data-ttu-id="78df4-192">對</span><span class="sxs-lookup"><span data-stu-id="78df4-192">True</span></span>                                      |
| <span data-ttu-id="78df4-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-193">In Global Catalog</span></span>      | <span data-ttu-id="78df4-194">對</span><span class="sxs-lookup"><span data-stu-id="78df4-194">True</span></span>                                      |
| <span data-ttu-id="78df4-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-197">Range-Lower</span></span>            | <span data-ttu-id="78df4-198">16</span><span class="sxs-lookup"><span data-stu-id="78df4-198">16</span></span>                                        |
| <span data-ttu-id="78df4-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-199">Range-Upper</span></span>            | <span data-ttu-id="78df4-200">16</span><span class="sxs-lookup"><span data-stu-id="78df4-200">16</span></span>                                        |
| <span data-ttu-id="78df4-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-201">Search-Flags</span></span>           | <span data-ttu-id="78df4-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-202">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-203">System-Flags</span></span>           | <span data-ttu-id="78df4-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-204">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-205">Classes used in</span></span>        | [<span data-ttu-id="78df4-206">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="78df4-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78df4-207">Windows Server 2008</span></span>



| <span data-ttu-id="78df4-208">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-208">Entry</span></span> | <span data-ttu-id="78df4-209">值</span><span class="sxs-lookup"><span data-stu-id="78df4-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-212">System-Only</span></span>            | <span data-ttu-id="78df4-213">否</span><span class="sxs-lookup"><span data-stu-id="78df4-213">False</span></span>                                     |
| <span data-ttu-id="78df4-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-214">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-215">對</span><span class="sxs-lookup"><span data-stu-id="78df4-215">True</span></span>                                      |
| <span data-ttu-id="78df4-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-216">Is Indexed</span></span>             | <span data-ttu-id="78df4-217">對</span><span class="sxs-lookup"><span data-stu-id="78df4-217">True</span></span>                                      |
| <span data-ttu-id="78df4-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-218">In Global Catalog</span></span>      | <span data-ttu-id="78df4-219">對</span><span class="sxs-lookup"><span data-stu-id="78df4-219">True</span></span>                                      |
| <span data-ttu-id="78df4-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-222">Range-Lower</span></span>            | <span data-ttu-id="78df4-223">16</span><span class="sxs-lookup"><span data-stu-id="78df4-223">16</span></span>                                        |
| <span data-ttu-id="78df4-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-224">Range-Upper</span></span>            | <span data-ttu-id="78df4-225">16</span><span class="sxs-lookup"><span data-stu-id="78df4-225">16</span></span>                                        |
| <span data-ttu-id="78df4-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-226">Search-Flags</span></span>           | <span data-ttu-id="78df4-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-227">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-228">System-Flags</span></span>           | <span data-ttu-id="78df4-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-229">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-230">Classes used in</span></span>        | [<span data-ttu-id="78df4-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="78df4-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78df4-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="78df4-233">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-233">Entry</span></span> | <span data-ttu-id="78df4-234">值</span><span class="sxs-lookup"><span data-stu-id="78df4-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-237">System-Only</span></span>            | <span data-ttu-id="78df4-238">否</span><span class="sxs-lookup"><span data-stu-id="78df4-238">False</span></span>                                     |
| <span data-ttu-id="78df4-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-239">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-240">對</span><span class="sxs-lookup"><span data-stu-id="78df4-240">True</span></span>                                      |
| <span data-ttu-id="78df4-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-241">Is Indexed</span></span>             | <span data-ttu-id="78df4-242">對</span><span class="sxs-lookup"><span data-stu-id="78df4-242">True</span></span>                                      |
| <span data-ttu-id="78df4-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-243">In Global Catalog</span></span>      | <span data-ttu-id="78df4-244">對</span><span class="sxs-lookup"><span data-stu-id="78df4-244">True</span></span>                                      |
| <span data-ttu-id="78df4-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-247">Range-Lower</span></span>            | <span data-ttu-id="78df4-248">16</span><span class="sxs-lookup"><span data-stu-id="78df4-248">16</span></span>                                        |
| <span data-ttu-id="78df4-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-249">Range-Upper</span></span>            | <span data-ttu-id="78df4-250">16</span><span class="sxs-lookup"><span data-stu-id="78df4-250">16</span></span>                                        |
| <span data-ttu-id="78df4-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-251">Search-Flags</span></span>           | <span data-ttu-id="78df4-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-252">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-253">System-Flags</span></span>           | <span data-ttu-id="78df4-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-254">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-255">Classes used in</span></span>        | [<span data-ttu-id="78df4-256">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="78df4-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78df4-257">Windows Server 2012</span></span>



| <span data-ttu-id="78df4-258">進入</span><span class="sxs-lookup"><span data-stu-id="78df4-258">Entry</span></span> | <span data-ttu-id="78df4-259">值</span><span class="sxs-lookup"><span data-stu-id="78df4-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="78df4-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="78df4-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="78df4-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="78df4-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="78df4-262">System-Only</span></span>            | <span data-ttu-id="78df4-263">否</span><span class="sxs-lookup"><span data-stu-id="78df4-263">False</span></span>                                     |
| <span data-ttu-id="78df4-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="78df4-264">Is-Single-Valued</span></span>       | <span data-ttu-id="78df4-265">對</span><span class="sxs-lookup"><span data-stu-id="78df4-265">True</span></span>                                      |
| <span data-ttu-id="78df4-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="78df4-266">Is Indexed</span></span>             | <span data-ttu-id="78df4-267">對</span><span class="sxs-lookup"><span data-stu-id="78df4-267">True</span></span>                                      |
| <span data-ttu-id="78df4-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="78df4-268">In Global Catalog</span></span>      | <span data-ttu-id="78df4-269">對</span><span class="sxs-lookup"><span data-stu-id="78df4-269">True</span></span>                                      |
| <span data-ttu-id="78df4-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="78df4-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="78df4-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="78df4-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="78df4-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="78df4-272">Range-Lower</span></span>            | <span data-ttu-id="78df4-273">16</span><span class="sxs-lookup"><span data-stu-id="78df4-273">16</span></span>                                        |
| <span data-ttu-id="78df4-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="78df4-274">Range-Upper</span></span>            | <span data-ttu-id="78df4-275">16</span><span class="sxs-lookup"><span data-stu-id="78df4-275">16</span></span>                                        |
| <span data-ttu-id="78df4-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-276">Search-Flags</span></span>           | <span data-ttu-id="78df4-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78df4-277">0x00000001</span></span>                                |
| <span data-ttu-id="78df4-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="78df4-278">System-Flags</span></span>           | <span data-ttu-id="78df4-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78df4-279">0x00000010</span></span>                                |
| <span data-ttu-id="78df4-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="78df4-280">Classes used in</span></span>        | [<span data-ttu-id="78df4-281">**電腦**</span><span class="sxs-lookup"><span data-stu-id="78df4-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





