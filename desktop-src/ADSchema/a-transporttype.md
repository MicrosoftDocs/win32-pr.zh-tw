---
title: Transport-Type 屬性
description: 用來將網站連接在一起的傳輸類型的分辨名稱。 此值可指向 IP 或 SMTP 傳輸。
ms.assetid: aed18e69-3118-4cb8-b959-829106602f95
ms.tgt_platform: multiple
keywords:
- Transport-Type 屬性 AD 架構
- transportType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Transport-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28c68347deb83d52b78564688a563431609fb81
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844900"
---
# <a name="transport-type-attribute"></a><span data-ttu-id="205b0-106">Transport-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="205b0-106">Transport-Type attribute</span></span>

<span data-ttu-id="205b0-107">用來將網站連接在一起的傳輸類型的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="205b0-107">The distinguished name for a type of transport being used to connect sites together.</span></span> <span data-ttu-id="205b0-108">此值可指向 IP 或 SMTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="205b0-108">This value can point to an IP or SMTP transport.</span></span>



| <span data-ttu-id="205b0-109">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-109">Entry</span></span> | <span data-ttu-id="205b0-110">值</span><span class="sxs-lookup"><span data-stu-id="205b0-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="205b0-111">CN</span><span class="sxs-lookup"><span data-stu-id="205b0-111">CN</span></span>                | <span data-ttu-id="205b0-112">Transport-Type</span><span class="sxs-lookup"><span data-stu-id="205b0-112">Transport-Type</span></span>                          |
| <span data-ttu-id="205b0-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="205b0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="205b0-114">transportType</span><span class="sxs-lookup"><span data-stu-id="205b0-114">transportType</span></span>                           |
| <span data-ttu-id="205b0-115">大小</span><span class="sxs-lookup"><span data-stu-id="205b0-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="205b0-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="205b0-116">Update Privilege</span></span>  | <span data-ttu-id="205b0-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="205b0-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="205b0-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="205b0-118">Update Frequency</span></span>  | <span data-ttu-id="205b0-119">連接網站時。</span><span class="sxs-lookup"><span data-stu-id="205b0-119">When connecting sites.</span></span>                  |
| <span data-ttu-id="205b0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-120">Attribute-Id</span></span>      | <span data-ttu-id="205b0-121">1.2.840.113556.1.4.791</span><span class="sxs-lookup"><span data-stu-id="205b0-121">1.2.840.113556.1.4.791</span></span>                  |
| <span data-ttu-id="205b0-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="205b0-122">System-Id-Guid</span></span>    | <span data-ttu-id="205b0-123">26d97374-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="205b0-123">26d97374-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="205b0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="205b0-124">Syntax</span></span>            | [<span data-ttu-id="205b0-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="205b0-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="205b0-126">實作</span><span class="sxs-lookup"><span data-stu-id="205b0-126">Implementations</span></span>

-   [<span data-ttu-id="205b0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="205b0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="205b0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="205b0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="205b0-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="205b0-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="205b0-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="205b0-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="205b0-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="205b0-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="205b0-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="205b0-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="205b0-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="205b0-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="205b0-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="205b0-134">Windows 2000 Server</span></span>



| <span data-ttu-id="205b0-135">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-135">Entry</span></span> | <span data-ttu-id="205b0-136">值</span><span class="sxs-lookup"><span data-stu-id="205b0-136">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-137">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-138">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-139">System-Only</span></span>            | <span data-ttu-id="205b0-140">否</span><span class="sxs-lookup"><span data-stu-id="205b0-140">False</span></span>                                                  |
| <span data-ttu-id="205b0-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-141">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-142">對</span><span class="sxs-lookup"><span data-stu-id="205b0-142">True</span></span>                                                   |
| <span data-ttu-id="205b0-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-143">Is Indexed</span></span>             | <span data-ttu-id="205b0-144">否</span><span class="sxs-lookup"><span data-stu-id="205b0-144">False</span></span>                                                  |
| <span data-ttu-id="205b0-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-145">In Global Catalog</span></span>      | <span data-ttu-id="205b0-146">否</span><span class="sxs-lookup"><span data-stu-id="205b0-146">False</span></span>                                                  |
| <span data-ttu-id="205b0-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-148">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-149">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-150">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-151">Search-Flags</span></span>           | <span data-ttu-id="205b0-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-152">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-153">System-Flags</span></span>           | <span data-ttu-id="205b0-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-154">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-155">Classes used in</span></span>        | [<span data-ttu-id="205b0-156">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-156">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="205b0-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="205b0-157">Windows Server 2003</span></span>



| <span data-ttu-id="205b0-158">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-158">Entry</span></span> | <span data-ttu-id="205b0-159">值</span><span class="sxs-lookup"><span data-stu-id="205b0-159">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-160">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-161">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-162">System-Only</span></span>            | <span data-ttu-id="205b0-163">否</span><span class="sxs-lookup"><span data-stu-id="205b0-163">False</span></span>                                                  |
| <span data-ttu-id="205b0-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-164">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-165">對</span><span class="sxs-lookup"><span data-stu-id="205b0-165">True</span></span>                                                   |
| <span data-ttu-id="205b0-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-166">Is Indexed</span></span>             | <span data-ttu-id="205b0-167">否</span><span class="sxs-lookup"><span data-stu-id="205b0-167">False</span></span>                                                  |
| <span data-ttu-id="205b0-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-168">In Global Catalog</span></span>      | <span data-ttu-id="205b0-169">否</span><span class="sxs-lookup"><span data-stu-id="205b0-169">False</span></span>                                                  |
| <span data-ttu-id="205b0-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-171">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-172">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-173">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-174">Search-Flags</span></span>           | <span data-ttu-id="205b0-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-175">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-176">System-Flags</span></span>           | <span data-ttu-id="205b0-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-177">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-178">Classes used in</span></span>        | [<span data-ttu-id="205b0-179">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-179">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="205b0-180">亞當</span><span class="sxs-lookup"><span data-stu-id="205b0-180">ADAM</span></span>



| <span data-ttu-id="205b0-181">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-181">Entry</span></span> | <span data-ttu-id="205b0-182">值</span><span class="sxs-lookup"><span data-stu-id="205b0-182">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-183">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-184">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-185">System-Only</span></span>            | <span data-ttu-id="205b0-186">否</span><span class="sxs-lookup"><span data-stu-id="205b0-186">False</span></span>                                                  |
| <span data-ttu-id="205b0-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-188">對</span><span class="sxs-lookup"><span data-stu-id="205b0-188">True</span></span>                                                   |
| <span data-ttu-id="205b0-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-189">Is Indexed</span></span>             | <span data-ttu-id="205b0-190">否</span><span class="sxs-lookup"><span data-stu-id="205b0-190">False</span></span>                                                  |
| <span data-ttu-id="205b0-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-191">In Global Catalog</span></span>      | <span data-ttu-id="205b0-192">否</span><span class="sxs-lookup"><span data-stu-id="205b0-192">False</span></span>                                                  |
| <span data-ttu-id="205b0-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-194">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-195">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-196">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-197">Search-Flags</span></span>           | <span data-ttu-id="205b0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-198">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-199">System-Flags</span></span>           | <span data-ttu-id="205b0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-200">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-201">Classes used in</span></span>        | [<span data-ttu-id="205b0-202">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-202">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="205b0-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="205b0-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="205b0-204">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-204">Entry</span></span> | <span data-ttu-id="205b0-205">值</span><span class="sxs-lookup"><span data-stu-id="205b0-205">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-206">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-207">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-208">System-Only</span></span>            | <span data-ttu-id="205b0-209">否</span><span class="sxs-lookup"><span data-stu-id="205b0-209">False</span></span>                                                  |
| <span data-ttu-id="205b0-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-210">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-211">對</span><span class="sxs-lookup"><span data-stu-id="205b0-211">True</span></span>                                                   |
| <span data-ttu-id="205b0-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-212">Is Indexed</span></span>             | <span data-ttu-id="205b0-213">否</span><span class="sxs-lookup"><span data-stu-id="205b0-213">False</span></span>                                                  |
| <span data-ttu-id="205b0-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-214">In Global Catalog</span></span>      | <span data-ttu-id="205b0-215">否</span><span class="sxs-lookup"><span data-stu-id="205b0-215">False</span></span>                                                  |
| <span data-ttu-id="205b0-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-217">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-218">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-219">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-220">Search-Flags</span></span>           | <span data-ttu-id="205b0-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-221">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-222">System-Flags</span></span>           | <span data-ttu-id="205b0-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-223">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-224">Classes used in</span></span>        | [<span data-ttu-id="205b0-225">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-225">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="205b0-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="205b0-226">Windows Server 2008</span></span>



| <span data-ttu-id="205b0-227">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-227">Entry</span></span> | <span data-ttu-id="205b0-228">值</span><span class="sxs-lookup"><span data-stu-id="205b0-228">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-229">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-230">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-231">System-Only</span></span>            | <span data-ttu-id="205b0-232">否</span><span class="sxs-lookup"><span data-stu-id="205b0-232">False</span></span>                                                  |
| <span data-ttu-id="205b0-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-233">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-234">對</span><span class="sxs-lookup"><span data-stu-id="205b0-234">True</span></span>                                                   |
| <span data-ttu-id="205b0-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-235">Is Indexed</span></span>             | <span data-ttu-id="205b0-236">否</span><span class="sxs-lookup"><span data-stu-id="205b0-236">False</span></span>                                                  |
| <span data-ttu-id="205b0-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-237">In Global Catalog</span></span>      | <span data-ttu-id="205b0-238">否</span><span class="sxs-lookup"><span data-stu-id="205b0-238">False</span></span>                                                  |
| <span data-ttu-id="205b0-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-240">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-241">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-242">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-243">Search-Flags</span></span>           | <span data-ttu-id="205b0-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-244">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-245">System-Flags</span></span>           | <span data-ttu-id="205b0-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-246">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-247">Classes used in</span></span>        | [<span data-ttu-id="205b0-248">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-248">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="205b0-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="205b0-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="205b0-250">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-250">Entry</span></span> | <span data-ttu-id="205b0-251">值</span><span class="sxs-lookup"><span data-stu-id="205b0-251">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-252">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-253">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-254">System-Only</span></span>            | <span data-ttu-id="205b0-255">否</span><span class="sxs-lookup"><span data-stu-id="205b0-255">False</span></span>                                                  |
| <span data-ttu-id="205b0-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-256">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-257">對</span><span class="sxs-lookup"><span data-stu-id="205b0-257">True</span></span>                                                   |
| <span data-ttu-id="205b0-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-258">Is Indexed</span></span>             | <span data-ttu-id="205b0-259">否</span><span class="sxs-lookup"><span data-stu-id="205b0-259">False</span></span>                                                  |
| <span data-ttu-id="205b0-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-260">In Global Catalog</span></span>      | <span data-ttu-id="205b0-261">否</span><span class="sxs-lookup"><span data-stu-id="205b0-261">False</span></span>                                                  |
| <span data-ttu-id="205b0-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-263">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-264">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-265">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-266">Search-Flags</span></span>           | <span data-ttu-id="205b0-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-267">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-268">System-Flags</span></span>           | <span data-ttu-id="205b0-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-269">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-270">Classes used in</span></span>        | [<span data-ttu-id="205b0-271">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-271">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="205b0-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="205b0-272">Windows Server 2012</span></span>



| <span data-ttu-id="205b0-273">進入</span><span class="sxs-lookup"><span data-stu-id="205b0-273">Entry</span></span> | <span data-ttu-id="205b0-274">值</span><span class="sxs-lookup"><span data-stu-id="205b0-274">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="205b0-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="205b0-275">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="205b0-276">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="205b0-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="205b0-277">System-Only</span></span>            | <span data-ttu-id="205b0-278">否</span><span class="sxs-lookup"><span data-stu-id="205b0-278">False</span></span>                                                  |
| <span data-ttu-id="205b0-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="205b0-279">Is-Single-Valued</span></span>       | <span data-ttu-id="205b0-280">對</span><span class="sxs-lookup"><span data-stu-id="205b0-280">True</span></span>                                                   |
| <span data-ttu-id="205b0-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="205b0-281">Is Indexed</span></span>             | <span data-ttu-id="205b0-282">否</span><span class="sxs-lookup"><span data-stu-id="205b0-282">False</span></span>                                                  |
| <span data-ttu-id="205b0-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="205b0-283">In Global Catalog</span></span>      | <span data-ttu-id="205b0-284">否</span><span class="sxs-lookup"><span data-stu-id="205b0-284">False</span></span>                                                  |
| <span data-ttu-id="205b0-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="205b0-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="205b0-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="205b0-286">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="205b0-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="205b0-287">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="205b0-288">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="205b0-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-289">Search-Flags</span></span>           | <span data-ttu-id="205b0-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="205b0-290">0x00000000</span></span>                                             |
| <span data-ttu-id="205b0-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="205b0-291">System-Flags</span></span>           | <span data-ttu-id="205b0-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="205b0-292">0x00000010</span></span>                                             |
| <span data-ttu-id="205b0-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="205b0-293">Classes used in</span></span>        | [<span data-ttu-id="205b0-294">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="205b0-294">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





