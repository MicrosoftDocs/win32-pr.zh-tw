---
title: ms-DS-其他 Dns-主機名稱屬性
description: 屬性是用來儲存電腦物件的其他 DNS 主機名稱。 當 DC 重新命名時，就會使用這個屬性。
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- ms DS-其他 Dns-主機名稱屬性 AD 架構
- AdditionalDnsHostName 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935431"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="fb2af-106">ms-DS-其他 Dns-主機名稱屬性</span><span class="sxs-lookup"><span data-stu-id="fb2af-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="fb2af-107">屬性是用來儲存電腦物件的其他 DNS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="fb2af-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="fb2af-108">這個屬性是在電腦重新命名時使用，或以 "netdom computername" 管理名稱。</span><span class="sxs-lookup"><span data-stu-id="fb2af-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="fb2af-109">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-109">Entry</span></span> | <span data-ttu-id="fb2af-110">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fb2af-111">CN</span><span class="sxs-lookup"><span data-stu-id="fb2af-111">CN</span></span>                | <span data-ttu-id="fb2af-112">ms-DS-其他 Dns-主機名稱</span><span class="sxs-lookup"><span data-stu-id="fb2af-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="fb2af-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fb2af-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fb2af-114">AdditionalDnsHostName</span><span class="sxs-lookup"><span data-stu-id="fb2af-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="fb2af-115">大小</span><span class="sxs-lookup"><span data-stu-id="fb2af-115">Size</span></span>              | <span data-ttu-id="fb2af-116">每個值都可以是2048個字元。</span><span class="sxs-lookup"><span data-stu-id="fb2af-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="fb2af-117">值的數目是大約1200值的資料庫限制。</span><span class="sxs-lookup"><span data-stu-id="fb2af-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="fb2af-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fb2af-118">Update Privilege</span></span>  | <span data-ttu-id="fb2af-119">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="fb2af-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="fb2af-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fb2af-120">Update Frequency</span></span>  | <span data-ttu-id="fb2af-121">重新命名電腦時。</span><span class="sxs-lookup"><span data-stu-id="fb2af-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="fb2af-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-122">Attribute-Id</span></span>      | <span data-ttu-id="fb2af-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="fb2af-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="fb2af-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fb2af-124">System-Id-Guid</span></span>    | <span data-ttu-id="fb2af-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="fb2af-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="fb2af-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb2af-126">Syntax</span></span>            | [<span data-ttu-id="fb2af-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="fb2af-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="fb2af-128">實作</span><span class="sxs-lookup"><span data-stu-id="fb2af-128">Implementations</span></span>

-   [<span data-ttu-id="fb2af-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fb2af-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fb2af-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fb2af-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fb2af-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fb2af-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fb2af-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fb2af-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fb2af-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fb2af-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fb2af-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb2af-134">Windows Server 2003</span></span>



| <span data-ttu-id="fb2af-135">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-135">Entry</span></span> | <span data-ttu-id="fb2af-136">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="fb2af-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb2af-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb2af-139">System-Only</span></span>            | <span data-ttu-id="fb2af-140">對</span><span class="sxs-lookup"><span data-stu-id="fb2af-140">True</span></span>                                      |
| <span data-ttu-id="fb2af-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb2af-141">Is-Single-Valued</span></span>       | <span data-ttu-id="fb2af-142">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-142">False</span></span>                                     |
| <span data-ttu-id="fb2af-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb2af-143">Is Indexed</span></span>             | <span data-ttu-id="fb2af-144">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-144">False</span></span>                                     |
| <span data-ttu-id="fb2af-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb2af-145">In Global Catalog</span></span>      | <span data-ttu-id="fb2af-146">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-146">False</span></span>                                     |
| <span data-ttu-id="fb2af-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb2af-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb2af-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb2af-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="fb2af-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb2af-149">Range-Lower</span></span>            | <span data-ttu-id="fb2af-150">0</span><span class="sxs-lookup"><span data-stu-id="fb2af-150">0</span></span>                                         |
| <span data-ttu-id="fb2af-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb2af-151">Range-Upper</span></span>            | <span data-ttu-id="fb2af-152">2048</span><span class="sxs-lookup"><span data-stu-id="fb2af-152">2048</span></span>                                      |
| <span data-ttu-id="fb2af-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-153">Search-Flags</span></span>           | <span data-ttu-id="fb2af-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb2af-154">0x00000000</span></span>                                |
| <span data-ttu-id="fb2af-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-155">System-Flags</span></span>           | <span data-ttu-id="fb2af-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb2af-156">0x00000010</span></span>                                |
| <span data-ttu-id="fb2af-157">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb2af-157">Classes used in</span></span>        | [<span data-ttu-id="fb2af-158">**電腦**</span><span class="sxs-lookup"><span data-stu-id="fb2af-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fb2af-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fb2af-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fb2af-160">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-160">Entry</span></span> | <span data-ttu-id="fb2af-161">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="fb2af-162">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb2af-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb2af-164">System-Only</span></span>            | <span data-ttu-id="fb2af-165">對</span><span class="sxs-lookup"><span data-stu-id="fb2af-165">True</span></span>                                      |
| <span data-ttu-id="fb2af-166">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb2af-166">Is-Single-Valued</span></span>       | <span data-ttu-id="fb2af-167">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-167">False</span></span>                                     |
| <span data-ttu-id="fb2af-168">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb2af-168">Is Indexed</span></span>             | <span data-ttu-id="fb2af-169">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-169">False</span></span>                                     |
| <span data-ttu-id="fb2af-170">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb2af-170">In Global Catalog</span></span>      | <span data-ttu-id="fb2af-171">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-171">False</span></span>                                     |
| <span data-ttu-id="fb2af-172">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb2af-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb2af-173">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb2af-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="fb2af-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb2af-174">Range-Lower</span></span>            | <span data-ttu-id="fb2af-175">0</span><span class="sxs-lookup"><span data-stu-id="fb2af-175">0</span></span>                                         |
| <span data-ttu-id="fb2af-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb2af-176">Range-Upper</span></span>            | <span data-ttu-id="fb2af-177">2048</span><span class="sxs-lookup"><span data-stu-id="fb2af-177">2048</span></span>                                      |
| <span data-ttu-id="fb2af-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-178">Search-Flags</span></span>           | <span data-ttu-id="fb2af-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb2af-179">0x00000000</span></span>                                |
| <span data-ttu-id="fb2af-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-180">System-Flags</span></span>           | <span data-ttu-id="fb2af-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb2af-181">0x00000010</span></span>                                |
| <span data-ttu-id="fb2af-182">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb2af-182">Classes used in</span></span>        | [<span data-ttu-id="fb2af-183">**電腦**</span><span class="sxs-lookup"><span data-stu-id="fb2af-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fb2af-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb2af-184">Windows Server 2008</span></span>



| <span data-ttu-id="fb2af-185">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-185">Entry</span></span> | <span data-ttu-id="fb2af-186">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="fb2af-187">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb2af-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb2af-189">System-Only</span></span>            | <span data-ttu-id="fb2af-190">對</span><span class="sxs-lookup"><span data-stu-id="fb2af-190">True</span></span>                                      |
| <span data-ttu-id="fb2af-191">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb2af-191">Is-Single-Valued</span></span>       | <span data-ttu-id="fb2af-192">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-192">False</span></span>                                     |
| <span data-ttu-id="fb2af-193">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb2af-193">Is Indexed</span></span>             | <span data-ttu-id="fb2af-194">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-194">False</span></span>                                     |
| <span data-ttu-id="fb2af-195">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb2af-195">In Global Catalog</span></span>      | <span data-ttu-id="fb2af-196">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-196">False</span></span>                                     |
| <span data-ttu-id="fb2af-197">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb2af-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb2af-198">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb2af-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="fb2af-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb2af-199">Range-Lower</span></span>            | <span data-ttu-id="fb2af-200">0</span><span class="sxs-lookup"><span data-stu-id="fb2af-200">0</span></span>                                         |
| <span data-ttu-id="fb2af-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb2af-201">Range-Upper</span></span>            | <span data-ttu-id="fb2af-202">2048</span><span class="sxs-lookup"><span data-stu-id="fb2af-202">2048</span></span>                                      |
| <span data-ttu-id="fb2af-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-203">Search-Flags</span></span>           | <span data-ttu-id="fb2af-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb2af-204">0x00000000</span></span>                                |
| <span data-ttu-id="fb2af-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-205">System-Flags</span></span>           | <span data-ttu-id="fb2af-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb2af-206">0x00000010</span></span>                                |
| <span data-ttu-id="fb2af-207">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb2af-207">Classes used in</span></span>        | [<span data-ttu-id="fb2af-208">**電腦**</span><span class="sxs-lookup"><span data-stu-id="fb2af-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fb2af-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb2af-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fb2af-210">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-210">Entry</span></span> | <span data-ttu-id="fb2af-211">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="fb2af-212">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb2af-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb2af-214">System-Only</span></span>            | <span data-ttu-id="fb2af-215">對</span><span class="sxs-lookup"><span data-stu-id="fb2af-215">True</span></span>                                      |
| <span data-ttu-id="fb2af-216">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb2af-216">Is-Single-Valued</span></span>       | <span data-ttu-id="fb2af-217">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-217">False</span></span>                                     |
| <span data-ttu-id="fb2af-218">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb2af-218">Is Indexed</span></span>             | <span data-ttu-id="fb2af-219">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-219">False</span></span>                                     |
| <span data-ttu-id="fb2af-220">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb2af-220">In Global Catalog</span></span>      | <span data-ttu-id="fb2af-221">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-221">False</span></span>                                     |
| <span data-ttu-id="fb2af-222">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb2af-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb2af-223">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb2af-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="fb2af-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb2af-224">Range-Lower</span></span>            | <span data-ttu-id="fb2af-225">0</span><span class="sxs-lookup"><span data-stu-id="fb2af-225">0</span></span>                                         |
| <span data-ttu-id="fb2af-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb2af-226">Range-Upper</span></span>            | <span data-ttu-id="fb2af-227">2048</span><span class="sxs-lookup"><span data-stu-id="fb2af-227">2048</span></span>                                      |
| <span data-ttu-id="fb2af-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-228">Search-Flags</span></span>           | <span data-ttu-id="fb2af-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb2af-229">0x00000000</span></span>                                |
| <span data-ttu-id="fb2af-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-230">System-Flags</span></span>           | <span data-ttu-id="fb2af-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb2af-231">0x00000010</span></span>                                |
| <span data-ttu-id="fb2af-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb2af-232">Classes used in</span></span>        | [<span data-ttu-id="fb2af-233">**電腦**</span><span class="sxs-lookup"><span data-stu-id="fb2af-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fb2af-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb2af-234">Windows Server 2012</span></span>



| <span data-ttu-id="fb2af-235">進入</span><span class="sxs-lookup"><span data-stu-id="fb2af-235">Entry</span></span> | <span data-ttu-id="fb2af-236">值</span><span class="sxs-lookup"><span data-stu-id="fb2af-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="fb2af-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fb2af-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fb2af-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="fb2af-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="fb2af-239">System-Only</span></span>            | <span data-ttu-id="fb2af-240">對</span><span class="sxs-lookup"><span data-stu-id="fb2af-240">True</span></span>                                      |
| <span data-ttu-id="fb2af-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fb2af-241">Is-Single-Valued</span></span>       | <span data-ttu-id="fb2af-242">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-242">False</span></span>                                     |
| <span data-ttu-id="fb2af-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fb2af-243">Is Indexed</span></span>             | <span data-ttu-id="fb2af-244">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-244">False</span></span>                                     |
| <span data-ttu-id="fb2af-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fb2af-245">In Global Catalog</span></span>      | <span data-ttu-id="fb2af-246">否</span><span class="sxs-lookup"><span data-stu-id="fb2af-246">False</span></span>                                     |
| <span data-ttu-id="fb2af-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fb2af-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="fb2af-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fb2af-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="fb2af-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fb2af-249">Range-Lower</span></span>            | <span data-ttu-id="fb2af-250">0</span><span class="sxs-lookup"><span data-stu-id="fb2af-250">0</span></span>                                         |
| <span data-ttu-id="fb2af-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fb2af-251">Range-Upper</span></span>            | <span data-ttu-id="fb2af-252">2048</span><span class="sxs-lookup"><span data-stu-id="fb2af-252">2048</span></span>                                      |
| <span data-ttu-id="fb2af-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-253">Search-Flags</span></span>           | <span data-ttu-id="fb2af-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fb2af-254">0x00000000</span></span>                                |
| <span data-ttu-id="fb2af-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fb2af-255">System-Flags</span></span>           | <span data-ttu-id="fb2af-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fb2af-256">0x00000010</span></span>                                |
| <span data-ttu-id="fb2af-257">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fb2af-257">Classes used in</span></span>        | [<span data-ttu-id="fb2af-258">**電腦**</span><span class="sxs-lookup"><span data-stu-id="fb2af-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





