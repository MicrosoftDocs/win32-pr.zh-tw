---
title: ms DS-SPN-尾碼屬性
description: 此屬性描述樹系中的伺服器所使用的 DNS 主機名稱尾碼。 這些 DNS 尾碼將與其他與此樹系有跨樹系信任的樹系共用。
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- ms DS-SPN-尾碼屬性 AD 架構
- SPNSuffixes 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91f7ce8c92e8a81437d90bb0d80383b9ad334ee
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935416"
---
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="ec560-106">ms DS-SPN-尾碼屬性</span><span class="sxs-lookup"><span data-stu-id="ec560-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="ec560-107">此屬性描述樹系中的伺服器所使用的 DNS 主機名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="ec560-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="ec560-108">這些 DNS 尾碼將與其他與此樹系有跨樹系信任的樹系共用。</span><span class="sxs-lookup"><span data-stu-id="ec560-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="ec560-109">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-109">Entry</span></span> | <span data-ttu-id="ec560-110">值</span><span class="sxs-lookup"><span data-stu-id="ec560-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="ec560-111">CN</span><span class="sxs-lookup"><span data-stu-id="ec560-111">CN</span></span>                | <span data-ttu-id="ec560-112">ms DS-SPN-尾碼</span><span class="sxs-lookup"><span data-stu-id="ec560-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="ec560-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ec560-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ec560-114">SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="ec560-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="ec560-115">大小</span><span class="sxs-lookup"><span data-stu-id="ec560-115">Size</span></span>              | <span data-ttu-id="ec560-116">255位元組</span><span class="sxs-lookup"><span data-stu-id="ec560-116">255 bytes</span></span>                                    |
| <span data-ttu-id="ec560-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ec560-117">Update Privilege</span></span>  | <span data-ttu-id="ec560-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="ec560-118">Domain administrator</span></span>                         |
| <span data-ttu-id="ec560-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ec560-119">Update Frequency</span></span>  | <span data-ttu-id="ec560-120">當樹系中的伺服器取得新的尾碼時。</span><span class="sxs-lookup"><span data-stu-id="ec560-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="ec560-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-121">Attribute-Id</span></span>      | <span data-ttu-id="ec560-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="ec560-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="ec560-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ec560-123">System-Id-Guid</span></span>    | <span data-ttu-id="ec560-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="ec560-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="ec560-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec560-125">Syntax</span></span>            | [<span data-ttu-id="ec560-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ec560-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="ec560-127">實作</span><span class="sxs-lookup"><span data-stu-id="ec560-127">Implementations</span></span>

-   [<span data-ttu-id="ec560-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec560-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec560-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec560-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec560-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec560-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec560-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec560-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec560-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec560-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ec560-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec560-133">Windows Server 2003</span></span>



| <span data-ttu-id="ec560-134">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-134">Entry</span></span> | <span data-ttu-id="ec560-135">值</span><span class="sxs-lookup"><span data-stu-id="ec560-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec560-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec560-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec560-138">System-Only</span></span>            | <span data-ttu-id="ec560-139">否</span><span class="sxs-lookup"><span data-stu-id="ec560-139">False</span></span>                                                         |
| <span data-ttu-id="ec560-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec560-140">Is-Single-Valued</span></span>       | <span data-ttu-id="ec560-141">否</span><span class="sxs-lookup"><span data-stu-id="ec560-141">False</span></span>                                                         |
| <span data-ttu-id="ec560-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec560-142">Is Indexed</span></span>             | <span data-ttu-id="ec560-143">否</span><span class="sxs-lookup"><span data-stu-id="ec560-143">False</span></span>                                                         |
| <span data-ttu-id="ec560-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec560-144">In Global Catalog</span></span>      | <span data-ttu-id="ec560-145">否</span><span class="sxs-lookup"><span data-stu-id="ec560-145">False</span></span>                                                         |
| <span data-ttu-id="ec560-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec560-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec560-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec560-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="ec560-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec560-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec560-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-150">Search-Flags</span></span>           | <span data-ttu-id="ec560-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec560-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="ec560-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-152">System-Flags</span></span>           | <span data-ttu-id="ec560-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec560-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="ec560-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec560-154">Classes used in</span></span>        | [<span data-ttu-id="ec560-155">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="ec560-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec560-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec560-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec560-157">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-157">Entry</span></span> | <span data-ttu-id="ec560-158">值</span><span class="sxs-lookup"><span data-stu-id="ec560-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec560-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec560-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec560-161">System-Only</span></span>            | <span data-ttu-id="ec560-162">否</span><span class="sxs-lookup"><span data-stu-id="ec560-162">False</span></span>                                                         |
| <span data-ttu-id="ec560-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec560-163">Is-Single-Valued</span></span>       | <span data-ttu-id="ec560-164">否</span><span class="sxs-lookup"><span data-stu-id="ec560-164">False</span></span>                                                         |
| <span data-ttu-id="ec560-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec560-165">Is Indexed</span></span>             | <span data-ttu-id="ec560-166">否</span><span class="sxs-lookup"><span data-stu-id="ec560-166">False</span></span>                                                         |
| <span data-ttu-id="ec560-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec560-167">In Global Catalog</span></span>      | <span data-ttu-id="ec560-168">否</span><span class="sxs-lookup"><span data-stu-id="ec560-168">False</span></span>                                                         |
| <span data-ttu-id="ec560-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec560-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec560-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec560-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="ec560-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec560-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec560-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-173">Search-Flags</span></span>           | <span data-ttu-id="ec560-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec560-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="ec560-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-175">System-Flags</span></span>           | <span data-ttu-id="ec560-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec560-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="ec560-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec560-177">Classes used in</span></span>        | [<span data-ttu-id="ec560-178">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="ec560-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec560-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec560-179">Windows Server 2008</span></span>



| <span data-ttu-id="ec560-180">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-180">Entry</span></span> | <span data-ttu-id="ec560-181">值</span><span class="sxs-lookup"><span data-stu-id="ec560-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec560-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec560-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec560-184">System-Only</span></span>            | <span data-ttu-id="ec560-185">否</span><span class="sxs-lookup"><span data-stu-id="ec560-185">False</span></span>                                                         |
| <span data-ttu-id="ec560-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec560-186">Is-Single-Valued</span></span>       | <span data-ttu-id="ec560-187">否</span><span class="sxs-lookup"><span data-stu-id="ec560-187">False</span></span>                                                         |
| <span data-ttu-id="ec560-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec560-188">Is Indexed</span></span>             | <span data-ttu-id="ec560-189">否</span><span class="sxs-lookup"><span data-stu-id="ec560-189">False</span></span>                                                         |
| <span data-ttu-id="ec560-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec560-190">In Global Catalog</span></span>      | <span data-ttu-id="ec560-191">否</span><span class="sxs-lookup"><span data-stu-id="ec560-191">False</span></span>                                                         |
| <span data-ttu-id="ec560-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec560-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec560-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec560-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="ec560-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec560-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec560-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-196">Search-Flags</span></span>           | <span data-ttu-id="ec560-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec560-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="ec560-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-198">System-Flags</span></span>           | <span data-ttu-id="ec560-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec560-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="ec560-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec560-200">Classes used in</span></span>        | [<span data-ttu-id="ec560-201">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="ec560-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec560-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec560-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec560-203">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-203">Entry</span></span> | <span data-ttu-id="ec560-204">值</span><span class="sxs-lookup"><span data-stu-id="ec560-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec560-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec560-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec560-207">System-Only</span></span>            | <span data-ttu-id="ec560-208">否</span><span class="sxs-lookup"><span data-stu-id="ec560-208">False</span></span>                                                         |
| <span data-ttu-id="ec560-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec560-209">Is-Single-Valued</span></span>       | <span data-ttu-id="ec560-210">否</span><span class="sxs-lookup"><span data-stu-id="ec560-210">False</span></span>                                                         |
| <span data-ttu-id="ec560-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec560-211">Is Indexed</span></span>             | <span data-ttu-id="ec560-212">否</span><span class="sxs-lookup"><span data-stu-id="ec560-212">False</span></span>                                                         |
| <span data-ttu-id="ec560-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec560-213">In Global Catalog</span></span>      | <span data-ttu-id="ec560-214">否</span><span class="sxs-lookup"><span data-stu-id="ec560-214">False</span></span>                                                         |
| <span data-ttu-id="ec560-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec560-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec560-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec560-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="ec560-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec560-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec560-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-219">Search-Flags</span></span>           | <span data-ttu-id="ec560-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec560-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="ec560-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-221">System-Flags</span></span>           | <span data-ttu-id="ec560-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec560-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="ec560-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec560-223">Classes used in</span></span>        | [<span data-ttu-id="ec560-224">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="ec560-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec560-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec560-225">Windows Server 2012</span></span>



| <span data-ttu-id="ec560-226">進入</span><span class="sxs-lookup"><span data-stu-id="ec560-226">Entry</span></span> | <span data-ttu-id="ec560-227">值</span><span class="sxs-lookup"><span data-stu-id="ec560-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec560-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ec560-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec560-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="ec560-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec560-230">System-Only</span></span>            | <span data-ttu-id="ec560-231">否</span><span class="sxs-lookup"><span data-stu-id="ec560-231">False</span></span>                                                         |
| <span data-ttu-id="ec560-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ec560-232">Is-Single-Valued</span></span>       | <span data-ttu-id="ec560-233">否</span><span class="sxs-lookup"><span data-stu-id="ec560-233">False</span></span>                                                         |
| <span data-ttu-id="ec560-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ec560-234">Is Indexed</span></span>             | <span data-ttu-id="ec560-235">否</span><span class="sxs-lookup"><span data-stu-id="ec560-235">False</span></span>                                                         |
| <span data-ttu-id="ec560-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ec560-236">In Global Catalog</span></span>      | <span data-ttu-id="ec560-237">否</span><span class="sxs-lookup"><span data-stu-id="ec560-237">False</span></span>                                                         |
| <span data-ttu-id="ec560-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ec560-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec560-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ec560-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="ec560-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec560-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec560-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="ec560-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-242">Search-Flags</span></span>           | <span data-ttu-id="ec560-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec560-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="ec560-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec560-244">System-Flags</span></span>           | <span data-ttu-id="ec560-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec560-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="ec560-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ec560-246">Classes used in</span></span>        | [<span data-ttu-id="ec560-247">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="ec560-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





