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
# <a name="transport-type-attribute"></a><span data-ttu-id="6dbb3-106">Transport-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="6dbb3-106">Transport-Type attribute</span></span>

<span data-ttu-id="6dbb3-107">用來將網站連接在一起的傳輸類型的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="6dbb3-107">The distinguished name for a type of transport being used to connect sites together.</span></span> <span data-ttu-id="6dbb3-108">此值可指向 IP 或 SMTP 傳輸。</span><span class="sxs-lookup"><span data-stu-id="6dbb3-108">This value can point to an IP or SMTP transport.</span></span>



| <span data-ttu-id="6dbb3-109">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-109">Entry</span></span> | <span data-ttu-id="6dbb3-110">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6dbb3-111">CN</span><span class="sxs-lookup"><span data-stu-id="6dbb3-111">CN</span></span>                | <span data-ttu-id="6dbb3-112">Transport-Type</span><span class="sxs-lookup"><span data-stu-id="6dbb3-112">Transport-Type</span></span>                          |
| <span data-ttu-id="6dbb3-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="6dbb3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6dbb3-114">transportType</span><span class="sxs-lookup"><span data-stu-id="6dbb3-114">transportType</span></span>                           |
| <span data-ttu-id="6dbb3-115">大小</span><span class="sxs-lookup"><span data-stu-id="6dbb3-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="6dbb3-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="6dbb3-116">Update Privilege</span></span>  | <span data-ttu-id="6dbb3-117">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="6dbb3-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="6dbb3-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="6dbb3-118">Update Frequency</span></span>  | <span data-ttu-id="6dbb3-119">連接網站時。</span><span class="sxs-lookup"><span data-stu-id="6dbb3-119">When connecting sites.</span></span>                  |
| <span data-ttu-id="6dbb3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-120">Attribute-Id</span></span>      | <span data-ttu-id="6dbb3-121">1.2.840.113556.1.4.791</span><span class="sxs-lookup"><span data-stu-id="6dbb3-121">1.2.840.113556.1.4.791</span></span>                  |
| <span data-ttu-id="6dbb3-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="6dbb3-122">System-Id-Guid</span></span>    | <span data-ttu-id="6dbb3-123">26d97374-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6dbb3-123">26d97374-6070-11d1-a9c6-0000f80367c1</span></span>    |
| <span data-ttu-id="6dbb3-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dbb3-124">Syntax</span></span>            | [<span data-ttu-id="6dbb3-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6dbb3-126">實作</span><span class="sxs-lookup"><span data-stu-id="6dbb3-126">Implementations</span></span>

-   [<span data-ttu-id="6dbb3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6dbb3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6dbb3-129">**亞當**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6dbb3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6dbb3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6dbb3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6dbb3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6dbb3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6dbb3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6dbb3-135">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-135">Entry</span></span> | <span data-ttu-id="6dbb3-136">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-136">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-137">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-138">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-139">System-Only</span></span>            | <span data-ttu-id="6dbb3-140">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-140">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-142">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-142">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-143">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-144">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-144">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-145">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-146">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-146">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-148">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-149">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-150">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-151">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-152">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-153">System-Flags</span></span>           | <span data-ttu-id="6dbb3-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-154">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-155">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-156">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-156">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6dbb3-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dbb3-157">Windows Server 2003</span></span>



| <span data-ttu-id="6dbb3-158">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-158">Entry</span></span> | <span data-ttu-id="6dbb3-159">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-159">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-160">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-161">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-162">System-Only</span></span>            | <span data-ttu-id="6dbb3-163">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-163">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-165">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-165">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-166">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-167">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-167">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-168">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-169">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-169">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-171">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-172">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-173">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-174">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-175">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-176">System-Flags</span></span>           | <span data-ttu-id="6dbb3-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-177">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-178">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-179">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-179">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6dbb3-180">亞當</span><span class="sxs-lookup"><span data-stu-id="6dbb3-180">ADAM</span></span>



| <span data-ttu-id="6dbb3-181">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-181">Entry</span></span> | <span data-ttu-id="6dbb3-182">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-182">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-183">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-184">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-185">System-Only</span></span>            | <span data-ttu-id="6dbb3-186">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-186">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-188">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-188">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-189">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-190">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-190">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-191">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-192">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-192">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-194">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-195">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-196">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-197">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-198">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-199">System-Flags</span></span>           | <span data-ttu-id="6dbb3-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-200">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-201">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-202">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-202">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6dbb3-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6dbb3-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6dbb3-204">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-204">Entry</span></span> | <span data-ttu-id="6dbb3-205">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-205">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-206">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-207">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-208">System-Only</span></span>            | <span data-ttu-id="6dbb3-209">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-209">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-211">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-211">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-212">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-213">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-213">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-214">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-215">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-215">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-217">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-218">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-219">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-220">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-221">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-222">System-Flags</span></span>           | <span data-ttu-id="6dbb3-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-223">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-224">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-225">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-225">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6dbb3-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6dbb3-226">Windows Server 2008</span></span>



| <span data-ttu-id="6dbb3-227">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-227">Entry</span></span> | <span data-ttu-id="6dbb3-228">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-228">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-229">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-230">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-231">System-Only</span></span>            | <span data-ttu-id="6dbb3-232">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-232">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-234">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-234">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-235">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-236">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-236">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-237">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-238">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-238">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-240">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-241">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-242">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-243">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-244">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-245">System-Flags</span></span>           | <span data-ttu-id="6dbb3-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-246">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-247">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-248">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-248">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6dbb3-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6dbb3-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6dbb3-250">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-250">Entry</span></span> | <span data-ttu-id="6dbb3-251">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-251">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-252">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-253">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-254">System-Only</span></span>            | <span data-ttu-id="6dbb3-255">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-255">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-257">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-257">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-258">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-259">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-259">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-260">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-261">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-261">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-263">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-264">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-265">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-266">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-267">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-268">System-Flags</span></span>           | <span data-ttu-id="6dbb3-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-269">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-270">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-271">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-271">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6dbb3-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6dbb3-272">Windows Server 2012</span></span>



| <span data-ttu-id="6dbb3-273">進入</span><span class="sxs-lookup"><span data-stu-id="6dbb3-273">Entry</span></span> | <span data-ttu-id="6dbb3-274">值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-274">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="6dbb3-275">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="6dbb3-275">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6dbb3-276">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="6dbb3-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="6dbb3-277">System-Only</span></span>            | <span data-ttu-id="6dbb3-278">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-278">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-279">是-單一值</span><span class="sxs-lookup"><span data-stu-id="6dbb3-279">Is-Single-Valued</span></span>       | <span data-ttu-id="6dbb3-280">對</span><span class="sxs-lookup"><span data-stu-id="6dbb3-280">True</span></span>                                                   |
| <span data-ttu-id="6dbb3-281">已編制索引</span><span class="sxs-lookup"><span data-stu-id="6dbb3-281">Is Indexed</span></span>             | <span data-ttu-id="6dbb3-282">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-282">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-283">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="6dbb3-283">In Global Catalog</span></span>      | <span data-ttu-id="6dbb3-284">否</span><span class="sxs-lookup"><span data-stu-id="6dbb3-284">False</span></span>                                                  |
| <span data-ttu-id="6dbb3-285">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="6dbb3-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="6dbb3-286">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="6dbb3-286">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="6dbb3-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6dbb3-287">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6dbb3-288">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="6dbb3-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-289">Search-Flags</span></span>           | <span data-ttu-id="6dbb3-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6dbb3-290">0x00000000</span></span>                                             |
| <span data-ttu-id="6dbb3-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6dbb3-291">System-Flags</span></span>           | <span data-ttu-id="6dbb3-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6dbb3-292">0x00000010</span></span>                                             |
| <span data-ttu-id="6dbb3-293">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="6dbb3-293">Classes used in</span></span>        | [<span data-ttu-id="6dbb3-294">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="6dbb3-294">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





