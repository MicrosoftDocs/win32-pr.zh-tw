---
title: 內容-索引-允許的屬性
description: 指出磁片區物件是否可以為內容編制索引。
ms.assetid: 65e3cc3a-be16-4dd1-8ff1-1a8ad0943291
ms.tgt_platform: multiple
keywords:
- 內容-索引-允許的屬性 AD 架構
- contentIndexingAllowed 屬性 AD 架構
topic_type:
- apiref
api_name:
- Content-Indexing-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608e7bd8e26675be85f3daaee288b2585a4f2c9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108280"
---
# <a name="content-indexing-allowed-attribute"></a><span data-ttu-id="31bfb-105">內容-索引-允許的屬性</span><span class="sxs-lookup"><span data-stu-id="31bfb-105">Content-Indexing-Allowed attribute</span></span>

<span data-ttu-id="31bfb-106">指出磁片區物件是否可以為內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="31bfb-106">Indicates whether the Volume object can be content indexed.</span></span>



| <span data-ttu-id="31bfb-107">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-107">Entry</span></span> | <span data-ttu-id="31bfb-108">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="31bfb-109">CN</span><span class="sxs-lookup"><span data-stu-id="31bfb-109">CN</span></span>                | <span data-ttu-id="31bfb-110">內容-索引-允許</span><span class="sxs-lookup"><span data-stu-id="31bfb-110">Content-Indexing-Allowed</span></span>             |
| <span data-ttu-id="31bfb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="31bfb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="31bfb-112">contentIndexingAllowed</span><span class="sxs-lookup"><span data-stu-id="31bfb-112">contentIndexingAllowed</span></span>               |
| <span data-ttu-id="31bfb-113">大小</span><span class="sxs-lookup"><span data-stu-id="31bfb-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="31bfb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="31bfb-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="31bfb-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="31bfb-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="31bfb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-116">Attribute-Id</span></span>      | <span data-ttu-id="31bfb-117">1.2.840.113556.1.4.24</span><span class="sxs-lookup"><span data-stu-id="31bfb-117">1.2.840.113556.1.4.24</span></span>                |
| <span data-ttu-id="31bfb-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="31bfb-118">System-Id-Guid</span></span>    | <span data-ttu-id="31bfb-119">bf967943-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="31bfb-119">bf967943-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="31bfb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="31bfb-120">Syntax</span></span>            | [<span data-ttu-id="31bfb-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="31bfb-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="31bfb-122">實作</span><span class="sxs-lookup"><span data-stu-id="31bfb-122">Implementations</span></span>

-   [<span data-ttu-id="31bfb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="31bfb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="31bfb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="31bfb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="31bfb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="31bfb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="31bfb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="31bfb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="31bfb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="31bfb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="31bfb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="31bfb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="31bfb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31bfb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="31bfb-130">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-130">Entry</span></span> | <span data-ttu-id="31bfb-131">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-131">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-132">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-133">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-134">System-Only</span></span>            | <span data-ttu-id="31bfb-135">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-135">False</span></span>                                 |
| <span data-ttu-id="31bfb-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-137">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-137">True</span></span>                                  |
| <span data-ttu-id="31bfb-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-138">Is Indexed</span></span>             | <span data-ttu-id="31bfb-139">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-139">False</span></span>                                 |
| <span data-ttu-id="31bfb-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-140">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-141">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-141">False</span></span>                                 |
| <span data-ttu-id="31bfb-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-143">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-144">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-145">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-146">Search-Flags</span></span>           | <span data-ttu-id="31bfb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-147">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-148">System-Flags</span></span>           | <span data-ttu-id="31bfb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-149">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-150">Classes used in</span></span>        | [<span data-ttu-id="31bfb-151">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-151">**Volume**</span></span>](c-volume.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="31bfb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31bfb-152">Windows Server 2003</span></span>



| <span data-ttu-id="31bfb-153">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-153">Entry</span></span> | <span data-ttu-id="31bfb-154">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-154">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-155">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-156">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-157">System-Only</span></span>            | <span data-ttu-id="31bfb-158">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-158">False</span></span>                                 |
| <span data-ttu-id="31bfb-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-160">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-160">True</span></span>                                  |
| <span data-ttu-id="31bfb-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-161">Is Indexed</span></span>             | <span data-ttu-id="31bfb-162">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-162">False</span></span>                                 |
| <span data-ttu-id="31bfb-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-163">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-164">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-164">False</span></span>                                 |
| <span data-ttu-id="31bfb-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-166">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-167">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-168">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-169">Search-Flags</span></span>           | <span data-ttu-id="31bfb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-170">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-171">System-Flags</span></span>           | <span data-ttu-id="31bfb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-172">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-173">Classes used in</span></span>        | [<span data-ttu-id="31bfb-174">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-174">**Volume**</span></span>](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="31bfb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="31bfb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="31bfb-176">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-176">Entry</span></span> | <span data-ttu-id="31bfb-177">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-177">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-178">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-179">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-180">System-Only</span></span>            | <span data-ttu-id="31bfb-181">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-181">False</span></span>                                 |
| <span data-ttu-id="31bfb-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-183">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-183">True</span></span>                                  |
| <span data-ttu-id="31bfb-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-184">Is Indexed</span></span>             | <span data-ttu-id="31bfb-185">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-185">False</span></span>                                 |
| <span data-ttu-id="31bfb-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-186">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-187">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-187">False</span></span>                                 |
| <span data-ttu-id="31bfb-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-189">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-190">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-191">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-192">Search-Flags</span></span>           | <span data-ttu-id="31bfb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-193">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-194">System-Flags</span></span>           | <span data-ttu-id="31bfb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-195">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-196">Classes used in</span></span>        | [<span data-ttu-id="31bfb-197">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-197">**Volume**</span></span>](c-volume.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="31bfb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31bfb-198">Windows Server 2008</span></span>



| <span data-ttu-id="31bfb-199">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-199">Entry</span></span> | <span data-ttu-id="31bfb-200">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-200">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-201">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-202">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-203">System-Only</span></span>            | <span data-ttu-id="31bfb-204">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-204">False</span></span>                                 |
| <span data-ttu-id="31bfb-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-206">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-206">True</span></span>                                  |
| <span data-ttu-id="31bfb-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-207">Is Indexed</span></span>             | <span data-ttu-id="31bfb-208">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-208">False</span></span>                                 |
| <span data-ttu-id="31bfb-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-209">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-210">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-210">False</span></span>                                 |
| <span data-ttu-id="31bfb-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-212">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-213">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-214">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-215">Search-Flags</span></span>           | <span data-ttu-id="31bfb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-216">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-217">System-Flags</span></span>           | <span data-ttu-id="31bfb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-218">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-219">Classes used in</span></span>        | [<span data-ttu-id="31bfb-220">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-220">**Volume**</span></span>](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="31bfb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31bfb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="31bfb-222">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-222">Entry</span></span> | <span data-ttu-id="31bfb-223">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-223">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-224">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-225">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-226">System-Only</span></span>            | <span data-ttu-id="31bfb-227">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-227">False</span></span>                                 |
| <span data-ttu-id="31bfb-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-229">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-229">True</span></span>                                  |
| <span data-ttu-id="31bfb-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-230">Is Indexed</span></span>             | <span data-ttu-id="31bfb-231">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-231">False</span></span>                                 |
| <span data-ttu-id="31bfb-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-232">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-233">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-233">False</span></span>                                 |
| <span data-ttu-id="31bfb-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-235">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-236">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-237">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-238">Search-Flags</span></span>           | <span data-ttu-id="31bfb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-239">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-240">System-Flags</span></span>           | <span data-ttu-id="31bfb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-241">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-242">Classes used in</span></span>        | [<span data-ttu-id="31bfb-243">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-243">**Volume**</span></span>](c-volume.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="31bfb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="31bfb-244">Windows Server 2012</span></span>



| <span data-ttu-id="31bfb-245">進入</span><span class="sxs-lookup"><span data-stu-id="31bfb-245">Entry</span></span> | <span data-ttu-id="31bfb-246">值</span><span class="sxs-lookup"><span data-stu-id="31bfb-246">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="31bfb-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="31bfb-247">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="31bfb-248">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="31bfb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="31bfb-249">System-Only</span></span>            | <span data-ttu-id="31bfb-250">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-250">False</span></span>                                 |
| <span data-ttu-id="31bfb-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="31bfb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="31bfb-252">對</span><span class="sxs-lookup"><span data-stu-id="31bfb-252">True</span></span>                                  |
| <span data-ttu-id="31bfb-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="31bfb-253">Is Indexed</span></span>             | <span data-ttu-id="31bfb-254">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-254">False</span></span>                                 |
| <span data-ttu-id="31bfb-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="31bfb-255">In Global Catalog</span></span>      | <span data-ttu-id="31bfb-256">否</span><span class="sxs-lookup"><span data-stu-id="31bfb-256">False</span></span>                                 |
| <span data-ttu-id="31bfb-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="31bfb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="31bfb-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="31bfb-258">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="31bfb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="31bfb-259">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="31bfb-260">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="31bfb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-261">Search-Flags</span></span>           | <span data-ttu-id="31bfb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="31bfb-262">0x00000000</span></span>                            |
| <span data-ttu-id="31bfb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="31bfb-263">System-Flags</span></span>           | <span data-ttu-id="31bfb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="31bfb-264">0x00000010</span></span>                            |
| <span data-ttu-id="31bfb-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="31bfb-265">Classes used in</span></span>        | [<span data-ttu-id="31bfb-266">**磁碟區**</span><span class="sxs-lookup"><span data-stu-id="31bfb-266">**Volume**</span></span>](c-volume.md)<br/> |



 

 





