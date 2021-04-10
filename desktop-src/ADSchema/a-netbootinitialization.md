---
title: Netboot-Initialization 屬性
description: 無磁片開機的預設開機路徑。
ms.assetid: 359f9fff-1630-4c47-9221-1a2cc6249567
ms.tgt_platform: multiple
keywords:
- Netboot-Initialization 屬性 AD 架構
- netbootInitialization 屬性 AD 架構
topic_type:
- apiref
api_name:
- Netboot-Initialization
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4232d57b38e87386b340810f5edea47f2e409c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686971"
---
# <a name="netboot-initialization-attribute"></a><span data-ttu-id="430fc-105">Netboot-Initialization 屬性</span><span class="sxs-lookup"><span data-stu-id="430fc-105">Netboot-Initialization attribute</span></span>

<span data-ttu-id="430fc-106">無磁片開機的預設開機路徑。</span><span class="sxs-lookup"><span data-stu-id="430fc-106">Default boot path for diskless boot.</span></span>



| <span data-ttu-id="430fc-107">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-107">Entry</span></span> | <span data-ttu-id="430fc-108">值</span><span class="sxs-lookup"><span data-stu-id="430fc-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="430fc-109">CN</span><span class="sxs-lookup"><span data-stu-id="430fc-109">CN</span></span>                | <span data-ttu-id="430fc-110">Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="430fc-110">Netboot-Initialization</span></span>                      |
| <span data-ttu-id="430fc-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="430fc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="430fc-112">netbootInitialization</span><span class="sxs-lookup"><span data-stu-id="430fc-112">netbootInitialization</span></span>                       |
| <span data-ttu-id="430fc-113">大小</span><span class="sxs-lookup"><span data-stu-id="430fc-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="430fc-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="430fc-114">Update Privilege</span></span>  | <span data-ttu-id="430fc-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="430fc-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="430fc-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="430fc-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="430fc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-117">Attribute-Id</span></span>      | <span data-ttu-id="430fc-118">1.2.840.113556.1.4.358</span><span class="sxs-lookup"><span data-stu-id="430fc-118">1.2.840.113556.1.4.358</span></span>                      |
| <span data-ttu-id="430fc-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="430fc-119">System-Id-Guid</span></span>    | <span data-ttu-id="430fc-120">3e978920-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="430fc-120">3e978920-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="430fc-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="430fc-121">Syntax</span></span>            | [<span data-ttu-id="430fc-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="430fc-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="430fc-123">實作</span><span class="sxs-lookup"><span data-stu-id="430fc-123">Implementations</span></span>

-   [<span data-ttu-id="430fc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="430fc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="430fc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="430fc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="430fc-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="430fc-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="430fc-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="430fc-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="430fc-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="430fc-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="430fc-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="430fc-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="430fc-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="430fc-130">Windows 2000 Server</span></span>



| <span data-ttu-id="430fc-131">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-131">Entry</span></span> | <span data-ttu-id="430fc-132">值</span><span class="sxs-lookup"><span data-stu-id="430fc-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-135">System-Only</span></span>            | <span data-ttu-id="430fc-136">否</span><span class="sxs-lookup"><span data-stu-id="430fc-136">False</span></span>                                     |
| <span data-ttu-id="430fc-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-137">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-138">對</span><span class="sxs-lookup"><span data-stu-id="430fc-138">True</span></span>                                      |
| <span data-ttu-id="430fc-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-139">Is Indexed</span></span>             | <span data-ttu-id="430fc-140">否</span><span class="sxs-lookup"><span data-stu-id="430fc-140">False</span></span>                                     |
| <span data-ttu-id="430fc-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-141">In Global Catalog</span></span>      | <span data-ttu-id="430fc-142">否</span><span class="sxs-lookup"><span data-stu-id="430fc-142">False</span></span>                                     |
| <span data-ttu-id="430fc-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-147">Search-Flags</span></span>           | <span data-ttu-id="430fc-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-148">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-149">System-Flags</span></span>           | <span data-ttu-id="430fc-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-150">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-151">Classes used in</span></span>        | [<span data-ttu-id="430fc-152">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="430fc-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="430fc-153">Windows Server 2003</span></span>



| <span data-ttu-id="430fc-154">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-154">Entry</span></span> | <span data-ttu-id="430fc-155">值</span><span class="sxs-lookup"><span data-stu-id="430fc-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-158">System-Only</span></span>            | <span data-ttu-id="430fc-159">否</span><span class="sxs-lookup"><span data-stu-id="430fc-159">False</span></span>                                     |
| <span data-ttu-id="430fc-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-160">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-161">對</span><span class="sxs-lookup"><span data-stu-id="430fc-161">True</span></span>                                      |
| <span data-ttu-id="430fc-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-162">Is Indexed</span></span>             | <span data-ttu-id="430fc-163">否</span><span class="sxs-lookup"><span data-stu-id="430fc-163">False</span></span>                                     |
| <span data-ttu-id="430fc-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-164">In Global Catalog</span></span>      | <span data-ttu-id="430fc-165">否</span><span class="sxs-lookup"><span data-stu-id="430fc-165">False</span></span>                                     |
| <span data-ttu-id="430fc-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-170">Search-Flags</span></span>           | <span data-ttu-id="430fc-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-171">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-172">System-Flags</span></span>           | <span data-ttu-id="430fc-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-173">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-174">Classes used in</span></span>        | [<span data-ttu-id="430fc-175">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="430fc-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="430fc-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="430fc-177">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-177">Entry</span></span> | <span data-ttu-id="430fc-178">值</span><span class="sxs-lookup"><span data-stu-id="430fc-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-181">System-Only</span></span>            | <span data-ttu-id="430fc-182">否</span><span class="sxs-lookup"><span data-stu-id="430fc-182">False</span></span>                                     |
| <span data-ttu-id="430fc-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-183">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-184">對</span><span class="sxs-lookup"><span data-stu-id="430fc-184">True</span></span>                                      |
| <span data-ttu-id="430fc-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-185">Is Indexed</span></span>             | <span data-ttu-id="430fc-186">否</span><span class="sxs-lookup"><span data-stu-id="430fc-186">False</span></span>                                     |
| <span data-ttu-id="430fc-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-187">In Global Catalog</span></span>      | <span data-ttu-id="430fc-188">否</span><span class="sxs-lookup"><span data-stu-id="430fc-188">False</span></span>                                     |
| <span data-ttu-id="430fc-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-193">Search-Flags</span></span>           | <span data-ttu-id="430fc-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-194">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-195">System-Flags</span></span>           | <span data-ttu-id="430fc-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-196">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-197">Classes used in</span></span>        | [<span data-ttu-id="430fc-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="430fc-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="430fc-199">Windows Server 2008</span></span>



| <span data-ttu-id="430fc-200">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-200">Entry</span></span> | <span data-ttu-id="430fc-201">值</span><span class="sxs-lookup"><span data-stu-id="430fc-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-204">System-Only</span></span>            | <span data-ttu-id="430fc-205">否</span><span class="sxs-lookup"><span data-stu-id="430fc-205">False</span></span>                                     |
| <span data-ttu-id="430fc-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-206">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-207">對</span><span class="sxs-lookup"><span data-stu-id="430fc-207">True</span></span>                                      |
| <span data-ttu-id="430fc-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-208">Is Indexed</span></span>             | <span data-ttu-id="430fc-209">否</span><span class="sxs-lookup"><span data-stu-id="430fc-209">False</span></span>                                     |
| <span data-ttu-id="430fc-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-210">In Global Catalog</span></span>      | <span data-ttu-id="430fc-211">否</span><span class="sxs-lookup"><span data-stu-id="430fc-211">False</span></span>                                     |
| <span data-ttu-id="430fc-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-216">Search-Flags</span></span>           | <span data-ttu-id="430fc-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-217">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-218">System-Flags</span></span>           | <span data-ttu-id="430fc-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-219">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-220">Classes used in</span></span>        | [<span data-ttu-id="430fc-221">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="430fc-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="430fc-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="430fc-223">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-223">Entry</span></span> | <span data-ttu-id="430fc-224">值</span><span class="sxs-lookup"><span data-stu-id="430fc-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-227">System-Only</span></span>            | <span data-ttu-id="430fc-228">否</span><span class="sxs-lookup"><span data-stu-id="430fc-228">False</span></span>                                     |
| <span data-ttu-id="430fc-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-229">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-230">對</span><span class="sxs-lookup"><span data-stu-id="430fc-230">True</span></span>                                      |
| <span data-ttu-id="430fc-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-231">Is Indexed</span></span>             | <span data-ttu-id="430fc-232">否</span><span class="sxs-lookup"><span data-stu-id="430fc-232">False</span></span>                                     |
| <span data-ttu-id="430fc-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-233">In Global Catalog</span></span>      | <span data-ttu-id="430fc-234">否</span><span class="sxs-lookup"><span data-stu-id="430fc-234">False</span></span>                                     |
| <span data-ttu-id="430fc-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-239">Search-Flags</span></span>           | <span data-ttu-id="430fc-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-240">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-241">System-Flags</span></span>           | <span data-ttu-id="430fc-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-242">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-243">Classes used in</span></span>        | [<span data-ttu-id="430fc-244">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="430fc-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="430fc-245">Windows Server 2012</span></span>



| <span data-ttu-id="430fc-246">進入</span><span class="sxs-lookup"><span data-stu-id="430fc-246">Entry</span></span> | <span data-ttu-id="430fc-247">值</span><span class="sxs-lookup"><span data-stu-id="430fc-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="430fc-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="430fc-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="430fc-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="430fc-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="430fc-250">System-Only</span></span>            | <span data-ttu-id="430fc-251">否</span><span class="sxs-lookup"><span data-stu-id="430fc-251">False</span></span>                                     |
| <span data-ttu-id="430fc-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="430fc-252">Is-Single-Valued</span></span>       | <span data-ttu-id="430fc-253">對</span><span class="sxs-lookup"><span data-stu-id="430fc-253">True</span></span>                                      |
| <span data-ttu-id="430fc-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="430fc-254">Is Indexed</span></span>             | <span data-ttu-id="430fc-255">否</span><span class="sxs-lookup"><span data-stu-id="430fc-255">False</span></span>                                     |
| <span data-ttu-id="430fc-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="430fc-256">In Global Catalog</span></span>      | <span data-ttu-id="430fc-257">否</span><span class="sxs-lookup"><span data-stu-id="430fc-257">False</span></span>                                     |
| <span data-ttu-id="430fc-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="430fc-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="430fc-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="430fc-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="430fc-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="430fc-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="430fc-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="430fc-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="430fc-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-262">Search-Flags</span></span>           | <span data-ttu-id="430fc-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="430fc-263">0x00000000</span></span>                                |
| <span data-ttu-id="430fc-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="430fc-264">System-Flags</span></span>           | <span data-ttu-id="430fc-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="430fc-265">0x00000010</span></span>                                |
| <span data-ttu-id="430fc-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="430fc-266">Classes used in</span></span>        | [<span data-ttu-id="430fc-267">**電腦**</span><span class="sxs-lookup"><span data-stu-id="430fc-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





