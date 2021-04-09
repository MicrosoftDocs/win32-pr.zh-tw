---
title: 橋頭-傳輸-清單屬性
description: 此伺服器為其橋頭的傳輸。
ms.assetid: ef024170-eee2-458d-8cd2-637892644991
ms.tgt_platform: multiple
keywords:
- 橋頭-傳輸-列出屬性 AD 架構
- bridgeheadTransportList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Bridgehead-Transport-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 083c987f9ed40c23db4141d772c07ec73763d985
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687319"
---
# <a name="bridgehead-transport-list-attribute"></a><span data-ttu-id="d47fe-105">橋頭-傳輸-清單屬性</span><span class="sxs-lookup"><span data-stu-id="d47fe-105">Bridgehead-Transport-List attribute</span></span>

<span data-ttu-id="d47fe-106">此伺服器為其橋頭的傳輸。</span><span class="sxs-lookup"><span data-stu-id="d47fe-106">Transports for which this server is a bridgehead.</span></span>



| <span data-ttu-id="d47fe-107">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-107">Entry</span></span> | <span data-ttu-id="d47fe-108">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d47fe-109">CN</span><span class="sxs-lookup"><span data-stu-id="d47fe-109">CN</span></span>                | <span data-ttu-id="d47fe-110">橋頭-傳輸-清單</span><span class="sxs-lookup"><span data-stu-id="d47fe-110">Bridgehead-Transport-List</span></span>               |
| <span data-ttu-id="d47fe-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d47fe-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d47fe-112">bridgeheadTransportList</span><span class="sxs-lookup"><span data-stu-id="d47fe-112">bridgeheadTransportList</span></span>                 |
| <span data-ttu-id="d47fe-113">大小</span><span class="sxs-lookup"><span data-stu-id="d47fe-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d47fe-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="d47fe-114">Update Privilege</span></span>  | <span data-ttu-id="d47fe-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="d47fe-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="d47fe-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="d47fe-116">Update Frequency</span></span>  | <span data-ttu-id="d47fe-117">每次設定網站時。</span><span class="sxs-lookup"><span data-stu-id="d47fe-117">Whenever a site is setup.</span></span>               |
| <span data-ttu-id="d47fe-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-118">Attribute-Id</span></span>      | <span data-ttu-id="d47fe-119">1.2.840.113556.1.4.819</span><span class="sxs-lookup"><span data-stu-id="d47fe-119">1.2.840.113556.1.4.819</span></span>                  |
| <span data-ttu-id="d47fe-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="d47fe-120">System-Id-Guid</span></span>    | <span data-ttu-id="d47fe-121">d50c2cda-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="d47fe-121">d50c2cda-8951-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="d47fe-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="d47fe-122">Syntax</span></span>            | [<span data-ttu-id="d47fe-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d47fe-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d47fe-124">實作</span><span class="sxs-lookup"><span data-stu-id="d47fe-124">Implementations</span></span>

-   [<span data-ttu-id="d47fe-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d47fe-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d47fe-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d47fe-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d47fe-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="d47fe-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d47fe-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d47fe-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d47fe-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d47fe-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d47fe-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d47fe-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d47fe-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d47fe-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d47fe-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d47fe-132">Windows 2000 Server</span></span>



| <span data-ttu-id="d47fe-133">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-133">Entry</span></span> | <span data-ttu-id="d47fe-134">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-135">Link-Id</span></span>                | <span data-ttu-id="d47fe-136">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-136">98</span></span>                                    |
| <span data-ttu-id="d47fe-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-138">System-Only</span></span>            | <span data-ttu-id="d47fe-139">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-139">False</span></span>                                 |
| <span data-ttu-id="d47fe-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-140">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-141">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-141">False</span></span>                                 |
| <span data-ttu-id="d47fe-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-142">Is Indexed</span></span>             | <span data-ttu-id="d47fe-143">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-143">False</span></span>                                 |
| <span data-ttu-id="d47fe-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-144">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-145">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-145">False</span></span>                                 |
| <span data-ttu-id="d47fe-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-150">Search-Flags</span></span>           | <span data-ttu-id="d47fe-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-151">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-152">System-Flags</span></span>           | <span data-ttu-id="d47fe-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-153">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-154">Classes used in</span></span>        | [<span data-ttu-id="d47fe-155">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-155">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d47fe-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d47fe-156">Windows Server 2003</span></span>



| <span data-ttu-id="d47fe-157">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-157">Entry</span></span> | <span data-ttu-id="d47fe-158">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-159">Link-Id</span></span>                | <span data-ttu-id="d47fe-160">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-160">98</span></span>                                    |
| <span data-ttu-id="d47fe-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-162">System-Only</span></span>            | <span data-ttu-id="d47fe-163">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-163">False</span></span>                                 |
| <span data-ttu-id="d47fe-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-164">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-165">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-165">False</span></span>                                 |
| <span data-ttu-id="d47fe-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-166">Is Indexed</span></span>             | <span data-ttu-id="d47fe-167">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-167">False</span></span>                                 |
| <span data-ttu-id="d47fe-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-168">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-169">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-169">False</span></span>                                 |
| <span data-ttu-id="d47fe-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-174">Search-Flags</span></span>           | <span data-ttu-id="d47fe-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-175">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-176">System-Flags</span></span>           | <span data-ttu-id="d47fe-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-177">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-178">Classes used in</span></span>        | [<span data-ttu-id="d47fe-179">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d47fe-180">亞當</span><span class="sxs-lookup"><span data-stu-id="d47fe-180">ADAM</span></span>



| <span data-ttu-id="d47fe-181">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-181">Entry</span></span> | <span data-ttu-id="d47fe-182">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-183">Link-Id</span></span>                | <span data-ttu-id="d47fe-184">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-184">98</span></span>                                    |
| <span data-ttu-id="d47fe-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-186">System-Only</span></span>            | <span data-ttu-id="d47fe-187">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-187">False</span></span>                                 |
| <span data-ttu-id="d47fe-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-189">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-189">False</span></span>                                 |
| <span data-ttu-id="d47fe-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-190">Is Indexed</span></span>             | <span data-ttu-id="d47fe-191">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-191">False</span></span>                                 |
| <span data-ttu-id="d47fe-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-192">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-193">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-193">False</span></span>                                 |
| <span data-ttu-id="d47fe-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-198">Search-Flags</span></span>           | <span data-ttu-id="d47fe-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-199">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-200">System-Flags</span></span>           | <span data-ttu-id="d47fe-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-201">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-202">Classes used in</span></span>        | [<span data-ttu-id="d47fe-203">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-203">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d47fe-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d47fe-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d47fe-205">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-205">Entry</span></span> | <span data-ttu-id="d47fe-206">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-207">Link-Id</span></span>                | <span data-ttu-id="d47fe-208">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-208">98</span></span>                                    |
| <span data-ttu-id="d47fe-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-210">System-Only</span></span>            | <span data-ttu-id="d47fe-211">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-211">False</span></span>                                 |
| <span data-ttu-id="d47fe-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-212">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-213">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-213">False</span></span>                                 |
| <span data-ttu-id="d47fe-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-214">Is Indexed</span></span>             | <span data-ttu-id="d47fe-215">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-215">False</span></span>                                 |
| <span data-ttu-id="d47fe-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-216">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-217">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-217">False</span></span>                                 |
| <span data-ttu-id="d47fe-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-222">Search-Flags</span></span>           | <span data-ttu-id="d47fe-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-223">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-224">System-Flags</span></span>           | <span data-ttu-id="d47fe-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-225">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-226">Classes used in</span></span>        | [<span data-ttu-id="d47fe-227">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-227">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d47fe-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d47fe-228">Windows Server 2008</span></span>



| <span data-ttu-id="d47fe-229">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-229">Entry</span></span> | <span data-ttu-id="d47fe-230">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-231">Link-Id</span></span>                | <span data-ttu-id="d47fe-232">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-232">98</span></span>                                    |
| <span data-ttu-id="d47fe-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-234">System-Only</span></span>            | <span data-ttu-id="d47fe-235">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-235">False</span></span>                                 |
| <span data-ttu-id="d47fe-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-236">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-237">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-237">False</span></span>                                 |
| <span data-ttu-id="d47fe-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-238">Is Indexed</span></span>             | <span data-ttu-id="d47fe-239">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-239">False</span></span>                                 |
| <span data-ttu-id="d47fe-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-240">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-241">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-241">False</span></span>                                 |
| <span data-ttu-id="d47fe-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-246">Search-Flags</span></span>           | <span data-ttu-id="d47fe-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-247">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-248">System-Flags</span></span>           | <span data-ttu-id="d47fe-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-249">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-250">Classes used in</span></span>        | [<span data-ttu-id="d47fe-251">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-251">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d47fe-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d47fe-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d47fe-253">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-253">Entry</span></span> | <span data-ttu-id="d47fe-254">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-255">Link-Id</span></span>                | <span data-ttu-id="d47fe-256">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-256">98</span></span>                                    |
| <span data-ttu-id="d47fe-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-258">System-Only</span></span>            | <span data-ttu-id="d47fe-259">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-259">False</span></span>                                 |
| <span data-ttu-id="d47fe-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-260">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-261">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-261">False</span></span>                                 |
| <span data-ttu-id="d47fe-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-262">Is Indexed</span></span>             | <span data-ttu-id="d47fe-263">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-263">False</span></span>                                 |
| <span data-ttu-id="d47fe-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-264">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-265">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-265">False</span></span>                                 |
| <span data-ttu-id="d47fe-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-270">Search-Flags</span></span>           | <span data-ttu-id="d47fe-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-271">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-272">System-Flags</span></span>           | <span data-ttu-id="d47fe-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-273">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-274">Classes used in</span></span>        | [<span data-ttu-id="d47fe-275">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-275">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d47fe-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d47fe-276">Windows Server 2012</span></span>



| <span data-ttu-id="d47fe-277">進入</span><span class="sxs-lookup"><span data-stu-id="d47fe-277">Entry</span></span> | <span data-ttu-id="d47fe-278">值</span><span class="sxs-lookup"><span data-stu-id="d47fe-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="d47fe-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="d47fe-279">Link-Id</span></span>                | <span data-ttu-id="d47fe-280">98</span><span class="sxs-lookup"><span data-stu-id="d47fe-280">98</span></span>                                    |
| <span data-ttu-id="d47fe-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d47fe-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="d47fe-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="d47fe-282">System-Only</span></span>            | <span data-ttu-id="d47fe-283">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-283">False</span></span>                                 |
| <span data-ttu-id="d47fe-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="d47fe-284">Is-Single-Valued</span></span>       | <span data-ttu-id="d47fe-285">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-285">False</span></span>                                 |
| <span data-ttu-id="d47fe-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="d47fe-286">Is Indexed</span></span>             | <span data-ttu-id="d47fe-287">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-287">False</span></span>                                 |
| <span data-ttu-id="d47fe-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="d47fe-288">In Global Catalog</span></span>      | <span data-ttu-id="d47fe-289">否</span><span class="sxs-lookup"><span data-stu-id="d47fe-289">False</span></span>                                 |
| <span data-ttu-id="d47fe-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="d47fe-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="d47fe-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="d47fe-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="d47fe-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d47fe-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d47fe-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="d47fe-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-294">Search-Flags</span></span>           | <span data-ttu-id="d47fe-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d47fe-295">0x00000000</span></span>                            |
| <span data-ttu-id="d47fe-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d47fe-296">System-Flags</span></span>           | <span data-ttu-id="d47fe-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d47fe-297">0x00000010</span></span>                            |
| <span data-ttu-id="d47fe-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="d47fe-298">Classes used in</span></span>        | [<span data-ttu-id="d47fe-299">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="d47fe-299">**Server**</span></span>](c-server.md)<br/> |



 

 





