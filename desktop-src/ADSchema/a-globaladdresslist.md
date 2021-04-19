---
title: 全域通訊清單屬性
description: 這個屬性在 Microsoft Exchange 容器中是用來儲存新建立的全域通訊清單 (GAL) 的分辨名稱。
ms.assetid: 0da2bafe-ecdf-4b75-9461-08a35151b85c
ms.tgt_platform: multiple
keywords:
- 全域通訊清單屬性 AD 架構
- globalAddressList 屬性 AD 架構
topic_type:
- apiref
api_name:
- Global-Address-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28178dfd6621593ee60e6e07043be544445cb6e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106967778"
---
# <a name="global-address-list-attribute"></a><span data-ttu-id="548db-105">全域通訊清單屬性</span><span class="sxs-lookup"><span data-stu-id="548db-105">Global-Address-List attribute</span></span>

<span data-ttu-id="548db-106">這個屬性在 Microsoft Exchange 容器中是用來儲存新建立的全域通訊清單 (GAL) 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="548db-106">This attribute is used on a Microsoft Exchange container to store the distinguished name of a newly created global address list (GAL).</span></span> <span data-ttu-id="548db-107">在您讓訊息應用程式發展介面 (MAPI) 用戶端使用 GAL 之前，這個屬性必須擁有一個項目。</span><span class="sxs-lookup"><span data-stu-id="548db-107">This attribute must have an entry before you can enable Messaging Application Programming Interface (MAPI) clients to use a GAL.</span></span>



| <span data-ttu-id="548db-108">進入</span><span class="sxs-lookup"><span data-stu-id="548db-108">Entry</span></span> | <span data-ttu-id="548db-109">值</span><span class="sxs-lookup"><span data-stu-id="548db-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="548db-110">CN</span><span class="sxs-lookup"><span data-stu-id="548db-110">CN</span></span>                | <span data-ttu-id="548db-111">全域通訊清單</span><span class="sxs-lookup"><span data-stu-id="548db-111">Global-Address-List</span></span>                     |
| <span data-ttu-id="548db-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="548db-112">Ldap-Display-Name</span></span> | <span data-ttu-id="548db-113">globalAddressList</span><span class="sxs-lookup"><span data-stu-id="548db-113">globalAddressList</span></span>                       |
| <span data-ttu-id="548db-114">大小</span><span class="sxs-lookup"><span data-stu-id="548db-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="548db-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="548db-115">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="548db-116">更新頻率</span><span class="sxs-lookup"><span data-stu-id="548db-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="548db-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="548db-117">Attribute-Id</span></span>      | <span data-ttu-id="548db-118">1.2.840.113556.1.4.1245</span><span class="sxs-lookup"><span data-stu-id="548db-118">1.2.840.113556.1.4.1245</span></span>                 |
| <span data-ttu-id="548db-119">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="548db-119">System-Id-Guid</span></span>    | <span data-ttu-id="548db-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span><span class="sxs-lookup"><span data-stu-id="548db-120">f754c748-06f4-11d2-aa53-00c04fd7d83a</span></span>    |
| <span data-ttu-id="548db-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="548db-121">Syntax</span></span>            | [<span data-ttu-id="548db-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="548db-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="548db-123">實作</span><span class="sxs-lookup"><span data-stu-id="548db-123">Implementations</span></span>

-   [<span data-ttu-id="548db-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="548db-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="548db-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="548db-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="548db-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="548db-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="548db-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="548db-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="548db-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="548db-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="548db-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="548db-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="548db-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="548db-130">Windows 2000 Server</span></span>



| <span data-ttu-id="548db-131">進入</span><span class="sxs-lookup"><span data-stu-id="548db-131">Entry</span></span> | <span data-ttu-id="548db-132">值</span><span class="sxs-lookup"><span data-stu-id="548db-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-133">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-134">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-135">System-Only</span></span>            | <span data-ttu-id="548db-136">否</span><span class="sxs-lookup"><span data-stu-id="548db-136">False</span></span>                                                                                |
| <span data-ttu-id="548db-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-137">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-138">否</span><span class="sxs-lookup"><span data-stu-id="548db-138">False</span></span>                                                                                |
| <span data-ttu-id="548db-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-139">Is Indexed</span></span>             | <span data-ttu-id="548db-140">否</span><span class="sxs-lookup"><span data-stu-id="548db-140">False</span></span>                                                                                |
| <span data-ttu-id="548db-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-141">In Global Catalog</span></span>      | <span data-ttu-id="548db-142">否</span><span class="sxs-lookup"><span data-stu-id="548db-142">False</span></span>                                                                                |
| <span data-ttu-id="548db-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-144">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-145">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-146">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-147">Search-Flags</span></span>           | <span data-ttu-id="548db-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-148">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-149">System-Flags</span></span>           | <span data-ttu-id="548db-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-150">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-151">Classes used in</span></span>        | [<span data-ttu-id="548db-152">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-152">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="548db-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="548db-153">Windows Server 2003</span></span>



| <span data-ttu-id="548db-154">進入</span><span class="sxs-lookup"><span data-stu-id="548db-154">Entry</span></span> | <span data-ttu-id="548db-155">值</span><span class="sxs-lookup"><span data-stu-id="548db-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-156">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-157">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-158">System-Only</span></span>            | <span data-ttu-id="548db-159">否</span><span class="sxs-lookup"><span data-stu-id="548db-159">False</span></span>                                                                                |
| <span data-ttu-id="548db-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-160">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-161">否</span><span class="sxs-lookup"><span data-stu-id="548db-161">False</span></span>                                                                                |
| <span data-ttu-id="548db-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-162">Is Indexed</span></span>             | <span data-ttu-id="548db-163">否</span><span class="sxs-lookup"><span data-stu-id="548db-163">False</span></span>                                                                                |
| <span data-ttu-id="548db-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-164">In Global Catalog</span></span>      | <span data-ttu-id="548db-165">否</span><span class="sxs-lookup"><span data-stu-id="548db-165">False</span></span>                                                                                |
| <span data-ttu-id="548db-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-167">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-168">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-169">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-170">Search-Flags</span></span>           | <span data-ttu-id="548db-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-171">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-172">System-Flags</span></span>           | <span data-ttu-id="548db-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-173">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-174">Classes used in</span></span>        | [<span data-ttu-id="548db-175">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-175">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="548db-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="548db-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="548db-177">進入</span><span class="sxs-lookup"><span data-stu-id="548db-177">Entry</span></span> | <span data-ttu-id="548db-178">值</span><span class="sxs-lookup"><span data-stu-id="548db-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-179">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-180">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-181">System-Only</span></span>            | <span data-ttu-id="548db-182">否</span><span class="sxs-lookup"><span data-stu-id="548db-182">False</span></span>                                                                                |
| <span data-ttu-id="548db-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-183">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-184">否</span><span class="sxs-lookup"><span data-stu-id="548db-184">False</span></span>                                                                                |
| <span data-ttu-id="548db-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-185">Is Indexed</span></span>             | <span data-ttu-id="548db-186">否</span><span class="sxs-lookup"><span data-stu-id="548db-186">False</span></span>                                                                                |
| <span data-ttu-id="548db-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-187">In Global Catalog</span></span>      | <span data-ttu-id="548db-188">否</span><span class="sxs-lookup"><span data-stu-id="548db-188">False</span></span>                                                                                |
| <span data-ttu-id="548db-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-190">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-191">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-192">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-193">Search-Flags</span></span>           | <span data-ttu-id="548db-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-194">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-195">System-Flags</span></span>           | <span data-ttu-id="548db-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-196">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-197">Classes used in</span></span>        | [<span data-ttu-id="548db-198">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-198">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="548db-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="548db-199">Windows Server 2008</span></span>



| <span data-ttu-id="548db-200">進入</span><span class="sxs-lookup"><span data-stu-id="548db-200">Entry</span></span> | <span data-ttu-id="548db-201">值</span><span class="sxs-lookup"><span data-stu-id="548db-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-202">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-203">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-204">System-Only</span></span>            | <span data-ttu-id="548db-205">否</span><span class="sxs-lookup"><span data-stu-id="548db-205">False</span></span>                                                                                |
| <span data-ttu-id="548db-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-206">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-207">否</span><span class="sxs-lookup"><span data-stu-id="548db-207">False</span></span>                                                                                |
| <span data-ttu-id="548db-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-208">Is Indexed</span></span>             | <span data-ttu-id="548db-209">否</span><span class="sxs-lookup"><span data-stu-id="548db-209">False</span></span>                                                                                |
| <span data-ttu-id="548db-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-210">In Global Catalog</span></span>      | <span data-ttu-id="548db-211">否</span><span class="sxs-lookup"><span data-stu-id="548db-211">False</span></span>                                                                                |
| <span data-ttu-id="548db-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-213">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-214">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-215">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-216">Search-Flags</span></span>           | <span data-ttu-id="548db-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-217">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-218">System-Flags</span></span>           | <span data-ttu-id="548db-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-219">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-220">Classes used in</span></span>        | [<span data-ttu-id="548db-221">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-221">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="548db-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="548db-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="548db-223">進入</span><span class="sxs-lookup"><span data-stu-id="548db-223">Entry</span></span> | <span data-ttu-id="548db-224">值</span><span class="sxs-lookup"><span data-stu-id="548db-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-225">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-226">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-227">System-Only</span></span>            | <span data-ttu-id="548db-228">否</span><span class="sxs-lookup"><span data-stu-id="548db-228">False</span></span>                                                                                |
| <span data-ttu-id="548db-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-229">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-230">否</span><span class="sxs-lookup"><span data-stu-id="548db-230">False</span></span>                                                                                |
| <span data-ttu-id="548db-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-231">Is Indexed</span></span>             | <span data-ttu-id="548db-232">否</span><span class="sxs-lookup"><span data-stu-id="548db-232">False</span></span>                                                                                |
| <span data-ttu-id="548db-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-233">In Global Catalog</span></span>      | <span data-ttu-id="548db-234">否</span><span class="sxs-lookup"><span data-stu-id="548db-234">False</span></span>                                                                                |
| <span data-ttu-id="548db-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-236">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-237">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-238">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-239">Search-Flags</span></span>           | <span data-ttu-id="548db-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-240">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-241">System-Flags</span></span>           | <span data-ttu-id="548db-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-242">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-243">Classes used in</span></span>        | [<span data-ttu-id="548db-244">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-244">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="548db-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="548db-245">Windows Server 2012</span></span>



| <span data-ttu-id="548db-246">進入</span><span class="sxs-lookup"><span data-stu-id="548db-246">Entry</span></span> | <span data-ttu-id="548db-247">值</span><span class="sxs-lookup"><span data-stu-id="548db-247">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="548db-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="548db-248">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="548db-249">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="548db-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="548db-250">System-Only</span></span>            | <span data-ttu-id="548db-251">否</span><span class="sxs-lookup"><span data-stu-id="548db-251">False</span></span>                                                                                |
| <span data-ttu-id="548db-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="548db-252">Is-Single-Valued</span></span>       | <span data-ttu-id="548db-253">否</span><span class="sxs-lookup"><span data-stu-id="548db-253">False</span></span>                                                                                |
| <span data-ttu-id="548db-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="548db-254">Is Indexed</span></span>             | <span data-ttu-id="548db-255">否</span><span class="sxs-lookup"><span data-stu-id="548db-255">False</span></span>                                                                                |
| <span data-ttu-id="548db-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="548db-256">In Global Catalog</span></span>      | <span data-ttu-id="548db-257">否</span><span class="sxs-lookup"><span data-stu-id="548db-257">False</span></span>                                                                                |
| <span data-ttu-id="548db-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="548db-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="548db-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="548db-259">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="548db-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="548db-260">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="548db-261">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="548db-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-262">Search-Flags</span></span>           | <span data-ttu-id="548db-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="548db-263">0x00000000</span></span>                                                                           |
| <span data-ttu-id="548db-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="548db-264">System-Flags</span></span>           | <span data-ttu-id="548db-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="548db-265">0x00000010</span></span>                                                                           |
| <span data-ttu-id="548db-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="548db-266">Classes used in</span></span>        | [<span data-ttu-id="548db-267">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="548db-267">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





