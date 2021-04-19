---
title: 通訊錄-根屬性
description: 供 Exchange 使用。 Exchange 設定通訊錄容器的樹狀目錄以顯示於 MAPI 通訊錄中。 Exchange 設定物件上的這個屬性會列出通訊錄容器樹狀結構的根。 |通訊錄-根屬性
ms.assetid: 7e6d2677-9818-4870-8429-50f73f9c8c1f
ms.tgt_platform: multiple
keywords:
- 通訊錄-根屬性 AD 架構
- addressBookRoots 屬性 AD 架構
topic_type:
- apiref
api_name:
- Address-Book-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab195744bb7fb5029a9a48aeca55d703e6e05b62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974790"
---
# <a name="address-book-roots-attribute"></a><span data-ttu-id="c1458-108">通訊錄-根屬性</span><span class="sxs-lookup"><span data-stu-id="c1458-108">Address-Book-Roots attribute</span></span>

<span data-ttu-id="c1458-109">供 Exchange 使用。</span><span class="sxs-lookup"><span data-stu-id="c1458-109">Used by Exchange.</span></span> <span data-ttu-id="c1458-110">Exchange 設定通訊錄容器的樹狀目錄以顯示於 MAPI 通訊錄中。</span><span class="sxs-lookup"><span data-stu-id="c1458-110">Exchange configures trees of address book containers to show up in the MAPI address book.</span></span> <span data-ttu-id="c1458-111">Exchange 設定物件上的這個屬性會列出通訊錄容器樹狀結構的根。</span><span class="sxs-lookup"><span data-stu-id="c1458-111">This attribute on the Exchange Config object lists the roots of the address book container trees.</span></span>



| <span data-ttu-id="c1458-112">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-112">Entry</span></span> | <span data-ttu-id="c1458-113">值</span><span class="sxs-lookup"><span data-stu-id="c1458-113">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c1458-114">CN</span><span class="sxs-lookup"><span data-stu-id="c1458-114">CN</span></span>                | <span data-ttu-id="c1458-115">位址-書籍-根目錄</span><span class="sxs-lookup"><span data-stu-id="c1458-115">Address-Book-Roots</span></span>                      |
| <span data-ttu-id="c1458-116">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c1458-116">Ldap-Display-Name</span></span> | <span data-ttu-id="c1458-117">addressBookRoots</span><span class="sxs-lookup"><span data-stu-id="c1458-117">addressBookRoots</span></span>                        |
| <span data-ttu-id="c1458-118">大小</span><span class="sxs-lookup"><span data-stu-id="c1458-118">Size</span></span>              | \-                                      |
| <span data-ttu-id="c1458-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c1458-119">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c1458-120">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c1458-120">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c1458-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-121">Attribute-Id</span></span>      | <span data-ttu-id="c1458-122">1.2.840.113556.1.4.1244</span><span class="sxs-lookup"><span data-stu-id="c1458-122">1.2.840.113556.1.4.1244</span></span>                 |
| <span data-ttu-id="c1458-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c1458-123">System-Id-Guid</span></span>    | <span data-ttu-id="c1458-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="c1458-124">f70b6e48-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="c1458-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1458-125">Syntax</span></span>            | [<span data-ttu-id="c1458-126">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c1458-126">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c1458-127">實作</span><span class="sxs-lookup"><span data-stu-id="c1458-127">Implementations</span></span>

-   [<span data-ttu-id="c1458-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c1458-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c1458-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c1458-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c1458-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c1458-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c1458-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c1458-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c1458-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c1458-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c1458-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c1458-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c1458-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1458-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c1458-135">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-135">Entry</span></span> | <span data-ttu-id="c1458-136">值</span><span class="sxs-lookup"><span data-stu-id="c1458-136">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-137">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-137">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-138">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-139">System-Only</span></span>            | <span data-ttu-id="c1458-140">否</span><span class="sxs-lookup"><span data-stu-id="c1458-140">False</span></span>                                                                                |
| <span data-ttu-id="c1458-141">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-142">否</span><span class="sxs-lookup"><span data-stu-id="c1458-142">False</span></span>                                                                                |
| <span data-ttu-id="c1458-143">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-143">Is Indexed</span></span>             | <span data-ttu-id="c1458-144">否</span><span class="sxs-lookup"><span data-stu-id="c1458-144">False</span></span>                                                                                |
| <span data-ttu-id="c1458-145">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-145">In Global Catalog</span></span>      | <span data-ttu-id="c1458-146">否</span><span class="sxs-lookup"><span data-stu-id="c1458-146">False</span></span>                                                                                |
| <span data-ttu-id="c1458-147">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-148">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-148">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-149">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-150">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-151">Search-Flags</span></span>           | <span data-ttu-id="c1458-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-152">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-153">System-Flags</span></span>           | <span data-ttu-id="c1458-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-154">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-155">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-155">Classes used in</span></span>        | [<span data-ttu-id="c1458-156">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-156">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c1458-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1458-157">Windows Server 2003</span></span>



| <span data-ttu-id="c1458-158">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-158">Entry</span></span> | <span data-ttu-id="c1458-159">值</span><span class="sxs-lookup"><span data-stu-id="c1458-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-160">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-161">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-162">System-Only</span></span>            | <span data-ttu-id="c1458-163">否</span><span class="sxs-lookup"><span data-stu-id="c1458-163">False</span></span>                                                                                |
| <span data-ttu-id="c1458-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-165">否</span><span class="sxs-lookup"><span data-stu-id="c1458-165">False</span></span>                                                                                |
| <span data-ttu-id="c1458-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-166">Is Indexed</span></span>             | <span data-ttu-id="c1458-167">否</span><span class="sxs-lookup"><span data-stu-id="c1458-167">False</span></span>                                                                                |
| <span data-ttu-id="c1458-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-168">In Global Catalog</span></span>      | <span data-ttu-id="c1458-169">否</span><span class="sxs-lookup"><span data-stu-id="c1458-169">False</span></span>                                                                                |
| <span data-ttu-id="c1458-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-171">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-172">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-173">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-174">Search-Flags</span></span>           | <span data-ttu-id="c1458-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-175">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-176">System-Flags</span></span>           | <span data-ttu-id="c1458-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-177">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-178">Classes used in</span></span>        | [<span data-ttu-id="c1458-179">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-179">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c1458-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c1458-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c1458-181">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-181">Entry</span></span> | <span data-ttu-id="c1458-182">值</span><span class="sxs-lookup"><span data-stu-id="c1458-182">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-183">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-184">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-185">System-Only</span></span>            | <span data-ttu-id="c1458-186">否</span><span class="sxs-lookup"><span data-stu-id="c1458-186">False</span></span>                                                                                |
| <span data-ttu-id="c1458-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-188">否</span><span class="sxs-lookup"><span data-stu-id="c1458-188">False</span></span>                                                                                |
| <span data-ttu-id="c1458-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-189">Is Indexed</span></span>             | <span data-ttu-id="c1458-190">否</span><span class="sxs-lookup"><span data-stu-id="c1458-190">False</span></span>                                                                                |
| <span data-ttu-id="c1458-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-191">In Global Catalog</span></span>      | <span data-ttu-id="c1458-192">否</span><span class="sxs-lookup"><span data-stu-id="c1458-192">False</span></span>                                                                                |
| <span data-ttu-id="c1458-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-194">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-195">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-196">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-197">Search-Flags</span></span>           | <span data-ttu-id="c1458-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-198">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-199">System-Flags</span></span>           | <span data-ttu-id="c1458-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-200">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-201">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-201">Classes used in</span></span>        | [<span data-ttu-id="c1458-202">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-202">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c1458-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1458-203">Windows Server 2008</span></span>



| <span data-ttu-id="c1458-204">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-204">Entry</span></span> | <span data-ttu-id="c1458-205">值</span><span class="sxs-lookup"><span data-stu-id="c1458-205">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-206">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-207">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-208">System-Only</span></span>            | <span data-ttu-id="c1458-209">否</span><span class="sxs-lookup"><span data-stu-id="c1458-209">False</span></span>                                                                                |
| <span data-ttu-id="c1458-210">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-211">否</span><span class="sxs-lookup"><span data-stu-id="c1458-211">False</span></span>                                                                                |
| <span data-ttu-id="c1458-212">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-212">Is Indexed</span></span>             | <span data-ttu-id="c1458-213">否</span><span class="sxs-lookup"><span data-stu-id="c1458-213">False</span></span>                                                                                |
| <span data-ttu-id="c1458-214">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-214">In Global Catalog</span></span>      | <span data-ttu-id="c1458-215">否</span><span class="sxs-lookup"><span data-stu-id="c1458-215">False</span></span>                                                                                |
| <span data-ttu-id="c1458-216">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-217">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-217">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-218">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-219">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-220">Search-Flags</span></span>           | <span data-ttu-id="c1458-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-221">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-222">System-Flags</span></span>           | <span data-ttu-id="c1458-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-223">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-224">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-224">Classes used in</span></span>        | [<span data-ttu-id="c1458-225">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-225">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c1458-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1458-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c1458-227">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-227">Entry</span></span> | <span data-ttu-id="c1458-228">值</span><span class="sxs-lookup"><span data-stu-id="c1458-228">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-229">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-229">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-230">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-231">System-Only</span></span>            | <span data-ttu-id="c1458-232">否</span><span class="sxs-lookup"><span data-stu-id="c1458-232">False</span></span>                                                                                |
| <span data-ttu-id="c1458-233">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-234">否</span><span class="sxs-lookup"><span data-stu-id="c1458-234">False</span></span>                                                                                |
| <span data-ttu-id="c1458-235">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-235">Is Indexed</span></span>             | <span data-ttu-id="c1458-236">否</span><span class="sxs-lookup"><span data-stu-id="c1458-236">False</span></span>                                                                                |
| <span data-ttu-id="c1458-237">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-237">In Global Catalog</span></span>      | <span data-ttu-id="c1458-238">否</span><span class="sxs-lookup"><span data-stu-id="c1458-238">False</span></span>                                                                                |
| <span data-ttu-id="c1458-239">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-240">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-240">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-241">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-242">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-243">Search-Flags</span></span>           | <span data-ttu-id="c1458-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-244">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-245">System-Flags</span></span>           | <span data-ttu-id="c1458-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-246">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-247">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-247">Classes used in</span></span>        | [<span data-ttu-id="c1458-248">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-248">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c1458-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c1458-249">Windows Server 2012</span></span>



| <span data-ttu-id="c1458-250">進入</span><span class="sxs-lookup"><span data-stu-id="c1458-250">Entry</span></span> | <span data-ttu-id="c1458-251">值</span><span class="sxs-lookup"><span data-stu-id="c1458-251">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1458-252">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c1458-252">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c1458-253">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="c1458-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c1458-254">System-Only</span></span>            | <span data-ttu-id="c1458-255">否</span><span class="sxs-lookup"><span data-stu-id="c1458-255">False</span></span>                                                                                |
| <span data-ttu-id="c1458-256">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c1458-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c1458-257">否</span><span class="sxs-lookup"><span data-stu-id="c1458-257">False</span></span>                                                                                |
| <span data-ttu-id="c1458-258">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c1458-258">Is Indexed</span></span>             | <span data-ttu-id="c1458-259">否</span><span class="sxs-lookup"><span data-stu-id="c1458-259">False</span></span>                                                                                |
| <span data-ttu-id="c1458-260">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c1458-260">In Global Catalog</span></span>      | <span data-ttu-id="c1458-261">否</span><span class="sxs-lookup"><span data-stu-id="c1458-261">False</span></span>                                                                                |
| <span data-ttu-id="c1458-262">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c1458-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c1458-263">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c1458-263">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="c1458-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c1458-264">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c1458-265">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="c1458-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-266">Search-Flags</span></span>           | <span data-ttu-id="c1458-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c1458-267">0x00000000</span></span>                                                                           |
| <span data-ttu-id="c1458-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c1458-268">System-Flags</span></span>           | <span data-ttu-id="c1458-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c1458-269">0x00000010</span></span>                                                                           |
| <span data-ttu-id="c1458-270">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c1458-270">Classes used in</span></span>        | [<span data-ttu-id="c1458-271">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="c1458-271">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





