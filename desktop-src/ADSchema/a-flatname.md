---
title: Flat-Name 屬性
description: 針對 Windows NT 網域，一般名稱是 NetBIOS 名稱。 適用于非8211的連結;Windows NT 網域中，一般名稱是該網域的識別名稱，或為 Null。
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Flat-Name 屬性 AD 架構
- flatName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467208"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="15b89-106">Flat-Name 屬性</span><span class="sxs-lookup"><span data-stu-id="15b89-106">Flat-Name attribute</span></span>

<span data-ttu-id="15b89-107">針對 Windows NT 網域，一般名稱是 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="15b89-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="15b89-108">若為非 Windows NT 網域的連結，則一般名稱是該網域的識別名稱，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15b89-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="15b89-109">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-109">Entry</span></span> | <span data-ttu-id="15b89-110">值</span><span class="sxs-lookup"><span data-stu-id="15b89-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="15b89-111">CN</span><span class="sxs-lookup"><span data-stu-id="15b89-111">CN</span></span>                | <span data-ttu-id="15b89-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="15b89-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="15b89-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="15b89-113">Ldap-Display-Name</span></span> | <span data-ttu-id="15b89-114">flatName</span><span class="sxs-lookup"><span data-stu-id="15b89-114">flatName</span></span>                                    |
| <span data-ttu-id="15b89-115">大小</span><span class="sxs-lookup"><span data-stu-id="15b89-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="15b89-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="15b89-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="15b89-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="15b89-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="15b89-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-118">Attribute-Id</span></span>      | <span data-ttu-id="15b89-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="15b89-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="15b89-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="15b89-120">System-Id-Guid</span></span>    | <span data-ttu-id="15b89-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="15b89-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="15b89-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b89-122">Syntax</span></span>            | [<span data-ttu-id="15b89-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="15b89-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="15b89-124">實作</span><span class="sxs-lookup"><span data-stu-id="15b89-124">Implementations</span></span>

-   [<span data-ttu-id="15b89-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="15b89-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="15b89-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="15b89-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="15b89-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="15b89-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="15b89-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="15b89-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="15b89-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="15b89-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="15b89-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="15b89-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="15b89-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15b89-131">Windows 2000 Server</span></span>



| <span data-ttu-id="15b89-132">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-132">Entry</span></span> | <span data-ttu-id="15b89-133">值</span><span class="sxs-lookup"><span data-stu-id="15b89-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-134">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-136">System-Only</span></span>            | <span data-ttu-id="15b89-137">否</span><span class="sxs-lookup"><span data-stu-id="15b89-137">False</span></span>                                                |
| <span data-ttu-id="15b89-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-138">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-139">對</span><span class="sxs-lookup"><span data-stu-id="15b89-139">True</span></span>                                                 |
| <span data-ttu-id="15b89-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-140">Is Indexed</span></span>             | <span data-ttu-id="15b89-141">對</span><span class="sxs-lookup"><span data-stu-id="15b89-141">True</span></span>                                                 |
| <span data-ttu-id="15b89-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-142">In Global Catalog</span></span>      | <span data-ttu-id="15b89-143">否</span><span class="sxs-lookup"><span data-stu-id="15b89-143">False</span></span>                                                |
| <span data-ttu-id="15b89-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-148">Search-Flags</span></span>           | <span data-ttu-id="15b89-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-149">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-150">System-Flags</span></span>           | <span data-ttu-id="15b89-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-151">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-152">Classes used in</span></span>        | [<span data-ttu-id="15b89-153">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="15b89-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15b89-154">Windows Server 2003</span></span>



| <span data-ttu-id="15b89-155">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-155">Entry</span></span> | <span data-ttu-id="15b89-156">值</span><span class="sxs-lookup"><span data-stu-id="15b89-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-159">System-Only</span></span>            | <span data-ttu-id="15b89-160">否</span><span class="sxs-lookup"><span data-stu-id="15b89-160">False</span></span>                                                |
| <span data-ttu-id="15b89-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-161">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-162">對</span><span class="sxs-lookup"><span data-stu-id="15b89-162">True</span></span>                                                 |
| <span data-ttu-id="15b89-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-163">Is Indexed</span></span>             | <span data-ttu-id="15b89-164">對</span><span class="sxs-lookup"><span data-stu-id="15b89-164">True</span></span>                                                 |
| <span data-ttu-id="15b89-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-165">In Global Catalog</span></span>      | <span data-ttu-id="15b89-166">否</span><span class="sxs-lookup"><span data-stu-id="15b89-166">False</span></span>                                                |
| <span data-ttu-id="15b89-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-171">Search-Flags</span></span>           | <span data-ttu-id="15b89-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-172">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-173">System-Flags</span></span>           | <span data-ttu-id="15b89-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-174">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-175">Classes used in</span></span>        | [<span data-ttu-id="15b89-176">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="15b89-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15b89-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="15b89-178">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-178">Entry</span></span> | <span data-ttu-id="15b89-179">值</span><span class="sxs-lookup"><span data-stu-id="15b89-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-182">System-Only</span></span>            | <span data-ttu-id="15b89-183">否</span><span class="sxs-lookup"><span data-stu-id="15b89-183">False</span></span>                                                |
| <span data-ttu-id="15b89-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-184">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-185">對</span><span class="sxs-lookup"><span data-stu-id="15b89-185">True</span></span>                                                 |
| <span data-ttu-id="15b89-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-186">Is Indexed</span></span>             | <span data-ttu-id="15b89-187">對</span><span class="sxs-lookup"><span data-stu-id="15b89-187">True</span></span>                                                 |
| <span data-ttu-id="15b89-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-188">In Global Catalog</span></span>      | <span data-ttu-id="15b89-189">否</span><span class="sxs-lookup"><span data-stu-id="15b89-189">False</span></span>                                                |
| <span data-ttu-id="15b89-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-194">Search-Flags</span></span>           | <span data-ttu-id="15b89-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-195">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-196">System-Flags</span></span>           | <span data-ttu-id="15b89-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-197">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-198">Classes used in</span></span>        | [<span data-ttu-id="15b89-199">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="15b89-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15b89-200">Windows Server 2008</span></span>



| <span data-ttu-id="15b89-201">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-201">Entry</span></span> | <span data-ttu-id="15b89-202">值</span><span class="sxs-lookup"><span data-stu-id="15b89-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-203">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-205">System-Only</span></span>            | <span data-ttu-id="15b89-206">否</span><span class="sxs-lookup"><span data-stu-id="15b89-206">False</span></span>                                                |
| <span data-ttu-id="15b89-207">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-207">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-208">對</span><span class="sxs-lookup"><span data-stu-id="15b89-208">True</span></span>                                                 |
| <span data-ttu-id="15b89-209">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-209">Is Indexed</span></span>             | <span data-ttu-id="15b89-210">對</span><span class="sxs-lookup"><span data-stu-id="15b89-210">True</span></span>                                                 |
| <span data-ttu-id="15b89-211">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-211">In Global Catalog</span></span>      | <span data-ttu-id="15b89-212">否</span><span class="sxs-lookup"><span data-stu-id="15b89-212">False</span></span>                                                |
| <span data-ttu-id="15b89-213">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-214">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-217">Search-Flags</span></span>           | <span data-ttu-id="15b89-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-218">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-219">System-Flags</span></span>           | <span data-ttu-id="15b89-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-220">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-221">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-221">Classes used in</span></span>        | [<span data-ttu-id="15b89-222">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="15b89-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15b89-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="15b89-224">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-224">Entry</span></span> | <span data-ttu-id="15b89-225">值</span><span class="sxs-lookup"><span data-stu-id="15b89-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-226">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-228">System-Only</span></span>            | <span data-ttu-id="15b89-229">否</span><span class="sxs-lookup"><span data-stu-id="15b89-229">False</span></span>                                                |
| <span data-ttu-id="15b89-230">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-230">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-231">對</span><span class="sxs-lookup"><span data-stu-id="15b89-231">True</span></span>                                                 |
| <span data-ttu-id="15b89-232">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-232">Is Indexed</span></span>             | <span data-ttu-id="15b89-233">對</span><span class="sxs-lookup"><span data-stu-id="15b89-233">True</span></span>                                                 |
| <span data-ttu-id="15b89-234">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-234">In Global Catalog</span></span>      | <span data-ttu-id="15b89-235">否</span><span class="sxs-lookup"><span data-stu-id="15b89-235">False</span></span>                                                |
| <span data-ttu-id="15b89-236">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-237">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-240">Search-Flags</span></span>           | <span data-ttu-id="15b89-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-241">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-242">System-Flags</span></span>           | <span data-ttu-id="15b89-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-243">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-244">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-244">Classes used in</span></span>        | [<span data-ttu-id="15b89-245">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="15b89-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15b89-246">Windows Server 2012</span></span>



| <span data-ttu-id="15b89-247">進入</span><span class="sxs-lookup"><span data-stu-id="15b89-247">Entry</span></span> | <span data-ttu-id="15b89-248">值</span><span class="sxs-lookup"><span data-stu-id="15b89-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="15b89-249">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="15b89-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="15b89-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="15b89-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="15b89-251">System-Only</span></span>            | <span data-ttu-id="15b89-252">否</span><span class="sxs-lookup"><span data-stu-id="15b89-252">False</span></span>                                                |
| <span data-ttu-id="15b89-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="15b89-253">Is-Single-Valued</span></span>       | <span data-ttu-id="15b89-254">對</span><span class="sxs-lookup"><span data-stu-id="15b89-254">True</span></span>                                                 |
| <span data-ttu-id="15b89-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="15b89-255">Is Indexed</span></span>             | <span data-ttu-id="15b89-256">對</span><span class="sxs-lookup"><span data-stu-id="15b89-256">True</span></span>                                                 |
| <span data-ttu-id="15b89-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="15b89-257">In Global Catalog</span></span>      | <span data-ttu-id="15b89-258">否</span><span class="sxs-lookup"><span data-stu-id="15b89-258">False</span></span>                                                |
| <span data-ttu-id="15b89-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="15b89-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="15b89-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="15b89-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="15b89-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="15b89-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="15b89-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="15b89-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-263">Search-Flags</span></span>           | <span data-ttu-id="15b89-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="15b89-264">0x00000001</span></span>                                           |
| <span data-ttu-id="15b89-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="15b89-265">System-Flags</span></span>           | <span data-ttu-id="15b89-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="15b89-266">0x00000010</span></span>                                           |
| <span data-ttu-id="15b89-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="15b89-267">Classes used in</span></span>        | [<span data-ttu-id="15b89-268">**信任網域**</span><span class="sxs-lookup"><span data-stu-id="15b89-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





