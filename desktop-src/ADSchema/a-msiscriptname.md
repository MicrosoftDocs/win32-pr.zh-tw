---
title: Msi-腳本-名稱屬性
description: 此應用程式的 Microsoft installer 公告腳本檔名稱。
ms.assetid: f4666441-f416-4103-8ad5-6cdb6f4b0a97
ms.tgt_platform: multiple
keywords:
- Msi-腳本-名稱屬性 AD 架構
- msiScriptName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Msi-Script-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f155bd9a1dd62bdd72f5a589c6583742ebaa65
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973332"
---
# <a name="msi-script-name-attribute"></a><span data-ttu-id="29587-105">Msi-腳本-名稱屬性</span><span class="sxs-lookup"><span data-stu-id="29587-105">Msi-Script-Name attribute</span></span>

<span data-ttu-id="29587-106">此應用程式的 Microsoft installer 公告腳本檔名稱。</span><span class="sxs-lookup"><span data-stu-id="29587-106">The name for the Microsoft installer advertisement script file for this application.</span></span>



| <span data-ttu-id="29587-107">進入</span><span class="sxs-lookup"><span data-stu-id="29587-107">Entry</span></span> | <span data-ttu-id="29587-108">值</span><span class="sxs-lookup"><span data-stu-id="29587-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="29587-109">CN</span><span class="sxs-lookup"><span data-stu-id="29587-109">CN</span></span>                | <span data-ttu-id="29587-110">Msi-腳本-名稱</span><span class="sxs-lookup"><span data-stu-id="29587-110">Msi-Script-Name</span></span>                             |
| <span data-ttu-id="29587-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="29587-111">Ldap-Display-Name</span></span> | <span data-ttu-id="29587-112">msiScriptName</span><span class="sxs-lookup"><span data-stu-id="29587-112">msiScriptName</span></span>                               |
| <span data-ttu-id="29587-113">大小</span><span class="sxs-lookup"><span data-stu-id="29587-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="29587-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="29587-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="29587-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="29587-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="29587-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29587-116">Attribute-Id</span></span>      | <span data-ttu-id="29587-117">1.2.840.113556.1.4.845</span><span class="sxs-lookup"><span data-stu-id="29587-117">1.2.840.113556.1.4.845</span></span>                      |
| <span data-ttu-id="29587-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="29587-118">System-Id-Guid</span></span>    | <span data-ttu-id="29587-119">96a7dd62-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="29587-119">96a7dd62-9118-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="29587-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="29587-120">Syntax</span></span>            | [<span data-ttu-id="29587-121">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="29587-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="29587-122">實作</span><span class="sxs-lookup"><span data-stu-id="29587-122">Implementations</span></span>

-   [<span data-ttu-id="29587-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29587-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29587-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29587-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29587-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29587-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29587-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29587-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29587-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29587-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29587-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29587-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29587-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29587-129">Windows 2000 Server</span></span>



| <span data-ttu-id="29587-130">進入</span><span class="sxs-lookup"><span data-stu-id="29587-130">Entry</span></span> | <span data-ttu-id="29587-131">值</span><span class="sxs-lookup"><span data-stu-id="29587-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-134">System-Only</span></span>            | <span data-ttu-id="29587-135">否</span><span class="sxs-lookup"><span data-stu-id="29587-135">False</span></span>                                                            |
| <span data-ttu-id="29587-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-136">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-137">對</span><span class="sxs-lookup"><span data-stu-id="29587-137">True</span></span>                                                             |
| <span data-ttu-id="29587-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-138">Is Indexed</span></span>             | <span data-ttu-id="29587-139">否</span><span class="sxs-lookup"><span data-stu-id="29587-139">False</span></span>                                                            |
| <span data-ttu-id="29587-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-140">In Global Catalog</span></span>      | <span data-ttu-id="29587-141">否</span><span class="sxs-lookup"><span data-stu-id="29587-141">False</span></span>                                                            |
| <span data-ttu-id="29587-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-146">Search-Flags</span></span>           | <span data-ttu-id="29587-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-148">System-Flags</span></span>           | <span data-ttu-id="29587-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-150">Classes used in</span></span>        | [<span data-ttu-id="29587-151">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29587-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29587-152">Windows Server 2003</span></span>



| <span data-ttu-id="29587-153">進入</span><span class="sxs-lookup"><span data-stu-id="29587-153">Entry</span></span> | <span data-ttu-id="29587-154">值</span><span class="sxs-lookup"><span data-stu-id="29587-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-157">System-Only</span></span>            | <span data-ttu-id="29587-158">否</span><span class="sxs-lookup"><span data-stu-id="29587-158">False</span></span>                                                            |
| <span data-ttu-id="29587-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-159">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-160">對</span><span class="sxs-lookup"><span data-stu-id="29587-160">True</span></span>                                                             |
| <span data-ttu-id="29587-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-161">Is Indexed</span></span>             | <span data-ttu-id="29587-162">否</span><span class="sxs-lookup"><span data-stu-id="29587-162">False</span></span>                                                            |
| <span data-ttu-id="29587-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-163">In Global Catalog</span></span>      | <span data-ttu-id="29587-164">否</span><span class="sxs-lookup"><span data-stu-id="29587-164">False</span></span>                                                            |
| <span data-ttu-id="29587-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-169">Search-Flags</span></span>           | <span data-ttu-id="29587-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-171">System-Flags</span></span>           | <span data-ttu-id="29587-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-173">Classes used in</span></span>        | [<span data-ttu-id="29587-174">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29587-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29587-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29587-176">進入</span><span class="sxs-lookup"><span data-stu-id="29587-176">Entry</span></span> | <span data-ttu-id="29587-177">值</span><span class="sxs-lookup"><span data-stu-id="29587-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-178">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-180">System-Only</span></span>            | <span data-ttu-id="29587-181">否</span><span class="sxs-lookup"><span data-stu-id="29587-181">False</span></span>                                                            |
| <span data-ttu-id="29587-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-182">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-183">對</span><span class="sxs-lookup"><span data-stu-id="29587-183">True</span></span>                                                             |
| <span data-ttu-id="29587-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-184">Is Indexed</span></span>             | <span data-ttu-id="29587-185">否</span><span class="sxs-lookup"><span data-stu-id="29587-185">False</span></span>                                                            |
| <span data-ttu-id="29587-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-186">In Global Catalog</span></span>      | <span data-ttu-id="29587-187">否</span><span class="sxs-lookup"><span data-stu-id="29587-187">False</span></span>                                                            |
| <span data-ttu-id="29587-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-192">Search-Flags</span></span>           | <span data-ttu-id="29587-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-194">System-Flags</span></span>           | <span data-ttu-id="29587-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-196">Classes used in</span></span>        | [<span data-ttu-id="29587-197">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29587-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29587-198">Windows Server 2008</span></span>



| <span data-ttu-id="29587-199">進入</span><span class="sxs-lookup"><span data-stu-id="29587-199">Entry</span></span> | <span data-ttu-id="29587-200">值</span><span class="sxs-lookup"><span data-stu-id="29587-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-201">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-203">System-Only</span></span>            | <span data-ttu-id="29587-204">否</span><span class="sxs-lookup"><span data-stu-id="29587-204">False</span></span>                                                            |
| <span data-ttu-id="29587-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-205">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-206">對</span><span class="sxs-lookup"><span data-stu-id="29587-206">True</span></span>                                                             |
| <span data-ttu-id="29587-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-207">Is Indexed</span></span>             | <span data-ttu-id="29587-208">否</span><span class="sxs-lookup"><span data-stu-id="29587-208">False</span></span>                                                            |
| <span data-ttu-id="29587-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-209">In Global Catalog</span></span>      | <span data-ttu-id="29587-210">否</span><span class="sxs-lookup"><span data-stu-id="29587-210">False</span></span>                                                            |
| <span data-ttu-id="29587-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-215">Search-Flags</span></span>           | <span data-ttu-id="29587-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-217">System-Flags</span></span>           | <span data-ttu-id="29587-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-219">Classes used in</span></span>        | [<span data-ttu-id="29587-220">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29587-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29587-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29587-222">進入</span><span class="sxs-lookup"><span data-stu-id="29587-222">Entry</span></span> | <span data-ttu-id="29587-223">值</span><span class="sxs-lookup"><span data-stu-id="29587-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-226">System-Only</span></span>            | <span data-ttu-id="29587-227">否</span><span class="sxs-lookup"><span data-stu-id="29587-227">False</span></span>                                                            |
| <span data-ttu-id="29587-228">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-228">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-229">對</span><span class="sxs-lookup"><span data-stu-id="29587-229">True</span></span>                                                             |
| <span data-ttu-id="29587-230">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-230">Is Indexed</span></span>             | <span data-ttu-id="29587-231">否</span><span class="sxs-lookup"><span data-stu-id="29587-231">False</span></span>                                                            |
| <span data-ttu-id="29587-232">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-232">In Global Catalog</span></span>      | <span data-ttu-id="29587-233">否</span><span class="sxs-lookup"><span data-stu-id="29587-233">False</span></span>                                                            |
| <span data-ttu-id="29587-234">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-235">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-238">Search-Flags</span></span>           | <span data-ttu-id="29587-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-240">System-Flags</span></span>           | <span data-ttu-id="29587-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-242">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-242">Classes used in</span></span>        | [<span data-ttu-id="29587-243">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29587-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29587-244">Windows Server 2012</span></span>



| <span data-ttu-id="29587-245">進入</span><span class="sxs-lookup"><span data-stu-id="29587-245">Entry</span></span> | <span data-ttu-id="29587-246">值</span><span class="sxs-lookup"><span data-stu-id="29587-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29587-247">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="29587-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29587-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29587-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="29587-249">System-Only</span></span>            | <span data-ttu-id="29587-250">否</span><span class="sxs-lookup"><span data-stu-id="29587-250">False</span></span>                                                            |
| <span data-ttu-id="29587-251">是-單一值</span><span class="sxs-lookup"><span data-stu-id="29587-251">Is-Single-Valued</span></span>       | <span data-ttu-id="29587-252">對</span><span class="sxs-lookup"><span data-stu-id="29587-252">True</span></span>                                                             |
| <span data-ttu-id="29587-253">已編制索引</span><span class="sxs-lookup"><span data-stu-id="29587-253">Is Indexed</span></span>             | <span data-ttu-id="29587-254">否</span><span class="sxs-lookup"><span data-stu-id="29587-254">False</span></span>                                                            |
| <span data-ttu-id="29587-255">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="29587-255">In Global Catalog</span></span>      | <span data-ttu-id="29587-256">否</span><span class="sxs-lookup"><span data-stu-id="29587-256">False</span></span>                                                            |
| <span data-ttu-id="29587-257">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="29587-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="29587-258">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="29587-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29587-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29587-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29587-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29587-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29587-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-261">Search-Flags</span></span>           | <span data-ttu-id="29587-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29587-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="29587-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29587-263">System-Flags</span></span>           | <span data-ttu-id="29587-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29587-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="29587-265">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="29587-265">Classes used in</span></span>        | [<span data-ttu-id="29587-266">**套件-註冊**</span><span class="sxs-lookup"><span data-stu-id="29587-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





