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
# <a name="instance-type-attribute"></a><span data-ttu-id="af87c-105">Instance-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="af87c-105">Instance-Type attribute</span></span>

<span data-ttu-id="af87c-106">用來指定如何在特定伺服器上具現化物件的位位。</span><span class="sxs-lookup"><span data-stu-id="af87c-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="af87c-107">即使複本已同步，這個屬性的值也可能會在不同的複本上有所不同。</span><span class="sxs-lookup"><span data-stu-id="af87c-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="af87c-108">這個屬性可以是零或一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="af87c-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="af87c-109">值</span><span class="sxs-lookup"><span data-stu-id="af87c-109">Value</span></span>      | <span data-ttu-id="af87c-110">描述</span><span class="sxs-lookup"><span data-stu-id="af87c-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af87c-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af87c-111">0x00000001</span></span> | <span data-ttu-id="af87c-112">命名內容的標頭。</span><span class="sxs-lookup"><span data-stu-id="af87c-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="af87c-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="af87c-113">0x00000002</span></span> | <span data-ttu-id="af87c-114">此複本未具現化。</span><span class="sxs-lookup"><span data-stu-id="af87c-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="af87c-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="af87c-115">0x00000004</span></span> | <span data-ttu-id="af87c-116">此物件在此目錄中為可寫入。</span><span class="sxs-lookup"><span data-stu-id="af87c-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="af87c-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-117">0x00000008</span></span> | <span data-ttu-id="af87c-118">此目錄上的命名內容會保留在此目錄上。</span><span class="sxs-lookup"><span data-stu-id="af87c-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="af87c-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="af87c-119">0x00000010</span></span> | <span data-ttu-id="af87c-120">命名內容正在使用複寫進行第一次的結構處理。</span><span class="sxs-lookup"><span data-stu-id="af87c-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="af87c-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="af87c-121">0x00000020</span></span> | <span data-ttu-id="af87c-122">正在從本機 DSA 移除命名內容。</span><span class="sxs-lookup"><span data-stu-id="af87c-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="af87c-123">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-123">Entry</span></span> | <span data-ttu-id="af87c-124">值</span><span class="sxs-lookup"><span data-stu-id="af87c-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="af87c-125">CN</span><span class="sxs-lookup"><span data-stu-id="af87c-125">CN</span></span>                | <span data-ttu-id="af87c-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="af87c-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="af87c-127">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="af87c-127">Ldap-Display-Name</span></span> | <span data-ttu-id="af87c-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="af87c-128">instanceType</span></span>                                   |
| <span data-ttu-id="af87c-129">大小</span><span class="sxs-lookup"><span data-stu-id="af87c-129">Size</span></span>              | <span data-ttu-id="af87c-130">4個位元組。</span><span class="sxs-lookup"><span data-stu-id="af87c-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="af87c-131">更新許可權</span><span class="sxs-lookup"><span data-stu-id="af87c-131">Update Privilege</span></span>  | <span data-ttu-id="af87c-132">此值是由架構管理員所設定。</span><span class="sxs-lookup"><span data-stu-id="af87c-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="af87c-133">更新頻率</span><span class="sxs-lookup"><span data-stu-id="af87c-133">Update Frequency</span></span>  | <span data-ttu-id="af87c-134">建立物件時。</span><span class="sxs-lookup"><span data-stu-id="af87c-134">When the object is created.</span></span>                    |
| <span data-ttu-id="af87c-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-135">Attribute-Id</span></span>      | <span data-ttu-id="af87c-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="af87c-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="af87c-137">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="af87c-137">System-Id-Guid</span></span>    | <span data-ttu-id="af87c-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="af87c-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="af87c-139">Syntax</span><span class="sxs-lookup"><span data-stu-id="af87c-139">Syntax</span></span>            | [<span data-ttu-id="af87c-140">**列舉型別**</span><span class="sxs-lookup"><span data-stu-id="af87c-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="af87c-141">實作</span><span class="sxs-lookup"><span data-stu-id="af87c-141">Implementations</span></span>

-   [<span data-ttu-id="af87c-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af87c-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af87c-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af87c-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af87c-144">**亞當**</span><span class="sxs-lookup"><span data-stu-id="af87c-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="af87c-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af87c-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af87c-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af87c-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af87c-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af87c-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af87c-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af87c-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af87c-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af87c-149">Windows 2000 Server</span></span>



| <span data-ttu-id="af87c-150">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-150">Entry</span></span> | <span data-ttu-id="af87c-151">值</span><span class="sxs-lookup"><span data-stu-id="af87c-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-152">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-153">MAPI-Id</span></span>                | <span data-ttu-id="af87c-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-154">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-155">System-Only</span></span>            | <span data-ttu-id="af87c-156">對</span><span class="sxs-lookup"><span data-stu-id="af87c-156">True</span></span>                            |
| <span data-ttu-id="af87c-157">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-157">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-158">對</span><span class="sxs-lookup"><span data-stu-id="af87c-158">True</span></span>                            |
| <span data-ttu-id="af87c-159">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-159">Is Indexed</span></span>             | <span data-ttu-id="af87c-160">否</span><span class="sxs-lookup"><span data-stu-id="af87c-160">False</span></span>                           |
| <span data-ttu-id="af87c-161">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-161">In Global Catalog</span></span>      | <span data-ttu-id="af87c-162">對</span><span class="sxs-lookup"><span data-stu-id="af87c-162">True</span></span>                            |
| <span data-ttu-id="af87c-163">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-164">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-167">Search-Flags</span></span>           | <span data-ttu-id="af87c-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-168">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-169">System-Flags</span></span>           | <span data-ttu-id="af87c-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-170">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-171">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-171">Classes used in</span></span>        | [<span data-ttu-id="af87c-172">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af87c-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af87c-173">Windows Server 2003</span></span>



| <span data-ttu-id="af87c-174">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-174">Entry</span></span> | <span data-ttu-id="af87c-175">值</span><span class="sxs-lookup"><span data-stu-id="af87c-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-176">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-177">MAPI-Id</span></span>                | <span data-ttu-id="af87c-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-178">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-179">System-Only</span></span>            | <span data-ttu-id="af87c-180">對</span><span class="sxs-lookup"><span data-stu-id="af87c-180">True</span></span>                            |
| <span data-ttu-id="af87c-181">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-181">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-182">對</span><span class="sxs-lookup"><span data-stu-id="af87c-182">True</span></span>                            |
| <span data-ttu-id="af87c-183">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-183">Is Indexed</span></span>             | <span data-ttu-id="af87c-184">否</span><span class="sxs-lookup"><span data-stu-id="af87c-184">False</span></span>                           |
| <span data-ttu-id="af87c-185">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-185">In Global Catalog</span></span>      | <span data-ttu-id="af87c-186">對</span><span class="sxs-lookup"><span data-stu-id="af87c-186">True</span></span>                            |
| <span data-ttu-id="af87c-187">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-188">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-191">Search-Flags</span></span>           | <span data-ttu-id="af87c-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-192">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-193">System-Flags</span></span>           | <span data-ttu-id="af87c-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-194">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-195">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-195">Classes used in</span></span>        | [<span data-ttu-id="af87c-196">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="af87c-197">亞當</span><span class="sxs-lookup"><span data-stu-id="af87c-197">ADAM</span></span>



| <span data-ttu-id="af87c-198">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-198">Entry</span></span> | <span data-ttu-id="af87c-199">值</span><span class="sxs-lookup"><span data-stu-id="af87c-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-200">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-201">MAPI-Id</span></span>                | <span data-ttu-id="af87c-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-202">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-203">System-Only</span></span>            | <span data-ttu-id="af87c-204">對</span><span class="sxs-lookup"><span data-stu-id="af87c-204">True</span></span>                            |
| <span data-ttu-id="af87c-205">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-206">對</span><span class="sxs-lookup"><span data-stu-id="af87c-206">True</span></span>                            |
| <span data-ttu-id="af87c-207">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-207">Is Indexed</span></span>             | <span data-ttu-id="af87c-208">否</span><span class="sxs-lookup"><span data-stu-id="af87c-208">False</span></span>                           |
| <span data-ttu-id="af87c-209">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-209">In Global Catalog</span></span>      | <span data-ttu-id="af87c-210">對</span><span class="sxs-lookup"><span data-stu-id="af87c-210">True</span></span>                            |
| <span data-ttu-id="af87c-211">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-212">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-215">Search-Flags</span></span>           | <span data-ttu-id="af87c-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-216">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-217">System-Flags</span></span>           | <span data-ttu-id="af87c-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-218">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-219">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-219">Classes used in</span></span>        | [<span data-ttu-id="af87c-220">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af87c-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af87c-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af87c-222">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-222">Entry</span></span> | <span data-ttu-id="af87c-223">值</span><span class="sxs-lookup"><span data-stu-id="af87c-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-224">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-225">MAPI-Id</span></span>                | <span data-ttu-id="af87c-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-226">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-227">System-Only</span></span>            | <span data-ttu-id="af87c-228">對</span><span class="sxs-lookup"><span data-stu-id="af87c-228">True</span></span>                            |
| <span data-ttu-id="af87c-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-230">對</span><span class="sxs-lookup"><span data-stu-id="af87c-230">True</span></span>                            |
| <span data-ttu-id="af87c-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-231">Is Indexed</span></span>             | <span data-ttu-id="af87c-232">否</span><span class="sxs-lookup"><span data-stu-id="af87c-232">False</span></span>                           |
| <span data-ttu-id="af87c-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-233">In Global Catalog</span></span>      | <span data-ttu-id="af87c-234">對</span><span class="sxs-lookup"><span data-stu-id="af87c-234">True</span></span>                            |
| <span data-ttu-id="af87c-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-239">Search-Flags</span></span>           | <span data-ttu-id="af87c-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-240">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-241">System-Flags</span></span>           | <span data-ttu-id="af87c-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-242">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-243">Classes used in</span></span>        | [<span data-ttu-id="af87c-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af87c-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af87c-245">Windows Server 2008</span></span>



| <span data-ttu-id="af87c-246">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-246">Entry</span></span> | <span data-ttu-id="af87c-247">值</span><span class="sxs-lookup"><span data-stu-id="af87c-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-249">MAPI-Id</span></span>                | <span data-ttu-id="af87c-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-250">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-251">System-Only</span></span>            | <span data-ttu-id="af87c-252">對</span><span class="sxs-lookup"><span data-stu-id="af87c-252">True</span></span>                            |
| <span data-ttu-id="af87c-253">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-254">對</span><span class="sxs-lookup"><span data-stu-id="af87c-254">True</span></span>                            |
| <span data-ttu-id="af87c-255">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-255">Is Indexed</span></span>             | <span data-ttu-id="af87c-256">否</span><span class="sxs-lookup"><span data-stu-id="af87c-256">False</span></span>                           |
| <span data-ttu-id="af87c-257">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-257">In Global Catalog</span></span>      | <span data-ttu-id="af87c-258">對</span><span class="sxs-lookup"><span data-stu-id="af87c-258">True</span></span>                            |
| <span data-ttu-id="af87c-259">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-260">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-263">Search-Flags</span></span>           | <span data-ttu-id="af87c-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-264">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-265">System-Flags</span></span>           | <span data-ttu-id="af87c-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-266">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-267">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-267">Classes used in</span></span>        | [<span data-ttu-id="af87c-268">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af87c-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af87c-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af87c-270">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-270">Entry</span></span> | <span data-ttu-id="af87c-271">值</span><span class="sxs-lookup"><span data-stu-id="af87c-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-272">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-273">MAPI-Id</span></span>                | <span data-ttu-id="af87c-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-274">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-275">System-Only</span></span>            | <span data-ttu-id="af87c-276">對</span><span class="sxs-lookup"><span data-stu-id="af87c-276">True</span></span>                            |
| <span data-ttu-id="af87c-277">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-277">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-278">對</span><span class="sxs-lookup"><span data-stu-id="af87c-278">True</span></span>                            |
| <span data-ttu-id="af87c-279">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-279">Is Indexed</span></span>             | <span data-ttu-id="af87c-280">否</span><span class="sxs-lookup"><span data-stu-id="af87c-280">False</span></span>                           |
| <span data-ttu-id="af87c-281">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-281">In Global Catalog</span></span>      | <span data-ttu-id="af87c-282">對</span><span class="sxs-lookup"><span data-stu-id="af87c-282">True</span></span>                            |
| <span data-ttu-id="af87c-283">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-284">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-287">Search-Flags</span></span>           | <span data-ttu-id="af87c-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-288">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-289">System-Flags</span></span>           | <span data-ttu-id="af87c-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-290">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-291">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-291">Classes used in</span></span>        | [<span data-ttu-id="af87c-292">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af87c-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af87c-293">Windows Server 2012</span></span>



| <span data-ttu-id="af87c-294">進入</span><span class="sxs-lookup"><span data-stu-id="af87c-294">Entry</span></span> | <span data-ttu-id="af87c-295">值</span><span class="sxs-lookup"><span data-stu-id="af87c-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="af87c-296">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="af87c-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="af87c-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af87c-297">MAPI-Id</span></span>                | <span data-ttu-id="af87c-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="af87c-298">0x80BD</span></span>                          |
| <span data-ttu-id="af87c-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="af87c-299">System-Only</span></span>            | <span data-ttu-id="af87c-300">對</span><span class="sxs-lookup"><span data-stu-id="af87c-300">True</span></span>                            |
| <span data-ttu-id="af87c-301">是-單一值</span><span class="sxs-lookup"><span data-stu-id="af87c-301">Is-Single-Valued</span></span>       | <span data-ttu-id="af87c-302">對</span><span class="sxs-lookup"><span data-stu-id="af87c-302">True</span></span>                            |
| <span data-ttu-id="af87c-303">已編制索引</span><span class="sxs-lookup"><span data-stu-id="af87c-303">Is Indexed</span></span>             | <span data-ttu-id="af87c-304">否</span><span class="sxs-lookup"><span data-stu-id="af87c-304">False</span></span>                           |
| <span data-ttu-id="af87c-305">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="af87c-305">In Global Catalog</span></span>      | <span data-ttu-id="af87c-306">對</span><span class="sxs-lookup"><span data-stu-id="af87c-306">True</span></span>                            |
| <span data-ttu-id="af87c-307">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="af87c-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="af87c-308">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="af87c-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="af87c-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af87c-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="af87c-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af87c-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="af87c-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-311">Search-Flags</span></span>           | <span data-ttu-id="af87c-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="af87c-312">0x00000008</span></span>                      |
| <span data-ttu-id="af87c-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af87c-313">System-Flags</span></span>           | <span data-ttu-id="af87c-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="af87c-314">0x00000012</span></span>                      |
| <span data-ttu-id="af87c-315">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="af87c-315">Classes used in</span></span>        | [<span data-ttu-id="af87c-316">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="af87c-316">**Top**</span></span>](c-top.md)<br/> |



 

 





