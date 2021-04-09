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
# <a name="bridgehead-transport-list-attribute"></a><span data-ttu-id="7aedf-105">橋頭-傳輸-清單屬性</span><span class="sxs-lookup"><span data-stu-id="7aedf-105">Bridgehead-Transport-List attribute</span></span>

<span data-ttu-id="7aedf-106">此伺服器為其橋頭的傳輸。</span><span class="sxs-lookup"><span data-stu-id="7aedf-106">Transports for which this server is a bridgehead.</span></span>



| <span data-ttu-id="7aedf-107">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-107">Entry</span></span> | <span data-ttu-id="7aedf-108">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7aedf-109">CN</span><span class="sxs-lookup"><span data-stu-id="7aedf-109">CN</span></span>                | <span data-ttu-id="7aedf-110">橋頭-傳輸-清單</span><span class="sxs-lookup"><span data-stu-id="7aedf-110">Bridgehead-Transport-List</span></span>               |
| <span data-ttu-id="7aedf-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7aedf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7aedf-112">bridgeheadTransportList</span><span class="sxs-lookup"><span data-stu-id="7aedf-112">bridgeheadTransportList</span></span>                 |
| <span data-ttu-id="7aedf-113">大小</span><span class="sxs-lookup"><span data-stu-id="7aedf-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7aedf-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7aedf-114">Update Privilege</span></span>  | <span data-ttu-id="7aedf-115">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="7aedf-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="7aedf-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7aedf-116">Update Frequency</span></span>  | <span data-ttu-id="7aedf-117">每次設定網站時。</span><span class="sxs-lookup"><span data-stu-id="7aedf-117">Whenever a site is setup.</span></span>               |
| <span data-ttu-id="7aedf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-118">Attribute-Id</span></span>      | <span data-ttu-id="7aedf-119">1.2.840.113556.1.4.819</span><span class="sxs-lookup"><span data-stu-id="7aedf-119">1.2.840.113556.1.4.819</span></span>                  |
| <span data-ttu-id="7aedf-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7aedf-120">System-Id-Guid</span></span>    | <span data-ttu-id="7aedf-121">d50c2cda-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="7aedf-121">d50c2cda-8951-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="7aedf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aedf-122">Syntax</span></span>            | [<span data-ttu-id="7aedf-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7aedf-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7aedf-124">實作</span><span class="sxs-lookup"><span data-stu-id="7aedf-124">Implementations</span></span>

-   [<span data-ttu-id="7aedf-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7aedf-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7aedf-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7aedf-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7aedf-127">**亞當**</span><span class="sxs-lookup"><span data-stu-id="7aedf-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7aedf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7aedf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7aedf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7aedf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7aedf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7aedf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7aedf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7aedf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7aedf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7aedf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="7aedf-133">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-133">Entry</span></span> | <span data-ttu-id="7aedf-134">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-134">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-135">Link-Id</span></span>                | <span data-ttu-id="7aedf-136">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-136">98</span></span>                                    |
| <span data-ttu-id="7aedf-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-137">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-138">System-Only</span></span>            | <span data-ttu-id="7aedf-139">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-139">False</span></span>                                 |
| <span data-ttu-id="7aedf-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-140">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-141">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-141">False</span></span>                                 |
| <span data-ttu-id="7aedf-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-142">Is Indexed</span></span>             | <span data-ttu-id="7aedf-143">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-143">False</span></span>                                 |
| <span data-ttu-id="7aedf-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-144">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-145">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-145">False</span></span>                                 |
| <span data-ttu-id="7aedf-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-147">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-148">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-149">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-150">Search-Flags</span></span>           | <span data-ttu-id="7aedf-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-151">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-152">System-Flags</span></span>           | <span data-ttu-id="7aedf-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-153">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-154">Classes used in</span></span>        | [<span data-ttu-id="7aedf-155">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-155">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7aedf-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7aedf-156">Windows Server 2003</span></span>



| <span data-ttu-id="7aedf-157">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-157">Entry</span></span> | <span data-ttu-id="7aedf-158">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-158">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-159">Link-Id</span></span>                | <span data-ttu-id="7aedf-160">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-160">98</span></span>                                    |
| <span data-ttu-id="7aedf-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-162">System-Only</span></span>            | <span data-ttu-id="7aedf-163">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-163">False</span></span>                                 |
| <span data-ttu-id="7aedf-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-165">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-165">False</span></span>                                 |
| <span data-ttu-id="7aedf-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-166">Is Indexed</span></span>             | <span data-ttu-id="7aedf-167">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-167">False</span></span>                                 |
| <span data-ttu-id="7aedf-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-168">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-169">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-169">False</span></span>                                 |
| <span data-ttu-id="7aedf-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-174">Search-Flags</span></span>           | <span data-ttu-id="7aedf-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-175">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-176">System-Flags</span></span>           | <span data-ttu-id="7aedf-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-177">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-178">Classes used in</span></span>        | [<span data-ttu-id="7aedf-179">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7aedf-180">亞當</span><span class="sxs-lookup"><span data-stu-id="7aedf-180">ADAM</span></span>



| <span data-ttu-id="7aedf-181">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-181">Entry</span></span> | <span data-ttu-id="7aedf-182">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-183">Link-Id</span></span>                | <span data-ttu-id="7aedf-184">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-184">98</span></span>                                    |
| <span data-ttu-id="7aedf-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-185">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-186">System-Only</span></span>            | <span data-ttu-id="7aedf-187">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-187">False</span></span>                                 |
| <span data-ttu-id="7aedf-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-188">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-189">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-189">False</span></span>                                 |
| <span data-ttu-id="7aedf-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-190">Is Indexed</span></span>             | <span data-ttu-id="7aedf-191">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-191">False</span></span>                                 |
| <span data-ttu-id="7aedf-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-192">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-193">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-193">False</span></span>                                 |
| <span data-ttu-id="7aedf-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-195">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-196">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-197">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-198">Search-Flags</span></span>           | <span data-ttu-id="7aedf-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-199">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-200">System-Flags</span></span>           | <span data-ttu-id="7aedf-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-201">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-202">Classes used in</span></span>        | [<span data-ttu-id="7aedf-203">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-203">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7aedf-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7aedf-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7aedf-205">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-205">Entry</span></span> | <span data-ttu-id="7aedf-206">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-206">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-207">Link-Id</span></span>                | <span data-ttu-id="7aedf-208">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-208">98</span></span>                                    |
| <span data-ttu-id="7aedf-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-209">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-210">System-Only</span></span>            | <span data-ttu-id="7aedf-211">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-211">False</span></span>                                 |
| <span data-ttu-id="7aedf-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-212">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-213">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-213">False</span></span>                                 |
| <span data-ttu-id="7aedf-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-214">Is Indexed</span></span>             | <span data-ttu-id="7aedf-215">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-215">False</span></span>                                 |
| <span data-ttu-id="7aedf-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-216">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-217">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-217">False</span></span>                                 |
| <span data-ttu-id="7aedf-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-219">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-220">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-221">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-222">Search-Flags</span></span>           | <span data-ttu-id="7aedf-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-223">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-224">System-Flags</span></span>           | <span data-ttu-id="7aedf-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-225">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-226">Classes used in</span></span>        | [<span data-ttu-id="7aedf-227">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-227">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7aedf-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aedf-228">Windows Server 2008</span></span>



| <span data-ttu-id="7aedf-229">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-229">Entry</span></span> | <span data-ttu-id="7aedf-230">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-230">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-231">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-231">Link-Id</span></span>                | <span data-ttu-id="7aedf-232">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-232">98</span></span>                                    |
| <span data-ttu-id="7aedf-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-233">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-234">System-Only</span></span>            | <span data-ttu-id="7aedf-235">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-235">False</span></span>                                 |
| <span data-ttu-id="7aedf-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-236">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-237">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-237">False</span></span>                                 |
| <span data-ttu-id="7aedf-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-238">Is Indexed</span></span>             | <span data-ttu-id="7aedf-239">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-239">False</span></span>                                 |
| <span data-ttu-id="7aedf-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-240">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-241">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-241">False</span></span>                                 |
| <span data-ttu-id="7aedf-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-243">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-244">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-245">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-246">Search-Flags</span></span>           | <span data-ttu-id="7aedf-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-247">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-248">System-Flags</span></span>           | <span data-ttu-id="7aedf-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-249">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-250">Classes used in</span></span>        | [<span data-ttu-id="7aedf-251">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-251">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7aedf-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7aedf-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7aedf-253">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-253">Entry</span></span> | <span data-ttu-id="7aedf-254">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-254">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-255">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-255">Link-Id</span></span>                | <span data-ttu-id="7aedf-256">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-256">98</span></span>                                    |
| <span data-ttu-id="7aedf-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-257">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-258">System-Only</span></span>            | <span data-ttu-id="7aedf-259">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-259">False</span></span>                                 |
| <span data-ttu-id="7aedf-260">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-260">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-261">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-261">False</span></span>                                 |
| <span data-ttu-id="7aedf-262">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-262">Is Indexed</span></span>             | <span data-ttu-id="7aedf-263">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-263">False</span></span>                                 |
| <span data-ttu-id="7aedf-264">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-264">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-265">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-265">False</span></span>                                 |
| <span data-ttu-id="7aedf-266">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-267">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-267">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-268">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-269">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-270">Search-Flags</span></span>           | <span data-ttu-id="7aedf-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-271">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-272">System-Flags</span></span>           | <span data-ttu-id="7aedf-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-273">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-274">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-274">Classes used in</span></span>        | [<span data-ttu-id="7aedf-275">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-275">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7aedf-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7aedf-276">Windows Server 2012</span></span>



| <span data-ttu-id="7aedf-277">進入</span><span class="sxs-lookup"><span data-stu-id="7aedf-277">Entry</span></span> | <span data-ttu-id="7aedf-278">值</span><span class="sxs-lookup"><span data-stu-id="7aedf-278">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="7aedf-279">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7aedf-279">Link-Id</span></span>                | <span data-ttu-id="7aedf-280">98</span><span class="sxs-lookup"><span data-stu-id="7aedf-280">98</span></span>                                    |
| <span data-ttu-id="7aedf-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7aedf-281">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="7aedf-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="7aedf-282">System-Only</span></span>            | <span data-ttu-id="7aedf-283">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-283">False</span></span>                                 |
| <span data-ttu-id="7aedf-284">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7aedf-284">Is-Single-Valued</span></span>       | <span data-ttu-id="7aedf-285">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-285">False</span></span>                                 |
| <span data-ttu-id="7aedf-286">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7aedf-286">Is Indexed</span></span>             | <span data-ttu-id="7aedf-287">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-287">False</span></span>                                 |
| <span data-ttu-id="7aedf-288">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7aedf-288">In Global Catalog</span></span>      | <span data-ttu-id="7aedf-289">否</span><span class="sxs-lookup"><span data-stu-id="7aedf-289">False</span></span>                                 |
| <span data-ttu-id="7aedf-290">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7aedf-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="7aedf-291">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7aedf-291">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="7aedf-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7aedf-292">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7aedf-293">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="7aedf-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-294">Search-Flags</span></span>           | <span data-ttu-id="7aedf-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7aedf-295">0x00000000</span></span>                            |
| <span data-ttu-id="7aedf-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7aedf-296">System-Flags</span></span>           | <span data-ttu-id="7aedf-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7aedf-297">0x00000010</span></span>                            |
| <span data-ttu-id="7aedf-298">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7aedf-298">Classes used in</span></span>        | [<span data-ttu-id="7aedf-299">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="7aedf-299">**Server**</span></span>](c-server.md)<br/> |



 

 





