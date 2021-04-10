---
title: Setup-Command 屬性
description: 這個屬性會指出設定此應用程式是否需要安裝命令。
ms.assetid: f6292605-b392-4de2-b0a0-cae3f0551184
ms.tgt_platform: multiple
keywords:
- Setup-Command 屬性 AD 架構
- setupCommand 屬性 AD 架構
topic_type:
- apiref
api_name:
- Setup-Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acea4a714c4175b77812e05880e8d9e78ca6645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107949"
---
# <a name="setup-command-attribute"></a><span data-ttu-id="f64cb-105">Setup-Command 屬性</span><span class="sxs-lookup"><span data-stu-id="f64cb-105">Setup-Command attribute</span></span>

<span data-ttu-id="f64cb-106">這個屬性會指出設定此應用程式是否需要安裝命令。</span><span class="sxs-lookup"><span data-stu-id="f64cb-106">This attribute indicates whether a setup command is required to set up this application.</span></span>



| <span data-ttu-id="f64cb-107">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-107">Entry</span></span> | <span data-ttu-id="f64cb-108">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f64cb-109">CN</span><span class="sxs-lookup"><span data-stu-id="f64cb-109">CN</span></span>                | <span data-ttu-id="f64cb-110">Setup-Command</span><span class="sxs-lookup"><span data-stu-id="f64cb-110">Setup-Command</span></span>                               |
| <span data-ttu-id="f64cb-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f64cb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f64cb-112">setupCommand</span><span class="sxs-lookup"><span data-stu-id="f64cb-112">setupCommand</span></span>                                |
| <span data-ttu-id="f64cb-113">大小</span><span class="sxs-lookup"><span data-stu-id="f64cb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f64cb-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f64cb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f64cb-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f64cb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f64cb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-116">Attribute-Id</span></span>      | <span data-ttu-id="f64cb-117">1.2.840.113556.1.4.325</span><span class="sxs-lookup"><span data-stu-id="f64cb-117">1.2.840.113556.1.4.325</span></span>                      |
| <span data-ttu-id="f64cb-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f64cb-118">System-Id-Guid</span></span>    | <span data-ttu-id="f64cb-119">7d6c0e97-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="f64cb-119">7d6c0e97-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="f64cb-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="f64cb-120">Syntax</span></span>            | [<span data-ttu-id="f64cb-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f64cb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f64cb-122">實作</span><span class="sxs-lookup"><span data-stu-id="f64cb-122">Implementations</span></span>

-   [<span data-ttu-id="f64cb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f64cb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f64cb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f64cb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f64cb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f64cb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f64cb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f64cb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f64cb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f64cb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f64cb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f64cb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f64cb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f64cb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f64cb-130">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-130">Entry</span></span> | <span data-ttu-id="f64cb-131">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-134">System-Only</span></span>            | <span data-ttu-id="f64cb-135">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-135">False</span></span>                                                            |
| <span data-ttu-id="f64cb-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-137">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-137">True</span></span>                                                             |
| <span data-ttu-id="f64cb-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-138">Is Indexed</span></span>             | <span data-ttu-id="f64cb-139">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-139">False</span></span>                                                            |
| <span data-ttu-id="f64cb-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-140">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-141">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-141">False</span></span>                                                            |
| <span data-ttu-id="f64cb-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-146">Search-Flags</span></span>           | <span data-ttu-id="f64cb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-148">System-Flags</span></span>           | <span data-ttu-id="f64cb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-150">Classes used in</span></span>        | [<span data-ttu-id="f64cb-151">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f64cb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f64cb-152">Windows Server 2003</span></span>



| <span data-ttu-id="f64cb-153">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-153">Entry</span></span> | <span data-ttu-id="f64cb-154">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-157">System-Only</span></span>            | <span data-ttu-id="f64cb-158">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-158">False</span></span>                                                            |
| <span data-ttu-id="f64cb-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-160">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-160">True</span></span>                                                             |
| <span data-ttu-id="f64cb-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-161">Is Indexed</span></span>             | <span data-ttu-id="f64cb-162">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-162">False</span></span>                                                            |
| <span data-ttu-id="f64cb-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-163">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-164">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-164">False</span></span>                                                            |
| <span data-ttu-id="f64cb-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-169">Search-Flags</span></span>           | <span data-ttu-id="f64cb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-171">System-Flags</span></span>           | <span data-ttu-id="f64cb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-173">Classes used in</span></span>        | [<span data-ttu-id="f64cb-174">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f64cb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f64cb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f64cb-176">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-176">Entry</span></span> | <span data-ttu-id="f64cb-177">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-180">System-Only</span></span>            | <span data-ttu-id="f64cb-181">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-181">False</span></span>                                                            |
| <span data-ttu-id="f64cb-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-183">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-183">True</span></span>                                                             |
| <span data-ttu-id="f64cb-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-184">Is Indexed</span></span>             | <span data-ttu-id="f64cb-185">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-185">False</span></span>                                                            |
| <span data-ttu-id="f64cb-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-186">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-187">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-187">False</span></span>                                                            |
| <span data-ttu-id="f64cb-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-192">Search-Flags</span></span>           | <span data-ttu-id="f64cb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-194">System-Flags</span></span>           | <span data-ttu-id="f64cb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-196">Classes used in</span></span>        | [<span data-ttu-id="f64cb-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f64cb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f64cb-198">Windows Server 2008</span></span>



| <span data-ttu-id="f64cb-199">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-199">Entry</span></span> | <span data-ttu-id="f64cb-200">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-203">System-Only</span></span>            | <span data-ttu-id="f64cb-204">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-204">False</span></span>                                                            |
| <span data-ttu-id="f64cb-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-206">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-206">True</span></span>                                                             |
| <span data-ttu-id="f64cb-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-207">Is Indexed</span></span>             | <span data-ttu-id="f64cb-208">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-208">False</span></span>                                                            |
| <span data-ttu-id="f64cb-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-209">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-210">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-210">False</span></span>                                                            |
| <span data-ttu-id="f64cb-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-215">Search-Flags</span></span>           | <span data-ttu-id="f64cb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-217">System-Flags</span></span>           | <span data-ttu-id="f64cb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-219">Classes used in</span></span>        | [<span data-ttu-id="f64cb-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f64cb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f64cb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f64cb-222">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-222">Entry</span></span> | <span data-ttu-id="f64cb-223">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-226">System-Only</span></span>            | <span data-ttu-id="f64cb-227">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-227">False</span></span>                                                            |
| <span data-ttu-id="f64cb-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-229">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-229">True</span></span>                                                             |
| <span data-ttu-id="f64cb-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-230">Is Indexed</span></span>             | <span data-ttu-id="f64cb-231">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-231">False</span></span>                                                            |
| <span data-ttu-id="f64cb-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-232">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-233">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-233">False</span></span>                                                            |
| <span data-ttu-id="f64cb-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-238">Search-Flags</span></span>           | <span data-ttu-id="f64cb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-240">System-Flags</span></span>           | <span data-ttu-id="f64cb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-242">Classes used in</span></span>        | [<span data-ttu-id="f64cb-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f64cb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f64cb-244">Windows Server 2012</span></span>



| <span data-ttu-id="f64cb-245">進入</span><span class="sxs-lookup"><span data-stu-id="f64cb-245">Entry</span></span> | <span data-ttu-id="f64cb-246">值</span><span class="sxs-lookup"><span data-stu-id="f64cb-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f64cb-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f64cb-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f64cb-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f64cb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f64cb-249">System-Only</span></span>            | <span data-ttu-id="f64cb-250">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-250">False</span></span>                                                            |
| <span data-ttu-id="f64cb-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f64cb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f64cb-252">對</span><span class="sxs-lookup"><span data-stu-id="f64cb-252">True</span></span>                                                             |
| <span data-ttu-id="f64cb-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f64cb-253">Is Indexed</span></span>             | <span data-ttu-id="f64cb-254">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-254">False</span></span>                                                            |
| <span data-ttu-id="f64cb-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f64cb-255">In Global Catalog</span></span>      | <span data-ttu-id="f64cb-256">否</span><span class="sxs-lookup"><span data-stu-id="f64cb-256">False</span></span>                                                            |
| <span data-ttu-id="f64cb-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f64cb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f64cb-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f64cb-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f64cb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f64cb-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f64cb-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f64cb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-261">Search-Flags</span></span>           | <span data-ttu-id="f64cb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f64cb-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="f64cb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f64cb-263">System-Flags</span></span>           | <span data-ttu-id="f64cb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f64cb-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="f64cb-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f64cb-265">Classes used in</span></span>        | [<span data-ttu-id="f64cb-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="f64cb-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





