---
title: ms-DS-網域-代表屬性
description: 適用于 Nc 的反向連結。 識別哪些 Dc 將該磁碟分割保留為其主域。 |ms-DS-網域-代表屬性
ms.assetid: ec63ddb4-c220-492b-92ce-e3da2069bcb8
ms.tgt_platform: multiple
keywords:
- ms-DS-網域-適用于屬性 AD 架構
- IsDomainFor 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Is-Domain-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56529497eb8081f53310e26b834194cdcdc11bf5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992673"
---
# <a name="ms-ds-is-domain-for-attribute"></a><span data-ttu-id="13af3-107">ms-DS-網域-代表屬性</span><span class="sxs-lookup"><span data-stu-id="13af3-107">ms-DS-Is-Domain-For attribute</span></span>

<span data-ttu-id="13af3-108">適用于 [**nc**](a-msds-hasdomainncs.md)的反向連結。</span><span class="sxs-lookup"><span data-stu-id="13af3-108">Backward link for [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md).</span></span> <span data-ttu-id="13af3-109">識別哪些 Dc 將該磁碟分割保留為其主域。</span><span class="sxs-lookup"><span data-stu-id="13af3-109">Identifies which DCs hold that partition as their primary domain.</span></span>



| <span data-ttu-id="13af3-110">進入</span><span class="sxs-lookup"><span data-stu-id="13af3-110">Entry</span></span> | <span data-ttu-id="13af3-111">值</span><span class="sxs-lookup"><span data-stu-id="13af3-111">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="13af3-112">CN</span><span class="sxs-lookup"><span data-stu-id="13af3-112">CN</span></span>                | <span data-ttu-id="13af3-113">ms-DS-Is-Domain-For</span><span class="sxs-lookup"><span data-stu-id="13af3-113">ms-DS-Is-Domain-For</span></span>                     |
| <span data-ttu-id="13af3-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="13af3-114">Ldap-Display-Name</span></span> | <span data-ttu-id="13af3-115">msDS-IsDomainFor</span><span class="sxs-lookup"><span data-stu-id="13af3-115">msDS-IsDomainFor</span></span>                        |
| <span data-ttu-id="13af3-116">大小</span><span class="sxs-lookup"><span data-stu-id="13af3-116">Size</span></span>              | \-                                      |
| <span data-ttu-id="13af3-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="13af3-117">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="13af3-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="13af3-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="13af3-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="13af3-119">Attribute-Id</span></span>      | <span data-ttu-id="13af3-120">1.2.840.113556.1.4.1933</span><span class="sxs-lookup"><span data-stu-id="13af3-120">1.2.840.113556.1.4.1933</span></span>                 |
| <span data-ttu-id="13af3-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="13af3-121">System-Id-Guid</span></span>    | <span data-ttu-id="13af3-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span><span class="sxs-lookup"><span data-stu-id="13af3-122">ff155a2a-44e5-4de0-8318-13a58988de4f</span></span>    |
| <span data-ttu-id="13af3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="13af3-123">Syntax</span></span>            | [<span data-ttu-id="13af3-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="13af3-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="13af3-125">實作</span><span class="sxs-lookup"><span data-stu-id="13af3-125">Implementations</span></span>

-   [<span data-ttu-id="13af3-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="13af3-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="13af3-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="13af3-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="13af3-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="13af3-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="13af3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13af3-129">Windows Server 2008</span></span>



| <span data-ttu-id="13af3-130">進入</span><span class="sxs-lookup"><span data-stu-id="13af3-130">Entry</span></span> | <span data-ttu-id="13af3-131">值</span><span class="sxs-lookup"><span data-stu-id="13af3-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="13af3-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13af3-132">Link-Id</span></span>                | <span data-ttu-id="13af3-133">2027</span><span class="sxs-lookup"><span data-stu-id="13af3-133">2027</span></span>                            |
| <span data-ttu-id="13af3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13af3-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="13af3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="13af3-135">System-Only</span></span>            | <span data-ttu-id="13af3-136">對</span><span class="sxs-lookup"><span data-stu-id="13af3-136">True</span></span>                            |
| <span data-ttu-id="13af3-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13af3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="13af3-138">否</span><span class="sxs-lookup"><span data-stu-id="13af3-138">False</span></span>                           |
| <span data-ttu-id="13af3-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13af3-139">Is Indexed</span></span>             | <span data-ttu-id="13af3-140">否</span><span class="sxs-lookup"><span data-stu-id="13af3-140">False</span></span>                           |
| <span data-ttu-id="13af3-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13af3-141">In Global Catalog</span></span>      | <span data-ttu-id="13af3-142">否</span><span class="sxs-lookup"><span data-stu-id="13af3-142">False</span></span>                           |
| <span data-ttu-id="13af3-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13af3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="13af3-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13af3-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="13af3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13af3-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="13af3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13af3-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="13af3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-147">Search-Flags</span></span>           | <span data-ttu-id="13af3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13af3-148">0x00000000</span></span>                      |
| <span data-ttu-id="13af3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-149">System-Flags</span></span>           | <span data-ttu-id="13af3-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="13af3-150">0x00000011</span></span>                      |
| <span data-ttu-id="13af3-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13af3-151">Classes used in</span></span>        | [<span data-ttu-id="13af3-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="13af3-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="13af3-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13af3-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="13af3-154">進入</span><span class="sxs-lookup"><span data-stu-id="13af3-154">Entry</span></span> | <span data-ttu-id="13af3-155">值</span><span class="sxs-lookup"><span data-stu-id="13af3-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="13af3-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13af3-156">Link-Id</span></span>                | <span data-ttu-id="13af3-157">2027</span><span class="sxs-lookup"><span data-stu-id="13af3-157">2027</span></span>                            |
| <span data-ttu-id="13af3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13af3-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="13af3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="13af3-159">System-Only</span></span>            | <span data-ttu-id="13af3-160">對</span><span class="sxs-lookup"><span data-stu-id="13af3-160">True</span></span>                            |
| <span data-ttu-id="13af3-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13af3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="13af3-162">否</span><span class="sxs-lookup"><span data-stu-id="13af3-162">False</span></span>                           |
| <span data-ttu-id="13af3-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13af3-163">Is Indexed</span></span>             | <span data-ttu-id="13af3-164">否</span><span class="sxs-lookup"><span data-stu-id="13af3-164">False</span></span>                           |
| <span data-ttu-id="13af3-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13af3-165">In Global Catalog</span></span>      | <span data-ttu-id="13af3-166">否</span><span class="sxs-lookup"><span data-stu-id="13af3-166">False</span></span>                           |
| <span data-ttu-id="13af3-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13af3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="13af3-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13af3-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="13af3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13af3-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="13af3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13af3-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="13af3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-171">Search-Flags</span></span>           | <span data-ttu-id="13af3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13af3-172">0x00000000</span></span>                      |
| <span data-ttu-id="13af3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-173">System-Flags</span></span>           | <span data-ttu-id="13af3-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="13af3-174">0x00000011</span></span>                      |
| <span data-ttu-id="13af3-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13af3-175">Classes used in</span></span>        | [<span data-ttu-id="13af3-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="13af3-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="13af3-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13af3-177">Windows Server 2012</span></span>



| <span data-ttu-id="13af3-178">進入</span><span class="sxs-lookup"><span data-stu-id="13af3-178">Entry</span></span> | <span data-ttu-id="13af3-179">值</span><span class="sxs-lookup"><span data-stu-id="13af3-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="13af3-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="13af3-180">Link-Id</span></span>                | <span data-ttu-id="13af3-181">2027</span><span class="sxs-lookup"><span data-stu-id="13af3-181">2027</span></span>                            |
| <span data-ttu-id="13af3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="13af3-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="13af3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="13af3-183">System-Only</span></span>            | <span data-ttu-id="13af3-184">對</span><span class="sxs-lookup"><span data-stu-id="13af3-184">True</span></span>                            |
| <span data-ttu-id="13af3-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="13af3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="13af3-186">否</span><span class="sxs-lookup"><span data-stu-id="13af3-186">False</span></span>                           |
| <span data-ttu-id="13af3-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="13af3-187">Is Indexed</span></span>             | <span data-ttu-id="13af3-188">否</span><span class="sxs-lookup"><span data-stu-id="13af3-188">False</span></span>                           |
| <span data-ttu-id="13af3-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="13af3-189">In Global Catalog</span></span>      | <span data-ttu-id="13af3-190">否</span><span class="sxs-lookup"><span data-stu-id="13af3-190">False</span></span>                           |
| <span data-ttu-id="13af3-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="13af3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="13af3-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="13af3-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="13af3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="13af3-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="13af3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="13af3-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="13af3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-195">Search-Flags</span></span>           | <span data-ttu-id="13af3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="13af3-196">0x00000000</span></span>                      |
| <span data-ttu-id="13af3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="13af3-197">System-Flags</span></span>           | <span data-ttu-id="13af3-198">0x00000011</span><span class="sxs-lookup"><span data-stu-id="13af3-198">0x00000011</span></span>                      |
| <span data-ttu-id="13af3-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="13af3-199">Classes used in</span></span>        | [<span data-ttu-id="13af3-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="13af3-200">**Top**</span></span>](c-top.md)<br/> |



 

 





