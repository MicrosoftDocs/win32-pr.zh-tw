---
title: ms-chap-為屬性的部分複本-
description: HasPartialReplicaNCs 的反向連結。 識別哪些 Dc 將該分割區保留為部分複本。
ms.assetid: b194b28b-0a25-4ded-b90c-50865c88ee6a
ms.tgt_platform: multiple
keywords:
- ms DS-----------適用于屬性 AD 架構
- IsPartialReplicaFor 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Is-Partial-Replica-For
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1c6e239ef25f1603d78a11beb65ee6ab0b64a85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845167"
---
# <a name="ms-ds-is-partial-replica-for-attribute"></a><span data-ttu-id="f0c9f-106">ms-chap-為屬性的部分複本-</span><span class="sxs-lookup"><span data-stu-id="f0c9f-106">ms-DS-Is-Partial-Replica-For attribute</span></span>

<span data-ttu-id="f0c9f-107">[**HasPartialReplicaNCs**](a-haspartialreplicancs.md)的反向連結。</span><span class="sxs-lookup"><span data-stu-id="f0c9f-107">Backward link for [**hasPartialReplicaNCs**](a-haspartialreplicancs.md).</span></span> <span data-ttu-id="f0c9f-108">識別哪些 Dc 將該分割區保留為部分複本。</span><span class="sxs-lookup"><span data-stu-id="f0c9f-108">Identifies which DCs hold that partition as a partial replica.</span></span>



| <span data-ttu-id="f0c9f-109">進入</span><span class="sxs-lookup"><span data-stu-id="f0c9f-109">Entry</span></span> | <span data-ttu-id="f0c9f-110">值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f0c9f-111">CN</span><span class="sxs-lookup"><span data-stu-id="f0c9f-111">CN</span></span>                | <span data-ttu-id="f0c9f-112">ms-DS-Is-Partial-Replica-For</span><span class="sxs-lookup"><span data-stu-id="f0c9f-112">ms-DS-Is-Partial-Replica-For</span></span>            |
| <span data-ttu-id="f0c9f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f0c9f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f0c9f-114">msDS-IsPartialReplicaFor</span><span class="sxs-lookup"><span data-stu-id="f0c9f-114">msDS-IsPartialReplicaFor</span></span>                |
| <span data-ttu-id="f0c9f-115">大小</span><span class="sxs-lookup"><span data-stu-id="f0c9f-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="f0c9f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f0c9f-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="f0c9f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f0c9f-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="f0c9f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0c9f-118">Attribute-Id</span></span>      | <span data-ttu-id="f0c9f-119">1.2.840.113556.1.4.1934</span><span class="sxs-lookup"><span data-stu-id="f0c9f-119">1.2.840.113556.1.4.1934</span></span>                 |
| <span data-ttu-id="f0c9f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f0c9f-120">System-Id-Guid</span></span>    | <span data-ttu-id="f0c9f-121">37c94ff6-c6d4-498f-b2f9-c6f7f8647809</span><span class="sxs-lookup"><span data-stu-id="f0c9f-121">37c94ff6-c6d4-498f-b2f9-c6f7f8647809</span></span>    |
| <span data-ttu-id="f0c9f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0c9f-122">Syntax</span></span>            | [<span data-ttu-id="f0c9f-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f0c9f-124">實作</span><span class="sxs-lookup"><span data-stu-id="f0c9f-124">Implementations</span></span>

-   [<span data-ttu-id="f0c9f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0c9f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0c9f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="f0c9f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0c9f-128">Windows Server 2008</span></span>



| <span data-ttu-id="f0c9f-129">進入</span><span class="sxs-lookup"><span data-stu-id="f0c9f-129">Entry</span></span> | <span data-ttu-id="f0c9f-130">值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f0c9f-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0c9f-131">Link-Id</span></span>                | <span data-ttu-id="f0c9f-132">75</span><span class="sxs-lookup"><span data-stu-id="f0c9f-132">75</span></span>                              |
| <span data-ttu-id="f0c9f-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0c9f-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f0c9f-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0c9f-134">System-Only</span></span>            | <span data-ttu-id="f0c9f-135">對</span><span class="sxs-lookup"><span data-stu-id="f0c9f-135">True</span></span>                            |
| <span data-ttu-id="f0c9f-136">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f0c9f-137">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-137">False</span></span>                           |
| <span data-ttu-id="f0c9f-138">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0c9f-138">Is Indexed</span></span>             | <span data-ttu-id="f0c9f-139">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-139">False</span></span>                           |
| <span data-ttu-id="f0c9f-140">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0c9f-140">In Global Catalog</span></span>      | <span data-ttu-id="f0c9f-141">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-141">False</span></span>                           |
| <span data-ttu-id="f0c9f-142">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0c9f-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0c9f-143">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0c9f-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f0c9f-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0c9f-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0c9f-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-146">Search-Flags</span></span>           | <span data-ttu-id="f0c9f-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0c9f-147">0x00000000</span></span>                      |
| <span data-ttu-id="f0c9f-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-148">System-Flags</span></span>           | <span data-ttu-id="f0c9f-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f0c9f-149">0x00000011</span></span>                      |
| <span data-ttu-id="f0c9f-150">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0c9f-150">Classes used in</span></span>        | [<span data-ttu-id="f0c9f-151">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0c9f-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0c9f-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0c9f-153">進入</span><span class="sxs-lookup"><span data-stu-id="f0c9f-153">Entry</span></span> | <span data-ttu-id="f0c9f-154">值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f0c9f-155">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0c9f-155">Link-Id</span></span>                | <span data-ttu-id="f0c9f-156">75</span><span class="sxs-lookup"><span data-stu-id="f0c9f-156">75</span></span>                              |
| <span data-ttu-id="f0c9f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0c9f-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f0c9f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0c9f-158">System-Only</span></span>            | <span data-ttu-id="f0c9f-159">對</span><span class="sxs-lookup"><span data-stu-id="f0c9f-159">True</span></span>                            |
| <span data-ttu-id="f0c9f-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f0c9f-161">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-161">False</span></span>                           |
| <span data-ttu-id="f0c9f-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0c9f-162">Is Indexed</span></span>             | <span data-ttu-id="f0c9f-163">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-163">False</span></span>                           |
| <span data-ttu-id="f0c9f-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0c9f-164">In Global Catalog</span></span>      | <span data-ttu-id="f0c9f-165">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-165">False</span></span>                           |
| <span data-ttu-id="f0c9f-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0c9f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0c9f-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0c9f-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f0c9f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0c9f-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0c9f-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-170">Search-Flags</span></span>           | <span data-ttu-id="f0c9f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0c9f-171">0x00000000</span></span>                      |
| <span data-ttu-id="f0c9f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-172">System-Flags</span></span>           | <span data-ttu-id="f0c9f-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f0c9f-173">0x00000011</span></span>                      |
| <span data-ttu-id="f0c9f-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0c9f-174">Classes used in</span></span>        | [<span data-ttu-id="f0c9f-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0c9f-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0c9f-176">Windows Server 2012</span></span>



| <span data-ttu-id="f0c9f-177">進入</span><span class="sxs-lookup"><span data-stu-id="f0c9f-177">Entry</span></span> | <span data-ttu-id="f0c9f-178">值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="f0c9f-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0c9f-179">Link-Id</span></span>                | <span data-ttu-id="f0c9f-180">75</span><span class="sxs-lookup"><span data-stu-id="f0c9f-180">75</span></span>                              |
| <span data-ttu-id="f0c9f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0c9f-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="f0c9f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0c9f-182">System-Only</span></span>            | <span data-ttu-id="f0c9f-183">對</span><span class="sxs-lookup"><span data-stu-id="f0c9f-183">True</span></span>                            |
| <span data-ttu-id="f0c9f-184">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0c9f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f0c9f-185">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-185">False</span></span>                           |
| <span data-ttu-id="f0c9f-186">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0c9f-186">Is Indexed</span></span>             | <span data-ttu-id="f0c9f-187">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-187">False</span></span>                           |
| <span data-ttu-id="f0c9f-188">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0c9f-188">In Global Catalog</span></span>      | <span data-ttu-id="f0c9f-189">否</span><span class="sxs-lookup"><span data-stu-id="f0c9f-189">False</span></span>                           |
| <span data-ttu-id="f0c9f-190">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0c9f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0c9f-191">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0c9f-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="f0c9f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0c9f-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0c9f-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="f0c9f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-194">Search-Flags</span></span>           | <span data-ttu-id="f0c9f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0c9f-195">0x00000000</span></span>                      |
| <span data-ttu-id="f0c9f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0c9f-196">System-Flags</span></span>           | <span data-ttu-id="f0c9f-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="f0c9f-197">0x00000011</span></span>                      |
| <span data-ttu-id="f0c9f-198">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0c9f-198">Classes used in</span></span>        | [<span data-ttu-id="f0c9f-199">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="f0c9f-199">**Top**</span></span>](c-top.md)<br/> |



 

 





