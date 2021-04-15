---
title: ms-DS-顯示的 Dsa 屬性
description: 以 ms DS 呈現的使用者反向連結。 識別哪個 RODC 保存該使用者的密碼。
ms.assetid: cd84db75-d961-4290-8aa7-2805febbd842
ms.tgt_platform: multiple
keywords:
- 以 ms DS 呈現的 Dsa 屬性 AD 架構
- RevealedDSAs 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Revealed-DSAs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77dfd69fafffc3286f0ff9419965d7ae9daaa0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467278"
---
# <a name="ms-ds-revealed-dsas-attribute"></a><span data-ttu-id="66347-106">ms-DS-顯示的 Dsa 屬性</span><span class="sxs-lookup"><span data-stu-id="66347-106">ms-DS-Revealed-DSAs attribute</span></span>

<span data-ttu-id="66347-107">以 [**MS DS**](a-msds-revealedusers.md)呈現的使用者反向連結。</span><span class="sxs-lookup"><span data-stu-id="66347-107">Backward link for [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span></span> <span data-ttu-id="66347-108">識別哪個 RODC 持有該使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="66347-108">Identifies which RODC holds that user's secret.</span></span>



| <span data-ttu-id="66347-109">進入</span><span class="sxs-lookup"><span data-stu-id="66347-109">Entry</span></span> | <span data-ttu-id="66347-110">值</span><span class="sxs-lookup"><span data-stu-id="66347-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="66347-111">CN</span><span class="sxs-lookup"><span data-stu-id="66347-111">CN</span></span>                | <span data-ttu-id="66347-112">ms-DS-Revealed-DSAs</span><span class="sxs-lookup"><span data-stu-id="66347-112">ms-DS-Revealed-DSAs</span></span>                     |
| <span data-ttu-id="66347-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="66347-113">Ldap-Display-Name</span></span> | <span data-ttu-id="66347-114">msDS-RevealedDSAs</span><span class="sxs-lookup"><span data-stu-id="66347-114">msDS-RevealedDSAs</span></span>                       |
| <span data-ttu-id="66347-115">大小</span><span class="sxs-lookup"><span data-stu-id="66347-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="66347-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="66347-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="66347-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="66347-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="66347-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66347-118">Attribute-Id</span></span>      | <span data-ttu-id="66347-119">1.2.840.113556.1.4.1930</span><span class="sxs-lookup"><span data-stu-id="66347-119">1.2.840.113556.1.4.1930</span></span>                 |
| <span data-ttu-id="66347-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="66347-120">System-Id-Guid</span></span>    | <span data-ttu-id="66347-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span><span class="sxs-lookup"><span data-stu-id="66347-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span></span>    |
| <span data-ttu-id="66347-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="66347-122">Syntax</span></span>            | [<span data-ttu-id="66347-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="66347-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="66347-124">實作</span><span class="sxs-lookup"><span data-stu-id="66347-124">Implementations</span></span>

-   [<span data-ttu-id="66347-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="66347-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="66347-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="66347-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="66347-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66347-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="66347-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66347-128">Windows Server 2008</span></span>



| <span data-ttu-id="66347-129">進入</span><span class="sxs-lookup"><span data-stu-id="66347-129">Entry</span></span> | <span data-ttu-id="66347-130">值</span><span class="sxs-lookup"><span data-stu-id="66347-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="66347-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66347-131">Link-Id</span></span>                | <span data-ttu-id="66347-132">2103</span><span class="sxs-lookup"><span data-stu-id="66347-132">2103</span></span>                            |
| <span data-ttu-id="66347-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66347-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="66347-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="66347-134">System-Only</span></span>            | <span data-ttu-id="66347-135">對</span><span class="sxs-lookup"><span data-stu-id="66347-135">True</span></span>                            |
| <span data-ttu-id="66347-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66347-136">Is-Single-Valued</span></span>       | <span data-ttu-id="66347-137">否</span><span class="sxs-lookup"><span data-stu-id="66347-137">False</span></span>                           |
| <span data-ttu-id="66347-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66347-138">Is Indexed</span></span>             | <span data-ttu-id="66347-139">否</span><span class="sxs-lookup"><span data-stu-id="66347-139">False</span></span>                           |
| <span data-ttu-id="66347-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66347-140">In Global Catalog</span></span>      | <span data-ttu-id="66347-141">否</span><span class="sxs-lookup"><span data-stu-id="66347-141">False</span></span>                           |
| <span data-ttu-id="66347-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66347-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="66347-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66347-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="66347-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66347-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="66347-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66347-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="66347-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-146">Search-Flags</span></span>           | <span data-ttu-id="66347-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66347-147">0x00000000</span></span>                      |
| <span data-ttu-id="66347-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-148">System-Flags</span></span>           | <span data-ttu-id="66347-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66347-149">0x00000011</span></span>                      |
| <span data-ttu-id="66347-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66347-150">Classes used in</span></span>        | [<span data-ttu-id="66347-151">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="66347-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="66347-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66347-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="66347-153">進入</span><span class="sxs-lookup"><span data-stu-id="66347-153">Entry</span></span> | <span data-ttu-id="66347-154">值</span><span class="sxs-lookup"><span data-stu-id="66347-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="66347-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66347-155">Link-Id</span></span>                | <span data-ttu-id="66347-156">2103</span><span class="sxs-lookup"><span data-stu-id="66347-156">2103</span></span>                            |
| <span data-ttu-id="66347-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66347-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="66347-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="66347-158">System-Only</span></span>            | <span data-ttu-id="66347-159">對</span><span class="sxs-lookup"><span data-stu-id="66347-159">True</span></span>                            |
| <span data-ttu-id="66347-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66347-160">Is-Single-Valued</span></span>       | <span data-ttu-id="66347-161">否</span><span class="sxs-lookup"><span data-stu-id="66347-161">False</span></span>                           |
| <span data-ttu-id="66347-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66347-162">Is Indexed</span></span>             | <span data-ttu-id="66347-163">否</span><span class="sxs-lookup"><span data-stu-id="66347-163">False</span></span>                           |
| <span data-ttu-id="66347-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66347-164">In Global Catalog</span></span>      | <span data-ttu-id="66347-165">否</span><span class="sxs-lookup"><span data-stu-id="66347-165">False</span></span>                           |
| <span data-ttu-id="66347-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66347-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="66347-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66347-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="66347-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66347-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="66347-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66347-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="66347-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-170">Search-Flags</span></span>           | <span data-ttu-id="66347-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66347-171">0x00000000</span></span>                      |
| <span data-ttu-id="66347-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-172">System-Flags</span></span>           | <span data-ttu-id="66347-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66347-173">0x00000011</span></span>                      |
| <span data-ttu-id="66347-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66347-174">Classes used in</span></span>        | [<span data-ttu-id="66347-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="66347-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="66347-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66347-176">Windows Server 2012</span></span>



| <span data-ttu-id="66347-177">進入</span><span class="sxs-lookup"><span data-stu-id="66347-177">Entry</span></span> | <span data-ttu-id="66347-178">值</span><span class="sxs-lookup"><span data-stu-id="66347-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="66347-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="66347-179">Link-Id</span></span>                | <span data-ttu-id="66347-180">2103</span><span class="sxs-lookup"><span data-stu-id="66347-180">2103</span></span>                            |
| <span data-ttu-id="66347-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66347-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="66347-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="66347-182">System-Only</span></span>            | <span data-ttu-id="66347-183">對</span><span class="sxs-lookup"><span data-stu-id="66347-183">True</span></span>                            |
| <span data-ttu-id="66347-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="66347-184">Is-Single-Valued</span></span>       | <span data-ttu-id="66347-185">否</span><span class="sxs-lookup"><span data-stu-id="66347-185">False</span></span>                           |
| <span data-ttu-id="66347-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="66347-186">Is Indexed</span></span>             | <span data-ttu-id="66347-187">否</span><span class="sxs-lookup"><span data-stu-id="66347-187">False</span></span>                           |
| <span data-ttu-id="66347-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="66347-188">In Global Catalog</span></span>      | <span data-ttu-id="66347-189">否</span><span class="sxs-lookup"><span data-stu-id="66347-189">False</span></span>                           |
| <span data-ttu-id="66347-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="66347-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="66347-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="66347-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="66347-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66347-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="66347-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66347-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="66347-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-194">Search-Flags</span></span>           | <span data-ttu-id="66347-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66347-195">0x00000000</span></span>                      |
| <span data-ttu-id="66347-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66347-196">System-Flags</span></span>           | <span data-ttu-id="66347-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="66347-197">0x00000011</span></span>                      |
| <span data-ttu-id="66347-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="66347-198">Classes used in</span></span>        | [<span data-ttu-id="66347-199">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="66347-199">**Top**</span></span>](c-top.md)<br/> |



 

 





