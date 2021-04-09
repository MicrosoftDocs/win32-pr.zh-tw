---
title: Enabled 屬性
description: 這個屬性是用來表示是否已啟用指定的交叉引用。
ms.assetid: 0c0ee4d7-0f0c-450e-9226-7dff03b68bcd
ms.tgt_platform: multiple
keywords:
- Enabled 屬性 AD 架構
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6d516770adf025ef673686ce1632dd8ec4217c8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686868"
---
# <a name="enabled-attribute"></a><span data-ttu-id="b3d70-104">Enabled 屬性</span><span class="sxs-lookup"><span data-stu-id="b3d70-104">Enabled attribute</span></span>

<span data-ttu-id="b3d70-105">這個屬性是用來表示是否已啟用指定的交叉引用。</span><span class="sxs-lookup"><span data-stu-id="b3d70-105">This attribute is used to signify whether a given crossRef is enabled.</span></span>



| <span data-ttu-id="b3d70-106">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-106">Entry</span></span> | <span data-ttu-id="b3d70-107">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-107">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b3d70-108">CN</span><span class="sxs-lookup"><span data-stu-id="b3d70-108">CN</span></span>                | <span data-ttu-id="b3d70-109">已啟用</span><span class="sxs-lookup"><span data-stu-id="b3d70-109">Enabled</span></span>                              |
| <span data-ttu-id="b3d70-110">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b3d70-110">Ldap-Display-Name</span></span> | <span data-ttu-id="b3d70-111">已啟用</span><span class="sxs-lookup"><span data-stu-id="b3d70-111">Enabled</span></span>                              |
| <span data-ttu-id="b3d70-112">大小</span><span class="sxs-lookup"><span data-stu-id="b3d70-112">Size</span></span>              | \-                                   |
| <span data-ttu-id="b3d70-113">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b3d70-113">Update Privilege</span></span>  | <span data-ttu-id="b3d70-114">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="b3d70-114">This value is set by the system.</span></span>     |
| <span data-ttu-id="b3d70-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b3d70-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b3d70-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-116">Attribute-Id</span></span>      | <span data-ttu-id="b3d70-117">1.2.840.113556.1.2.557</span><span class="sxs-lookup"><span data-stu-id="b3d70-117">1.2.840.113556.1.2.557</span></span>               |
| <span data-ttu-id="b3d70-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b3d70-118">System-Id-Guid</span></span>    | <span data-ttu-id="b3d70-119">a8df73f2-c5ea-11d1-bbcb-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b3d70-119">a8df73f2-c5ea-11d1-bbcb-0080c76670c0</span></span> |
| <span data-ttu-id="b3d70-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d70-120">Syntax</span></span>            | [<span data-ttu-id="b3d70-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b3d70-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b3d70-122">實作</span><span class="sxs-lookup"><span data-stu-id="b3d70-122">Implementations</span></span>

-   [<span data-ttu-id="b3d70-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3d70-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3d70-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3d70-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3d70-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b3d70-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b3d70-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3d70-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3d70-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3d70-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3d70-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3d70-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3d70-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3d70-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3d70-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3d70-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b3d70-131">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-131">Entry</span></span> | <span data-ttu-id="b3d70-132">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-134">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-135">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-135">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-136">System-Only</span></span>            | <span data-ttu-id="b3d70-137">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-137">False</span></span>                                      |
| <span data-ttu-id="b3d70-138">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-138">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-139">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-139">True</span></span>                                       |
| <span data-ttu-id="b3d70-140">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-140">Is Indexed</span></span>             | <span data-ttu-id="b3d70-141">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-141">False</span></span>                                      |
| <span data-ttu-id="b3d70-142">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-142">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-143">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-143">False</span></span>                                      |
| <span data-ttu-id="b3d70-144">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-145">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-148">Search-Flags</span></span>           | <span data-ttu-id="b3d70-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-149">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-150">System-Flags</span></span>           | <span data-ttu-id="b3d70-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-151">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-152">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-152">Classes used in</span></span>        | [<span data-ttu-id="b3d70-153">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3d70-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3d70-154">Windows Server 2003</span></span>



| <span data-ttu-id="b3d70-155">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-155">Entry</span></span> | <span data-ttu-id="b3d70-156">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-158">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-159">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-159">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-160">System-Only</span></span>            | <span data-ttu-id="b3d70-161">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-161">False</span></span>                                      |
| <span data-ttu-id="b3d70-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-163">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-163">True</span></span>                                       |
| <span data-ttu-id="b3d70-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-164">Is Indexed</span></span>             | <span data-ttu-id="b3d70-165">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-165">False</span></span>                                      |
| <span data-ttu-id="b3d70-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-166">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-167">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-167">False</span></span>                                      |
| <span data-ttu-id="b3d70-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-172">Search-Flags</span></span>           | <span data-ttu-id="b3d70-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-173">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-174">System-Flags</span></span>           | <span data-ttu-id="b3d70-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-175">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-176">Classes used in</span></span>        | [<span data-ttu-id="b3d70-177">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b3d70-178">亞當</span><span class="sxs-lookup"><span data-stu-id="b3d70-178">ADAM</span></span>



| <span data-ttu-id="b3d70-179">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-179">Entry</span></span> | <span data-ttu-id="b3d70-180">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d70-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-181">Link-Id</span></span>                | \-                                                                                                                                                                  |
| <span data-ttu-id="b3d70-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-182">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-183">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-183">0x8C21</span></span>                                                                                                                                                              |
| <span data-ttu-id="b3d70-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-184">System-Only</span></span>            | <span data-ttu-id="b3d70-185">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-185">False</span></span>                                                                                                                                                               |
| <span data-ttu-id="b3d70-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-187">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-187">True</span></span>                                                                                                                                                                |
| <span data-ttu-id="b3d70-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-188">Is Indexed</span></span>             | <span data-ttu-id="b3d70-189">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-189">False</span></span>                                                                                                                                                               |
| <span data-ttu-id="b3d70-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-190">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-191">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-191">False</span></span>                                                                                                                                                               |
| <span data-ttu-id="b3d70-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-193">O:BAG:BAD:S:</span></span>                                                                                                                                                        |
| <span data-ttu-id="b3d70-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-194">Range-Lower</span></span>            | \-                                                                                                                                                                  |
| <span data-ttu-id="b3d70-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-195">Range-Upper</span></span>            | \-                                                                                                                                                                  |
| <span data-ttu-id="b3d70-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-196">Search-Flags</span></span>           | <span data-ttu-id="b3d70-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-197">0x00000000</span></span>                                                                                                                                                          |
| <span data-ttu-id="b3d70-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-198">System-Flags</span></span>           | <span data-ttu-id="b3d70-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-199">0x00000010</span></span>                                                                                                                                                          |
| <span data-ttu-id="b3d70-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-200">Classes used in</span></span>        | [<span data-ttu-id="b3d70-201">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-201">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="b3d70-202">**ms-DS-服務-連接點-發行集-服務**</span><span class="sxs-lookup"><span data-stu-id="b3d70-202">**ms-DS-Service-Connection-Point-Publication-Service**</span></span>](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3d70-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3d70-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3d70-204">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-204">Entry</span></span> | <span data-ttu-id="b3d70-205">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-205">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-206">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-206">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-207">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-208">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-208">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-209">System-Only</span></span>            | <span data-ttu-id="b3d70-210">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-210">False</span></span>                                      |
| <span data-ttu-id="b3d70-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-212">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-212">True</span></span>                                       |
| <span data-ttu-id="b3d70-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-213">Is Indexed</span></span>             | <span data-ttu-id="b3d70-214">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-214">False</span></span>                                      |
| <span data-ttu-id="b3d70-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-215">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-216">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-216">False</span></span>                                      |
| <span data-ttu-id="b3d70-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-218">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-219">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-220">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-221">Search-Flags</span></span>           | <span data-ttu-id="b3d70-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-222">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-223">System-Flags</span></span>           | <span data-ttu-id="b3d70-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-224">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-225">Classes used in</span></span>        | [<span data-ttu-id="b3d70-226">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3d70-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3d70-227">Windows Server 2008</span></span>



| <span data-ttu-id="b3d70-228">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-228">Entry</span></span> | <span data-ttu-id="b3d70-229">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-229">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-230">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-231">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-232">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-232">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-233">System-Only</span></span>            | <span data-ttu-id="b3d70-234">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-234">False</span></span>                                      |
| <span data-ttu-id="b3d70-235">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-235">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-236">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-236">True</span></span>                                       |
| <span data-ttu-id="b3d70-237">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-237">Is Indexed</span></span>             | <span data-ttu-id="b3d70-238">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-238">False</span></span>                                      |
| <span data-ttu-id="b3d70-239">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-239">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-240">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-240">False</span></span>                                      |
| <span data-ttu-id="b3d70-241">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-242">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-242">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-243">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-244">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-245">Search-Flags</span></span>           | <span data-ttu-id="b3d70-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-246">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-247">System-Flags</span></span>           | <span data-ttu-id="b3d70-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-248">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-249">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-249">Classes used in</span></span>        | [<span data-ttu-id="b3d70-250">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3d70-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3d70-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3d70-252">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-252">Entry</span></span> | <span data-ttu-id="b3d70-253">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-253">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-254">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-254">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-255">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-256">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-256">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-257">System-Only</span></span>            | <span data-ttu-id="b3d70-258">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-258">False</span></span>                                      |
| <span data-ttu-id="b3d70-259">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-259">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-260">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-260">True</span></span>                                       |
| <span data-ttu-id="b3d70-261">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-261">Is Indexed</span></span>             | <span data-ttu-id="b3d70-262">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-262">False</span></span>                                      |
| <span data-ttu-id="b3d70-263">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-263">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-264">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-264">False</span></span>                                      |
| <span data-ttu-id="b3d70-265">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-266">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-266">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-267">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-268">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-269">Search-Flags</span></span>           | <span data-ttu-id="b3d70-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-270">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-271">System-Flags</span></span>           | <span data-ttu-id="b3d70-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-272">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-273">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-273">Classes used in</span></span>        | [<span data-ttu-id="b3d70-274">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3d70-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3d70-275">Windows Server 2012</span></span>



| <span data-ttu-id="b3d70-276">進入</span><span class="sxs-lookup"><span data-stu-id="b3d70-276">Entry</span></span> | <span data-ttu-id="b3d70-277">值</span><span class="sxs-lookup"><span data-stu-id="b3d70-277">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="b3d70-278">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d70-278">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="b3d70-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d70-279">MAPI-Id</span></span>                | <span data-ttu-id="b3d70-280">0x8C21</span><span class="sxs-lookup"><span data-stu-id="b3d70-280">0x8C21</span></span>                                     |
| <span data-ttu-id="b3d70-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d70-281">System-Only</span></span>            | <span data-ttu-id="b3d70-282">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-282">False</span></span>                                      |
| <span data-ttu-id="b3d70-283">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d70-283">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d70-284">對</span><span class="sxs-lookup"><span data-stu-id="b3d70-284">True</span></span>                                       |
| <span data-ttu-id="b3d70-285">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d70-285">Is Indexed</span></span>             | <span data-ttu-id="b3d70-286">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-286">False</span></span>                                      |
| <span data-ttu-id="b3d70-287">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d70-287">In Global Catalog</span></span>      | <span data-ttu-id="b3d70-288">否</span><span class="sxs-lookup"><span data-stu-id="b3d70-288">False</span></span>                                      |
| <span data-ttu-id="b3d70-289">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d70-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d70-290">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d70-290">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="b3d70-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d70-291">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d70-292">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="b3d70-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-293">Search-Flags</span></span>           | <span data-ttu-id="b3d70-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d70-294">0x00000000</span></span>                                 |
| <span data-ttu-id="b3d70-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d70-295">System-Flags</span></span>           | <span data-ttu-id="b3d70-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d70-296">0x00000010</span></span>                                 |
| <span data-ttu-id="b3d70-297">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d70-297">Classes used in</span></span>        | [<span data-ttu-id="b3d70-298">**交叉參考**</span><span class="sxs-lookup"><span data-stu-id="b3d70-298">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





