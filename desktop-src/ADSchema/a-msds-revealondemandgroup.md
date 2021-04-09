---
title: ms-DS-顯示 OnDemand-群組屬性
description: 與 Rodc 搭配使用，以定義哪些使用者、電腦和群組可以在 RODC 上快取其密碼。
ms.assetid: ee31957c-66a2-49d8-865c-7f599754dcdd
ms.tgt_platform: multiple
keywords:
- ms-DS-顯示 OnDemand-群組屬性 AD 架構
- RevealOnDemandGroup 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Reveal-OnDemand-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc89e0aabf1d82a9b7171530c5d297c668dbcb99
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845123"
---
# <a name="ms-ds-reveal-ondemand-group-attribute"></a><span data-ttu-id="629e9-105">ms-DS-顯示 OnDemand-群組屬性</span><span class="sxs-lookup"><span data-stu-id="629e9-105">ms-DS-Reveal-OnDemand-Group attribute</span></span>

<span data-ttu-id="629e9-106">與 Rodc 搭配使用，以定義哪些使用者、電腦和群組可以在 RODC 上快取其密碼。</span><span class="sxs-lookup"><span data-stu-id="629e9-106">Used with RODCs to define which users, computers, and groups are allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="629e9-107">進入</span><span class="sxs-lookup"><span data-stu-id="629e9-107">Entry</span></span> | <span data-ttu-id="629e9-108">值</span><span class="sxs-lookup"><span data-stu-id="629e9-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="629e9-109">CN</span><span class="sxs-lookup"><span data-stu-id="629e9-109">CN</span></span>                | <span data-ttu-id="629e9-110">ms-DS-Reveal-OnDemand-Group</span><span class="sxs-lookup"><span data-stu-id="629e9-110">ms-DS-Reveal-OnDemand-Group</span></span>             |
| <span data-ttu-id="629e9-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="629e9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="629e9-112">msDS-RevealOnDemandGroup</span><span class="sxs-lookup"><span data-stu-id="629e9-112">msDS-RevealOnDemandGroup</span></span>                |
| <span data-ttu-id="629e9-113">大小</span><span class="sxs-lookup"><span data-stu-id="629e9-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="629e9-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="629e9-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="629e9-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="629e9-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="629e9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="629e9-116">Attribute-Id</span></span>      | <span data-ttu-id="629e9-117">1.2.840.113556.1.4.1928</span><span class="sxs-lookup"><span data-stu-id="629e9-117">1.2.840.113556.1.4.1928</span></span>                 |
| <span data-ttu-id="629e9-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="629e9-118">System-Id-Guid</span></span>    | <span data-ttu-id="629e9-119">303d9f4a-1dd6-4b38-8fc5-33afe8c988ad</span><span class="sxs-lookup"><span data-stu-id="629e9-119">303d9f4a-1dd6-4b38-8fc5-33afe8c988ad</span></span>    |
| <span data-ttu-id="629e9-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="629e9-120">Syntax</span></span>            | [<span data-ttu-id="629e9-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="629e9-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="629e9-122">實作</span><span class="sxs-lookup"><span data-stu-id="629e9-122">Implementations</span></span>

-   [<span data-ttu-id="629e9-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="629e9-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="629e9-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="629e9-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="629e9-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="629e9-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="629e9-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="629e9-126">Windows Server 2008</span></span>



| <span data-ttu-id="629e9-127">進入</span><span class="sxs-lookup"><span data-stu-id="629e9-127">Entry</span></span> | <span data-ttu-id="629e9-128">值</span><span class="sxs-lookup"><span data-stu-id="629e9-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="629e9-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629e9-129">Link-Id</span></span>                | <span data-ttu-id="629e9-130">2110</span><span class="sxs-lookup"><span data-stu-id="629e9-130">2110</span></span>                                                                               |
| <span data-ttu-id="629e9-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629e9-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="629e9-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="629e9-132">System-Only</span></span>            | <span data-ttu-id="629e9-133">否</span><span class="sxs-lookup"><span data-stu-id="629e9-133">False</span></span>                                                                              |
| <span data-ttu-id="629e9-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629e9-134">Is-Single-Valued</span></span>       | <span data-ttu-id="629e9-135">否</span><span class="sxs-lookup"><span data-stu-id="629e9-135">False</span></span>                                                                              |
| <span data-ttu-id="629e9-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629e9-136">Is Indexed</span></span>             | <span data-ttu-id="629e9-137">否</span><span class="sxs-lookup"><span data-stu-id="629e9-137">False</span></span>                                                                              |
| <span data-ttu-id="629e9-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629e9-138">In Global Catalog</span></span>      | <span data-ttu-id="629e9-139">否</span><span class="sxs-lookup"><span data-stu-id="629e9-139">False</span></span>                                                                              |
| <span data-ttu-id="629e9-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629e9-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="629e9-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629e9-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="629e9-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629e9-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629e9-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-144">Search-Flags</span></span>           | <span data-ttu-id="629e9-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629e9-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="629e9-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-146">System-Flags</span></span>           | <span data-ttu-id="629e9-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="629e9-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="629e9-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629e9-148">Classes used in</span></span>        | [<span data-ttu-id="629e9-149">**電腦**</span><span class="sxs-lookup"><span data-stu-id="629e9-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="629e9-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="629e9-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="629e9-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="629e9-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="629e9-152">進入</span><span class="sxs-lookup"><span data-stu-id="629e9-152">Entry</span></span> | <span data-ttu-id="629e9-153">值</span><span class="sxs-lookup"><span data-stu-id="629e9-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="629e9-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629e9-154">Link-Id</span></span>                | <span data-ttu-id="629e9-155">2110</span><span class="sxs-lookup"><span data-stu-id="629e9-155">2110</span></span>                                                                               |
| <span data-ttu-id="629e9-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629e9-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="629e9-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="629e9-157">System-Only</span></span>            | <span data-ttu-id="629e9-158">否</span><span class="sxs-lookup"><span data-stu-id="629e9-158">False</span></span>                                                                              |
| <span data-ttu-id="629e9-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629e9-159">Is-Single-Valued</span></span>       | <span data-ttu-id="629e9-160">否</span><span class="sxs-lookup"><span data-stu-id="629e9-160">False</span></span>                                                                              |
| <span data-ttu-id="629e9-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629e9-161">Is Indexed</span></span>             | <span data-ttu-id="629e9-162">否</span><span class="sxs-lookup"><span data-stu-id="629e9-162">False</span></span>                                                                              |
| <span data-ttu-id="629e9-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629e9-163">In Global Catalog</span></span>      | <span data-ttu-id="629e9-164">否</span><span class="sxs-lookup"><span data-stu-id="629e9-164">False</span></span>                                                                              |
| <span data-ttu-id="629e9-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629e9-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="629e9-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629e9-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="629e9-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629e9-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629e9-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-169">Search-Flags</span></span>           | <span data-ttu-id="629e9-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629e9-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="629e9-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-171">System-Flags</span></span>           | <span data-ttu-id="629e9-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="629e9-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="629e9-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629e9-173">Classes used in</span></span>        | [<span data-ttu-id="629e9-174">**電腦**</span><span class="sxs-lookup"><span data-stu-id="629e9-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="629e9-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="629e9-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="629e9-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="629e9-176">Windows Server 2012</span></span>



| <span data-ttu-id="629e9-177">進入</span><span class="sxs-lookup"><span data-stu-id="629e9-177">Entry</span></span> | <span data-ttu-id="629e9-178">值</span><span class="sxs-lookup"><span data-stu-id="629e9-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="629e9-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="629e9-179">Link-Id</span></span>                | <span data-ttu-id="629e9-180">2110</span><span class="sxs-lookup"><span data-stu-id="629e9-180">2110</span></span>                                                                               |
| <span data-ttu-id="629e9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="629e9-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="629e9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="629e9-182">System-Only</span></span>            | <span data-ttu-id="629e9-183">否</span><span class="sxs-lookup"><span data-stu-id="629e9-183">False</span></span>                                                                              |
| <span data-ttu-id="629e9-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="629e9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="629e9-185">否</span><span class="sxs-lookup"><span data-stu-id="629e9-185">False</span></span>                                                                              |
| <span data-ttu-id="629e9-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="629e9-186">Is Indexed</span></span>             | <span data-ttu-id="629e9-187">否</span><span class="sxs-lookup"><span data-stu-id="629e9-187">False</span></span>                                                                              |
| <span data-ttu-id="629e9-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="629e9-188">In Global Catalog</span></span>      | <span data-ttu-id="629e9-189">否</span><span class="sxs-lookup"><span data-stu-id="629e9-189">False</span></span>                                                                              |
| <span data-ttu-id="629e9-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="629e9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="629e9-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="629e9-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="629e9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="629e9-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="629e9-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="629e9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-194">Search-Flags</span></span>           | <span data-ttu-id="629e9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="629e9-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="629e9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="629e9-196">System-Flags</span></span>           | <span data-ttu-id="629e9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="629e9-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="629e9-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="629e9-198">Classes used in</span></span>        | [<span data-ttu-id="629e9-199">**電腦**</span><span class="sxs-lookup"><span data-stu-id="629e9-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="629e9-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="629e9-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





