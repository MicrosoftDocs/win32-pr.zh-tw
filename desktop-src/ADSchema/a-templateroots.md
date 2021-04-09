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
# <a name="template-roots-attribute"></a><span data-ttu-id="9edb6-106">Template-Roots 屬性</span><span class="sxs-lookup"><span data-stu-id="9edb6-106">Template-Roots attribute</span></span>

<span data-ttu-id="9edb6-107">這個屬性在 Exchange config 容器中用來指出範本容器的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="9edb6-107">This attribute is used on the Exchange config container to indicate where the template containers are stored.</span></span> <span data-ttu-id="9edb6-108">此資訊供 Active Directory MAPI 提供者使用。</span><span class="sxs-lookup"><span data-stu-id="9edb6-108">This information is used by the Active Directory MAPI provider.</span></span>



| <span data-ttu-id="9edb6-109">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-109">Entry</span></span> | <span data-ttu-id="9edb6-110">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="9edb6-111">CN</span><span class="sxs-lookup"><span data-stu-id="9edb6-111">CN</span></span>                | <span data-ttu-id="9edb6-112">Template-Roots</span><span class="sxs-lookup"><span data-stu-id="9edb6-112">Template-Roots</span></span>                          |
| <span data-ttu-id="9edb6-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="9edb6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9edb6-114">templateRoots</span><span class="sxs-lookup"><span data-stu-id="9edb6-114">templateRoots</span></span>                           |
| <span data-ttu-id="9edb6-115">大小</span><span class="sxs-lookup"><span data-stu-id="9edb6-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="9edb6-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="9edb6-116">Update Privilege</span></span>  | <span data-ttu-id="9edb6-117">系統會使用此方法。</span><span class="sxs-lookup"><span data-stu-id="9edb6-117">This is used by the system.</span></span>             |
| <span data-ttu-id="9edb6-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="9edb6-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="9edb6-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-119">Attribute-Id</span></span>      | <span data-ttu-id="9edb6-120">1.2.840.113556.1.4.1346</span><span class="sxs-lookup"><span data-stu-id="9edb6-120">1.2.840.113556.1.4.1346</span></span>                 |
| <span data-ttu-id="9edb6-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="9edb6-121">System-Id-Guid</span></span>    | <span data-ttu-id="9edb6-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="9edb6-122">ed9de9a0-7041-11d2-9905-0000f87a57d4</span></span>    |
| <span data-ttu-id="9edb6-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="9edb6-123">Syntax</span></span>            | [<span data-ttu-id="9edb6-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="9edb6-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="9edb6-125">實作</span><span class="sxs-lookup"><span data-stu-id="9edb6-125">Implementations</span></span>

-   [<span data-ttu-id="9edb6-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9edb6-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9edb6-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9edb6-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9edb6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9edb6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9edb6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9edb6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9edb6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9edb6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9edb6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9edb6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9edb6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9edb6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="9edb6-133">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-133">Entry</span></span> | <span data-ttu-id="9edb6-134">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-135">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-136">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-137">System-Only</span></span>            | <span data-ttu-id="9edb6-138">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-138">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-139">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-140">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-140">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-141">Is Indexed</span></span>             | <span data-ttu-id="9edb6-142">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-142">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-143">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-144">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-144">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-146">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-147">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-148">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-149">Search-Flags</span></span>           | <span data-ttu-id="9edb6-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-150">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-151">System-Flags</span></span>           | <span data-ttu-id="9edb6-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-152">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-153">Classes used in</span></span>        | [<span data-ttu-id="9edb6-154">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-154">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9edb6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9edb6-155">Windows Server 2003</span></span>



| <span data-ttu-id="9edb6-156">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-156">Entry</span></span> | <span data-ttu-id="9edb6-157">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-158">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-159">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-160">System-Only</span></span>            | <span data-ttu-id="9edb6-161">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-161">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-163">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-163">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-164">Is Indexed</span></span>             | <span data-ttu-id="9edb6-165">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-165">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-166">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-167">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-167">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-169">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-170">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-171">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-172">Search-Flags</span></span>           | <span data-ttu-id="9edb6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-173">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-174">System-Flags</span></span>           | <span data-ttu-id="9edb6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-175">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-176">Classes used in</span></span>        | [<span data-ttu-id="9edb6-177">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-177">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9edb6-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9edb6-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9edb6-179">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-179">Entry</span></span> | <span data-ttu-id="9edb6-180">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-181">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-182">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-183">System-Only</span></span>            | <span data-ttu-id="9edb6-184">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-184">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-185">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-186">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-186">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-187">Is Indexed</span></span>             | <span data-ttu-id="9edb6-188">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-188">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-189">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-190">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-190">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-192">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-193">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-194">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-195">Search-Flags</span></span>           | <span data-ttu-id="9edb6-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-196">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-197">System-Flags</span></span>           | <span data-ttu-id="9edb6-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-198">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-199">Classes used in</span></span>        | [<span data-ttu-id="9edb6-200">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-200">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9edb6-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9edb6-201">Windows Server 2008</span></span>



| <span data-ttu-id="9edb6-202">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-202">Entry</span></span> | <span data-ttu-id="9edb6-203">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-204">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-205">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-206">System-Only</span></span>            | <span data-ttu-id="9edb6-207">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-207">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-208">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-209">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-209">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-210">Is Indexed</span></span>             | <span data-ttu-id="9edb6-211">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-211">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-212">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-213">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-213">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-215">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-216">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-217">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-218">Search-Flags</span></span>           | <span data-ttu-id="9edb6-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-219">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-220">System-Flags</span></span>           | <span data-ttu-id="9edb6-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-221">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-222">Classes used in</span></span>        | [<span data-ttu-id="9edb6-223">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-223">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9edb6-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9edb6-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9edb6-225">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-225">Entry</span></span> | <span data-ttu-id="9edb6-226">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-227">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-228">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-229">System-Only</span></span>            | <span data-ttu-id="9edb6-230">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-230">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-231">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-232">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-232">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-233">Is Indexed</span></span>             | <span data-ttu-id="9edb6-234">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-234">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-235">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-236">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-236">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-238">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-239">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-240">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-241">Search-Flags</span></span>           | <span data-ttu-id="9edb6-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-242">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-243">System-Flags</span></span>           | <span data-ttu-id="9edb6-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-244">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-245">Classes used in</span></span>        | [<span data-ttu-id="9edb6-246">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-246">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9edb6-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9edb6-247">Windows Server 2012</span></span>



| <span data-ttu-id="9edb6-248">進入</span><span class="sxs-lookup"><span data-stu-id="9edb6-248">Entry</span></span> | <span data-ttu-id="9edb6-249">值</span><span class="sxs-lookup"><span data-stu-id="9edb6-249">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9edb6-250">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="9edb6-250">Link-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9edb6-251">MAPI-Id</span></span>                | \-                                                                                   |
| <span data-ttu-id="9edb6-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="9edb6-252">System-Only</span></span>            | <span data-ttu-id="9edb6-253">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-253">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-254">是-單一值</span><span class="sxs-lookup"><span data-stu-id="9edb6-254">Is-Single-Valued</span></span>       | <span data-ttu-id="9edb6-255">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-255">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-256">已編制索引</span><span class="sxs-lookup"><span data-stu-id="9edb6-256">Is Indexed</span></span>             | <span data-ttu-id="9edb6-257">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-257">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-258">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="9edb6-258">In Global Catalog</span></span>      | <span data-ttu-id="9edb6-259">否</span><span class="sxs-lookup"><span data-stu-id="9edb6-259">False</span></span>                                                                                |
| <span data-ttu-id="9edb6-260">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="9edb6-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="9edb6-261">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="9edb6-261">O:BAG:BAD:S:</span></span>                                                                         |
| <span data-ttu-id="9edb6-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9edb6-262">Range-Lower</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9edb6-263">Range-Upper</span></span>            | \-                                                                                   |
| <span data-ttu-id="9edb6-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-264">Search-Flags</span></span>           | <span data-ttu-id="9edb6-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9edb6-265">0x00000000</span></span>                                                                           |
| <span data-ttu-id="9edb6-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9edb6-266">System-Flags</span></span>           | <span data-ttu-id="9edb6-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9edb6-267">0x00000010</span></span>                                                                           |
| <span data-ttu-id="9edb6-268">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="9edb6-268">Classes used in</span></span>        | [<span data-ttu-id="9edb6-269">**Ms-exch-assistant-name-Configuration-容器**</span><span class="sxs-lookup"><span data-stu-id="9edb6-269">**ms-Exch-Configuration-Container**</span></span>](c-msexchconfigurationcontainer.md)<br/> |



 

 





