---
title: ms-FRS-拓撲-Pref 屬性
description: Pref 屬性是用來記錄慣用的 NTFRS 拓撲設定。
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- ms-chap-拓撲-Pref 屬性 AD 架構
- msFRS-拓撲-Pref 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687011"
---
# <a name="ms-frs-topology-pref-attribute"></a><span data-ttu-id="c4bed-105">ms-FRS-拓撲-Pref 屬性</span><span class="sxs-lookup"><span data-stu-id="c4bed-105">ms-FRS-Topology-Pref attribute</span></span>

<span data-ttu-id="c4bed-106">**Pref** 屬性是用來記錄慣用的 NTFRS 拓撲設定。</span><span class="sxs-lookup"><span data-stu-id="c4bed-106">The **ms-FRS-Topology-Pref** attribute is used to record the preferred NTFRS topology settings.</span></span> <span data-ttu-id="c4bed-107">將 FRS 成員新增或刪除至複本集時，會參考這些屬性，並在複本集中的其他 FRS 成員之間進行的連接調整。</span><span class="sxs-lookup"><span data-stu-id="c4bed-107">When an FRS member gets added or deleted to the replica set, these attributes are referred, and adjustments made to the connections between the rest of the FRS members in the replica set.</span></span>

<span data-ttu-id="c4bed-108">這個屬性的有效值如下所示。</span><span class="sxs-lookup"><span data-stu-id="c4bed-108">Valid values for this attribute are as follows.</span></span>

| <span data-ttu-id="c4bed-109">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-109">Value</span></span> | <span data-ttu-id="c4bed-110">描述</span><span class="sxs-lookup"><span data-stu-id="c4bed-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="c4bed-111">1</span><span class="sxs-lookup"><span data-stu-id="c4bed-111">1</span></span>     | <span data-ttu-id="c4bed-112">FRS \_ RSTOPOLOGYPREF \_ 環形</span><span class="sxs-lookup"><span data-stu-id="c4bed-112">FRS\_RSTOPOLOGYPREF\_RING</span></span><br/>     |
| <span data-ttu-id="c4bed-113">2</span><span class="sxs-lookup"><span data-stu-id="c4bed-113">2</span></span>     | <span data-ttu-id="c4bed-114">FRS \_ RSTOPOLOGYPREF \_ >PEER-HUBSPOKE</span><span class="sxs-lookup"><span data-stu-id="c4bed-114">FRS\_RSTOPOLOGYPREF\_HUBSPOKE</span></span><br/> |
| <span data-ttu-id="c4bed-115">3</span><span class="sxs-lookup"><span data-stu-id="c4bed-115">3</span></span>     | <span data-ttu-id="c4bed-116">FRS \_ RSTOPOLOGYPREF \_ FULLMESH</span><span class="sxs-lookup"><span data-stu-id="c4bed-116">FRS\_RSTOPOLOGYPREF\_FULLMESH</span></span><br/> |
| <span data-ttu-id="c4bed-117">4</span><span class="sxs-lookup"><span data-stu-id="c4bed-117">4</span></span>     | <span data-ttu-id="c4bed-118">FRS \_ RSTOPOLOGYPREF \_ 自訂</span><span class="sxs-lookup"><span data-stu-id="c4bed-118">FRS\_RSTOPOLOGYPREF\_CUSTOM</span></span><br/>   |



 



| <span data-ttu-id="c4bed-119">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-119">Entry</span></span> | <span data-ttu-id="c4bed-120">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-120">Value</span></span> |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c4bed-121">CN</span><span class="sxs-lookup"><span data-stu-id="c4bed-121">CN</span></span>                | <span data-ttu-id="c4bed-122">毫秒-FRS-拓撲-Pref</span><span class="sxs-lookup"><span data-stu-id="c4bed-122">ms-FRS-Topology-Pref</span></span>                                               |
| <span data-ttu-id="c4bed-123">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="c4bed-123">Ldap-Display-Name</span></span> | <span data-ttu-id="c4bed-124">msFRS-拓撲-Pref</span><span class="sxs-lookup"><span data-stu-id="c4bed-124">msFRS-Topology-Pref</span></span>                                                |
| <span data-ttu-id="c4bed-125">大小</span><span class="sxs-lookup"><span data-stu-id="c4bed-125">Size</span></span>              | \-                                                                 |
| <span data-ttu-id="c4bed-126">更新許可權</span><span class="sxs-lookup"><span data-stu-id="c4bed-126">Update Privilege</span></span>  | <span data-ttu-id="c4bed-127">網域系統管理員</span><span class="sxs-lookup"><span data-stu-id="c4bed-127">Domain administrator</span></span>                                               |
| <span data-ttu-id="c4bed-128">更新頻率</span><span class="sxs-lookup"><span data-stu-id="c4bed-128">Update Frequency</span></span>  | <span data-ttu-id="c4bed-129">建立複本集或偏好的拓撲變更時。</span><span class="sxs-lookup"><span data-stu-id="c4bed-129">When the replica set is created or the preferred topology changes.</span></span> |
| <span data-ttu-id="c4bed-130">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-130">Attribute-Id</span></span>      | <span data-ttu-id="c4bed-131">1.2.840.113556.1.4.1692</span><span class="sxs-lookup"><span data-stu-id="c4bed-131">1.2.840.113556.1.4.1692</span></span>                                            |
| <span data-ttu-id="c4bed-132">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="c4bed-132">System-Id-Guid</span></span>    | <span data-ttu-id="c4bed-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span><span class="sxs-lookup"><span data-stu-id="c4bed-133">92aa27e0-5c50-402d-9ec1-ee847def9788</span></span>                               |
| <span data-ttu-id="c4bed-134">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4bed-134">Syntax</span></span>            | [<span data-ttu-id="c4bed-135">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c4bed-135">**String(Unicode)**</span></span>](s-string-unicode.md)                        |



## <a name="implementations"></a><span data-ttu-id="c4bed-136">實作</span><span class="sxs-lookup"><span data-stu-id="c4bed-136">Implementations</span></span>

-   [<span data-ttu-id="c4bed-137">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c4bed-137">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c4bed-138">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c4bed-138">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c4bed-139">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c4bed-139">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c4bed-140">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c4bed-140">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c4bed-141">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c4bed-141">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c4bed-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4bed-142">Windows Server 2003</span></span>



| <span data-ttu-id="c4bed-143">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-143">Entry</span></span> | <span data-ttu-id="c4bed-144">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-144">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c4bed-145">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4bed-145">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-146">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-146">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-147">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4bed-147">System-Only</span></span>            | <span data-ttu-id="c4bed-148">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-148">False</span></span>                                                     |
| <span data-ttu-id="c4bed-149">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4bed-149">Is-Single-Valued</span></span>       | <span data-ttu-id="c4bed-150">對</span><span class="sxs-lookup"><span data-stu-id="c4bed-150">True</span></span>                                                      |
| <span data-ttu-id="c4bed-151">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4bed-151">Is Indexed</span></span>             | <span data-ttu-id="c4bed-152">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-152">False</span></span>                                                     |
| <span data-ttu-id="c4bed-153">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4bed-153">In Global Catalog</span></span>      | <span data-ttu-id="c4bed-154">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-154">False</span></span>                                                     |
| <span data-ttu-id="c4bed-155">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4bed-155">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4bed-156">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4bed-156">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c4bed-157">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4bed-157">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-158">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4bed-158">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-159">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-159">Search-Flags</span></span>           | <span data-ttu-id="c4bed-160">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-160">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-161">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-161">System-Flags</span></span>           | <span data-ttu-id="c4bed-162">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-162">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-163">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4bed-163">Classes used in</span></span>        | [<span data-ttu-id="c4bed-164">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c4bed-164">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c4bed-165">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c4bed-165">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c4bed-166">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-166">Entry</span></span> | <span data-ttu-id="c4bed-167">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-167">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c4bed-168">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4bed-168">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-169">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-169">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-170">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4bed-170">System-Only</span></span>            | <span data-ttu-id="c4bed-171">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-171">False</span></span>                                                     |
| <span data-ttu-id="c4bed-172">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4bed-172">Is-Single-Valued</span></span>       | <span data-ttu-id="c4bed-173">對</span><span class="sxs-lookup"><span data-stu-id="c4bed-173">True</span></span>                                                      |
| <span data-ttu-id="c4bed-174">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4bed-174">Is Indexed</span></span>             | <span data-ttu-id="c4bed-175">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-175">False</span></span>                                                     |
| <span data-ttu-id="c4bed-176">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4bed-176">In Global Catalog</span></span>      | <span data-ttu-id="c4bed-177">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-177">False</span></span>                                                     |
| <span data-ttu-id="c4bed-178">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4bed-178">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4bed-179">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4bed-179">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c4bed-180">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4bed-180">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-181">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4bed-181">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-182">Search-Flags</span></span>           | <span data-ttu-id="c4bed-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-183">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-184">System-Flags</span></span>           | <span data-ttu-id="c4bed-185">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-185">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-186">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4bed-186">Classes used in</span></span>        | [<span data-ttu-id="c4bed-187">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c4bed-187">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c4bed-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4bed-188">Windows Server 2008</span></span>



| <span data-ttu-id="c4bed-189">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-189">Entry</span></span> | <span data-ttu-id="c4bed-190">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-190">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c4bed-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4bed-191">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-192">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4bed-193">System-Only</span></span>            | <span data-ttu-id="c4bed-194">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-194">False</span></span>                                                     |
| <span data-ttu-id="c4bed-195">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4bed-195">Is-Single-Valued</span></span>       | <span data-ttu-id="c4bed-196">對</span><span class="sxs-lookup"><span data-stu-id="c4bed-196">True</span></span>                                                      |
| <span data-ttu-id="c4bed-197">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4bed-197">Is Indexed</span></span>             | <span data-ttu-id="c4bed-198">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-198">False</span></span>                                                     |
| <span data-ttu-id="c4bed-199">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4bed-199">In Global Catalog</span></span>      | <span data-ttu-id="c4bed-200">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-200">False</span></span>                                                     |
| <span data-ttu-id="c4bed-201">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4bed-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4bed-202">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4bed-202">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c4bed-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4bed-203">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4bed-204">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-205">Search-Flags</span></span>           | <span data-ttu-id="c4bed-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-206">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-207">System-Flags</span></span>           | <span data-ttu-id="c4bed-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-208">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-209">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4bed-209">Classes used in</span></span>        | [<span data-ttu-id="c4bed-210">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c4bed-210">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c4bed-211">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4bed-211">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c4bed-212">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-212">Entry</span></span> | <span data-ttu-id="c4bed-213">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-213">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c4bed-214">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4bed-214">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-215">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4bed-216">System-Only</span></span>            | <span data-ttu-id="c4bed-217">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-217">False</span></span>                                                     |
| <span data-ttu-id="c4bed-218">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4bed-218">Is-Single-Valued</span></span>       | <span data-ttu-id="c4bed-219">對</span><span class="sxs-lookup"><span data-stu-id="c4bed-219">True</span></span>                                                      |
| <span data-ttu-id="c4bed-220">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4bed-220">Is Indexed</span></span>             | <span data-ttu-id="c4bed-221">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-221">False</span></span>                                                     |
| <span data-ttu-id="c4bed-222">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4bed-222">In Global Catalog</span></span>      | <span data-ttu-id="c4bed-223">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-223">False</span></span>                                                     |
| <span data-ttu-id="c4bed-224">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4bed-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4bed-225">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4bed-225">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c4bed-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4bed-226">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4bed-227">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-228">Search-Flags</span></span>           | <span data-ttu-id="c4bed-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-229">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-230">System-Flags</span></span>           | <span data-ttu-id="c4bed-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-231">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-232">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4bed-232">Classes used in</span></span>        | [<span data-ttu-id="c4bed-233">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c4bed-233">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c4bed-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4bed-234">Windows Server 2012</span></span>



| <span data-ttu-id="c4bed-235">進入</span><span class="sxs-lookup"><span data-stu-id="c4bed-235">Entry</span></span> | <span data-ttu-id="c4bed-236">值</span><span class="sxs-lookup"><span data-stu-id="c4bed-236">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="c4bed-237">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="c4bed-237">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c4bed-238">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="c4bed-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="c4bed-239">System-Only</span></span>            | <span data-ttu-id="c4bed-240">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-240">False</span></span>                                                     |
| <span data-ttu-id="c4bed-241">是-單一值</span><span class="sxs-lookup"><span data-stu-id="c4bed-241">Is-Single-Valued</span></span>       | <span data-ttu-id="c4bed-242">對</span><span class="sxs-lookup"><span data-stu-id="c4bed-242">True</span></span>                                                      |
| <span data-ttu-id="c4bed-243">已編制索引</span><span class="sxs-lookup"><span data-stu-id="c4bed-243">Is Indexed</span></span>             | <span data-ttu-id="c4bed-244">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-244">False</span></span>                                                     |
| <span data-ttu-id="c4bed-245">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="c4bed-245">In Global Catalog</span></span>      | <span data-ttu-id="c4bed-246">否</span><span class="sxs-lookup"><span data-stu-id="c4bed-246">False</span></span>                                                     |
| <span data-ttu-id="c4bed-247">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="c4bed-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="c4bed-248">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="c4bed-248">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="c4bed-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c4bed-249">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c4bed-250">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="c4bed-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-251">Search-Flags</span></span>           | <span data-ttu-id="c4bed-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-252">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c4bed-253">System-Flags</span></span>           | <span data-ttu-id="c4bed-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c4bed-254">0x00000000</span></span>                                                |
| <span data-ttu-id="c4bed-255">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="c4bed-255">Classes used in</span></span>        | [<span data-ttu-id="c4bed-256">**NTFRS-複本集**</span><span class="sxs-lookup"><span data-stu-id="c4bed-256">**NTFRS-Replica-Set**</span></span>](c-ntfrsreplicaset.md)<br/> |



 

 





