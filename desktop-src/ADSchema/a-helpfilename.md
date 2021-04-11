---
title: 說明-檔案名屬性
description: 這個屬性是用於 Exchange 4.0。 它包含當提供者將說明資料下載到用戶端電腦時，該檔案應使用的名稱。 它不會用於任何其他版本的 Exchange。
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- 說明-檔案名屬性 AD 架構
- helpFileName 屬性 AD 架構
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845243"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="710d5-107">說明-檔案名屬性</span><span class="sxs-lookup"><span data-stu-id="710d5-107">Help-File-Name attribute</span></span>

<span data-ttu-id="710d5-108">這個屬性是用於 Exchange 4.0。</span><span class="sxs-lookup"><span data-stu-id="710d5-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="710d5-109">它包含當提供者將說明資料下載到用戶端電腦時，該檔案應使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="710d5-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="710d5-110">它不會用於任何其他版本的 Exchange。</span><span class="sxs-lookup"><span data-stu-id="710d5-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="710d5-111">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-111">Entry</span></span> | <span data-ttu-id="710d5-112">值</span><span class="sxs-lookup"><span data-stu-id="710d5-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="710d5-113">CN</span><span class="sxs-lookup"><span data-stu-id="710d5-113">CN</span></span>                | <span data-ttu-id="710d5-114">說明檔-檔案名</span><span class="sxs-lookup"><span data-stu-id="710d5-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="710d5-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="710d5-115">Ldap-Display-Name</span></span> | <span data-ttu-id="710d5-116">helpFileName</span><span class="sxs-lookup"><span data-stu-id="710d5-116">helpFileName</span></span>                                |
| <span data-ttu-id="710d5-117">大小</span><span class="sxs-lookup"><span data-stu-id="710d5-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="710d5-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="710d5-118">Update Privilege</span></span>  | <span data-ttu-id="710d5-119">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="710d5-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="710d5-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="710d5-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="710d5-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-121">Attribute-Id</span></span>      | <span data-ttu-id="710d5-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="710d5-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="710d5-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="710d5-123">System-Id-Guid</span></span>    | <span data-ttu-id="710d5-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="710d5-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="710d5-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="710d5-125">Syntax</span></span>            | [<span data-ttu-id="710d5-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="710d5-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="710d5-127">實作</span><span class="sxs-lookup"><span data-stu-id="710d5-127">Implementations</span></span>

-   [<span data-ttu-id="710d5-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="710d5-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="710d5-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="710d5-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="710d5-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="710d5-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="710d5-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="710d5-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="710d5-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="710d5-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="710d5-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="710d5-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="710d5-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="710d5-134">Windows 2000 Server</span></span>



| <span data-ttu-id="710d5-135">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-135">Entry</span></span> | <span data-ttu-id="710d5-136">值</span><span class="sxs-lookup"><span data-stu-id="710d5-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-138">MAPI-Id</span></span>                | <span data-ttu-id="710d5-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-139">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-140">System-Only</span></span>            | <span data-ttu-id="710d5-141">否</span><span class="sxs-lookup"><span data-stu-id="710d5-141">False</span></span>                                                    |
| <span data-ttu-id="710d5-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-142">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-143">對</span><span class="sxs-lookup"><span data-stu-id="710d5-143">True</span></span>                                                     |
| <span data-ttu-id="710d5-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-144">Is Indexed</span></span>             | <span data-ttu-id="710d5-145">否</span><span class="sxs-lookup"><span data-stu-id="710d5-145">False</span></span>                                                    |
| <span data-ttu-id="710d5-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-146">In Global Catalog</span></span>      | <span data-ttu-id="710d5-147">否</span><span class="sxs-lookup"><span data-stu-id="710d5-147">False</span></span>                                                    |
| <span data-ttu-id="710d5-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-150">Range-Lower</span></span>            | <span data-ttu-id="710d5-151">1</span><span class="sxs-lookup"><span data-stu-id="710d5-151">1</span></span>                                                        |
| <span data-ttu-id="710d5-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-152">Range-Upper</span></span>            | <span data-ttu-id="710d5-153">13</span><span class="sxs-lookup"><span data-stu-id="710d5-153">13</span></span>                                                       |
| <span data-ttu-id="710d5-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-154">Search-Flags</span></span>           | <span data-ttu-id="710d5-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-155">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-156">System-Flags</span></span>           | <span data-ttu-id="710d5-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-157">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-158">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-158">Classes used in</span></span>        | [<span data-ttu-id="710d5-159">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="710d5-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="710d5-160">Windows Server 2003</span></span>



| <span data-ttu-id="710d5-161">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-161">Entry</span></span> | <span data-ttu-id="710d5-162">值</span><span class="sxs-lookup"><span data-stu-id="710d5-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-163">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-164">MAPI-Id</span></span>                | <span data-ttu-id="710d5-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-165">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-166">System-Only</span></span>            | <span data-ttu-id="710d5-167">否</span><span class="sxs-lookup"><span data-stu-id="710d5-167">False</span></span>                                                    |
| <span data-ttu-id="710d5-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-168">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-169">對</span><span class="sxs-lookup"><span data-stu-id="710d5-169">True</span></span>                                                     |
| <span data-ttu-id="710d5-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-170">Is Indexed</span></span>             | <span data-ttu-id="710d5-171">否</span><span class="sxs-lookup"><span data-stu-id="710d5-171">False</span></span>                                                    |
| <span data-ttu-id="710d5-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-172">In Global Catalog</span></span>      | <span data-ttu-id="710d5-173">否</span><span class="sxs-lookup"><span data-stu-id="710d5-173">False</span></span>                                                    |
| <span data-ttu-id="710d5-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-176">Range-Lower</span></span>            | <span data-ttu-id="710d5-177">1</span><span class="sxs-lookup"><span data-stu-id="710d5-177">1</span></span>                                                        |
| <span data-ttu-id="710d5-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-178">Range-Upper</span></span>            | <span data-ttu-id="710d5-179">13</span><span class="sxs-lookup"><span data-stu-id="710d5-179">13</span></span>                                                       |
| <span data-ttu-id="710d5-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-180">Search-Flags</span></span>           | <span data-ttu-id="710d5-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-181">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-182">System-Flags</span></span>           | <span data-ttu-id="710d5-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-183">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-184">Classes used in</span></span>        | [<span data-ttu-id="710d5-185">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="710d5-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="710d5-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="710d5-187">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-187">Entry</span></span> | <span data-ttu-id="710d5-188">值</span><span class="sxs-lookup"><span data-stu-id="710d5-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-190">MAPI-Id</span></span>                | <span data-ttu-id="710d5-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-191">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-192">System-Only</span></span>            | <span data-ttu-id="710d5-193">否</span><span class="sxs-lookup"><span data-stu-id="710d5-193">False</span></span>                                                    |
| <span data-ttu-id="710d5-194">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-194">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-195">對</span><span class="sxs-lookup"><span data-stu-id="710d5-195">True</span></span>                                                     |
| <span data-ttu-id="710d5-196">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-196">Is Indexed</span></span>             | <span data-ttu-id="710d5-197">否</span><span class="sxs-lookup"><span data-stu-id="710d5-197">False</span></span>                                                    |
| <span data-ttu-id="710d5-198">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-198">In Global Catalog</span></span>      | <span data-ttu-id="710d5-199">否</span><span class="sxs-lookup"><span data-stu-id="710d5-199">False</span></span>                                                    |
| <span data-ttu-id="710d5-200">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-201">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-202">Range-Lower</span></span>            | <span data-ttu-id="710d5-203">1</span><span class="sxs-lookup"><span data-stu-id="710d5-203">1</span></span>                                                        |
| <span data-ttu-id="710d5-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-204">Range-Upper</span></span>            | <span data-ttu-id="710d5-205">13</span><span class="sxs-lookup"><span data-stu-id="710d5-205">13</span></span>                                                       |
| <span data-ttu-id="710d5-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-206">Search-Flags</span></span>           | <span data-ttu-id="710d5-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-207">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-208">System-Flags</span></span>           | <span data-ttu-id="710d5-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-209">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-210">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-210">Classes used in</span></span>        | [<span data-ttu-id="710d5-211">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="710d5-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="710d5-212">Windows Server 2008</span></span>



| <span data-ttu-id="710d5-213">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-213">Entry</span></span> | <span data-ttu-id="710d5-214">值</span><span class="sxs-lookup"><span data-stu-id="710d5-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-215">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-216">MAPI-Id</span></span>                | <span data-ttu-id="710d5-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-217">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-218">System-Only</span></span>            | <span data-ttu-id="710d5-219">否</span><span class="sxs-lookup"><span data-stu-id="710d5-219">False</span></span>                                                    |
| <span data-ttu-id="710d5-220">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-220">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-221">對</span><span class="sxs-lookup"><span data-stu-id="710d5-221">True</span></span>                                                     |
| <span data-ttu-id="710d5-222">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-222">Is Indexed</span></span>             | <span data-ttu-id="710d5-223">否</span><span class="sxs-lookup"><span data-stu-id="710d5-223">False</span></span>                                                    |
| <span data-ttu-id="710d5-224">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-224">In Global Catalog</span></span>      | <span data-ttu-id="710d5-225">否</span><span class="sxs-lookup"><span data-stu-id="710d5-225">False</span></span>                                                    |
| <span data-ttu-id="710d5-226">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-227">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-228">Range-Lower</span></span>            | <span data-ttu-id="710d5-229">1</span><span class="sxs-lookup"><span data-stu-id="710d5-229">1</span></span>                                                        |
| <span data-ttu-id="710d5-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-230">Range-Upper</span></span>            | <span data-ttu-id="710d5-231">13</span><span class="sxs-lookup"><span data-stu-id="710d5-231">13</span></span>                                                       |
| <span data-ttu-id="710d5-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-232">Search-Flags</span></span>           | <span data-ttu-id="710d5-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-233">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-234">System-Flags</span></span>           | <span data-ttu-id="710d5-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-235">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-236">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-236">Classes used in</span></span>        | [<span data-ttu-id="710d5-237">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="710d5-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="710d5-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="710d5-239">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-239">Entry</span></span> | <span data-ttu-id="710d5-240">值</span><span class="sxs-lookup"><span data-stu-id="710d5-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-241">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-242">MAPI-Id</span></span>                | <span data-ttu-id="710d5-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-243">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-244">System-Only</span></span>            | <span data-ttu-id="710d5-245">否</span><span class="sxs-lookup"><span data-stu-id="710d5-245">False</span></span>                                                    |
| <span data-ttu-id="710d5-246">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-246">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-247">對</span><span class="sxs-lookup"><span data-stu-id="710d5-247">True</span></span>                                                     |
| <span data-ttu-id="710d5-248">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-248">Is Indexed</span></span>             | <span data-ttu-id="710d5-249">否</span><span class="sxs-lookup"><span data-stu-id="710d5-249">False</span></span>                                                    |
| <span data-ttu-id="710d5-250">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-250">In Global Catalog</span></span>      | <span data-ttu-id="710d5-251">否</span><span class="sxs-lookup"><span data-stu-id="710d5-251">False</span></span>                                                    |
| <span data-ttu-id="710d5-252">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-253">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-254">Range-Lower</span></span>            | <span data-ttu-id="710d5-255">1</span><span class="sxs-lookup"><span data-stu-id="710d5-255">1</span></span>                                                        |
| <span data-ttu-id="710d5-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-256">Range-Upper</span></span>            | <span data-ttu-id="710d5-257">13</span><span class="sxs-lookup"><span data-stu-id="710d5-257">13</span></span>                                                       |
| <span data-ttu-id="710d5-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-258">Search-Flags</span></span>           | <span data-ttu-id="710d5-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-259">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-260">System-Flags</span></span>           | <span data-ttu-id="710d5-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-261">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-262">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-262">Classes used in</span></span>        | [<span data-ttu-id="710d5-263">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="710d5-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="710d5-264">Windows Server 2012</span></span>



| <span data-ttu-id="710d5-265">進入</span><span class="sxs-lookup"><span data-stu-id="710d5-265">Entry</span></span> | <span data-ttu-id="710d5-266">值</span><span class="sxs-lookup"><span data-stu-id="710d5-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="710d5-267">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="710d5-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="710d5-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="710d5-268">MAPI-Id</span></span>                | <span data-ttu-id="710d5-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="710d5-269">0x803B</span></span>                                                   |
| <span data-ttu-id="710d5-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="710d5-270">System-Only</span></span>            | <span data-ttu-id="710d5-271">否</span><span class="sxs-lookup"><span data-stu-id="710d5-271">False</span></span>                                                    |
| <span data-ttu-id="710d5-272">是-單一值</span><span class="sxs-lookup"><span data-stu-id="710d5-272">Is-Single-Valued</span></span>       | <span data-ttu-id="710d5-273">對</span><span class="sxs-lookup"><span data-stu-id="710d5-273">True</span></span>                                                     |
| <span data-ttu-id="710d5-274">已編制索引</span><span class="sxs-lookup"><span data-stu-id="710d5-274">Is Indexed</span></span>             | <span data-ttu-id="710d5-275">否</span><span class="sxs-lookup"><span data-stu-id="710d5-275">False</span></span>                                                    |
| <span data-ttu-id="710d5-276">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="710d5-276">In Global Catalog</span></span>      | <span data-ttu-id="710d5-277">否</span><span class="sxs-lookup"><span data-stu-id="710d5-277">False</span></span>                                                    |
| <span data-ttu-id="710d5-278">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="710d5-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="710d5-279">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="710d5-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="710d5-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="710d5-280">Range-Lower</span></span>            | <span data-ttu-id="710d5-281">1</span><span class="sxs-lookup"><span data-stu-id="710d5-281">1</span></span>                                                        |
| <span data-ttu-id="710d5-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="710d5-282">Range-Upper</span></span>            | <span data-ttu-id="710d5-283">13</span><span class="sxs-lookup"><span data-stu-id="710d5-283">13</span></span>                                                       |
| <span data-ttu-id="710d5-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-284">Search-Flags</span></span>           | <span data-ttu-id="710d5-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="710d5-285">0x00000000</span></span>                                               |
| <span data-ttu-id="710d5-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="710d5-286">System-Flags</span></span>           | <span data-ttu-id="710d5-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="710d5-287">0x00000010</span></span>                                               |
| <span data-ttu-id="710d5-288">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="710d5-288">Classes used in</span></span>        | [<span data-ttu-id="710d5-289">**顯示範本**</span><span class="sxs-lookup"><span data-stu-id="710d5-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





