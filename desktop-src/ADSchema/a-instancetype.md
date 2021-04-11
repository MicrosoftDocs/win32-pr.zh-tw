---
title: Instance-Type 屬性
description: 用來指定如何在特定伺服器上具現化物件的位位。
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Instance-Type 屬性 AD 架構
- instanceType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687095"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="a66c4-105">Instance-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="a66c4-105">Instance-Type attribute</span></span>

<span data-ttu-id="a66c4-106">用來指定如何在特定伺服器上具現化物件的位位。</span><span class="sxs-lookup"><span data-stu-id="a66c4-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="a66c4-107">即使複本已同步，這個屬性的值也可能會在不同的複本上有所不同。</span><span class="sxs-lookup"><span data-stu-id="a66c4-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="a66c4-108">這個屬性可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="a66c4-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="a66c4-109">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-109">Value</span></span>      | <span data-ttu-id="a66c4-110">描述</span><span class="sxs-lookup"><span data-stu-id="a66c4-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a66c4-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a66c4-111">0x00000001</span></span> | <span data-ttu-id="a66c4-112">命名內容的標頭。</span><span class="sxs-lookup"><span data-stu-id="a66c4-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="a66c4-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a66c4-113">0x00000002</span></span> | <span data-ttu-id="a66c4-114">此複本未具現化。</span><span class="sxs-lookup"><span data-stu-id="a66c4-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="a66c4-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a66c4-115">0x00000004</span></span> | <span data-ttu-id="a66c4-116">此物件在此目錄中為可寫入。</span><span class="sxs-lookup"><span data-stu-id="a66c4-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="a66c4-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-117">0x00000008</span></span> | <span data-ttu-id="a66c4-118">此目錄上的命名內容會保留在此目錄上。</span><span class="sxs-lookup"><span data-stu-id="a66c4-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="a66c4-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a66c4-119">0x00000010</span></span> | <span data-ttu-id="a66c4-120">命名內容正在使用複寫進行第一次的結構處理。</span><span class="sxs-lookup"><span data-stu-id="a66c4-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="a66c4-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a66c4-121">0x00000020</span></span> | <span data-ttu-id="a66c4-122">正在從本機 DSA 移除命名內容。</span><span class="sxs-lookup"><span data-stu-id="a66c4-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="a66c4-123">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-123">Entry</span></span> | <span data-ttu-id="a66c4-124">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="a66c4-125">CN</span><span class="sxs-lookup"><span data-stu-id="a66c4-125">CN</span></span>                | <span data-ttu-id="a66c4-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="a66c4-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="a66c4-127">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="a66c4-127">Ldap-Display-Name</span></span> | <span data-ttu-id="a66c4-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="a66c4-128">instanceType</span></span>                                   |
| <span data-ttu-id="a66c4-129">大小</span><span class="sxs-lookup"><span data-stu-id="a66c4-129">Size</span></span>              | <span data-ttu-id="a66c4-130">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="a66c4-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="a66c4-131">更新許可權</span><span class="sxs-lookup"><span data-stu-id="a66c4-131">Update Privilege</span></span>  | <span data-ttu-id="a66c4-132">此值是由架構管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="a66c4-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="a66c4-133">更新頻率</span><span class="sxs-lookup"><span data-stu-id="a66c4-133">Update Frequency</span></span>  | <span data-ttu-id="a66c4-134">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="a66c4-134">When the object is created.</span></span>                    |
| <span data-ttu-id="a66c4-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-135">Attribute-Id</span></span>      | <span data-ttu-id="a66c4-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="a66c4-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="a66c4-137">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="a66c4-137">System-Id-Guid</span></span>    | <span data-ttu-id="a66c4-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a66c4-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="a66c4-139">Syntax</span><span class="sxs-lookup"><span data-stu-id="a66c4-139">Syntax</span></span>            | [<span data-ttu-id="a66c4-140">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="a66c4-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="a66c4-141">實作</span><span class="sxs-lookup"><span data-stu-id="a66c4-141">Implementations</span></span>

-   [<span data-ttu-id="a66c4-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a66c4-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a66c4-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a66c4-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a66c4-144">**亞當**</span><span class="sxs-lookup"><span data-stu-id="a66c4-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a66c4-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a66c4-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a66c4-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a66c4-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a66c4-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a66c4-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a66c4-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a66c4-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a66c4-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a66c4-149">Windows 2000 Server</span></span>



| <span data-ttu-id="a66c4-150">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-150">Entry</span></span> | <span data-ttu-id="a66c4-151">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-152">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-153">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-154">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-155">System-Only</span></span>            | <span data-ttu-id="a66c4-156">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-156">True</span></span>                            |
| <span data-ttu-id="a66c4-157">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-157">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-158">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-158">True</span></span>                            |
| <span data-ttu-id="a66c4-159">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-159">Is Indexed</span></span>             | <span data-ttu-id="a66c4-160">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-160">False</span></span>                           |
| <span data-ttu-id="a66c4-161">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-161">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-162">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-162">True</span></span>                            |
| <span data-ttu-id="a66c4-163">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-164">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-167">Search-Flags</span></span>           | <span data-ttu-id="a66c4-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-168">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-169">System-Flags</span></span>           | <span data-ttu-id="a66c4-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-170">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-171">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-171">Classes used in</span></span>        | [<span data-ttu-id="a66c4-172">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a66c4-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a66c4-173">Windows Server 2003</span></span>



| <span data-ttu-id="a66c4-174">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-174">Entry</span></span> | <span data-ttu-id="a66c4-175">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-177">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-178">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-179">System-Only</span></span>            | <span data-ttu-id="a66c4-180">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-180">True</span></span>                            |
| <span data-ttu-id="a66c4-181">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-181">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-182">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-182">True</span></span>                            |
| <span data-ttu-id="a66c4-183">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-183">Is Indexed</span></span>             | <span data-ttu-id="a66c4-184">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-184">False</span></span>                           |
| <span data-ttu-id="a66c4-185">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-185">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-186">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-186">True</span></span>                            |
| <span data-ttu-id="a66c4-187">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-188">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-191">Search-Flags</span></span>           | <span data-ttu-id="a66c4-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-192">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-193">System-Flags</span></span>           | <span data-ttu-id="a66c4-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-194">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-195">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-195">Classes used in</span></span>        | [<span data-ttu-id="a66c4-196">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a66c4-197">亞當</span><span class="sxs-lookup"><span data-stu-id="a66c4-197">ADAM</span></span>



| <span data-ttu-id="a66c4-198">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-198">Entry</span></span> | <span data-ttu-id="a66c4-199">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-200">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-201">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-202">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-203">System-Only</span></span>            | <span data-ttu-id="a66c4-204">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-204">True</span></span>                            |
| <span data-ttu-id="a66c4-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-206">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-206">True</span></span>                            |
| <span data-ttu-id="a66c4-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-207">Is Indexed</span></span>             | <span data-ttu-id="a66c4-208">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-208">False</span></span>                           |
| <span data-ttu-id="a66c4-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-209">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-210">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-210">True</span></span>                            |
| <span data-ttu-id="a66c4-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-215">Search-Flags</span></span>           | <span data-ttu-id="a66c4-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-216">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-217">System-Flags</span></span>           | <span data-ttu-id="a66c4-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-218">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-219">Classes used in</span></span>        | [<span data-ttu-id="a66c4-220">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a66c4-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a66c4-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a66c4-222">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-222">Entry</span></span> | <span data-ttu-id="a66c4-223">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-225">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-226">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-227">System-Only</span></span>            | <span data-ttu-id="a66c4-228">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-228">True</span></span>                            |
| <span data-ttu-id="a66c4-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-230">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-230">True</span></span>                            |
| <span data-ttu-id="a66c4-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-231">Is Indexed</span></span>             | <span data-ttu-id="a66c4-232">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-232">False</span></span>                           |
| <span data-ttu-id="a66c4-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-233">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-234">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-234">True</span></span>                            |
| <span data-ttu-id="a66c4-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-239">Search-Flags</span></span>           | <span data-ttu-id="a66c4-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-240">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-241">System-Flags</span></span>           | <span data-ttu-id="a66c4-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-242">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-243">Classes used in</span></span>        | [<span data-ttu-id="a66c4-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a66c4-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a66c4-245">Windows Server 2008</span></span>



| <span data-ttu-id="a66c4-246">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-246">Entry</span></span> | <span data-ttu-id="a66c4-247">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-249">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-250">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-251">System-Only</span></span>            | <span data-ttu-id="a66c4-252">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-252">True</span></span>                            |
| <span data-ttu-id="a66c4-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-254">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-254">True</span></span>                            |
| <span data-ttu-id="a66c4-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-255">Is Indexed</span></span>             | <span data-ttu-id="a66c4-256">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-256">False</span></span>                           |
| <span data-ttu-id="a66c4-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-257">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-258">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-258">True</span></span>                            |
| <span data-ttu-id="a66c4-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-263">Search-Flags</span></span>           | <span data-ttu-id="a66c4-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-264">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-265">System-Flags</span></span>           | <span data-ttu-id="a66c4-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-266">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-267">Classes used in</span></span>        | [<span data-ttu-id="a66c4-268">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a66c4-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a66c4-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a66c4-270">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-270">Entry</span></span> | <span data-ttu-id="a66c4-271">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-273">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-274">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-275">System-Only</span></span>            | <span data-ttu-id="a66c4-276">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-276">True</span></span>                            |
| <span data-ttu-id="a66c4-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-277">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-278">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-278">True</span></span>                            |
| <span data-ttu-id="a66c4-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-279">Is Indexed</span></span>             | <span data-ttu-id="a66c4-280">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-280">False</span></span>                           |
| <span data-ttu-id="a66c4-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-281">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-282">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-282">True</span></span>                            |
| <span data-ttu-id="a66c4-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-287">Search-Flags</span></span>           | <span data-ttu-id="a66c4-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-288">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-289">System-Flags</span></span>           | <span data-ttu-id="a66c4-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-290">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-291">Classes used in</span></span>        | [<span data-ttu-id="a66c4-292">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a66c4-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a66c4-293">Windows Server 2012</span></span>



| <span data-ttu-id="a66c4-294">進入</span><span class="sxs-lookup"><span data-stu-id="a66c4-294">Entry</span></span> | <span data-ttu-id="a66c4-295">值</span><span class="sxs-lookup"><span data-stu-id="a66c4-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="a66c4-296">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="a66c4-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="a66c4-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a66c4-297">MAPI-Id</span></span>                | <span data-ttu-id="a66c4-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="a66c4-298">0x80BD</span></span>                          |
| <span data-ttu-id="a66c4-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="a66c4-299">System-Only</span></span>            | <span data-ttu-id="a66c4-300">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-300">True</span></span>                            |
| <span data-ttu-id="a66c4-301">是-單一值</span><span class="sxs-lookup"><span data-stu-id="a66c4-301">Is-Single-Valued</span></span>       | <span data-ttu-id="a66c4-302">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-302">True</span></span>                            |
| <span data-ttu-id="a66c4-303">已編制索引</span><span class="sxs-lookup"><span data-stu-id="a66c4-303">Is Indexed</span></span>             | <span data-ttu-id="a66c4-304">否</span><span class="sxs-lookup"><span data-stu-id="a66c4-304">False</span></span>                           |
| <span data-ttu-id="a66c4-305">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="a66c4-305">In Global Catalog</span></span>      | <span data-ttu-id="a66c4-306">對</span><span class="sxs-lookup"><span data-stu-id="a66c4-306">True</span></span>                            |
| <span data-ttu-id="a66c4-307">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="a66c4-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="a66c4-308">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="a66c4-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="a66c4-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a66c4-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="a66c4-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a66c4-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="a66c4-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-311">Search-Flags</span></span>           | <span data-ttu-id="a66c4-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a66c4-312">0x00000008</span></span>                      |
| <span data-ttu-id="a66c4-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a66c4-313">System-Flags</span></span>           | <span data-ttu-id="a66c4-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="a66c4-314">0x00000012</span></span>                      |
| <span data-ttu-id="a66c4-315">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="a66c4-315">Classes used in</span></span>        | [<span data-ttu-id="a66c4-316">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="a66c4-316">**Top**</span></span>](c-top.md)<br/> |



 

 





