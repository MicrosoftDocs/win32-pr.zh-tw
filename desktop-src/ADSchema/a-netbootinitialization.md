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
# <a name="netboot-initialization-attribute"></a><span data-ttu-id="bed0d-105">Netboot-Initialization 屬性</span><span class="sxs-lookup"><span data-stu-id="bed0d-105">Netboot-Initialization attribute</span></span>

<span data-ttu-id="bed0d-106">無磁片開機的預設開機路徑。</span><span class="sxs-lookup"><span data-stu-id="bed0d-106">Default boot path for diskless boot.</span></span>



| <span data-ttu-id="bed0d-107">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-107">Entry</span></span> | <span data-ttu-id="bed0d-108">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bed0d-109">CN</span><span class="sxs-lookup"><span data-stu-id="bed0d-109">CN</span></span>                | <span data-ttu-id="bed0d-110">Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="bed0d-110">Netboot-Initialization</span></span>                      |
| <span data-ttu-id="bed0d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bed0d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bed0d-112">netbootInitialization</span><span class="sxs-lookup"><span data-stu-id="bed0d-112">netbootInitialization</span></span>                       |
| <span data-ttu-id="bed0d-113">大小</span><span class="sxs-lookup"><span data-stu-id="bed0d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bed0d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="bed0d-114">Update Privilege</span></span>  | <span data-ttu-id="bed0d-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="bed0d-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="bed0d-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="bed0d-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bed0d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-117">Attribute-Id</span></span>      | <span data-ttu-id="bed0d-118">1.2.840.113556.1.4.358</span><span class="sxs-lookup"><span data-stu-id="bed0d-118">1.2.840.113556.1.4.358</span></span>                      |
| <span data-ttu-id="bed0d-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="bed0d-119">System-Id-Guid</span></span>    | <span data-ttu-id="bed0d-120">3e978920-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="bed0d-120">3e978920-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="bed0d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="bed0d-121">Syntax</span></span>            | [<span data-ttu-id="bed0d-122">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bed0d-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bed0d-123">實作</span><span class="sxs-lookup"><span data-stu-id="bed0d-123">Implementations</span></span>

-   [<span data-ttu-id="bed0d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bed0d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bed0d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bed0d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bed0d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bed0d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bed0d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bed0d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bed0d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bed0d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bed0d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bed0d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bed0d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bed0d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="bed0d-131">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-131">Entry</span></span> | <span data-ttu-id="bed0d-132">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-135">System-Only</span></span>            | <span data-ttu-id="bed0d-136">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-136">False</span></span>                                     |
| <span data-ttu-id="bed0d-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-138">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-138">True</span></span>                                      |
| <span data-ttu-id="bed0d-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-139">Is Indexed</span></span>             | <span data-ttu-id="bed0d-140">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-140">False</span></span>                                     |
| <span data-ttu-id="bed0d-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-141">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-142">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-142">False</span></span>                                     |
| <span data-ttu-id="bed0d-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-147">Search-Flags</span></span>           | <span data-ttu-id="bed0d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-148">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-149">System-Flags</span></span>           | <span data-ttu-id="bed0d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-150">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-151">Classes used in</span></span>        | [<span data-ttu-id="bed0d-152">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bed0d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bed0d-153">Windows Server 2003</span></span>



| <span data-ttu-id="bed0d-154">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-154">Entry</span></span> | <span data-ttu-id="bed0d-155">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-158">System-Only</span></span>            | <span data-ttu-id="bed0d-159">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-159">False</span></span>                                     |
| <span data-ttu-id="bed0d-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-161">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-161">True</span></span>                                      |
| <span data-ttu-id="bed0d-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-162">Is Indexed</span></span>             | <span data-ttu-id="bed0d-163">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-163">False</span></span>                                     |
| <span data-ttu-id="bed0d-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-164">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-165">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-165">False</span></span>                                     |
| <span data-ttu-id="bed0d-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-170">Search-Flags</span></span>           | <span data-ttu-id="bed0d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-171">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-172">System-Flags</span></span>           | <span data-ttu-id="bed0d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-173">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-174">Classes used in</span></span>        | [<span data-ttu-id="bed0d-175">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bed0d-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bed0d-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bed0d-177">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-177">Entry</span></span> | <span data-ttu-id="bed0d-178">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-181">System-Only</span></span>            | <span data-ttu-id="bed0d-182">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-182">False</span></span>                                     |
| <span data-ttu-id="bed0d-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-184">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-184">True</span></span>                                      |
| <span data-ttu-id="bed0d-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-185">Is Indexed</span></span>             | <span data-ttu-id="bed0d-186">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-186">False</span></span>                                     |
| <span data-ttu-id="bed0d-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-187">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-188">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-188">False</span></span>                                     |
| <span data-ttu-id="bed0d-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-193">Search-Flags</span></span>           | <span data-ttu-id="bed0d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-194">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-195">System-Flags</span></span>           | <span data-ttu-id="bed0d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-196">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-197">Classes used in</span></span>        | [<span data-ttu-id="bed0d-198">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bed0d-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bed0d-199">Windows Server 2008</span></span>



| <span data-ttu-id="bed0d-200">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-200">Entry</span></span> | <span data-ttu-id="bed0d-201">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-204">System-Only</span></span>            | <span data-ttu-id="bed0d-205">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-205">False</span></span>                                     |
| <span data-ttu-id="bed0d-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-207">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-207">True</span></span>                                      |
| <span data-ttu-id="bed0d-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-208">Is Indexed</span></span>             | <span data-ttu-id="bed0d-209">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-209">False</span></span>                                     |
| <span data-ttu-id="bed0d-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-210">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-211">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-211">False</span></span>                                     |
| <span data-ttu-id="bed0d-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-216">Search-Flags</span></span>           | <span data-ttu-id="bed0d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-217">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-218">System-Flags</span></span>           | <span data-ttu-id="bed0d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-219">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-220">Classes used in</span></span>        | [<span data-ttu-id="bed0d-221">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bed0d-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bed0d-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bed0d-223">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-223">Entry</span></span> | <span data-ttu-id="bed0d-224">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-227">System-Only</span></span>            | <span data-ttu-id="bed0d-228">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-228">False</span></span>                                     |
| <span data-ttu-id="bed0d-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-230">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-230">True</span></span>                                      |
| <span data-ttu-id="bed0d-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-231">Is Indexed</span></span>             | <span data-ttu-id="bed0d-232">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-232">False</span></span>                                     |
| <span data-ttu-id="bed0d-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-233">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-234">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-234">False</span></span>                                     |
| <span data-ttu-id="bed0d-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-239">Search-Flags</span></span>           | <span data-ttu-id="bed0d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-240">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-241">System-Flags</span></span>           | <span data-ttu-id="bed0d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-242">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-243">Classes used in</span></span>        | [<span data-ttu-id="bed0d-244">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bed0d-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bed0d-245">Windows Server 2012</span></span>



| <span data-ttu-id="bed0d-246">進入</span><span class="sxs-lookup"><span data-stu-id="bed0d-246">Entry</span></span> | <span data-ttu-id="bed0d-247">值</span><span class="sxs-lookup"><span data-stu-id="bed0d-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="bed0d-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="bed0d-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bed0d-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="bed0d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="bed0d-250">System-Only</span></span>            | <span data-ttu-id="bed0d-251">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-251">False</span></span>                                     |
| <span data-ttu-id="bed0d-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="bed0d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="bed0d-253">對</span><span class="sxs-lookup"><span data-stu-id="bed0d-253">True</span></span>                                      |
| <span data-ttu-id="bed0d-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="bed0d-254">Is Indexed</span></span>             | <span data-ttu-id="bed0d-255">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-255">False</span></span>                                     |
| <span data-ttu-id="bed0d-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="bed0d-256">In Global Catalog</span></span>      | <span data-ttu-id="bed0d-257">否</span><span class="sxs-lookup"><span data-stu-id="bed0d-257">False</span></span>                                     |
| <span data-ttu-id="bed0d-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="bed0d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="bed0d-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="bed0d-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="bed0d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bed0d-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bed0d-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="bed0d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-262">Search-Flags</span></span>           | <span data-ttu-id="bed0d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bed0d-263">0x00000000</span></span>                                |
| <span data-ttu-id="bed0d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bed0d-264">System-Flags</span></span>           | <span data-ttu-id="bed0d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bed0d-265">0x00000010</span></span>                                |
| <span data-ttu-id="bed0d-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="bed0d-266">Classes used in</span></span>        | [<span data-ttu-id="bed0d-267">**電腦**</span><span class="sxs-lookup"><span data-stu-id="bed0d-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





