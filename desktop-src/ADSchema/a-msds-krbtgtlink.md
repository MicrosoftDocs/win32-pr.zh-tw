---
title: ms DS-KrbTgt-連結屬性
description: 與 Rodc 搭配使用，以定義 \_ 每個 RODC 對應的 krbtgt XXXX 帳戶。
ms.assetid: 08c3e50f-7f2a-4746-86b6-77780316679c
ms.tgt_platform: multiple
keywords:
- ms DS-KrbTgt-連結屬性 AD 架構
- KrbTgtLink 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-KrbTgt-Link
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcf8ddfee6f15532e4dad91fc1e34e1f136ea99b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845487"
---
# <a name="ms-ds-krbtgt-link-attribute"></a><span data-ttu-id="75b7e-105">ms DS-KrbTgt-連結屬性</span><span class="sxs-lookup"><span data-stu-id="75b7e-105">ms-DS-KrbTgt-Link attribute</span></span>

<span data-ttu-id="75b7e-106">與 Rodc 搭配使用，以定義 \_ 每個 RODC 對應的 krbtgt XXXX 帳戶。</span><span class="sxs-lookup"><span data-stu-id="75b7e-106">Used with RODCs to define which krbtgt\_XXXX account corresponds to each RODC.</span></span>



| <span data-ttu-id="75b7e-107">進入</span><span class="sxs-lookup"><span data-stu-id="75b7e-107">Entry</span></span> | <span data-ttu-id="75b7e-108">值</span><span class="sxs-lookup"><span data-stu-id="75b7e-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="75b7e-109">CN</span><span class="sxs-lookup"><span data-stu-id="75b7e-109">CN</span></span>                | <span data-ttu-id="75b7e-110">ms-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="75b7e-110">ms-DS-KrbTgt-Link</span></span>                       |
| <span data-ttu-id="75b7e-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="75b7e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="75b7e-112">msDS-KrbTgtLink</span><span class="sxs-lookup"><span data-stu-id="75b7e-112">msDS-KrbTgtLink</span></span>                         |
| <span data-ttu-id="75b7e-113">大小</span><span class="sxs-lookup"><span data-stu-id="75b7e-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="75b7e-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="75b7e-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="75b7e-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="75b7e-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="75b7e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75b7e-116">Attribute-Id</span></span>      | <span data-ttu-id="75b7e-117">1.2.840.113556.1.4.1923</span><span class="sxs-lookup"><span data-stu-id="75b7e-117">1.2.840.113556.1.4.1923</span></span>                 |
| <span data-ttu-id="75b7e-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="75b7e-118">System-Id-Guid</span></span>    | <span data-ttu-id="75b7e-119">778ff5c9-6f4e-4b74-856a-d68383313910</span><span class="sxs-lookup"><span data-stu-id="75b7e-119">778ff5c9-6f4e-4b74-856a-d68383313910</span></span>    |
| <span data-ttu-id="75b7e-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b7e-120">Syntax</span></span>            | [<span data-ttu-id="75b7e-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="75b7e-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="75b7e-122">實作</span><span class="sxs-lookup"><span data-stu-id="75b7e-122">Implementations</span></span>

-   [<span data-ttu-id="75b7e-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75b7e-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75b7e-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75b7e-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75b7e-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75b7e-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="75b7e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75b7e-126">Windows Server 2008</span></span>



| <span data-ttu-id="75b7e-127">進入</span><span class="sxs-lookup"><span data-stu-id="75b7e-127">Entry</span></span> | <span data-ttu-id="75b7e-128">值</span><span class="sxs-lookup"><span data-stu-id="75b7e-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="75b7e-129">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75b7e-129">Link-Id</span></span>                | <span data-ttu-id="75b7e-130">2100</span><span class="sxs-lookup"><span data-stu-id="75b7e-130">2100</span></span>                                      |
| <span data-ttu-id="75b7e-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75b7e-131">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="75b7e-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="75b7e-132">System-Only</span></span>            | <span data-ttu-id="75b7e-133">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-133">False</span></span>                                     |
| <span data-ttu-id="75b7e-134">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75b7e-134">Is-Single-Valued</span></span>       | <span data-ttu-id="75b7e-135">對</span><span class="sxs-lookup"><span data-stu-id="75b7e-135">True</span></span>                                      |
| <span data-ttu-id="75b7e-136">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75b7e-136">Is Indexed</span></span>             | <span data-ttu-id="75b7e-137">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-137">False</span></span>                                     |
| <span data-ttu-id="75b7e-138">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75b7e-138">In Global Catalog</span></span>      | <span data-ttu-id="75b7e-139">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-139">False</span></span>                                     |
| <span data-ttu-id="75b7e-140">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75b7e-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="75b7e-141">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75b7e-141">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="75b7e-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75b7e-142">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75b7e-143">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-144">Search-Flags</span></span>           | <span data-ttu-id="75b7e-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75b7e-145">0x00000000</span></span>                                |
| <span data-ttu-id="75b7e-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-146">System-Flags</span></span>           | <span data-ttu-id="75b7e-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75b7e-147">0x00000010</span></span>                                |
| <span data-ttu-id="75b7e-148">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75b7e-148">Classes used in</span></span>        | [<span data-ttu-id="75b7e-149">**電腦**</span><span class="sxs-lookup"><span data-stu-id="75b7e-149">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75b7e-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75b7e-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75b7e-151">進入</span><span class="sxs-lookup"><span data-stu-id="75b7e-151">Entry</span></span> | <span data-ttu-id="75b7e-152">值</span><span class="sxs-lookup"><span data-stu-id="75b7e-152">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="75b7e-153">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75b7e-153">Link-Id</span></span>                | <span data-ttu-id="75b7e-154">2100</span><span class="sxs-lookup"><span data-stu-id="75b7e-154">2100</span></span>                                      |
| <span data-ttu-id="75b7e-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75b7e-155">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="75b7e-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="75b7e-156">System-Only</span></span>            | <span data-ttu-id="75b7e-157">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-157">False</span></span>                                     |
| <span data-ttu-id="75b7e-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75b7e-158">Is-Single-Valued</span></span>       | <span data-ttu-id="75b7e-159">對</span><span class="sxs-lookup"><span data-stu-id="75b7e-159">True</span></span>                                      |
| <span data-ttu-id="75b7e-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75b7e-160">Is Indexed</span></span>             | <span data-ttu-id="75b7e-161">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-161">False</span></span>                                     |
| <span data-ttu-id="75b7e-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75b7e-162">In Global Catalog</span></span>      | <span data-ttu-id="75b7e-163">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-163">False</span></span>                                     |
| <span data-ttu-id="75b7e-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75b7e-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="75b7e-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75b7e-165">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="75b7e-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75b7e-166">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75b7e-167">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-168">Search-Flags</span></span>           | <span data-ttu-id="75b7e-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75b7e-169">0x00000000</span></span>                                |
| <span data-ttu-id="75b7e-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-170">System-Flags</span></span>           | <span data-ttu-id="75b7e-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75b7e-171">0x00000010</span></span>                                |
| <span data-ttu-id="75b7e-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75b7e-172">Classes used in</span></span>        | [<span data-ttu-id="75b7e-173">**電腦**</span><span class="sxs-lookup"><span data-stu-id="75b7e-173">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75b7e-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75b7e-174">Windows Server 2012</span></span>



| <span data-ttu-id="75b7e-175">進入</span><span class="sxs-lookup"><span data-stu-id="75b7e-175">Entry</span></span> | <span data-ttu-id="75b7e-176">值</span><span class="sxs-lookup"><span data-stu-id="75b7e-176">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="75b7e-177">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="75b7e-177">Link-Id</span></span>                | <span data-ttu-id="75b7e-178">2100</span><span class="sxs-lookup"><span data-stu-id="75b7e-178">2100</span></span>                                      |
| <span data-ttu-id="75b7e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75b7e-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="75b7e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="75b7e-180">System-Only</span></span>            | <span data-ttu-id="75b7e-181">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-181">False</span></span>                                     |
| <span data-ttu-id="75b7e-182">是-單一值</span><span class="sxs-lookup"><span data-stu-id="75b7e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="75b7e-183">對</span><span class="sxs-lookup"><span data-stu-id="75b7e-183">True</span></span>                                      |
| <span data-ttu-id="75b7e-184">已編制索引</span><span class="sxs-lookup"><span data-stu-id="75b7e-184">Is Indexed</span></span>             | <span data-ttu-id="75b7e-185">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-185">False</span></span>                                     |
| <span data-ttu-id="75b7e-186">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="75b7e-186">In Global Catalog</span></span>      | <span data-ttu-id="75b7e-187">否</span><span class="sxs-lookup"><span data-stu-id="75b7e-187">False</span></span>                                     |
| <span data-ttu-id="75b7e-188">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="75b7e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="75b7e-189">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="75b7e-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="75b7e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75b7e-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75b7e-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="75b7e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-192">Search-Flags</span></span>           | <span data-ttu-id="75b7e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75b7e-193">0x00000000</span></span>                                |
| <span data-ttu-id="75b7e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75b7e-194">System-Flags</span></span>           | <span data-ttu-id="75b7e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75b7e-195">0x00000010</span></span>                                |
| <span data-ttu-id="75b7e-196">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="75b7e-196">Classes used in</span></span>        | [<span data-ttu-id="75b7e-197">**電腦**</span><span class="sxs-lookup"><span data-stu-id="75b7e-197">**Computer**</span></span>](c-computer.md)<br/> |



 

 





