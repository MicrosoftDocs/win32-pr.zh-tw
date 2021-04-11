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
# <a name="netboot-guid-attribute"></a><span data-ttu-id="63edd-106">Netboot-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="63edd-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="63edd-107">無磁片開機：電腦的機載 GUID。</span><span class="sxs-lookup"><span data-stu-id="63edd-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="63edd-108">對應于電腦的網路介面卡 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="63edd-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="63edd-109">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-109">Entry</span></span> | <span data-ttu-id="63edd-110">值</span><span class="sxs-lookup"><span data-stu-id="63edd-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="63edd-111">CN</span><span class="sxs-lookup"><span data-stu-id="63edd-111">CN</span></span>                | <span data-ttu-id="63edd-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="63edd-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="63edd-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="63edd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="63edd-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="63edd-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="63edd-115">大小</span><span class="sxs-lookup"><span data-stu-id="63edd-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="63edd-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="63edd-116">Update Privilege</span></span>  | <span data-ttu-id="63edd-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="63edd-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="63edd-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="63edd-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="63edd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-119">Attribute-Id</span></span>      | <span data-ttu-id="63edd-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="63edd-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="63edd-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="63edd-121">System-Id-Guid</span></span>    | <span data-ttu-id="63edd-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="63edd-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="63edd-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="63edd-123">Syntax</span></span>            | [<span data-ttu-id="63edd-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="63edd-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="63edd-125">實作</span><span class="sxs-lookup"><span data-stu-id="63edd-125">Implementations</span></span>

-   [<span data-ttu-id="63edd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63edd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63edd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63edd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63edd-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63edd-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63edd-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63edd-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63edd-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63edd-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63edd-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63edd-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63edd-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63edd-132">Windows 2000 Server</span></span>



| <span data-ttu-id="63edd-133">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-133">Entry</span></span> | <span data-ttu-id="63edd-134">值</span><span class="sxs-lookup"><span data-stu-id="63edd-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-137">System-Only</span></span>            | <span data-ttu-id="63edd-138">否</span><span class="sxs-lookup"><span data-stu-id="63edd-138">False</span></span>                                     |
| <span data-ttu-id="63edd-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-139">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-140">對</span><span class="sxs-lookup"><span data-stu-id="63edd-140">True</span></span>                                      |
| <span data-ttu-id="63edd-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-141">Is Indexed</span></span>             | <span data-ttu-id="63edd-142">對</span><span class="sxs-lookup"><span data-stu-id="63edd-142">True</span></span>                                      |
| <span data-ttu-id="63edd-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-143">In Global Catalog</span></span>      | <span data-ttu-id="63edd-144">對</span><span class="sxs-lookup"><span data-stu-id="63edd-144">True</span></span>                                      |
| <span data-ttu-id="63edd-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-147">Range-Lower</span></span>            | <span data-ttu-id="63edd-148">16</span><span class="sxs-lookup"><span data-stu-id="63edd-148">16</span></span>                                        |
| <span data-ttu-id="63edd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-149">Range-Upper</span></span>            | <span data-ttu-id="63edd-150">16</span><span class="sxs-lookup"><span data-stu-id="63edd-150">16</span></span>                                        |
| <span data-ttu-id="63edd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-151">Search-Flags</span></span>           | <span data-ttu-id="63edd-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-152">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-153">System-Flags</span></span>           | <span data-ttu-id="63edd-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-154">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-155">Classes used in</span></span>        | [<span data-ttu-id="63edd-156">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63edd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63edd-157">Windows Server 2003</span></span>



| <span data-ttu-id="63edd-158">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-158">Entry</span></span> | <span data-ttu-id="63edd-159">值</span><span class="sxs-lookup"><span data-stu-id="63edd-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-162">System-Only</span></span>            | <span data-ttu-id="63edd-163">否</span><span class="sxs-lookup"><span data-stu-id="63edd-163">False</span></span>                                     |
| <span data-ttu-id="63edd-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-165">對</span><span class="sxs-lookup"><span data-stu-id="63edd-165">True</span></span>                                      |
| <span data-ttu-id="63edd-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-166">Is Indexed</span></span>             | <span data-ttu-id="63edd-167">對</span><span class="sxs-lookup"><span data-stu-id="63edd-167">True</span></span>                                      |
| <span data-ttu-id="63edd-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-168">In Global Catalog</span></span>      | <span data-ttu-id="63edd-169">對</span><span class="sxs-lookup"><span data-stu-id="63edd-169">True</span></span>                                      |
| <span data-ttu-id="63edd-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-172">Range-Lower</span></span>            | <span data-ttu-id="63edd-173">16</span><span class="sxs-lookup"><span data-stu-id="63edd-173">16</span></span>                                        |
| <span data-ttu-id="63edd-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-174">Range-Upper</span></span>            | <span data-ttu-id="63edd-175">16</span><span class="sxs-lookup"><span data-stu-id="63edd-175">16</span></span>                                        |
| <span data-ttu-id="63edd-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-176">Search-Flags</span></span>           | <span data-ttu-id="63edd-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-177">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-178">System-Flags</span></span>           | <span data-ttu-id="63edd-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-179">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-180">Classes used in</span></span>        | [<span data-ttu-id="63edd-181">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63edd-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63edd-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63edd-183">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-183">Entry</span></span> | <span data-ttu-id="63edd-184">值</span><span class="sxs-lookup"><span data-stu-id="63edd-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-187">System-Only</span></span>            | <span data-ttu-id="63edd-188">否</span><span class="sxs-lookup"><span data-stu-id="63edd-188">False</span></span>                                     |
| <span data-ttu-id="63edd-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-189">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-190">對</span><span class="sxs-lookup"><span data-stu-id="63edd-190">True</span></span>                                      |
| <span data-ttu-id="63edd-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-191">Is Indexed</span></span>             | <span data-ttu-id="63edd-192">對</span><span class="sxs-lookup"><span data-stu-id="63edd-192">True</span></span>                                      |
| <span data-ttu-id="63edd-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-193">In Global Catalog</span></span>      | <span data-ttu-id="63edd-194">對</span><span class="sxs-lookup"><span data-stu-id="63edd-194">True</span></span>                                      |
| <span data-ttu-id="63edd-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-197">Range-Lower</span></span>            | <span data-ttu-id="63edd-198">16</span><span class="sxs-lookup"><span data-stu-id="63edd-198">16</span></span>                                        |
| <span data-ttu-id="63edd-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-199">Range-Upper</span></span>            | <span data-ttu-id="63edd-200">16</span><span class="sxs-lookup"><span data-stu-id="63edd-200">16</span></span>                                        |
| <span data-ttu-id="63edd-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-201">Search-Flags</span></span>           | <span data-ttu-id="63edd-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-202">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-203">System-Flags</span></span>           | <span data-ttu-id="63edd-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-204">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-205">Classes used in</span></span>        | [<span data-ttu-id="63edd-206">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63edd-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63edd-207">Windows Server 2008</span></span>



| <span data-ttu-id="63edd-208">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-208">Entry</span></span> | <span data-ttu-id="63edd-209">值</span><span class="sxs-lookup"><span data-stu-id="63edd-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-212">System-Only</span></span>            | <span data-ttu-id="63edd-213">否</span><span class="sxs-lookup"><span data-stu-id="63edd-213">False</span></span>                                     |
| <span data-ttu-id="63edd-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-214">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-215">對</span><span class="sxs-lookup"><span data-stu-id="63edd-215">True</span></span>                                      |
| <span data-ttu-id="63edd-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-216">Is Indexed</span></span>             | <span data-ttu-id="63edd-217">對</span><span class="sxs-lookup"><span data-stu-id="63edd-217">True</span></span>                                      |
| <span data-ttu-id="63edd-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-218">In Global Catalog</span></span>      | <span data-ttu-id="63edd-219">對</span><span class="sxs-lookup"><span data-stu-id="63edd-219">True</span></span>                                      |
| <span data-ttu-id="63edd-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-222">Range-Lower</span></span>            | <span data-ttu-id="63edd-223">16</span><span class="sxs-lookup"><span data-stu-id="63edd-223">16</span></span>                                        |
| <span data-ttu-id="63edd-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-224">Range-Upper</span></span>            | <span data-ttu-id="63edd-225">16</span><span class="sxs-lookup"><span data-stu-id="63edd-225">16</span></span>                                        |
| <span data-ttu-id="63edd-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-226">Search-Flags</span></span>           | <span data-ttu-id="63edd-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-227">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-228">System-Flags</span></span>           | <span data-ttu-id="63edd-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-229">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-230">Classes used in</span></span>        | [<span data-ttu-id="63edd-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63edd-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63edd-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63edd-233">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-233">Entry</span></span> | <span data-ttu-id="63edd-234">值</span><span class="sxs-lookup"><span data-stu-id="63edd-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-237">System-Only</span></span>            | <span data-ttu-id="63edd-238">否</span><span class="sxs-lookup"><span data-stu-id="63edd-238">False</span></span>                                     |
| <span data-ttu-id="63edd-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-239">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-240">對</span><span class="sxs-lookup"><span data-stu-id="63edd-240">True</span></span>                                      |
| <span data-ttu-id="63edd-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-241">Is Indexed</span></span>             | <span data-ttu-id="63edd-242">對</span><span class="sxs-lookup"><span data-stu-id="63edd-242">True</span></span>                                      |
| <span data-ttu-id="63edd-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-243">In Global Catalog</span></span>      | <span data-ttu-id="63edd-244">對</span><span class="sxs-lookup"><span data-stu-id="63edd-244">True</span></span>                                      |
| <span data-ttu-id="63edd-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-247">Range-Lower</span></span>            | <span data-ttu-id="63edd-248">16</span><span class="sxs-lookup"><span data-stu-id="63edd-248">16</span></span>                                        |
| <span data-ttu-id="63edd-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-249">Range-Upper</span></span>            | <span data-ttu-id="63edd-250">16</span><span class="sxs-lookup"><span data-stu-id="63edd-250">16</span></span>                                        |
| <span data-ttu-id="63edd-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-251">Search-Flags</span></span>           | <span data-ttu-id="63edd-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-252">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-253">System-Flags</span></span>           | <span data-ttu-id="63edd-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-254">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-255">Classes used in</span></span>        | [<span data-ttu-id="63edd-256">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63edd-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63edd-257">Windows Server 2012</span></span>



| <span data-ttu-id="63edd-258">進入</span><span class="sxs-lookup"><span data-stu-id="63edd-258">Entry</span></span> | <span data-ttu-id="63edd-259">值</span><span class="sxs-lookup"><span data-stu-id="63edd-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="63edd-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="63edd-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63edd-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="63edd-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="63edd-262">System-Only</span></span>            | <span data-ttu-id="63edd-263">否</span><span class="sxs-lookup"><span data-stu-id="63edd-263">False</span></span>                                     |
| <span data-ttu-id="63edd-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="63edd-264">Is-Single-Valued</span></span>       | <span data-ttu-id="63edd-265">對</span><span class="sxs-lookup"><span data-stu-id="63edd-265">True</span></span>                                      |
| <span data-ttu-id="63edd-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="63edd-266">Is Indexed</span></span>             | <span data-ttu-id="63edd-267">對</span><span class="sxs-lookup"><span data-stu-id="63edd-267">True</span></span>                                      |
| <span data-ttu-id="63edd-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="63edd-268">In Global Catalog</span></span>      | <span data-ttu-id="63edd-269">對</span><span class="sxs-lookup"><span data-stu-id="63edd-269">True</span></span>                                      |
| <span data-ttu-id="63edd-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="63edd-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="63edd-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="63edd-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="63edd-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63edd-272">Range-Lower</span></span>            | <span data-ttu-id="63edd-273">16</span><span class="sxs-lookup"><span data-stu-id="63edd-273">16</span></span>                                        |
| <span data-ttu-id="63edd-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63edd-274">Range-Upper</span></span>            | <span data-ttu-id="63edd-275">16</span><span class="sxs-lookup"><span data-stu-id="63edd-275">16</span></span>                                        |
| <span data-ttu-id="63edd-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-276">Search-Flags</span></span>           | <span data-ttu-id="63edd-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63edd-277">0x00000001</span></span>                                |
| <span data-ttu-id="63edd-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63edd-278">System-Flags</span></span>           | <span data-ttu-id="63edd-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63edd-279">0x00000010</span></span>                                |
| <span data-ttu-id="63edd-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="63edd-280">Classes used in</span></span>        | [<span data-ttu-id="63edd-281">**電腦**</span><span class="sxs-lookup"><span data-stu-id="63edd-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





