---
title: ms-DS-不顯示群組屬性
description: 與 Rodc 搭配使用，定義不允許在 RODC 上快取其密碼的使用者、電腦和群組。
ms.assetid: 203a660b-503e-4cf1-a796-eac024629b3e
ms.tgt_platform: multiple
keywords:
- ms-DS-不顯示群組屬性 AD 架構
- Msds-neverrevealgroup 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Never-Reveal-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1308fb1bc0818601a037e66b764e607c0a32532
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106970658"
---
# <a name="ms-ds-never-reveal-group-attribute"></a><span data-ttu-id="eeeed-105">ms-DS-不顯示群組屬性</span><span class="sxs-lookup"><span data-stu-id="eeeed-105">ms-DS-Never-Reveal-Group attribute</span></span>

<span data-ttu-id="eeeed-106">與 Rodc 搭配使用，定義不允許在 RODC 上快取其密碼的使用者、電腦和群組。</span><span class="sxs-lookup"><span data-stu-id="eeeed-106">Used with RODCs to define which users, computers, and groups are not allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="eeeed-107">進入</span><span class="sxs-lookup"><span data-stu-id="eeeed-107">Entry</span></span> | <span data-ttu-id="eeeed-108">值</span><span class="sxs-lookup"><span data-stu-id="eeeed-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="eeeed-109">CN</span><span class="sxs-lookup"><span data-stu-id="eeeed-109">CN</span></span>                | <span data-ttu-id="eeeed-110">ms-DS-Never-Reveal-Group</span><span class="sxs-lookup"><span data-stu-id="eeeed-110">ms-DS-Never-Reveal-Group</span></span>                |
| <span data-ttu-id="eeeed-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="eeeed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eeeed-112">msDS-NeverRevealGroup</span><span class="sxs-lookup"><span data-stu-id="eeeed-112">msDS-NeverRevealGroup</span></span>                   |
| <span data-ttu-id="eeeed-113">大小</span><span class="sxs-lookup"><span data-stu-id="eeeed-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="eeeed-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="eeeed-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="eeeed-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="eeeed-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="eeeed-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eeeed-116">Attribute-Id</span></span>      | <span data-ttu-id="eeeed-117">1.2.840.113556.1.4.1926</span><span class="sxs-lookup"><span data-stu-id="eeeed-117">1.2.840.113556.1.4.1926</span></span>                 |
| <span data-ttu-id="eeeed-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="eeeed-118">System-Id-Guid</span></span>    | <span data-ttu-id="eeeed-119">15585999-fd49-4d66-b25d-eeb96aba8174</span><span class="sxs-lookup"><span data-stu-id="eeeed-119">15585999-fd49-4d66-b25d-eeb96aba8174</span></span>    |
| <span data-ttu-id="eeeed-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeeed-120">Syntax</span></span>            | [<span data-ttu-id="eeeed-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="eeeed-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="eeeed-122">實作</span><span class="sxs-lookup"><span data-stu-id="eeeed-122">Implementations</span></span>

-   [<span data-ttu-id="eeeed-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eeeed-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eeeed-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eeeed-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eeeed-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eeeed-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="eeeed-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeeed-126">Windows Server 2008</span></span>



| <span data-ttu-id="eeeed-127">進入</span><span class="sxs-lookup"><span data-stu-id="eeeed-127">Entry</span></span> | <span data-ttu-id="eeeed-128">值</span><span class="sxs-lookup"><span data-stu-id="eeeed-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeed-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeeed-129">Link-Id</span></span>                | <span data-ttu-id="eeeed-130">2106</span><span class="sxs-lookup"><span data-stu-id="eeeed-130">2106</span></span>                                                                               |
| <span data-ttu-id="eeeed-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeeed-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="eeeed-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeeed-132">System-Only</span></span>            | <span data-ttu-id="eeeed-133">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-133">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeeed-134">Is-Single-Valued</span></span>       | <span data-ttu-id="eeeed-135">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-135">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeeed-136">Is Indexed</span></span>             | <span data-ttu-id="eeeed-137">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-137">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeeed-138">In Global Catalog</span></span>      | <span data-ttu-id="eeeed-139">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-139">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeeed-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeeed-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeeed-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="eeeed-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeeed-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeeed-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-144">Search-Flags</span></span>           | <span data-ttu-id="eeeed-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeeed-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="eeeed-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-146">System-Flags</span></span>           | <span data-ttu-id="eeeed-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eeeed-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="eeeed-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeeed-148">Classes used in</span></span>        | [<span data-ttu-id="eeeed-149">**電腦**</span><span class="sxs-lookup"><span data-stu-id="eeeed-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eeeed-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="eeeed-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eeeed-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eeeed-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eeeed-152">進入</span><span class="sxs-lookup"><span data-stu-id="eeeed-152">Entry</span></span> | <span data-ttu-id="eeeed-153">值</span><span class="sxs-lookup"><span data-stu-id="eeeed-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeed-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeeed-154">Link-Id</span></span>                | <span data-ttu-id="eeeed-155">2106</span><span class="sxs-lookup"><span data-stu-id="eeeed-155">2106</span></span>                                                                               |
| <span data-ttu-id="eeeed-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeeed-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="eeeed-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeeed-157">System-Only</span></span>            | <span data-ttu-id="eeeed-158">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-158">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-159">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeeed-159">Is-Single-Valued</span></span>       | <span data-ttu-id="eeeed-160">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-160">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-161">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeeed-161">Is Indexed</span></span>             | <span data-ttu-id="eeeed-162">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-162">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-163">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeeed-163">In Global Catalog</span></span>      | <span data-ttu-id="eeeed-164">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-164">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-165">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeeed-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeeed-166">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeeed-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="eeeed-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeeed-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeeed-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-169">Search-Flags</span></span>           | <span data-ttu-id="eeeed-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeeed-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="eeeed-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-171">System-Flags</span></span>           | <span data-ttu-id="eeeed-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eeeed-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="eeeed-173">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeeed-173">Classes used in</span></span>        | [<span data-ttu-id="eeeed-174">**電腦**</span><span class="sxs-lookup"><span data-stu-id="eeeed-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eeeed-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="eeeed-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eeeed-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eeeed-176">Windows Server 2012</span></span>



| <span data-ttu-id="eeeed-177">進入</span><span class="sxs-lookup"><span data-stu-id="eeeed-177">Entry</span></span> | <span data-ttu-id="eeeed-178">值</span><span class="sxs-lookup"><span data-stu-id="eeeed-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeed-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="eeeed-179">Link-Id</span></span>                | <span data-ttu-id="eeeed-180">2106</span><span class="sxs-lookup"><span data-stu-id="eeeed-180">2106</span></span>                                                                               |
| <span data-ttu-id="eeeed-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eeeed-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="eeeed-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="eeeed-182">System-Only</span></span>            | <span data-ttu-id="eeeed-183">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-183">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="eeeed-184">Is-Single-Valued</span></span>       | <span data-ttu-id="eeeed-185">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-185">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="eeeed-186">Is Indexed</span></span>             | <span data-ttu-id="eeeed-187">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-187">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="eeeed-188">In Global Catalog</span></span>      | <span data-ttu-id="eeeed-189">否</span><span class="sxs-lookup"><span data-stu-id="eeeed-189">False</span></span>                                                                              |
| <span data-ttu-id="eeeed-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="eeeed-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="eeeed-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="eeeed-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="eeeed-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eeeed-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eeeed-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="eeeed-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-194">Search-Flags</span></span>           | <span data-ttu-id="eeeed-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eeeed-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="eeeed-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eeeed-196">System-Flags</span></span>           | <span data-ttu-id="eeeed-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eeeed-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="eeeed-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="eeeed-198">Classes used in</span></span>        | [<span data-ttu-id="eeeed-199">**電腦**</span><span class="sxs-lookup"><span data-stu-id="eeeed-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="eeeed-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="eeeed-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





