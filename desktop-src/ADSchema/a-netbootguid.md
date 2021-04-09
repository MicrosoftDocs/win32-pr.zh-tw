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
# <a name="netboot-guid-attribute"></a><span data-ttu-id="dc2b1-106">Netboot-GUID 屬性</span><span class="sxs-lookup"><span data-stu-id="dc2b1-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="dc2b1-107">無磁片開機：電腦的機載 GUID。</span><span class="sxs-lookup"><span data-stu-id="dc2b1-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="dc2b1-108">對應于電腦的網路介面卡 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="dc2b1-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="dc2b1-109">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-109">Entry</span></span> | <span data-ttu-id="dc2b1-110">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="dc2b1-111">CN</span><span class="sxs-lookup"><span data-stu-id="dc2b1-111">CN</span></span>                | <span data-ttu-id="dc2b1-112">Netboot-GUID</span><span class="sxs-lookup"><span data-stu-id="dc2b1-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="dc2b1-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="dc2b1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dc2b1-114">netbootGUID</span><span class="sxs-lookup"><span data-stu-id="dc2b1-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="dc2b1-115">大小</span><span class="sxs-lookup"><span data-stu-id="dc2b1-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="dc2b1-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="dc2b1-116">Update Privilege</span></span>  | <span data-ttu-id="dc2b1-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="dc2b1-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="dc2b1-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="dc2b1-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="dc2b1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-119">Attribute-Id</span></span>      | <span data-ttu-id="dc2b1-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="dc2b1-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="dc2b1-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="dc2b1-121">System-Id-Guid</span></span>    | <span data-ttu-id="dc2b1-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="dc2b1-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="dc2b1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc2b1-123">Syntax</span></span>            | [<span data-ttu-id="dc2b1-124">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="dc2b1-125">實作</span><span class="sxs-lookup"><span data-stu-id="dc2b1-125">Implementations</span></span>

-   [<span data-ttu-id="dc2b1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dc2b1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dc2b1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dc2b1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dc2b1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dc2b1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dc2b1-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc2b1-132">Windows 2000 Server</span></span>



| <span data-ttu-id="dc2b1-133">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-133">Entry</span></span> | <span data-ttu-id="dc2b1-134">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-137">System-Only</span></span>            | <span data-ttu-id="dc2b1-138">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-138">False</span></span>                                     |
| <span data-ttu-id="dc2b1-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-140">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-140">True</span></span>                                      |
| <span data-ttu-id="dc2b1-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-141">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-142">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-142">True</span></span>                                      |
| <span data-ttu-id="dc2b1-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-143">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-144">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-144">True</span></span>                                      |
| <span data-ttu-id="dc2b1-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-147">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-148">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-148">16</span></span>                                        |
| <span data-ttu-id="dc2b1-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-149">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-150">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-150">16</span></span>                                        |
| <span data-ttu-id="dc2b1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-151">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-152">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-153">System-Flags</span></span>           | <span data-ttu-id="dc2b1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-154">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-155">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-156">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dc2b1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc2b1-157">Windows Server 2003</span></span>



| <span data-ttu-id="dc2b1-158">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-158">Entry</span></span> | <span data-ttu-id="dc2b1-159">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-162">System-Only</span></span>            | <span data-ttu-id="dc2b1-163">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-163">False</span></span>                                     |
| <span data-ttu-id="dc2b1-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-164">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-165">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-165">True</span></span>                                      |
| <span data-ttu-id="dc2b1-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-166">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-167">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-167">True</span></span>                                      |
| <span data-ttu-id="dc2b1-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-168">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-169">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-169">True</span></span>                                      |
| <span data-ttu-id="dc2b1-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-172">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-173">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-173">16</span></span>                                        |
| <span data-ttu-id="dc2b1-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-174">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-175">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-175">16</span></span>                                        |
| <span data-ttu-id="dc2b1-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-176">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-177">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-178">System-Flags</span></span>           | <span data-ttu-id="dc2b1-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-179">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-180">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-180">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-181">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dc2b1-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dc2b1-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dc2b1-183">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-183">Entry</span></span> | <span data-ttu-id="dc2b1-184">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-185">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-187">System-Only</span></span>            | <span data-ttu-id="dc2b1-188">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-188">False</span></span>                                     |
| <span data-ttu-id="dc2b1-189">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-190">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-190">True</span></span>                                      |
| <span data-ttu-id="dc2b1-191">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-191">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-192">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-192">True</span></span>                                      |
| <span data-ttu-id="dc2b1-193">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-193">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-194">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-194">True</span></span>                                      |
| <span data-ttu-id="dc2b1-195">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-196">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-197">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-198">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-198">16</span></span>                                        |
| <span data-ttu-id="dc2b1-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-199">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-200">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-200">16</span></span>                                        |
| <span data-ttu-id="dc2b1-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-201">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-202">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-203">System-Flags</span></span>           | <span data-ttu-id="dc2b1-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-204">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-205">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-205">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-206">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dc2b1-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc2b1-207">Windows Server 2008</span></span>



| <span data-ttu-id="dc2b1-208">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-208">Entry</span></span> | <span data-ttu-id="dc2b1-209">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-210">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-212">System-Only</span></span>            | <span data-ttu-id="dc2b1-213">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-213">False</span></span>                                     |
| <span data-ttu-id="dc2b1-214">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-214">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-215">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-215">True</span></span>                                      |
| <span data-ttu-id="dc2b1-216">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-216">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-217">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-217">True</span></span>                                      |
| <span data-ttu-id="dc2b1-218">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-218">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-219">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-219">True</span></span>                                      |
| <span data-ttu-id="dc2b1-220">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-221">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-222">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-223">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-223">16</span></span>                                        |
| <span data-ttu-id="dc2b1-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-224">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-225">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-225">16</span></span>                                        |
| <span data-ttu-id="dc2b1-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-226">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-227">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-228">System-Flags</span></span>           | <span data-ttu-id="dc2b1-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-229">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-230">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-230">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-231">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dc2b1-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc2b1-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dc2b1-233">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-233">Entry</span></span> | <span data-ttu-id="dc2b1-234">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-235">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-237">System-Only</span></span>            | <span data-ttu-id="dc2b1-238">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-238">False</span></span>                                     |
| <span data-ttu-id="dc2b1-239">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-239">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-240">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-240">True</span></span>                                      |
| <span data-ttu-id="dc2b1-241">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-241">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-242">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-242">True</span></span>                                      |
| <span data-ttu-id="dc2b1-243">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-243">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-244">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-244">True</span></span>                                      |
| <span data-ttu-id="dc2b1-245">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-246">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-247">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-248">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-248">16</span></span>                                        |
| <span data-ttu-id="dc2b1-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-249">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-250">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-250">16</span></span>                                        |
| <span data-ttu-id="dc2b1-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-251">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-252">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-253">System-Flags</span></span>           | <span data-ttu-id="dc2b1-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-254">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-255">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-256">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dc2b1-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc2b1-257">Windows Server 2012</span></span>



| <span data-ttu-id="dc2b1-258">進入</span><span class="sxs-lookup"><span data-stu-id="dc2b1-258">Entry</span></span> | <span data-ttu-id="dc2b1-259">值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="dc2b1-260">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="dc2b1-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dc2b1-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="dc2b1-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="dc2b1-262">System-Only</span></span>            | <span data-ttu-id="dc2b1-263">否</span><span class="sxs-lookup"><span data-stu-id="dc2b1-263">False</span></span>                                     |
| <span data-ttu-id="dc2b1-264">是-單一值</span><span class="sxs-lookup"><span data-stu-id="dc2b1-264">Is-Single-Valued</span></span>       | <span data-ttu-id="dc2b1-265">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-265">True</span></span>                                      |
| <span data-ttu-id="dc2b1-266">已編制索引</span><span class="sxs-lookup"><span data-stu-id="dc2b1-266">Is Indexed</span></span>             | <span data-ttu-id="dc2b1-267">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-267">True</span></span>                                      |
| <span data-ttu-id="dc2b1-268">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="dc2b1-268">In Global Catalog</span></span>      | <span data-ttu-id="dc2b1-269">對</span><span class="sxs-lookup"><span data-stu-id="dc2b1-269">True</span></span>                                      |
| <span data-ttu-id="dc2b1-270">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="dc2b1-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="dc2b1-271">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="dc2b1-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="dc2b1-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dc2b1-272">Range-Lower</span></span>            | <span data-ttu-id="dc2b1-273">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-273">16</span></span>                                        |
| <span data-ttu-id="dc2b1-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dc2b1-274">Range-Upper</span></span>            | <span data-ttu-id="dc2b1-275">16</span><span class="sxs-lookup"><span data-stu-id="dc2b1-275">16</span></span>                                        |
| <span data-ttu-id="dc2b1-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-276">Search-Flags</span></span>           | <span data-ttu-id="dc2b1-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc2b1-277">0x00000001</span></span>                                |
| <span data-ttu-id="dc2b1-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dc2b1-278">System-Flags</span></span>           | <span data-ttu-id="dc2b1-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dc2b1-279">0x00000010</span></span>                                |
| <span data-ttu-id="dc2b1-280">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="dc2b1-280">Classes used in</span></span>        | [<span data-ttu-id="dc2b1-281">**電腦**</span><span class="sxs-lookup"><span data-stu-id="dc2b1-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





