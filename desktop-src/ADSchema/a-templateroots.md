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
# <a name="template-roots-attribute"></a><span data-ttu-id="92c94-106">Template-Roots 屬性</span><span class="sxs-lookup"><span data-stu-id="92c94-106">Template-Roots attribute</span></span>

<span data-ttu-id="92c94-107">這個屬性在 Exchange config 容器中用來指出範本容器的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="92c94-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="92c94-108">此資訊供 Active Directory MAPI 提供者使用。</span><span class="sxs-lookup"><span data-stu-id="92c94-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="92c94-109">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-109">Entry</span></span> | <span data-ttu-id="92c94-110">值</span><span class="sxs-lookup"><span data-stu-id="92c94-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="92c94-111">CN</span><span class="sxs-lookup"><span data-stu-id="92c94-111">CN</span></span>                | <span data-ttu-id="92c94-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="92c94-112">Template-Roots</span></span>                          |
| <span data-ttu-id="92c94-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="92c94-113">Ldap-Display-Name</span></span> | <span data-ttu-id="92c94-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="92c94-114">templateRoots</span></span>                           |
| <span data-ttu-id="92c94-115">大小</span><span class="sxs-lookup"><span data-stu-id="92c94-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="92c94-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="92c94-116">Update Privilege</span></span>  | <span data-ttu-id="92c94-117">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="92c94-117">This is used by the system.</span></span>             |
| <span data-ttu-id="92c94-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="92c94-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="92c94-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-119">Attribute-Id</span></span>      | <span data-ttu-id="92c94-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="92c94-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="92c94-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="92c94-121">System-Id-Guid</span></span>    | <span data-ttu-id="92c94-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="92c94-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="92c94-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="92c94-123">Syntax</span></span>            | [<span data-ttu-id="92c94-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="92c94-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="92c94-125">實作</span><span class="sxs-lookup"><span data-stu-id="92c94-125">Implementations</span></span>

-   [<span data-ttu-id="92c94-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="92c94-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="92c94-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="92c94-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="92c94-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="92c94-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="92c94-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="92c94-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="92c94-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="92c94-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="92c94-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="92c94-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="92c94-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92c94-132">Windows 2000 Server</span></span>



| <span data-ttu-id="92c94-133">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-133">Entry</span></span> | <span data-ttu-id="92c94-134">值</span><span class="sxs-lookup"><span data-stu-id="92c94-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-137">System-Only</span></span>            | <span data-ttu-id="92c94-138">否</span><span class="sxs-lookup"><span data-stu-id="92c94-138">False</span></span>                                                                                |
| <span data-ttu-id="92c94-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-139">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-140">否</span><span class="sxs-lookup"><span data-stu-id="92c94-140">False</span></span>                                                                                |
| <span data-ttu-id="92c94-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-141">Is Indexed</span></span>             | <span data-ttu-id="92c94-142">否</span><span class="sxs-lookup"><span data-stu-id="92c94-142">False</span></span>                                                                                |
| <span data-ttu-id="92c94-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-143">In Global Catalog</span></span>      | <span data-ttu-id="92c94-144">否</span><span class="sxs-lookup"><span data-stu-id="92c94-144">False</span></span>                                                                                |
| <span data-ttu-id="92c94-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-149">Search-Flags</span></span>           | <span data-ttu-id="92c94-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-151">System-Flags</span></span>           | <span data-ttu-id="92c94-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-153">Classes used in</span></span>        | [<span data-ttu-id="92c94-154">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="92c94-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92c94-155">Windows Server 2003</span></span>



| <span data-ttu-id="92c94-156">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-156">Entry</span></span> | <span data-ttu-id="92c94-157">值</span><span class="sxs-lookup"><span data-stu-id="92c94-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-160">System-Only</span></span>            | <span data-ttu-id="92c94-161">否</span><span class="sxs-lookup"><span data-stu-id="92c94-161">False</span></span>                                                                                |
| <span data-ttu-id="92c94-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-162">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-163">否</span><span class="sxs-lookup"><span data-stu-id="92c94-163">False</span></span>                                                                                |
| <span data-ttu-id="92c94-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-164">Is Indexed</span></span>             | <span data-ttu-id="92c94-165">否</span><span class="sxs-lookup"><span data-stu-id="92c94-165">False</span></span>                                                                                |
| <span data-ttu-id="92c94-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-166">In Global Catalog</span></span>      | <span data-ttu-id="92c94-167">否</span><span class="sxs-lookup"><span data-stu-id="92c94-167">False</span></span>                                                                                |
| <span data-ttu-id="92c94-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-172">Search-Flags</span></span>           | <span data-ttu-id="92c94-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-174">System-Flags</span></span>           | <span data-ttu-id="92c94-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-176">Classes used in</span></span>        | [<span data-ttu-id="92c94-177">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="92c94-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="92c94-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="92c94-179">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-179">Entry</span></span> | <span data-ttu-id="92c94-180">值</span><span class="sxs-lookup"><span data-stu-id="92c94-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-183">System-Only</span></span>            | <span data-ttu-id="92c94-184">否</span><span class="sxs-lookup"><span data-stu-id="92c94-184">False</span></span>                                                                                |
| <span data-ttu-id="92c94-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-185">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-186">否</span><span class="sxs-lookup"><span data-stu-id="92c94-186">False</span></span>                                                                                |
| <span data-ttu-id="92c94-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-187">Is Indexed</span></span>             | <span data-ttu-id="92c94-188">否</span><span class="sxs-lookup"><span data-stu-id="92c94-188">False</span></span>                                                                                |
| <span data-ttu-id="92c94-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-189">In Global Catalog</span></span>      | <span data-ttu-id="92c94-190">否</span><span class="sxs-lookup"><span data-stu-id="92c94-190">False</span></span>                                                                                |
| <span data-ttu-id="92c94-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-195">Search-Flags</span></span>           | <span data-ttu-id="92c94-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-197">System-Flags</span></span>           | <span data-ttu-id="92c94-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-199">Classes used in</span></span>        | [<span data-ttu-id="92c94-200">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="92c94-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c94-201">Windows Server 2008</span></span>



| <span data-ttu-id="92c94-202">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-202">Entry</span></span> | <span data-ttu-id="92c94-203">值</span><span class="sxs-lookup"><span data-stu-id="92c94-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-206">System-Only</span></span>            | <span data-ttu-id="92c94-207">否</span><span class="sxs-lookup"><span data-stu-id="92c94-207">False</span></span>                                                                                |
| <span data-ttu-id="92c94-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-208">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-209">否</span><span class="sxs-lookup"><span data-stu-id="92c94-209">False</span></span>                                                                                |
| <span data-ttu-id="92c94-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-210">Is Indexed</span></span>             | <span data-ttu-id="92c94-211">否</span><span class="sxs-lookup"><span data-stu-id="92c94-211">False</span></span>                                                                                |
| <span data-ttu-id="92c94-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-212">In Global Catalog</span></span>      | <span data-ttu-id="92c94-213">否</span><span class="sxs-lookup"><span data-stu-id="92c94-213">False</span></span>                                                                                |
| <span data-ttu-id="92c94-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-218">Search-Flags</span></span>           | <span data-ttu-id="92c94-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-220">System-Flags</span></span>           | <span data-ttu-id="92c94-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-222">Classes used in</span></span>        | [<span data-ttu-id="92c94-223">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="92c94-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92c94-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="92c94-225">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-225">Entry</span></span> | <span data-ttu-id="92c94-226">值</span><span class="sxs-lookup"><span data-stu-id="92c94-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-229">System-Only</span></span>            | <span data-ttu-id="92c94-230">否</span><span class="sxs-lookup"><span data-stu-id="92c94-230">False</span></span>                                                                                |
| <span data-ttu-id="92c94-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-231">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-232">否</span><span class="sxs-lookup"><span data-stu-id="92c94-232">False</span></span>                                                                                |
| <span data-ttu-id="92c94-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-233">Is Indexed</span></span>             | <span data-ttu-id="92c94-234">否</span><span class="sxs-lookup"><span data-stu-id="92c94-234">False</span></span>                                                                                |
| <span data-ttu-id="92c94-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-235">In Global Catalog</span></span>      | <span data-ttu-id="92c94-236">否</span><span class="sxs-lookup"><span data-stu-id="92c94-236">False</span></span>                                                                                |
| <span data-ttu-id="92c94-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-241">Search-Flags</span></span>           | <span data-ttu-id="92c94-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-243">System-Flags</span></span>           | <span data-ttu-id="92c94-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-245">Classes used in</span></span>        | [<span data-ttu-id="92c94-246">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="92c94-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92c94-247">Windows Server 2012</span></span>



| <span data-ttu-id="92c94-248">進入</span><span class="sxs-lookup"><span data-stu-id="92c94-248">Entry</span></span> | <span data-ttu-id="92c94-249">值</span><span class="sxs-lookup"><span data-stu-id="92c94-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92c94-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="92c94-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="92c94-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="92c94-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="92c94-252">System-Only</span></span>            | <span data-ttu-id="92c94-253">否</span><span class="sxs-lookup"><span data-stu-id="92c94-253">False</span></span>                                                                                |
| <span data-ttu-id="92c94-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="92c94-254">Is-Single-Valued</span></span>       | <span data-ttu-id="92c94-255">否</span><span class="sxs-lookup"><span data-stu-id="92c94-255">False</span></span>                                                                                |
| <span data-ttu-id="92c94-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="92c94-256">Is Indexed</span></span>             | <span data-ttu-id="92c94-257">否</span><span class="sxs-lookup"><span data-stu-id="92c94-257">False</span></span>                                                                                |
| <span data-ttu-id="92c94-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="92c94-258">In Global Catalog</span></span>      | <span data-ttu-id="92c94-259">否</span><span class="sxs-lookup"><span data-stu-id="92c94-259">False</span></span>                                                                                |
| <span data-ttu-id="92c94-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="92c94-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="92c94-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="92c94-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="92c94-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="92c94-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="92c94-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="92c94-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-264">Search-Flags</span></span>           | <span data-ttu-id="92c94-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="92c94-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="92c94-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="92c94-266">System-Flags</span></span>           | <span data-ttu-id="92c94-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="92c94-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="92c94-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="92c94-268">Classes used in</span></span>        | [<span data-ttu-id="92c94-269">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="92c94-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





