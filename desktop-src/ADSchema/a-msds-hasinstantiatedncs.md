---
title: ms-chap-已具現化-Nc 屬性
description: DS 複寫狀態資訊，類似于 (，以及) 現有屬性 hasMasterNCs 和 hasPartialReplicaNCs 的超集合。 供 KCC 在設定複寫夥伴時使用。
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- ms-chap-已具現化-Nc 屬性 AD 架構
- HasInstantiatedNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467284"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a><span data-ttu-id="f4221-106">ms-chap-已具現化-Nc 屬性</span><span class="sxs-lookup"><span data-stu-id="f4221-106">ms-DS-Has-Instantiated-NCs attribute</span></span>

<span data-ttu-id="f4221-107">DS 複寫狀態資訊，類似于 (，以及) 現有屬性 hasMasterNCs 和 hasPartialReplicaNCs 的超集合。</span><span class="sxs-lookup"><span data-stu-id="f4221-107">DS replication state information, analogous to (and a superset of) the existing attributes hasMasterNCs and hasPartialReplicaNCs.</span></span> <span data-ttu-id="f4221-108">供 KCC 在設定複寫夥伴時使用。</span><span class="sxs-lookup"><span data-stu-id="f4221-108">To be used by the KCC when setting up replication partners.</span></span>



| <span data-ttu-id="f4221-109">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-109">Entry</span></span> | <span data-ttu-id="f4221-110">值</span><span class="sxs-lookup"><span data-stu-id="f4221-110">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4221-111">CN</span><span class="sxs-lookup"><span data-stu-id="f4221-111">CN</span></span>                | <span data-ttu-id="f4221-112">ms-DS-具現化-Nc</span><span class="sxs-lookup"><span data-stu-id="f4221-112">ms-DS-Has-Instantiated-NCs</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="f4221-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f4221-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f4221-114">HasInstantiatedNCs</span><span class="sxs-lookup"><span data-stu-id="f4221-114">msDS-HasInstantiatedNCs</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="f4221-115">大小</span><span class="sxs-lookup"><span data-stu-id="f4221-115">Size</span></span>              | <span data-ttu-id="f4221-116">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="f4221-116">4 bytes</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="f4221-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f4221-117">Update Privilege</span></span>  | <span data-ttu-id="f4221-118">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="f4221-118">This value is set by the system.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="f4221-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f4221-119">Update Frequency</span></span>  | <span data-ttu-id="f4221-120">大約兩倍的 hasMasterNCs/hasPartialReplicaNCs。</span><span class="sxs-lookup"><span data-stu-id="f4221-120">Roughly twice as often as hasMasterNCs / hasPartialReplicaNCs.</span></span> <span data-ttu-id="f4221-121">只有當 DC 新增或移除分割區時，才會更新這些現有的屬性 (例如，從 DC 變更為 GC 時，) 。</span><span class="sxs-lookup"><span data-stu-id="f4221-121">These existing attributes are updated only when the DC adds or removes a partition (For example, when changing from DC to GC or vice versa).</span></span> |
| <span data-ttu-id="f4221-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-122">Attribute-Id</span></span>      | <span data-ttu-id="f4221-123">1.2.840.113556.1.4.1709</span><span class="sxs-lookup"><span data-stu-id="f4221-123">1.2.840.113556.1.4.1709</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="f4221-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f4221-124">System-Id-Guid</span></span>    | <span data-ttu-id="f4221-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span><span class="sxs-lookup"><span data-stu-id="f4221-125">11e9a5bc-4517-4049-af9c-51554fb0fc09</span></span>                                                                                                                                                                        |
| <span data-ttu-id="f4221-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4221-126">Syntax</span></span>            | [<span data-ttu-id="f4221-127">**Object(DN-Binary)**</span><span class="sxs-lookup"><span data-stu-id="f4221-127">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a><span data-ttu-id="f4221-128">實作</span><span class="sxs-lookup"><span data-stu-id="f4221-128">Implementations</span></span>

-   [<span data-ttu-id="f4221-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4221-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4221-130">**亞當**</span><span class="sxs-lookup"><span data-stu-id="f4221-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f4221-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4221-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4221-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4221-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4221-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4221-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4221-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4221-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f4221-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4221-135">Windows Server 2003</span></span>



| <span data-ttu-id="f4221-136">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-136">Entry</span></span> | <span data-ttu-id="f4221-137">值</span><span class="sxs-lookup"><span data-stu-id="f4221-137">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-138">Link-Id</span></span>                | <span data-ttu-id="f4221-139">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-139">2002</span></span>                                     |
| <span data-ttu-id="f4221-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-141">System-Only</span></span>            | <span data-ttu-id="f4221-142">對</span><span class="sxs-lookup"><span data-stu-id="f4221-142">True</span></span>                                     |
| <span data-ttu-id="f4221-143">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-143">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-144">否</span><span class="sxs-lookup"><span data-stu-id="f4221-144">False</span></span>                                    |
| <span data-ttu-id="f4221-145">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-145">Is Indexed</span></span>             | <span data-ttu-id="f4221-146">否</span><span class="sxs-lookup"><span data-stu-id="f4221-146">False</span></span>                                    |
| <span data-ttu-id="f4221-147">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-147">In Global Catalog</span></span>      | <span data-ttu-id="f4221-148">否</span><span class="sxs-lookup"><span data-stu-id="f4221-148">False</span></span>                                    |
| <span data-ttu-id="f4221-149">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-150">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-151">Range-Lower</span></span>            | <span data-ttu-id="f4221-152">4</span><span class="sxs-lookup"><span data-stu-id="f4221-152">4</span></span>                                        |
| <span data-ttu-id="f4221-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-153">Range-Upper</span></span>            | <span data-ttu-id="f4221-154">4</span><span class="sxs-lookup"><span data-stu-id="f4221-154">4</span></span>                                        |
| <span data-ttu-id="f4221-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-155">Search-Flags</span></span>           | <span data-ttu-id="f4221-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-156">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-157">System-Flags</span></span>           | <span data-ttu-id="f4221-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-158">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-159">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-159">Classes used in</span></span>        | [<span data-ttu-id="f4221-160">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-160">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f4221-161">亞當</span><span class="sxs-lookup"><span data-stu-id="f4221-161">ADAM</span></span>



| <span data-ttu-id="f4221-162">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-162">Entry</span></span> | <span data-ttu-id="f4221-163">值</span><span class="sxs-lookup"><span data-stu-id="f4221-163">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-164">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-164">Link-Id</span></span>                | <span data-ttu-id="f4221-165">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-165">2002</span></span>                                     |
| <span data-ttu-id="f4221-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-166">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-167">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-167">System-Only</span></span>            | <span data-ttu-id="f4221-168">對</span><span class="sxs-lookup"><span data-stu-id="f4221-168">True</span></span>                                     |
| <span data-ttu-id="f4221-169">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-169">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-170">否</span><span class="sxs-lookup"><span data-stu-id="f4221-170">False</span></span>                                    |
| <span data-ttu-id="f4221-171">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-171">Is Indexed</span></span>             | <span data-ttu-id="f4221-172">否</span><span class="sxs-lookup"><span data-stu-id="f4221-172">False</span></span>                                    |
| <span data-ttu-id="f4221-173">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-173">In Global Catalog</span></span>      | <span data-ttu-id="f4221-174">否</span><span class="sxs-lookup"><span data-stu-id="f4221-174">False</span></span>                                    |
| <span data-ttu-id="f4221-175">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-175">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-176">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-176">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-177">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-177">Range-Lower</span></span>            | <span data-ttu-id="f4221-178">4</span><span class="sxs-lookup"><span data-stu-id="f4221-178">4</span></span>                                        |
| <span data-ttu-id="f4221-179">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-179">Range-Upper</span></span>            | <span data-ttu-id="f4221-180">4</span><span class="sxs-lookup"><span data-stu-id="f4221-180">4</span></span>                                        |
| <span data-ttu-id="f4221-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-181">Search-Flags</span></span>           | <span data-ttu-id="f4221-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-182">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-183">System-Flags</span></span>           | <span data-ttu-id="f4221-184">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-184">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-185">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-185">Classes used in</span></span>        | [<span data-ttu-id="f4221-186">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-186">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4221-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4221-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4221-188">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-188">Entry</span></span> | <span data-ttu-id="f4221-189">值</span><span class="sxs-lookup"><span data-stu-id="f4221-189">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-190">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-190">Link-Id</span></span>                | <span data-ttu-id="f4221-191">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-191">2002</span></span>                                     |
| <span data-ttu-id="f4221-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-192">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-193">System-Only</span></span>            | <span data-ttu-id="f4221-194">對</span><span class="sxs-lookup"><span data-stu-id="f4221-194">True</span></span>                                     |
| <span data-ttu-id="f4221-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-195">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-196">否</span><span class="sxs-lookup"><span data-stu-id="f4221-196">False</span></span>                                    |
| <span data-ttu-id="f4221-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-197">Is Indexed</span></span>             | <span data-ttu-id="f4221-198">否</span><span class="sxs-lookup"><span data-stu-id="f4221-198">False</span></span>                                    |
| <span data-ttu-id="f4221-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-199">In Global Catalog</span></span>      | <span data-ttu-id="f4221-200">否</span><span class="sxs-lookup"><span data-stu-id="f4221-200">False</span></span>                                    |
| <span data-ttu-id="f4221-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-202">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-203">Range-Lower</span></span>            | <span data-ttu-id="f4221-204">4</span><span class="sxs-lookup"><span data-stu-id="f4221-204">4</span></span>                                        |
| <span data-ttu-id="f4221-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-205">Range-Upper</span></span>            | <span data-ttu-id="f4221-206">4</span><span class="sxs-lookup"><span data-stu-id="f4221-206">4</span></span>                                        |
| <span data-ttu-id="f4221-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-207">Search-Flags</span></span>           | <span data-ttu-id="f4221-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-208">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-209">System-Flags</span></span>           | <span data-ttu-id="f4221-210">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-210">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-211">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-211">Classes used in</span></span>        | [<span data-ttu-id="f4221-212">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-212">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4221-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4221-213">Windows Server 2008</span></span>



| <span data-ttu-id="f4221-214">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-214">Entry</span></span> | <span data-ttu-id="f4221-215">值</span><span class="sxs-lookup"><span data-stu-id="f4221-215">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-216">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-216">Link-Id</span></span>                | <span data-ttu-id="f4221-217">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-217">2002</span></span>                                     |
| <span data-ttu-id="f4221-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-218">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-219">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-219">System-Only</span></span>            | <span data-ttu-id="f4221-220">對</span><span class="sxs-lookup"><span data-stu-id="f4221-220">True</span></span>                                     |
| <span data-ttu-id="f4221-221">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-221">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-222">否</span><span class="sxs-lookup"><span data-stu-id="f4221-222">False</span></span>                                    |
| <span data-ttu-id="f4221-223">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-223">Is Indexed</span></span>             | <span data-ttu-id="f4221-224">否</span><span class="sxs-lookup"><span data-stu-id="f4221-224">False</span></span>                                    |
| <span data-ttu-id="f4221-225">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-225">In Global Catalog</span></span>      | <span data-ttu-id="f4221-226">否</span><span class="sxs-lookup"><span data-stu-id="f4221-226">False</span></span>                                    |
| <span data-ttu-id="f4221-227">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-227">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-228">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-228">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-229">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-229">Range-Lower</span></span>            | <span data-ttu-id="f4221-230">4</span><span class="sxs-lookup"><span data-stu-id="f4221-230">4</span></span>                                        |
| <span data-ttu-id="f4221-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-231">Range-Upper</span></span>            | <span data-ttu-id="f4221-232">4</span><span class="sxs-lookup"><span data-stu-id="f4221-232">4</span></span>                                        |
| <span data-ttu-id="f4221-233">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-233">Search-Flags</span></span>           | <span data-ttu-id="f4221-234">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-234">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-235">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-235">System-Flags</span></span>           | <span data-ttu-id="f4221-236">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-236">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-237">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-237">Classes used in</span></span>        | [<span data-ttu-id="f4221-238">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-238">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4221-239">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4221-239">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4221-240">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-240">Entry</span></span> | <span data-ttu-id="f4221-241">值</span><span class="sxs-lookup"><span data-stu-id="f4221-241">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-242">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-242">Link-Id</span></span>                | <span data-ttu-id="f4221-243">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-243">2002</span></span>                                     |
| <span data-ttu-id="f4221-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-244">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-245">System-Only</span></span>            | <span data-ttu-id="f4221-246">對</span><span class="sxs-lookup"><span data-stu-id="f4221-246">True</span></span>                                     |
| <span data-ttu-id="f4221-247">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-247">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-248">否</span><span class="sxs-lookup"><span data-stu-id="f4221-248">False</span></span>                                    |
| <span data-ttu-id="f4221-249">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-249">Is Indexed</span></span>             | <span data-ttu-id="f4221-250">否</span><span class="sxs-lookup"><span data-stu-id="f4221-250">False</span></span>                                    |
| <span data-ttu-id="f4221-251">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-251">In Global Catalog</span></span>      | <span data-ttu-id="f4221-252">否</span><span class="sxs-lookup"><span data-stu-id="f4221-252">False</span></span>                                    |
| <span data-ttu-id="f4221-253">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-254">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-254">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-255">Range-Lower</span></span>            | <span data-ttu-id="f4221-256">4</span><span class="sxs-lookup"><span data-stu-id="f4221-256">4</span></span>                                        |
| <span data-ttu-id="f4221-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-257">Range-Upper</span></span>            | <span data-ttu-id="f4221-258">4</span><span class="sxs-lookup"><span data-stu-id="f4221-258">4</span></span>                                        |
| <span data-ttu-id="f4221-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-259">Search-Flags</span></span>           | <span data-ttu-id="f4221-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-260">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-261">System-Flags</span></span>           | <span data-ttu-id="f4221-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-262">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-263">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-263">Classes used in</span></span>        | [<span data-ttu-id="f4221-264">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-264">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4221-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4221-265">Windows Server 2012</span></span>



| <span data-ttu-id="f4221-266">進入</span><span class="sxs-lookup"><span data-stu-id="f4221-266">Entry</span></span> | <span data-ttu-id="f4221-267">值</span><span class="sxs-lookup"><span data-stu-id="f4221-267">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="f4221-268">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f4221-268">Link-Id</span></span>                | <span data-ttu-id="f4221-269">2002</span><span class="sxs-lookup"><span data-stu-id="f4221-269">2002</span></span>                                     |
| <span data-ttu-id="f4221-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4221-270">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="f4221-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4221-271">System-Only</span></span>            | <span data-ttu-id="f4221-272">對</span><span class="sxs-lookup"><span data-stu-id="f4221-272">True</span></span>                                     |
| <span data-ttu-id="f4221-273">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f4221-273">Is-Single-Valued</span></span>       | <span data-ttu-id="f4221-274">否</span><span class="sxs-lookup"><span data-stu-id="f4221-274">False</span></span>                                    |
| <span data-ttu-id="f4221-275">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f4221-275">Is Indexed</span></span>             | <span data-ttu-id="f4221-276">否</span><span class="sxs-lookup"><span data-stu-id="f4221-276">False</span></span>                                    |
| <span data-ttu-id="f4221-277">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f4221-277">In Global Catalog</span></span>      | <span data-ttu-id="f4221-278">否</span><span class="sxs-lookup"><span data-stu-id="f4221-278">False</span></span>                                    |
| <span data-ttu-id="f4221-279">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f4221-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4221-280">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f4221-280">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="f4221-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4221-281">Range-Lower</span></span>            | <span data-ttu-id="f4221-282">4</span><span class="sxs-lookup"><span data-stu-id="f4221-282">4</span></span>                                        |
| <span data-ttu-id="f4221-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4221-283">Range-Upper</span></span>            | <span data-ttu-id="f4221-284">4</span><span class="sxs-lookup"><span data-stu-id="f4221-284">4</span></span>                                        |
| <span data-ttu-id="f4221-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-285">Search-Flags</span></span>           | <span data-ttu-id="f4221-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4221-286">0x00000000</span></span>                               |
| <span data-ttu-id="f4221-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4221-287">System-Flags</span></span>           | <span data-ttu-id="f4221-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4221-288">0x00000010</span></span>                               |
| <span data-ttu-id="f4221-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f4221-289">Classes used in</span></span>        | [<span data-ttu-id="f4221-290">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="f4221-290">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





