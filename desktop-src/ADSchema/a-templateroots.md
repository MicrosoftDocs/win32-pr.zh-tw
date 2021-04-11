---
title: Template-Roots 屬性
description: 這個屬性在 Exchange config 容器中用來指出範本容器的儲存位置。 此資訊供 Active Directory MAPI 提供者使用。
ms.assetid: 1416ce4a-ca07-4ca9-8ea1-e1a6ad19e7ad
ms.tgt_platform: multiple
keywords:
- Template-Roots 屬性 AD 架構
- templateRoots 屬性 AD 架構
topic_type:
- apiref
api_name:
- Template-Roots
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761c6d3d79bbf45e9a4d391b612956d6893cd314
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687127"
---
# <a name="template-roots-attribute"></a><span data-ttu-id="fcafa-106">Template-Roots 屬性</span><span class="sxs-lookup"><span data-stu-id="fcafa-106">Template-Roots attribute</span></span>

<span data-ttu-id="fcafa-107">這個屬性在 Exchange config 容器中用來指出範本容器的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="fcafa-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="fcafa-108">此資訊供 Active Directory MAPI 提供者使用。</span><span class="sxs-lookup"><span data-stu-id="fcafa-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="fcafa-109">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-109">Entry</span></span> | <span data-ttu-id="fcafa-110">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="fcafa-111">CN</span><span class="sxs-lookup"><span data-stu-id="fcafa-111">CN</span></span>                | <span data-ttu-id="fcafa-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="fcafa-112">Template-Roots</span></span>                          |
| <span data-ttu-id="fcafa-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fcafa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fcafa-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="fcafa-114">templateRoots</span></span>                           |
| <span data-ttu-id="fcafa-115">大小</span><span class="sxs-lookup"><span data-stu-id="fcafa-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="fcafa-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="fcafa-116">Update Privilege</span></span>  | <span data-ttu-id="fcafa-117">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="fcafa-117">This is used by the system.</span></span>             |
| <span data-ttu-id="fcafa-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="fcafa-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="fcafa-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-119">Attribute-Id</span></span>      | <span data-ttu-id="fcafa-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="fcafa-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="fcafa-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="fcafa-121">System-Id-Guid</span></span>    | <span data-ttu-id="fcafa-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="fcafa-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="fcafa-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcafa-123">Syntax</span></span>            | [<span data-ttu-id="fcafa-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="fcafa-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="fcafa-125">實作</span><span class="sxs-lookup"><span data-stu-id="fcafa-125">Implementations</span></span>

-   [<span data-ttu-id="fcafa-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fcafa-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fcafa-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fcafa-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fcafa-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fcafa-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fcafa-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fcafa-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fcafa-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fcafa-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fcafa-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fcafa-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fcafa-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fcafa-132">Windows 2000 Server</span></span>



| <span data-ttu-id="fcafa-133">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-133">Entry</span></span> | <span data-ttu-id="fcafa-134">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-137">System-Only</span></span>            | <span data-ttu-id="fcafa-138">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-138">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-139">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-140">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-140">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-141">Is Indexed</span></span>             | <span data-ttu-id="fcafa-142">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-142">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-143">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-144">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-144">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-149">Search-Flags</span></span>           | <span data-ttu-id="fcafa-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-151">System-Flags</span></span>           | <span data-ttu-id="fcafa-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-153">Classes used in</span></span>        | [<span data-ttu-id="fcafa-154">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fcafa-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fcafa-155">Windows Server 2003</span></span>



| <span data-ttu-id="fcafa-156">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-156">Entry</span></span> | <span data-ttu-id="fcafa-157">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-160">System-Only</span></span>            | <span data-ttu-id="fcafa-161">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-161">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-163">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-163">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-164">Is Indexed</span></span>             | <span data-ttu-id="fcafa-165">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-165">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-166">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-167">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-167">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-172">Search-Flags</span></span>           | <span data-ttu-id="fcafa-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-174">System-Flags</span></span>           | <span data-ttu-id="fcafa-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-176">Classes used in</span></span>        | [<span data-ttu-id="fcafa-177">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fcafa-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fcafa-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fcafa-179">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-179">Entry</span></span> | <span data-ttu-id="fcafa-180">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-183">System-Only</span></span>            | <span data-ttu-id="fcafa-184">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-184">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-186">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-186">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-187">Is Indexed</span></span>             | <span data-ttu-id="fcafa-188">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-188">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-189">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-190">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-190">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-195">Search-Flags</span></span>           | <span data-ttu-id="fcafa-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-197">System-Flags</span></span>           | <span data-ttu-id="fcafa-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-199">Classes used in</span></span>        | [<span data-ttu-id="fcafa-200">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fcafa-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcafa-201">Windows Server 2008</span></span>



| <span data-ttu-id="fcafa-202">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-202">Entry</span></span> | <span data-ttu-id="fcafa-203">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-206">System-Only</span></span>            | <span data-ttu-id="fcafa-207">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-207">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-208">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-209">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-209">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-210">Is Indexed</span></span>             | <span data-ttu-id="fcafa-211">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-211">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-212">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-213">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-213">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-218">Search-Flags</span></span>           | <span data-ttu-id="fcafa-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-220">System-Flags</span></span>           | <span data-ttu-id="fcafa-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-222">Classes used in</span></span>        | [<span data-ttu-id="fcafa-223">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fcafa-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fcafa-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fcafa-225">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-225">Entry</span></span> | <span data-ttu-id="fcafa-226">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-229">System-Only</span></span>            | <span data-ttu-id="fcafa-230">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-230">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-231">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-232">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-232">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-233">Is Indexed</span></span>             | <span data-ttu-id="fcafa-234">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-234">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-235">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-236">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-236">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-241">Search-Flags</span></span>           | <span data-ttu-id="fcafa-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-243">System-Flags</span></span>           | <span data-ttu-id="fcafa-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-245">Classes used in</span></span>        | [<span data-ttu-id="fcafa-246">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fcafa-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fcafa-247">Windows Server 2012</span></span>



| <span data-ttu-id="fcafa-248">進入</span><span class="sxs-lookup"><span data-stu-id="fcafa-248">Entry</span></span> | <span data-ttu-id="fcafa-249">值</span><span class="sxs-lookup"><span data-stu-id="fcafa-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="fcafa-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fcafa-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="fcafa-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="fcafa-252">System-Only</span></span>            | <span data-ttu-id="fcafa-253">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-253">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="fcafa-254">Is-Single-Valued</span></span>       | <span data-ttu-id="fcafa-255">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-255">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="fcafa-256">Is Indexed</span></span>             | <span data-ttu-id="fcafa-257">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-257">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="fcafa-258">In Global Catalog</span></span>      | <span data-ttu-id="fcafa-259">否</span><span class="sxs-lookup"><span data-stu-id="fcafa-259">False</span></span>                                                                                |
| <span data-ttu-id="fcafa-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="fcafa-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="fcafa-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="fcafa-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="fcafa-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fcafa-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fcafa-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="fcafa-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-264">Search-Flags</span></span>           | <span data-ttu-id="fcafa-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fcafa-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="fcafa-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fcafa-266">System-Flags</span></span>           | <span data-ttu-id="fcafa-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fcafa-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="fcafa-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="fcafa-268">Classes used in</span></span>        | [<span data-ttu-id="fcafa-269">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="fcafa-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





