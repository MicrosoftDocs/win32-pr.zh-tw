---
title: 專案-TTL 屬性
description: 此操作屬性是由伺服器維護，並且似乎出現在每個動態專案中。
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- 專案-TTL 屬性 AD 架構
- entryTTL 屬性 AD 架構
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467188"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="b343c-105">專案-TTL 屬性</span><span class="sxs-lookup"><span data-stu-id="b343c-105">Entry-TTL attribute</span></span>

<span data-ttu-id="b343c-106">此操作屬性是由伺服器維護，並且似乎出現在每個動態專案中。</span><span class="sxs-lookup"><span data-stu-id="b343c-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="b343c-107">當專案不包含 dynamicObject 物件類別時，屬性不會出現。</span><span class="sxs-lookup"><span data-stu-id="b343c-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="b343c-108">這個屬性的值是以秒為單位的時間，此專案會在從目錄中消失之前繼續存在。</span><span class="sxs-lookup"><span data-stu-id="b343c-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="b343c-109">如果沒有中間的「重新整理」作業，則在兩個連續搜尋中讀取屬性所傳回的值一定會 nonincreasing。</span><span class="sxs-lookup"><span data-stu-id="b343c-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="b343c-110">允許的最小值為0，表示專案可能會消失而不發出警告。</span><span class="sxs-lookup"><span data-stu-id="b343c-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="b343c-111">屬性標示為無使用者修改，因為它只能使用重新整理作業來變更。</span><span class="sxs-lookup"><span data-stu-id="b343c-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="b343c-112">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-112">Entry</span></span> | <span data-ttu-id="b343c-113">值</span><span class="sxs-lookup"><span data-stu-id="b343c-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b343c-114">CN</span><span class="sxs-lookup"><span data-stu-id="b343c-114">CN</span></span>                | <span data-ttu-id="b343c-115">專案-TTL</span><span class="sxs-lookup"><span data-stu-id="b343c-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="b343c-116">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b343c-116">Ldap-Display-Name</span></span> | <span data-ttu-id="b343c-117">entryTTL</span><span class="sxs-lookup"><span data-stu-id="b343c-117">entryTTL</span></span>                                    |
| <span data-ttu-id="b343c-118">大小</span><span class="sxs-lookup"><span data-stu-id="b343c-118">Size</span></span>              | <span data-ttu-id="b343c-119">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="b343c-119">4 bytes.</span></span> <span data-ttu-id="b343c-120">最大值 = 1 年，預設值 = 1 天。</span><span class="sxs-lookup"><span data-stu-id="b343c-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="b343c-121">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b343c-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b343c-122">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b343c-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b343c-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-123">Attribute-Id</span></span>      | <span data-ttu-id="b343c-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="b343c-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="b343c-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b343c-125">System-Id-Guid</span></span>    | <span data-ttu-id="b343c-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="b343c-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="b343c-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="b343c-127">Syntax</span></span>            | [<span data-ttu-id="b343c-128">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="b343c-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="b343c-129">實作</span><span class="sxs-lookup"><span data-stu-id="b343c-129">Implementations</span></span>

-   [<span data-ttu-id="b343c-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b343c-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b343c-131">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b343c-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b343c-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b343c-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b343c-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b343c-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b343c-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b343c-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b343c-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b343c-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="b343c-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b343c-136">Windows Server 2003</span></span>



| <span data-ttu-id="b343c-137">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-137">Entry</span></span> | <span data-ttu-id="b343c-138">值</span><span class="sxs-lookup"><span data-stu-id="b343c-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-141">System-Only</span></span>            | <span data-ttu-id="b343c-142">否</span><span class="sxs-lookup"><span data-stu-id="b343c-142">False</span></span>                                                |
| <span data-ttu-id="b343c-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-143">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-144">對</span><span class="sxs-lookup"><span data-stu-id="b343c-144">True</span></span>                                                 |
| <span data-ttu-id="b343c-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-145">Is Indexed</span></span>             | <span data-ttu-id="b343c-146">否</span><span class="sxs-lookup"><span data-stu-id="b343c-146">False</span></span>                                                |
| <span data-ttu-id="b343c-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-147">In Global Catalog</span></span>      | <span data-ttu-id="b343c-148">否</span><span class="sxs-lookup"><span data-stu-id="b343c-148">False</span></span>                                                |
| <span data-ttu-id="b343c-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-151">Range-Lower</span></span>            | <span data-ttu-id="b343c-152">0</span><span class="sxs-lookup"><span data-stu-id="b343c-152">0</span></span>                                                    |
| <span data-ttu-id="b343c-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-153">Range-Upper</span></span>            | <span data-ttu-id="b343c-154">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-154">31557600</span></span>                                             |
| <span data-ttu-id="b343c-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-155">Search-Flags</span></span>           | <span data-ttu-id="b343c-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-156">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-157">System-Flags</span></span>           | <span data-ttu-id="b343c-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-158">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-159">Classes used in</span></span>        | [<span data-ttu-id="b343c-160">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b343c-161">亞當</span><span class="sxs-lookup"><span data-stu-id="b343c-161">ADAM</span></span>



| <span data-ttu-id="b343c-162">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-162">Entry</span></span> | <span data-ttu-id="b343c-163">值</span><span class="sxs-lookup"><span data-stu-id="b343c-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-166">System-Only</span></span>            | <span data-ttu-id="b343c-167">否</span><span class="sxs-lookup"><span data-stu-id="b343c-167">False</span></span>                                                |
| <span data-ttu-id="b343c-168">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-168">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-169">對</span><span class="sxs-lookup"><span data-stu-id="b343c-169">True</span></span>                                                 |
| <span data-ttu-id="b343c-170">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-170">Is Indexed</span></span>             | <span data-ttu-id="b343c-171">否</span><span class="sxs-lookup"><span data-stu-id="b343c-171">False</span></span>                                                |
| <span data-ttu-id="b343c-172">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-172">In Global Catalog</span></span>      | <span data-ttu-id="b343c-173">否</span><span class="sxs-lookup"><span data-stu-id="b343c-173">False</span></span>                                                |
| <span data-ttu-id="b343c-174">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-175">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-176">Range-Lower</span></span>            | <span data-ttu-id="b343c-177">0</span><span class="sxs-lookup"><span data-stu-id="b343c-177">0</span></span>                                                    |
| <span data-ttu-id="b343c-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-178">Range-Upper</span></span>            | <span data-ttu-id="b343c-179">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-179">31557600</span></span>                                             |
| <span data-ttu-id="b343c-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-180">Search-Flags</span></span>           | <span data-ttu-id="b343c-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-181">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-182">System-Flags</span></span>           | <span data-ttu-id="b343c-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-183">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-184">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-184">Classes used in</span></span>        | [<span data-ttu-id="b343c-185">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b343c-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b343c-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b343c-187">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-187">Entry</span></span> | <span data-ttu-id="b343c-188">值</span><span class="sxs-lookup"><span data-stu-id="b343c-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-189">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-191">System-Only</span></span>            | <span data-ttu-id="b343c-192">否</span><span class="sxs-lookup"><span data-stu-id="b343c-192">False</span></span>                                                |
| <span data-ttu-id="b343c-193">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-193">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-194">對</span><span class="sxs-lookup"><span data-stu-id="b343c-194">True</span></span>                                                 |
| <span data-ttu-id="b343c-195">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-195">Is Indexed</span></span>             | <span data-ttu-id="b343c-196">否</span><span class="sxs-lookup"><span data-stu-id="b343c-196">False</span></span>                                                |
| <span data-ttu-id="b343c-197">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-197">In Global Catalog</span></span>      | <span data-ttu-id="b343c-198">否</span><span class="sxs-lookup"><span data-stu-id="b343c-198">False</span></span>                                                |
| <span data-ttu-id="b343c-199">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-200">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-201">Range-Lower</span></span>            | <span data-ttu-id="b343c-202">0</span><span class="sxs-lookup"><span data-stu-id="b343c-202">0</span></span>                                                    |
| <span data-ttu-id="b343c-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-203">Range-Upper</span></span>            | <span data-ttu-id="b343c-204">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-204">31557600</span></span>                                             |
| <span data-ttu-id="b343c-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-205">Search-Flags</span></span>           | <span data-ttu-id="b343c-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-206">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-207">System-Flags</span></span>           | <span data-ttu-id="b343c-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-208">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-209">Classes used in</span></span>        | [<span data-ttu-id="b343c-210">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b343c-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b343c-211">Windows Server 2008</span></span>



| <span data-ttu-id="b343c-212">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-212">Entry</span></span> | <span data-ttu-id="b343c-213">值</span><span class="sxs-lookup"><span data-stu-id="b343c-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-216">System-Only</span></span>            | <span data-ttu-id="b343c-217">否</span><span class="sxs-lookup"><span data-stu-id="b343c-217">False</span></span>                                                |
| <span data-ttu-id="b343c-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-218">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-219">對</span><span class="sxs-lookup"><span data-stu-id="b343c-219">True</span></span>                                                 |
| <span data-ttu-id="b343c-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-220">Is Indexed</span></span>             | <span data-ttu-id="b343c-221">否</span><span class="sxs-lookup"><span data-stu-id="b343c-221">False</span></span>                                                |
| <span data-ttu-id="b343c-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-222">In Global Catalog</span></span>      | <span data-ttu-id="b343c-223">否</span><span class="sxs-lookup"><span data-stu-id="b343c-223">False</span></span>                                                |
| <span data-ttu-id="b343c-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-226">Range-Lower</span></span>            | <span data-ttu-id="b343c-227">0</span><span class="sxs-lookup"><span data-stu-id="b343c-227">0</span></span>                                                    |
| <span data-ttu-id="b343c-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-228">Range-Upper</span></span>            | <span data-ttu-id="b343c-229">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-229">31557600</span></span>                                             |
| <span data-ttu-id="b343c-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-230">Search-Flags</span></span>           | <span data-ttu-id="b343c-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-231">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-232">System-Flags</span></span>           | <span data-ttu-id="b343c-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-233">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-234">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-234">Classes used in</span></span>        | [<span data-ttu-id="b343c-235">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b343c-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b343c-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b343c-237">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-237">Entry</span></span> | <span data-ttu-id="b343c-238">值</span><span class="sxs-lookup"><span data-stu-id="b343c-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-239">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-241">System-Only</span></span>            | <span data-ttu-id="b343c-242">否</span><span class="sxs-lookup"><span data-stu-id="b343c-242">False</span></span>                                                |
| <span data-ttu-id="b343c-243">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-243">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-244">對</span><span class="sxs-lookup"><span data-stu-id="b343c-244">True</span></span>                                                 |
| <span data-ttu-id="b343c-245">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-245">Is Indexed</span></span>             | <span data-ttu-id="b343c-246">否</span><span class="sxs-lookup"><span data-stu-id="b343c-246">False</span></span>                                                |
| <span data-ttu-id="b343c-247">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-247">In Global Catalog</span></span>      | <span data-ttu-id="b343c-248">否</span><span class="sxs-lookup"><span data-stu-id="b343c-248">False</span></span>                                                |
| <span data-ttu-id="b343c-249">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-250">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-251">Range-Lower</span></span>            | <span data-ttu-id="b343c-252">0</span><span class="sxs-lookup"><span data-stu-id="b343c-252">0</span></span>                                                    |
| <span data-ttu-id="b343c-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-253">Range-Upper</span></span>            | <span data-ttu-id="b343c-254">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-254">31557600</span></span>                                             |
| <span data-ttu-id="b343c-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-255">Search-Flags</span></span>           | <span data-ttu-id="b343c-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-256">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-257">System-Flags</span></span>           | <span data-ttu-id="b343c-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-258">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-259">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-259">Classes used in</span></span>        | [<span data-ttu-id="b343c-260">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b343c-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b343c-261">Windows Server 2012</span></span>



| <span data-ttu-id="b343c-262">進入</span><span class="sxs-lookup"><span data-stu-id="b343c-262">Entry</span></span> | <span data-ttu-id="b343c-263">值</span><span class="sxs-lookup"><span data-stu-id="b343c-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="b343c-264">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b343c-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b343c-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="b343c-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="b343c-266">System-Only</span></span>            | <span data-ttu-id="b343c-267">否</span><span class="sxs-lookup"><span data-stu-id="b343c-267">False</span></span>                                                |
| <span data-ttu-id="b343c-268">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b343c-268">Is-Single-Valued</span></span>       | <span data-ttu-id="b343c-269">對</span><span class="sxs-lookup"><span data-stu-id="b343c-269">True</span></span>                                                 |
| <span data-ttu-id="b343c-270">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b343c-270">Is Indexed</span></span>             | <span data-ttu-id="b343c-271">否</span><span class="sxs-lookup"><span data-stu-id="b343c-271">False</span></span>                                                |
| <span data-ttu-id="b343c-272">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b343c-272">In Global Catalog</span></span>      | <span data-ttu-id="b343c-273">否</span><span class="sxs-lookup"><span data-stu-id="b343c-273">False</span></span>                                                |
| <span data-ttu-id="b343c-274">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b343c-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="b343c-275">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b343c-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="b343c-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b343c-276">Range-Lower</span></span>            | <span data-ttu-id="b343c-277">0</span><span class="sxs-lookup"><span data-stu-id="b343c-277">0</span></span>                                                    |
| <span data-ttu-id="b343c-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b343c-278">Range-Upper</span></span>            | <span data-ttu-id="b343c-279">31557600</span><span class="sxs-lookup"><span data-stu-id="b343c-279">31557600</span></span>                                             |
| <span data-ttu-id="b343c-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-280">Search-Flags</span></span>           | <span data-ttu-id="b343c-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b343c-281">0x00000000</span></span>                                           |
| <span data-ttu-id="b343c-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b343c-282">System-Flags</span></span>           | <span data-ttu-id="b343c-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="b343c-283">0x00000014</span></span>                                           |
| <span data-ttu-id="b343c-284">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b343c-284">Classes used in</span></span>        | [<span data-ttu-id="b343c-285">**動態物件**</span><span class="sxs-lookup"><span data-stu-id="b343c-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





