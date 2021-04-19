---
title: ms-chap-已滿-複本-代表屬性
description: 適用于 Nc 的反向連結。 識別哪些 Dc 將該磁碟分割保留為其主域。 |ms-chap-已滿-複本-代表屬性
ms.assetid: 0e5457e5-57c7-4896-9ea0-7fc2195a17e7
ms.tgt_platform: multiple
keywords:
- ms DS----------------attribute AD 架構
- IsFullReplicaFor 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Is-Full-Replica-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f2b8846c8f615a1251960c9ae3e7b06def08b9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988543"
---
# <a name="ms-ds-is-full-replica-for-attribute"></a><span data-ttu-id="04892-107">ms-chap-已滿-複本-代表屬性</span><span class="sxs-lookup"><span data-stu-id="04892-107">ms-DS-Is-Full-Replica-For attribute</span></span>

<span data-ttu-id="04892-108">適用于 [**nc**](a-msds-hasdomainncs.md)的反向連結。</span><span class="sxs-lookup"><span data-stu-id="04892-108">Backward link for [**ms-DS-Has-Domain-NCs**](a-msds-hasdomainncs.md).</span></span> <span data-ttu-id="04892-109">識別哪些 Dc 將該磁碟分割保留為其主域。</span><span class="sxs-lookup"><span data-stu-id="04892-109">Identifies which DCs hold that partition as their primary domain.</span></span>



| <span data-ttu-id="04892-110">進入</span><span class="sxs-lookup"><span data-stu-id="04892-110">Entry</span></span> | <span data-ttu-id="04892-111">值</span><span class="sxs-lookup"><span data-stu-id="04892-111">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="04892-112">CN</span><span class="sxs-lookup"><span data-stu-id="04892-112">CN</span></span>                | <span data-ttu-id="04892-113">ms-DS-Is-Full-Replica-For</span><span class="sxs-lookup"><span data-stu-id="04892-113">ms-DS-Is-Full-Replica-For</span></span>               |
| <span data-ttu-id="04892-114">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="04892-114">Ldap-Display-Name</span></span> | <span data-ttu-id="04892-115">msDS-IsFullReplicaFor</span><span class="sxs-lookup"><span data-stu-id="04892-115">msDS-IsFullReplicaFor</span></span>                   |
| <span data-ttu-id="04892-116">大小</span><span class="sxs-lookup"><span data-stu-id="04892-116">Size</span></span>              | \-                                      |
| <span data-ttu-id="04892-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="04892-117">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="04892-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="04892-118">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="04892-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04892-119">Attribute-Id</span></span>      | <span data-ttu-id="04892-120">1.2.840.113556.1.4.1932</span><span class="sxs-lookup"><span data-stu-id="04892-120">1.2.840.113556.1.4.1932</span></span>                 |
| <span data-ttu-id="04892-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="04892-121">System-Id-Guid</span></span>    | <span data-ttu-id="04892-122">c8bc72e0-a6b4-48f0-94a5-fd76a88c9987</span><span class="sxs-lookup"><span data-stu-id="04892-122">c8bc72e0-a6b4-48f0-94a5-fd76a88c9987</span></span>    |
| <span data-ttu-id="04892-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="04892-123">Syntax</span></span>            | [<span data-ttu-id="04892-124">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="04892-124">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="04892-125">實作</span><span class="sxs-lookup"><span data-stu-id="04892-125">Implementations</span></span>

-   [<span data-ttu-id="04892-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04892-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04892-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04892-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04892-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04892-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="04892-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04892-129">Windows Server 2008</span></span>



| <span data-ttu-id="04892-130">進入</span><span class="sxs-lookup"><span data-stu-id="04892-130">Entry</span></span> | <span data-ttu-id="04892-131">值</span><span class="sxs-lookup"><span data-stu-id="04892-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="04892-132">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="04892-132">Link-Id</span></span>                | <span data-ttu-id="04892-133">2105</span><span class="sxs-lookup"><span data-stu-id="04892-133">2105</span></span>                            |
| <span data-ttu-id="04892-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04892-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="04892-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="04892-135">System-Only</span></span>            | <span data-ttu-id="04892-136">對</span><span class="sxs-lookup"><span data-stu-id="04892-136">True</span></span>                            |
| <span data-ttu-id="04892-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="04892-137">Is-Single-Valued</span></span>       | <span data-ttu-id="04892-138">否</span><span class="sxs-lookup"><span data-stu-id="04892-138">False</span></span>                           |
| <span data-ttu-id="04892-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="04892-139">Is Indexed</span></span>             | <span data-ttu-id="04892-140">否</span><span class="sxs-lookup"><span data-stu-id="04892-140">False</span></span>                           |
| <span data-ttu-id="04892-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="04892-141">In Global Catalog</span></span>      | <span data-ttu-id="04892-142">否</span><span class="sxs-lookup"><span data-stu-id="04892-142">False</span></span>                           |
| <span data-ttu-id="04892-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="04892-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="04892-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="04892-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="04892-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04892-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="04892-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04892-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="04892-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-147">Search-Flags</span></span>           | <span data-ttu-id="04892-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04892-148">0x00000000</span></span>                      |
| <span data-ttu-id="04892-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-149">System-Flags</span></span>           | <span data-ttu-id="04892-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04892-150">0x00000011</span></span>                      |
| <span data-ttu-id="04892-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="04892-151">Classes used in</span></span>        | [<span data-ttu-id="04892-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="04892-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04892-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04892-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04892-154">進入</span><span class="sxs-lookup"><span data-stu-id="04892-154">Entry</span></span> | <span data-ttu-id="04892-155">值</span><span class="sxs-lookup"><span data-stu-id="04892-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="04892-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="04892-156">Link-Id</span></span>                | <span data-ttu-id="04892-157">2105</span><span class="sxs-lookup"><span data-stu-id="04892-157">2105</span></span>                            |
| <span data-ttu-id="04892-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04892-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="04892-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="04892-159">System-Only</span></span>            | <span data-ttu-id="04892-160">對</span><span class="sxs-lookup"><span data-stu-id="04892-160">True</span></span>                            |
| <span data-ttu-id="04892-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="04892-161">Is-Single-Valued</span></span>       | <span data-ttu-id="04892-162">否</span><span class="sxs-lookup"><span data-stu-id="04892-162">False</span></span>                           |
| <span data-ttu-id="04892-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="04892-163">Is Indexed</span></span>             | <span data-ttu-id="04892-164">否</span><span class="sxs-lookup"><span data-stu-id="04892-164">False</span></span>                           |
| <span data-ttu-id="04892-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="04892-165">In Global Catalog</span></span>      | <span data-ttu-id="04892-166">否</span><span class="sxs-lookup"><span data-stu-id="04892-166">False</span></span>                           |
| <span data-ttu-id="04892-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="04892-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="04892-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="04892-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="04892-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04892-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="04892-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04892-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="04892-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-171">Search-Flags</span></span>           | <span data-ttu-id="04892-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04892-172">0x00000000</span></span>                      |
| <span data-ttu-id="04892-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-173">System-Flags</span></span>           | <span data-ttu-id="04892-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04892-174">0x00000011</span></span>                      |
| <span data-ttu-id="04892-175">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="04892-175">Classes used in</span></span>        | [<span data-ttu-id="04892-176">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="04892-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04892-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04892-177">Windows Server 2012</span></span>



| <span data-ttu-id="04892-178">進入</span><span class="sxs-lookup"><span data-stu-id="04892-178">Entry</span></span> | <span data-ttu-id="04892-179">值</span><span class="sxs-lookup"><span data-stu-id="04892-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="04892-180">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="04892-180">Link-Id</span></span>                | <span data-ttu-id="04892-181">2105</span><span class="sxs-lookup"><span data-stu-id="04892-181">2105</span></span>                            |
| <span data-ttu-id="04892-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04892-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="04892-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="04892-183">System-Only</span></span>            | <span data-ttu-id="04892-184">對</span><span class="sxs-lookup"><span data-stu-id="04892-184">True</span></span>                            |
| <span data-ttu-id="04892-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="04892-185">Is-Single-Valued</span></span>       | <span data-ttu-id="04892-186">否</span><span class="sxs-lookup"><span data-stu-id="04892-186">False</span></span>                           |
| <span data-ttu-id="04892-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="04892-187">Is Indexed</span></span>             | <span data-ttu-id="04892-188">否</span><span class="sxs-lookup"><span data-stu-id="04892-188">False</span></span>                           |
| <span data-ttu-id="04892-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="04892-189">In Global Catalog</span></span>      | <span data-ttu-id="04892-190">否</span><span class="sxs-lookup"><span data-stu-id="04892-190">False</span></span>                           |
| <span data-ttu-id="04892-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="04892-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="04892-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="04892-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="04892-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04892-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="04892-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04892-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="04892-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-195">Search-Flags</span></span>           | <span data-ttu-id="04892-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04892-196">0x00000000</span></span>                      |
| <span data-ttu-id="04892-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04892-197">System-Flags</span></span>           | <span data-ttu-id="04892-198">0x00000011</span><span class="sxs-lookup"><span data-stu-id="04892-198">0x00000011</span></span>                      |
| <span data-ttu-id="04892-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="04892-199">Classes used in</span></span>        | [<span data-ttu-id="04892-200">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="04892-200">**Top**</span></span>](c-top.md)<br/> |



 

 





