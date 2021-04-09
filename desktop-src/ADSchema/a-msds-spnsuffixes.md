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
# <a name="ms-ds-spn-suffixes-attribute"></a><span data-ttu-id="308e3-106">ms DS-SPN-尾碼屬性</span><span class="sxs-lookup"><span data-stu-id="308e3-106">ms-DS-SPN-Suffixes attribute</span></span>

<span data-ttu-id="308e3-107">此屬性描述樹系中的伺服器所使用的 DNS 主機名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="308e3-107">This attribute describes the suffixes of DNS host names used by servers in the forest.</span></span> <span data-ttu-id="308e3-108">這些 DNS 尾碼將與其他與此樹系有跨樹系信任的樹系共用。</span><span class="sxs-lookup"><span data-stu-id="308e3-108">These DNS suffixes will be shared with other forests that have cross-forest trust with this forest.</span></span>



| <span data-ttu-id="308e3-109">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-109">Entry</span></span> | <span data-ttu-id="308e3-110">值</span><span class="sxs-lookup"><span data-stu-id="308e3-110">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="308e3-111">CN</span><span class="sxs-lookup"><span data-stu-id="308e3-111">CN</span></span>                | <span data-ttu-id="308e3-112">ms DS-SPN-尾碼</span><span class="sxs-lookup"><span data-stu-id="308e3-112">ms-DS-SPN-Suffixes</span></span>                           |
| <span data-ttu-id="308e3-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="308e3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="308e3-114">SPNSuffixes</span><span class="sxs-lookup"><span data-stu-id="308e3-114">msDS-SPNSuffixes</span></span>                             |
| <span data-ttu-id="308e3-115">大小</span><span class="sxs-lookup"><span data-stu-id="308e3-115">Size</span></span>              | <span data-ttu-id="308e3-116">255位元組</span><span class="sxs-lookup"><span data-stu-id="308e3-116">255 bytes</span></span>                                    |
| <span data-ttu-id="308e3-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="308e3-117">Update Privilege</span></span>  | <span data-ttu-id="308e3-118">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="308e3-118">Domain administrator</span></span>                         |
| <span data-ttu-id="308e3-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="308e3-119">Update Frequency</span></span>  | <span data-ttu-id="308e3-120">當樹系中的伺服器取得新的尾碼時。</span><span class="sxs-lookup"><span data-stu-id="308e3-120">When servers in the forest get a new suffix.</span></span> |
| <span data-ttu-id="308e3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-121">Attribute-Id</span></span>      | <span data-ttu-id="308e3-122">1.2.840.113556.1.4.1715</span><span class="sxs-lookup"><span data-stu-id="308e3-122">1.2.840.113556.1.4.1715</span></span>                      |
| <span data-ttu-id="308e3-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="308e3-123">System-Id-Guid</span></span>    | <span data-ttu-id="308e3-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span><span class="sxs-lookup"><span data-stu-id="308e3-124">789ee1eb-8c8e-4e4c-8cec-79b31b7617b5</span></span>         |
| <span data-ttu-id="308e3-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="308e3-125">Syntax</span></span>            | [<span data-ttu-id="308e3-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="308e3-126">**String(Unicode)**</span></span>](s-string-unicode.md)  |



## <a name="implementations"></a><span data-ttu-id="308e3-127">實作</span><span class="sxs-lookup"><span data-stu-id="308e3-127">Implementations</span></span>

-   [<span data-ttu-id="308e3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="308e3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="308e3-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="308e3-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="308e3-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="308e3-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="308e3-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="308e3-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="308e3-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="308e3-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="308e3-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="308e3-133">Windows Server 2003</span></span>



| <span data-ttu-id="308e3-134">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-134">Entry</span></span> | <span data-ttu-id="308e3-135">值</span><span class="sxs-lookup"><span data-stu-id="308e3-135">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="308e3-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="308e3-136">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-137">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="308e3-138">System-Only</span></span>            | <span data-ttu-id="308e3-139">否</span><span class="sxs-lookup"><span data-stu-id="308e3-139">False</span></span>                                                         |
| <span data-ttu-id="308e3-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="308e3-140">Is-Single-Valued</span></span>       | <span data-ttu-id="308e3-141">否</span><span class="sxs-lookup"><span data-stu-id="308e3-141">False</span></span>                                                         |
| <span data-ttu-id="308e3-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="308e3-142">Is Indexed</span></span>             | <span data-ttu-id="308e3-143">否</span><span class="sxs-lookup"><span data-stu-id="308e3-143">False</span></span>                                                         |
| <span data-ttu-id="308e3-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="308e3-144">In Global Catalog</span></span>      | <span data-ttu-id="308e3-145">否</span><span class="sxs-lookup"><span data-stu-id="308e3-145">False</span></span>                                                         |
| <span data-ttu-id="308e3-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="308e3-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="308e3-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="308e3-147">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="308e3-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="308e3-148">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="308e3-149">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-150">Search-Flags</span></span>           | <span data-ttu-id="308e3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="308e3-151">0x00000000</span></span>                                                    |
| <span data-ttu-id="308e3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-152">System-Flags</span></span>           | <span data-ttu-id="308e3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="308e3-153">0x00000010</span></span>                                                    |
| <span data-ttu-id="308e3-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="308e3-154">Classes used in</span></span>        | [<span data-ttu-id="308e3-155">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="308e3-155">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="308e3-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="308e3-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="308e3-157">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-157">Entry</span></span> | <span data-ttu-id="308e3-158">值</span><span class="sxs-lookup"><span data-stu-id="308e3-158">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="308e3-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="308e3-159">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-160">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="308e3-161">System-Only</span></span>            | <span data-ttu-id="308e3-162">否</span><span class="sxs-lookup"><span data-stu-id="308e3-162">False</span></span>                                                         |
| <span data-ttu-id="308e3-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="308e3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="308e3-164">否</span><span class="sxs-lookup"><span data-stu-id="308e3-164">False</span></span>                                                         |
| <span data-ttu-id="308e3-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="308e3-165">Is Indexed</span></span>             | <span data-ttu-id="308e3-166">否</span><span class="sxs-lookup"><span data-stu-id="308e3-166">False</span></span>                                                         |
| <span data-ttu-id="308e3-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="308e3-167">In Global Catalog</span></span>      | <span data-ttu-id="308e3-168">否</span><span class="sxs-lookup"><span data-stu-id="308e3-168">False</span></span>                                                         |
| <span data-ttu-id="308e3-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="308e3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="308e3-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="308e3-170">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="308e3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="308e3-171">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="308e3-172">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-173">Search-Flags</span></span>           | <span data-ttu-id="308e3-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="308e3-174">0x00000000</span></span>                                                    |
| <span data-ttu-id="308e3-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-175">System-Flags</span></span>           | <span data-ttu-id="308e3-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="308e3-176">0x00000010</span></span>                                                    |
| <span data-ttu-id="308e3-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="308e3-177">Classes used in</span></span>        | [<span data-ttu-id="308e3-178">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="308e3-178">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="308e3-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="308e3-179">Windows Server 2008</span></span>



| <span data-ttu-id="308e3-180">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-180">Entry</span></span> | <span data-ttu-id="308e3-181">值</span><span class="sxs-lookup"><span data-stu-id="308e3-181">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="308e3-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="308e3-182">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-183">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="308e3-184">System-Only</span></span>            | <span data-ttu-id="308e3-185">否</span><span class="sxs-lookup"><span data-stu-id="308e3-185">False</span></span>                                                         |
| <span data-ttu-id="308e3-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="308e3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="308e3-187">否</span><span class="sxs-lookup"><span data-stu-id="308e3-187">False</span></span>                                                         |
| <span data-ttu-id="308e3-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="308e3-188">Is Indexed</span></span>             | <span data-ttu-id="308e3-189">否</span><span class="sxs-lookup"><span data-stu-id="308e3-189">False</span></span>                                                         |
| <span data-ttu-id="308e3-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="308e3-190">In Global Catalog</span></span>      | <span data-ttu-id="308e3-191">否</span><span class="sxs-lookup"><span data-stu-id="308e3-191">False</span></span>                                                         |
| <span data-ttu-id="308e3-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="308e3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="308e3-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="308e3-193">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="308e3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="308e3-194">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="308e3-195">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-196">Search-Flags</span></span>           | <span data-ttu-id="308e3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="308e3-197">0x00000000</span></span>                                                    |
| <span data-ttu-id="308e3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-198">System-Flags</span></span>           | <span data-ttu-id="308e3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="308e3-199">0x00000010</span></span>                                                    |
| <span data-ttu-id="308e3-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="308e3-200">Classes used in</span></span>        | [<span data-ttu-id="308e3-201">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="308e3-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="308e3-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="308e3-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="308e3-203">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-203">Entry</span></span> | <span data-ttu-id="308e3-204">值</span><span class="sxs-lookup"><span data-stu-id="308e3-204">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="308e3-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="308e3-205">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-206">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="308e3-207">System-Only</span></span>            | <span data-ttu-id="308e3-208">否</span><span class="sxs-lookup"><span data-stu-id="308e3-208">False</span></span>                                                         |
| <span data-ttu-id="308e3-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="308e3-209">Is-Single-Valued</span></span>       | <span data-ttu-id="308e3-210">否</span><span class="sxs-lookup"><span data-stu-id="308e3-210">False</span></span>                                                         |
| <span data-ttu-id="308e3-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="308e3-211">Is Indexed</span></span>             | <span data-ttu-id="308e3-212">否</span><span class="sxs-lookup"><span data-stu-id="308e3-212">False</span></span>                                                         |
| <span data-ttu-id="308e3-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="308e3-213">In Global Catalog</span></span>      | <span data-ttu-id="308e3-214">否</span><span class="sxs-lookup"><span data-stu-id="308e3-214">False</span></span>                                                         |
| <span data-ttu-id="308e3-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="308e3-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="308e3-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="308e3-216">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="308e3-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="308e3-217">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="308e3-218">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-219">Search-Flags</span></span>           | <span data-ttu-id="308e3-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="308e3-220">0x00000000</span></span>                                                    |
| <span data-ttu-id="308e3-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-221">System-Flags</span></span>           | <span data-ttu-id="308e3-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="308e3-222">0x00000010</span></span>                                                    |
| <span data-ttu-id="308e3-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="308e3-223">Classes used in</span></span>        | [<span data-ttu-id="308e3-224">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="308e3-224">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="308e3-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="308e3-225">Windows Server 2012</span></span>



| <span data-ttu-id="308e3-226">進入</span><span class="sxs-lookup"><span data-stu-id="308e3-226">Entry</span></span> | <span data-ttu-id="308e3-227">值</span><span class="sxs-lookup"><span data-stu-id="308e3-227">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="308e3-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="308e3-228">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="308e3-229">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="308e3-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="308e3-230">System-Only</span></span>            | <span data-ttu-id="308e3-231">否</span><span class="sxs-lookup"><span data-stu-id="308e3-231">False</span></span>                                                         |
| <span data-ttu-id="308e3-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="308e3-232">Is-Single-Valued</span></span>       | <span data-ttu-id="308e3-233">否</span><span class="sxs-lookup"><span data-stu-id="308e3-233">False</span></span>                                                         |
| <span data-ttu-id="308e3-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="308e3-234">Is Indexed</span></span>             | <span data-ttu-id="308e3-235">否</span><span class="sxs-lookup"><span data-stu-id="308e3-235">False</span></span>                                                         |
| <span data-ttu-id="308e3-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="308e3-236">In Global Catalog</span></span>      | <span data-ttu-id="308e3-237">否</span><span class="sxs-lookup"><span data-stu-id="308e3-237">False</span></span>                                                         |
| <span data-ttu-id="308e3-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="308e3-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="308e3-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="308e3-239">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="308e3-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="308e3-240">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="308e3-241">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="308e3-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-242">Search-Flags</span></span>           | <span data-ttu-id="308e3-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="308e3-243">0x00000000</span></span>                                                    |
| <span data-ttu-id="308e3-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="308e3-244">System-Flags</span></span>           | <span data-ttu-id="308e3-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="308e3-245">0x00000010</span></span>                                                    |
| <span data-ttu-id="308e3-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="308e3-246">Classes used in</span></span>        | [<span data-ttu-id="308e3-247">**交叉參考容器**</span><span class="sxs-lookup"><span data-stu-id="308e3-247">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





