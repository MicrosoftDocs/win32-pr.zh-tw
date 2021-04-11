---
title: MS-DS-複寫-NC-Reason 屬性
description: NtdsConnection 物件的屬性，指出 (或) KCC 顯示連接在複寫拓撲中是否有用。 是多重值，而且具有 DistName + 二進位語法，其中二進位部分是 int 大小的位。
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-複寫-NC-原因屬性 AD 架構
- ReplicatesNCReason 屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385338"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a><span data-ttu-id="10e41-106">MS-DS-複寫-NC-Reason 屬性</span><span class="sxs-lookup"><span data-stu-id="10e41-106">MS-DS-Replicates-NC-Reason attribute</span></span>

<span data-ttu-id="10e41-107">NtdsConnection 物件的屬性，指出 (或) KCC 顯示連接在複寫拓撲中是否有用。</span><span class="sxs-lookup"><span data-stu-id="10e41-107">Attribute of ntdsConnection object that indicates why (or whether) the KCC shows the connection is useful in the replication topology.</span></span> <span data-ttu-id="10e41-108">是多重值，而且具有 DistName + 二進位語法，其中二進位部分是 int 大小的位。</span><span class="sxs-lookup"><span data-stu-id="10e41-108">Is multiple-valued and has DistName+Binary syntax, where the binary part is an int-size bitfield.</span></span>



| <span data-ttu-id="10e41-109">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-109">Entry</span></span> | <span data-ttu-id="10e41-110">值</span><span class="sxs-lookup"><span data-stu-id="10e41-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e41-111">CN</span><span class="sxs-lookup"><span data-stu-id="10e41-111">CN</span></span>                | <span data-ttu-id="10e41-112">MS-DS-複寫-NC-原因</span><span class="sxs-lookup"><span data-stu-id="10e41-112">MS-DS-Replicates-NC-Reason</span></span>                                                                                                                 |
| <span data-ttu-id="10e41-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="10e41-113">Ldap-Display-Name</span></span> | <span data-ttu-id="10e41-114">ReplicatesNCReason</span><span class="sxs-lookup"><span data-stu-id="10e41-114">mS-DS-ReplicatesNCReason</span></span>                                                                                                                   |
| <span data-ttu-id="10e41-115">大小</span><span class="sxs-lookup"><span data-stu-id="10e41-115">Size</span></span>              | <span data-ttu-id="10e41-116">二進位部分的值： 0 = 否 \_ 原因，1 = GC \_ 拓撲，2 = 環形 \_ 拓撲，4 = 將 \_ 躍點拓撲降至最低 \_ ，8 = 過時 \_ 伺服器 \_ 拓撲。</span><span class="sxs-lookup"><span data-stu-id="10e41-116">Value for binary portion: 0 = NO\_REASON,1 = GC\_TOPOLOGY, 2 = RING\_TOPOLOGY, 4 = MINIMIZE\_HOPS\_TOPOLOGY, 8 = STALE\_SERVERS\_TOPOLOGY.</span></span> |
| <span data-ttu-id="10e41-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="10e41-117">Update Privilege</span></span>  | <span data-ttu-id="10e41-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="10e41-118">This value is set by the system.</span></span>                                                                                                           |
| <span data-ttu-id="10e41-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="10e41-119">Update Frequency</span></span>  | <span data-ttu-id="10e41-120">可以變更以回應網路拓撲中的變更。</span><span class="sxs-lookup"><span data-stu-id="10e41-120">Can change in response to changes in the network topology.</span></span>                                                                                 |
| <span data-ttu-id="10e41-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-121">Attribute-Id</span></span>      | <span data-ttu-id="10e41-122">1.2.840.113556.1.4.1408</span><span class="sxs-lookup"><span data-stu-id="10e41-122">1.2.840.113556.1.4.1408</span></span>                                                                                                                    |
| <span data-ttu-id="10e41-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="10e41-123">System-Id-Guid</span></span>    | <span data-ttu-id="10e41-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="10e41-124">0ea12b84-08b3-11d3-91bc-0000f87a57d4</span></span>                                                                                                       |
| <span data-ttu-id="10e41-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="10e41-125">Syntax</span></span>            | [<span data-ttu-id="10e41-126">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="10e41-126">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                            |



## <a name="implementations"></a><span data-ttu-id="10e41-127">實作</span><span class="sxs-lookup"><span data-stu-id="10e41-127">Implementations</span></span>

-   [<span data-ttu-id="10e41-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="10e41-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="10e41-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="10e41-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="10e41-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="10e41-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="10e41-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="10e41-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="10e41-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="10e41-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="10e41-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="10e41-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="10e41-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="10e41-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="10e41-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="10e41-135">Windows 2000 Server</span></span>



| <span data-ttu-id="10e41-136">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-136">Entry</span></span> | <span data-ttu-id="10e41-137">值</span><span class="sxs-lookup"><span data-stu-id="10e41-137">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-138">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-139">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-140">System-Only</span></span>            | <span data-ttu-id="10e41-141">否</span><span class="sxs-lookup"><span data-stu-id="10e41-141">False</span></span>                                                  |
| <span data-ttu-id="10e41-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-142">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-143">否</span><span class="sxs-lookup"><span data-stu-id="10e41-143">False</span></span>                                                  |
| <span data-ttu-id="10e41-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-144">Is Indexed</span></span>             | <span data-ttu-id="10e41-145">否</span><span class="sxs-lookup"><span data-stu-id="10e41-145">False</span></span>                                                  |
| <span data-ttu-id="10e41-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-146">In Global Catalog</span></span>      | <span data-ttu-id="10e41-147">否</span><span class="sxs-lookup"><span data-stu-id="10e41-147">False</span></span>                                                  |
| <span data-ttu-id="10e41-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-149">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-150">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-151">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-152">Search-Flags</span></span>           | <span data-ttu-id="10e41-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-153">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-154">System-Flags</span></span>           | <span data-ttu-id="10e41-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-155">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-156">Classes used in</span></span>        | [<span data-ttu-id="10e41-157">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-157">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="10e41-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="10e41-158">Windows Server 2003</span></span>



| <span data-ttu-id="10e41-159">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-159">Entry</span></span> | <span data-ttu-id="10e41-160">值</span><span class="sxs-lookup"><span data-stu-id="10e41-160">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-161">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-162">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-163">System-Only</span></span>            | <span data-ttu-id="10e41-164">否</span><span class="sxs-lookup"><span data-stu-id="10e41-164">False</span></span>                                                  |
| <span data-ttu-id="10e41-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-165">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-166">否</span><span class="sxs-lookup"><span data-stu-id="10e41-166">False</span></span>                                                  |
| <span data-ttu-id="10e41-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-167">Is Indexed</span></span>             | <span data-ttu-id="10e41-168">否</span><span class="sxs-lookup"><span data-stu-id="10e41-168">False</span></span>                                                  |
| <span data-ttu-id="10e41-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-169">In Global Catalog</span></span>      | <span data-ttu-id="10e41-170">否</span><span class="sxs-lookup"><span data-stu-id="10e41-170">False</span></span>                                                  |
| <span data-ttu-id="10e41-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-172">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-173">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-174">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-175">Search-Flags</span></span>           | <span data-ttu-id="10e41-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-176">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-177">System-Flags</span></span>           | <span data-ttu-id="10e41-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-178">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-179">Classes used in</span></span>        | [<span data-ttu-id="10e41-180">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-180">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="10e41-181">亞當</span><span class="sxs-lookup"><span data-stu-id="10e41-181">ADAM</span></span>



| <span data-ttu-id="10e41-182">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-182">Entry</span></span> | <span data-ttu-id="10e41-183">值</span><span class="sxs-lookup"><span data-stu-id="10e41-183">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-184">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-185">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-186">System-Only</span></span>            | <span data-ttu-id="10e41-187">否</span><span class="sxs-lookup"><span data-stu-id="10e41-187">False</span></span>                                                  |
| <span data-ttu-id="10e41-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-188">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-189">否</span><span class="sxs-lookup"><span data-stu-id="10e41-189">False</span></span>                                                  |
| <span data-ttu-id="10e41-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-190">Is Indexed</span></span>             | <span data-ttu-id="10e41-191">否</span><span class="sxs-lookup"><span data-stu-id="10e41-191">False</span></span>                                                  |
| <span data-ttu-id="10e41-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-192">In Global Catalog</span></span>      | <span data-ttu-id="10e41-193">否</span><span class="sxs-lookup"><span data-stu-id="10e41-193">False</span></span>                                                  |
| <span data-ttu-id="10e41-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-195">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-196">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-197">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-198">Search-Flags</span></span>           | <span data-ttu-id="10e41-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-199">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-200">System-Flags</span></span>           | <span data-ttu-id="10e41-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-201">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-202">Classes used in</span></span>        | [<span data-ttu-id="10e41-203">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-203">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="10e41-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10e41-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="10e41-205">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-205">Entry</span></span> | <span data-ttu-id="10e41-206">值</span><span class="sxs-lookup"><span data-stu-id="10e41-206">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-207">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-208">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-209">System-Only</span></span>            | <span data-ttu-id="10e41-210">否</span><span class="sxs-lookup"><span data-stu-id="10e41-210">False</span></span>                                                  |
| <span data-ttu-id="10e41-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-211">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-212">否</span><span class="sxs-lookup"><span data-stu-id="10e41-212">False</span></span>                                                  |
| <span data-ttu-id="10e41-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-213">Is Indexed</span></span>             | <span data-ttu-id="10e41-214">否</span><span class="sxs-lookup"><span data-stu-id="10e41-214">False</span></span>                                                  |
| <span data-ttu-id="10e41-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-215">In Global Catalog</span></span>      | <span data-ttu-id="10e41-216">否</span><span class="sxs-lookup"><span data-stu-id="10e41-216">False</span></span>                                                  |
| <span data-ttu-id="10e41-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-218">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-219">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-220">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-221">Search-Flags</span></span>           | <span data-ttu-id="10e41-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-222">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-223">System-Flags</span></span>           | <span data-ttu-id="10e41-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-224">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-225">Classes used in</span></span>        | [<span data-ttu-id="10e41-226">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-226">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="10e41-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10e41-227">Windows Server 2008</span></span>



| <span data-ttu-id="10e41-228">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-228">Entry</span></span> | <span data-ttu-id="10e41-229">值</span><span class="sxs-lookup"><span data-stu-id="10e41-229">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-230">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-231">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-232">System-Only</span></span>            | <span data-ttu-id="10e41-233">否</span><span class="sxs-lookup"><span data-stu-id="10e41-233">False</span></span>                                                  |
| <span data-ttu-id="10e41-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-234">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-235">否</span><span class="sxs-lookup"><span data-stu-id="10e41-235">False</span></span>                                                  |
| <span data-ttu-id="10e41-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-236">Is Indexed</span></span>             | <span data-ttu-id="10e41-237">否</span><span class="sxs-lookup"><span data-stu-id="10e41-237">False</span></span>                                                  |
| <span data-ttu-id="10e41-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-238">In Global Catalog</span></span>      | <span data-ttu-id="10e41-239">否</span><span class="sxs-lookup"><span data-stu-id="10e41-239">False</span></span>                                                  |
| <span data-ttu-id="10e41-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-241">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-242">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-243">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-244">Search-Flags</span></span>           | <span data-ttu-id="10e41-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-245">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-246">System-Flags</span></span>           | <span data-ttu-id="10e41-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-247">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-248">Classes used in</span></span>        | [<span data-ttu-id="10e41-249">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-249">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="10e41-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10e41-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="10e41-251">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-251">Entry</span></span> | <span data-ttu-id="10e41-252">值</span><span class="sxs-lookup"><span data-stu-id="10e41-252">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-253">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-254">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-255">System-Only</span></span>            | <span data-ttu-id="10e41-256">否</span><span class="sxs-lookup"><span data-stu-id="10e41-256">False</span></span>                                                  |
| <span data-ttu-id="10e41-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-257">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-258">否</span><span class="sxs-lookup"><span data-stu-id="10e41-258">False</span></span>                                                  |
| <span data-ttu-id="10e41-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-259">Is Indexed</span></span>             | <span data-ttu-id="10e41-260">否</span><span class="sxs-lookup"><span data-stu-id="10e41-260">False</span></span>                                                  |
| <span data-ttu-id="10e41-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-261">In Global Catalog</span></span>      | <span data-ttu-id="10e41-262">否</span><span class="sxs-lookup"><span data-stu-id="10e41-262">False</span></span>                                                  |
| <span data-ttu-id="10e41-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-264">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-265">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-266">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-267">Search-Flags</span></span>           | <span data-ttu-id="10e41-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-268">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-269">System-Flags</span></span>           | <span data-ttu-id="10e41-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-270">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-271">Classes used in</span></span>        | [<span data-ttu-id="10e41-272">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-272">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="10e41-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10e41-273">Windows Server 2012</span></span>



| <span data-ttu-id="10e41-274">進入</span><span class="sxs-lookup"><span data-stu-id="10e41-274">Entry</span></span> | <span data-ttu-id="10e41-275">值</span><span class="sxs-lookup"><span data-stu-id="10e41-275">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="10e41-276">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="10e41-276">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="10e41-277">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="10e41-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="10e41-278">System-Only</span></span>            | <span data-ttu-id="10e41-279">否</span><span class="sxs-lookup"><span data-stu-id="10e41-279">False</span></span>                                                  |
| <span data-ttu-id="10e41-280">是-單一值</span><span class="sxs-lookup"><span data-stu-id="10e41-280">Is-Single-Valued</span></span>       | <span data-ttu-id="10e41-281">否</span><span class="sxs-lookup"><span data-stu-id="10e41-281">False</span></span>                                                  |
| <span data-ttu-id="10e41-282">已編制索引</span><span class="sxs-lookup"><span data-stu-id="10e41-282">Is Indexed</span></span>             | <span data-ttu-id="10e41-283">否</span><span class="sxs-lookup"><span data-stu-id="10e41-283">False</span></span>                                                  |
| <span data-ttu-id="10e41-284">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="10e41-284">In Global Catalog</span></span>      | <span data-ttu-id="10e41-285">否</span><span class="sxs-lookup"><span data-stu-id="10e41-285">False</span></span>                                                  |
| <span data-ttu-id="10e41-286">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="10e41-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="10e41-287">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="10e41-287">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="10e41-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="10e41-288">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="10e41-289">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="10e41-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-290">Search-Flags</span></span>           | <span data-ttu-id="10e41-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10e41-291">0x00000000</span></span>                                             |
| <span data-ttu-id="10e41-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="10e41-292">System-Flags</span></span>           | <span data-ttu-id="10e41-293">0x00000010</span><span class="sxs-lookup"><span data-stu-id="10e41-293">0x00000010</span></span>                                             |
| <span data-ttu-id="10e41-294">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="10e41-294">Classes used in</span></span>        | [<span data-ttu-id="10e41-295">**NTDS 連接**</span><span class="sxs-lookup"><span data-stu-id="10e41-295">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





