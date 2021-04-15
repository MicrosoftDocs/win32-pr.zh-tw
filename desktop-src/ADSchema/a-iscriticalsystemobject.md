---
title: 為關鍵-系統物件屬性
description: 若為 TRUE，則在安裝新的複本期間，必須複寫裝載這個屬性的物件。
ms.assetid: 736c8b25-0f82-4b3c-a4fc-4643cd71474e
ms.tgt_platform: multiple
keywords:
- 為關鍵-系統物件屬性 AD 架構
- isCriticalSystemObject 屬性 AD 架構
topic_type:
- apiref
api_name:
- Is-Critical-System-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6030da908fe96a4bea5267872e8bae928a6555e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467180"
---
# <a name="is-critical-system-object-attribute"></a><span data-ttu-id="b3d2d-105">為關鍵-系統物件屬性</span><span class="sxs-lookup"><span data-stu-id="b3d2d-105">Is-Critical-System-Object attribute</span></span>

<span data-ttu-id="b3d2d-106">若 **為 TRUE**，則在安裝新的複本期間，必須複寫裝載這個屬性的物件。</span><span class="sxs-lookup"><span data-stu-id="b3d2d-106">If **TRUE**, the object hosting this attribute must be replicated during installation of a new replica.</span></span>



| <span data-ttu-id="b3d2d-107">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-107">Entry</span></span> | <span data-ttu-id="b3d2d-108">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b3d2d-109">CN</span><span class="sxs-lookup"><span data-stu-id="b3d2d-109">CN</span></span>                | <span data-ttu-id="b3d2d-110">為關鍵-系統物件</span><span class="sxs-lookup"><span data-stu-id="b3d2d-110">Is-Critical-System-Object</span></span>            |
| <span data-ttu-id="b3d2d-111">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b3d2d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b3d2d-112">isCriticalSystemObject</span><span class="sxs-lookup"><span data-stu-id="b3d2d-112">isCriticalSystemObject</span></span>               |
| <span data-ttu-id="b3d2d-113">大小</span><span class="sxs-lookup"><span data-stu-id="b3d2d-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b3d2d-114">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b3d2d-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b3d2d-115">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b3d2d-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b3d2d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-116">Attribute-Id</span></span>      | <span data-ttu-id="b3d2d-117">1.2.840.113556.1.4.868</span><span class="sxs-lookup"><span data-stu-id="b3d2d-117">1.2.840.113556.1.4.868</span></span>               |
| <span data-ttu-id="b3d2d-118">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b3d2d-118">System-Id-Guid</span></span>    | <span data-ttu-id="b3d2d-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b3d2d-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="b3d2d-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d2d-120">Syntax</span></span>            | [<span data-ttu-id="b3d2d-121">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b3d2d-122">實作</span><span class="sxs-lookup"><span data-stu-id="b3d2d-122">Implementations</span></span>

-   [<span data-ttu-id="b3d2d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b3d2d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b3d2d-125">**亞當**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b3d2d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b3d2d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b3d2d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b3d2d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b3d2d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3d2d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b3d2d-131">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-131">Entry</span></span> | <span data-ttu-id="b3d2d-132">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-133">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-135">System-Only</span></span>            | <span data-ttu-id="b3d2d-136">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-136">False</span></span>                           |
| <span data-ttu-id="b3d2d-137">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-138">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-138">True</span></span>                            |
| <span data-ttu-id="b3d2d-139">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-139">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-140">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-140">False</span></span>                           |
| <span data-ttu-id="b3d2d-141">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-141">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-142">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-142">False</span></span>                           |
| <span data-ttu-id="b3d2d-143">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-144">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-147">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-148">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-149">System-Flags</span></span>           | <span data-ttu-id="b3d2d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-150">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-151">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-152">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b3d2d-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3d2d-153">Windows Server 2003</span></span>



| <span data-ttu-id="b3d2d-154">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-154">Entry</span></span> | <span data-ttu-id="b3d2d-155">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-156">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-158">System-Only</span></span>            | <span data-ttu-id="b3d2d-159">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-159">False</span></span>                           |
| <span data-ttu-id="b3d2d-160">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-161">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-161">True</span></span>                            |
| <span data-ttu-id="b3d2d-162">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-162">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-163">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-163">False</span></span>                           |
| <span data-ttu-id="b3d2d-164">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-164">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-165">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-165">False</span></span>                           |
| <span data-ttu-id="b3d2d-166">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-167">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-170">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-171">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-172">System-Flags</span></span>           | <span data-ttu-id="b3d2d-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-173">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-174">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-174">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-175">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b3d2d-176">亞當</span><span class="sxs-lookup"><span data-stu-id="b3d2d-176">ADAM</span></span>



| <span data-ttu-id="b3d2d-177">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-177">Entry</span></span> | <span data-ttu-id="b3d2d-178">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-179">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-181">System-Only</span></span>            | <span data-ttu-id="b3d2d-182">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-182">False</span></span>                           |
| <span data-ttu-id="b3d2d-183">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-184">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-184">True</span></span>                            |
| <span data-ttu-id="b3d2d-185">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-185">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-186">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-186">False</span></span>                           |
| <span data-ttu-id="b3d2d-187">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-187">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-188">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-188">False</span></span>                           |
| <span data-ttu-id="b3d2d-189">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-190">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-193">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-194">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-195">System-Flags</span></span>           | <span data-ttu-id="b3d2d-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-196">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-197">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-197">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-198">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b3d2d-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b3d2d-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b3d2d-200">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-200">Entry</span></span> | <span data-ttu-id="b3d2d-201">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-202">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-204">System-Only</span></span>            | <span data-ttu-id="b3d2d-205">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-205">False</span></span>                           |
| <span data-ttu-id="b3d2d-206">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-207">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-207">True</span></span>                            |
| <span data-ttu-id="b3d2d-208">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-208">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-209">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-209">False</span></span>                           |
| <span data-ttu-id="b3d2d-210">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-210">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-211">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-211">False</span></span>                           |
| <span data-ttu-id="b3d2d-212">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-213">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-216">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-217">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-218">System-Flags</span></span>           | <span data-ttu-id="b3d2d-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-219">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-220">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-220">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-221">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b3d2d-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3d2d-222">Windows Server 2008</span></span>



| <span data-ttu-id="b3d2d-223">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-223">Entry</span></span> | <span data-ttu-id="b3d2d-224">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-225">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-227">System-Only</span></span>            | <span data-ttu-id="b3d2d-228">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-228">False</span></span>                           |
| <span data-ttu-id="b3d2d-229">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-230">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-230">True</span></span>                            |
| <span data-ttu-id="b3d2d-231">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-231">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-232">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-232">False</span></span>                           |
| <span data-ttu-id="b3d2d-233">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-233">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-234">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-234">False</span></span>                           |
| <span data-ttu-id="b3d2d-235">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-236">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-239">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-240">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-241">System-Flags</span></span>           | <span data-ttu-id="b3d2d-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-242">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-243">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-243">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-244">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b3d2d-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3d2d-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b3d2d-246">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-246">Entry</span></span> | <span data-ttu-id="b3d2d-247">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-248">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-250">System-Only</span></span>            | <span data-ttu-id="b3d2d-251">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-251">False</span></span>                           |
| <span data-ttu-id="b3d2d-252">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-253">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-253">True</span></span>                            |
| <span data-ttu-id="b3d2d-254">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-254">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-255">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-255">False</span></span>                           |
| <span data-ttu-id="b3d2d-256">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-256">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-257">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-257">False</span></span>                           |
| <span data-ttu-id="b3d2d-258">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-259">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-262">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-263">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-264">System-Flags</span></span>           | <span data-ttu-id="b3d2d-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-265">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-266">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-266">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-267">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b3d2d-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3d2d-268">Windows Server 2012</span></span>



| <span data-ttu-id="b3d2d-269">進入</span><span class="sxs-lookup"><span data-stu-id="b3d2d-269">Entry</span></span> | <span data-ttu-id="b3d2d-270">值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b3d2d-271">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b3d2d-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b3d2d-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b3d2d-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="b3d2d-273">System-Only</span></span>            | <span data-ttu-id="b3d2d-274">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-274">False</span></span>                           |
| <span data-ttu-id="b3d2d-275">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b3d2d-275">Is-Single-Valued</span></span>       | <span data-ttu-id="b3d2d-276">對</span><span class="sxs-lookup"><span data-stu-id="b3d2d-276">True</span></span>                            |
| <span data-ttu-id="b3d2d-277">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b3d2d-277">Is Indexed</span></span>             | <span data-ttu-id="b3d2d-278">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-278">False</span></span>                           |
| <span data-ttu-id="b3d2d-279">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b3d2d-279">In Global Catalog</span></span>      | <span data-ttu-id="b3d2d-280">否</span><span class="sxs-lookup"><span data-stu-id="b3d2d-280">False</span></span>                           |
| <span data-ttu-id="b3d2d-281">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b3d2d-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="b3d2d-282">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b3d2d-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b3d2d-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b3d2d-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b3d2d-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b3d2d-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-285">Search-Flags</span></span>           | <span data-ttu-id="b3d2d-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b3d2d-286">0x00000000</span></span>                      |
| <span data-ttu-id="b3d2d-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b3d2d-287">System-Flags</span></span>           | <span data-ttu-id="b3d2d-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b3d2d-288">0x00000010</span></span>                      |
| <span data-ttu-id="b3d2d-289">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b3d2d-289">Classes used in</span></span>        | [<span data-ttu-id="b3d2d-290">**返回頁首**</span><span class="sxs-lookup"><span data-stu-id="b3d2d-290">**Top**</span></span>](c-top.md)<br/> |



 

 





