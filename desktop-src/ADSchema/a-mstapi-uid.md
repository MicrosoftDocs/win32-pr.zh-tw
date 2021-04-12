---
title: ms-TAPI-唯一識別碼屬性
description: 提供 TAPI 多播會議的名稱。 它是 Rt-Conference 類別的命名屬性。
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- ms-TAPI-唯一識別碼屬性 AD 架構
- msTAPI-uid 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385382"
---
# <a name="ms-tapi-unique-identifier-attribute"></a><span data-ttu-id="3e5ab-106">ms-TAPI-唯一識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="3e5ab-106">ms-TAPI-Unique-Identifier attribute</span></span>

<span data-ttu-id="3e5ab-107">提供 TAPI 多播會議的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e5ab-107">Provides the name of a TAPI multicast conference.</span></span> <span data-ttu-id="3e5ab-108">它是 Rt-Conference 類別的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="3e5ab-108">It is the naming attribute of the Rt-Conference class.</span></span>



| <span data-ttu-id="3e5ab-109">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-109">Entry</span></span> | <span data-ttu-id="3e5ab-110">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-111">CN</span><span class="sxs-lookup"><span data-stu-id="3e5ab-111">CN</span></span>                | <span data-ttu-id="3e5ab-112">ms-TAPI-唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-112">ms-TAPI-Unique-Identifier</span></span>                                             |
| <span data-ttu-id="3e5ab-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="3e5ab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3e5ab-114">msTAPI-uid</span><span class="sxs-lookup"><span data-stu-id="3e5ab-114">msTAPI-uid</span></span>                                                            |
| <span data-ttu-id="3e5ab-115">大小</span><span class="sxs-lookup"><span data-stu-id="3e5ab-115">Size</span></span>              | <span data-ttu-id="3e5ab-116">可以是任一字元串，其長度通常低於100個字元。</span><span class="sxs-lookup"><span data-stu-id="3e5ab-116">Can be an arbitrary string, typically under 100 characters in length.</span></span> |
| <span data-ttu-id="3e5ab-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="3e5ab-117">Update Privilege</span></span>  | <span data-ttu-id="3e5ab-118">不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="3e5ab-118">No special privileges required.</span></span>                                       |
| <span data-ttu-id="3e5ab-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="3e5ab-119">Update Frequency</span></span>  | <span data-ttu-id="3e5ab-120">在建立 Rt-Conference 物件時設定一次。</span><span class="sxs-lookup"><span data-stu-id="3e5ab-120">Set once at the time of creating the Rt-Conference object.</span></span>            |
| <span data-ttu-id="3e5ab-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-121">Attribute-Id</span></span>      | <span data-ttu-id="3e5ab-122">1.2.840.113556.1.4.1698</span><span class="sxs-lookup"><span data-stu-id="3e5ab-122">1.2.840.113556.1.4.1698</span></span>                                               |
| <span data-ttu-id="3e5ab-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="3e5ab-123">System-Id-Guid</span></span>    | <span data-ttu-id="3e5ab-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span><span class="sxs-lookup"><span data-stu-id="3e5ab-124">70a4e7ea-b3b9-4643-8918-e6dd2471bfd4</span></span>                                  |
| <span data-ttu-id="3e5ab-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e5ab-125">Syntax</span></span>            | [<span data-ttu-id="3e5ab-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-126">**String(Unicode)**</span></span>](s-string-unicode.md)                           |



## <a name="implementations"></a><span data-ttu-id="3e5ab-127">實作</span><span class="sxs-lookup"><span data-stu-id="3e5ab-127">Implementations</span></span>

-   [<span data-ttu-id="3e5ab-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e5ab-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e5ab-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e5ab-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e5ab-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="3e5ab-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e5ab-133">Windows Server 2003</span></span>



| <span data-ttu-id="3e5ab-134">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-134">Entry</span></span> | <span data-ttu-id="3e5ab-135">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-136">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-137">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5ab-138">System-Only</span></span>            | <span data-ttu-id="3e5ab-139">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-139">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-140">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5ab-141">對</span><span class="sxs-lookup"><span data-stu-id="3e5ab-141">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e5ab-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3e5ab-142">Is Indexed</span></span>             | <span data-ttu-id="3e5ab-143">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-143">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3e5ab-144">In Global Catalog</span></span>      | <span data-ttu-id="3e5ab-145">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-145">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3e5ab-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5ab-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3e5ab-147">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="3e5ab-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5ab-148">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5ab-149">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-150">Search-Flags</span></span>           | <span data-ttu-id="3e5ab-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5ab-151">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-152">System-Flags</span></span>           | <span data-ttu-id="3e5ab-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5ab-153">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3e5ab-154">Classes used in</span></span>        | [<span data-ttu-id="3e5ab-155">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-155">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="3e5ab-156">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-156">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e5ab-157">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e5ab-157">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e5ab-158">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-158">Entry</span></span> | <span data-ttu-id="3e5ab-159">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-160">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-160">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-161">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5ab-162">System-Only</span></span>            | <span data-ttu-id="3e5ab-163">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-163">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-164">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-164">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5ab-165">對</span><span class="sxs-lookup"><span data-stu-id="3e5ab-165">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e5ab-166">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3e5ab-166">Is Indexed</span></span>             | <span data-ttu-id="3e5ab-167">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-167">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-168">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3e5ab-168">In Global Catalog</span></span>      | <span data-ttu-id="3e5ab-169">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-169">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-170">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3e5ab-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5ab-171">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3e5ab-171">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="3e5ab-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5ab-172">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5ab-173">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-174">Search-Flags</span></span>           | <span data-ttu-id="3e5ab-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5ab-175">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-176">System-Flags</span></span>           | <span data-ttu-id="3e5ab-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5ab-177">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-178">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3e5ab-178">Classes used in</span></span>        | [<span data-ttu-id="3e5ab-179">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-179">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="3e5ab-180">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-180">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e5ab-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e5ab-181">Windows Server 2008</span></span>



| <span data-ttu-id="3e5ab-182">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-182">Entry</span></span> | <span data-ttu-id="3e5ab-183">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-183">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-184">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-185">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5ab-186">System-Only</span></span>            | <span data-ttu-id="3e5ab-187">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-187">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-188">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5ab-189">對</span><span class="sxs-lookup"><span data-stu-id="3e5ab-189">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e5ab-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3e5ab-190">Is Indexed</span></span>             | <span data-ttu-id="3e5ab-191">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-191">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3e5ab-192">In Global Catalog</span></span>      | <span data-ttu-id="3e5ab-193">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-193">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3e5ab-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5ab-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3e5ab-195">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="3e5ab-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5ab-196">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5ab-197">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-198">Search-Flags</span></span>           | <span data-ttu-id="3e5ab-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5ab-199">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-200">System-Flags</span></span>           | <span data-ttu-id="3e5ab-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5ab-201">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3e5ab-202">Classes used in</span></span>        | [<span data-ttu-id="3e5ab-203">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="3e5ab-204">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-204">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e5ab-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e5ab-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e5ab-206">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-206">Entry</span></span> | <span data-ttu-id="3e5ab-207">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-207">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-208">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-208">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-209">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5ab-210">System-Only</span></span>            | <span data-ttu-id="3e5ab-211">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-211">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-212">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-212">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5ab-213">對</span><span class="sxs-lookup"><span data-stu-id="3e5ab-213">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e5ab-214">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3e5ab-214">Is Indexed</span></span>             | <span data-ttu-id="3e5ab-215">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-215">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-216">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3e5ab-216">In Global Catalog</span></span>      | <span data-ttu-id="3e5ab-217">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-217">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-218">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3e5ab-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5ab-219">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3e5ab-219">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="3e5ab-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5ab-220">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5ab-221">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-222">Search-Flags</span></span>           | <span data-ttu-id="3e5ab-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5ab-223">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-224">System-Flags</span></span>           | <span data-ttu-id="3e5ab-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5ab-225">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-226">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3e5ab-226">Classes used in</span></span>        | [<span data-ttu-id="3e5ab-227">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-227">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="3e5ab-228">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-228">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e5ab-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e5ab-229">Windows Server 2012</span></span>



| <span data-ttu-id="3e5ab-230">進入</span><span class="sxs-lookup"><span data-stu-id="3e5ab-230">Entry</span></span> | <span data-ttu-id="3e5ab-231">值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-231">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ab-232">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="3e5ab-232">Link-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e5ab-233">MAPI-Id</span></span>                | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e5ab-234">System-Only</span></span>            | <span data-ttu-id="3e5ab-235">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-235">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-236">是-單一值</span><span class="sxs-lookup"><span data-stu-id="3e5ab-236">Is-Single-Valued</span></span>       | <span data-ttu-id="3e5ab-237">對</span><span class="sxs-lookup"><span data-stu-id="3e5ab-237">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e5ab-238">已編制索引</span><span class="sxs-lookup"><span data-stu-id="3e5ab-238">Is Indexed</span></span>             | <span data-ttu-id="3e5ab-239">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-239">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-240">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="3e5ab-240">In Global Catalog</span></span>      | <span data-ttu-id="3e5ab-241">否</span><span class="sxs-lookup"><span data-stu-id="3e5ab-241">False</span></span>                                                                                                                       |
| <span data-ttu-id="3e5ab-242">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="3e5ab-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e5ab-243">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="3e5ab-243">O:BAG:BAD:S:</span></span>                                                                                                                |
| <span data-ttu-id="3e5ab-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e5ab-244">Range-Lower</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e5ab-245">Range-Upper</span></span>            | \-                                                                                                                          |
| <span data-ttu-id="3e5ab-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-246">Search-Flags</span></span>           | <span data-ttu-id="3e5ab-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e5ab-247">0x00000000</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e5ab-248">System-Flags</span></span>           | <span data-ttu-id="3e5ab-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3e5ab-249">0x00000010</span></span>                                                                                                                  |
| <span data-ttu-id="3e5ab-250">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="3e5ab-250">Classes used in</span></span>        | [<span data-ttu-id="3e5ab-251">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-251">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> [<span data-ttu-id="3e5ab-252">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-252">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





