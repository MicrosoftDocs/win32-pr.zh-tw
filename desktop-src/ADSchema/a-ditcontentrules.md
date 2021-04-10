---
title: DIT-Content 規則屬性
description: 這會藉由使用一組選擇性的輔助物件類別，以及必要的、選擇性和排除屬性，來指定特定結構物件類別的專案所允許的內容。
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- DIT-Content 規則屬性 AD 架構
- dITContentRules 屬性 AD 架構
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108224"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="e274e-105">DIT-Content 規則屬性</span><span class="sxs-lookup"><span data-stu-id="e274e-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="e274e-106">這會藉由使用一組選擇性的輔助物件類別，以及必要的、選擇性和排除屬性，來指定特定結構物件類別的專案所允許的內容。</span><span class="sxs-lookup"><span data-stu-id="e274e-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="e274e-107">集體屬性包含在 DIT 內容規則中，如 RFC 2251 中所定義。</span><span class="sxs-lookup"><span data-stu-id="e274e-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="e274e-108">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-108">Entry</span></span> | <span data-ttu-id="e274e-109">值</span><span class="sxs-lookup"><span data-stu-id="e274e-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e274e-110">CN</span><span class="sxs-lookup"><span data-stu-id="e274e-110">CN</span></span>                | <span data-ttu-id="e274e-111">DIT-內容-規則</span><span class="sxs-lookup"><span data-stu-id="e274e-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="e274e-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="e274e-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e274e-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="e274e-113">dITContentRules</span></span>                             |
| <span data-ttu-id="e274e-114">大小</span><span class="sxs-lookup"><span data-stu-id="e274e-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="e274e-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="e274e-115">Update Privilege</span></span>  | <span data-ttu-id="e274e-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="e274e-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="e274e-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="e274e-117">Update Frequency</span></span>  | <span data-ttu-id="e274e-118">每次建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="e274e-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="e274e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-119">Attribute-Id</span></span>      | <span data-ttu-id="e274e-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="e274e-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="e274e-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="e274e-121">System-Id-Guid</span></span>    | <span data-ttu-id="e274e-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e274e-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="e274e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e274e-123">Syntax</span></span>            | [<span data-ttu-id="e274e-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e274e-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e274e-125">實作</span><span class="sxs-lookup"><span data-stu-id="e274e-125">Implementations</span></span>

-   [<span data-ttu-id="e274e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e274e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e274e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e274e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e274e-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="e274e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e274e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e274e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e274e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e274e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e274e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e274e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e274e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e274e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e274e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e274e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="e274e-134">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-134">Entry</span></span> | <span data-ttu-id="e274e-135">值</span><span class="sxs-lookup"><span data-stu-id="e274e-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-138">System-Only</span></span>            | <span data-ttu-id="e274e-139">對</span><span class="sxs-lookup"><span data-stu-id="e274e-139">True</span></span>                                        |
| <span data-ttu-id="e274e-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-141">否</span><span class="sxs-lookup"><span data-stu-id="e274e-141">False</span></span>                                       |
| <span data-ttu-id="e274e-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-142">Is Indexed</span></span>             | <span data-ttu-id="e274e-143">否</span><span class="sxs-lookup"><span data-stu-id="e274e-143">False</span></span>                                       |
| <span data-ttu-id="e274e-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-144">In Global Catalog</span></span>      | <span data-ttu-id="e274e-145">否</span><span class="sxs-lookup"><span data-stu-id="e274e-145">False</span></span>                                       |
| <span data-ttu-id="e274e-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-150">Search-Flags</span></span>           | <span data-ttu-id="e274e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-151">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-152">System-Flags</span></span>           | <span data-ttu-id="e274e-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-153">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-154">Classes used in</span></span>        | [<span data-ttu-id="e274e-155">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e274e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e274e-156">Windows Server 2003</span></span>



| <span data-ttu-id="e274e-157">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-157">Entry</span></span> | <span data-ttu-id="e274e-158">值</span><span class="sxs-lookup"><span data-stu-id="e274e-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-161">System-Only</span></span>            | <span data-ttu-id="e274e-162">對</span><span class="sxs-lookup"><span data-stu-id="e274e-162">True</span></span>                                        |
| <span data-ttu-id="e274e-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-164">否</span><span class="sxs-lookup"><span data-stu-id="e274e-164">False</span></span>                                       |
| <span data-ttu-id="e274e-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-165">Is Indexed</span></span>             | <span data-ttu-id="e274e-166">否</span><span class="sxs-lookup"><span data-stu-id="e274e-166">False</span></span>                                       |
| <span data-ttu-id="e274e-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-167">In Global Catalog</span></span>      | <span data-ttu-id="e274e-168">否</span><span class="sxs-lookup"><span data-stu-id="e274e-168">False</span></span>                                       |
| <span data-ttu-id="e274e-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-173">Search-Flags</span></span>           | <span data-ttu-id="e274e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-174">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-175">System-Flags</span></span>           | <span data-ttu-id="e274e-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-176">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-177">Classes used in</span></span>        | [<span data-ttu-id="e274e-178">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e274e-179">亞當</span><span class="sxs-lookup"><span data-stu-id="e274e-179">ADAM</span></span>



| <span data-ttu-id="e274e-180">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-180">Entry</span></span> | <span data-ttu-id="e274e-181">值</span><span class="sxs-lookup"><span data-stu-id="e274e-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-184">System-Only</span></span>            | <span data-ttu-id="e274e-185">對</span><span class="sxs-lookup"><span data-stu-id="e274e-185">True</span></span>                                        |
| <span data-ttu-id="e274e-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-187">否</span><span class="sxs-lookup"><span data-stu-id="e274e-187">False</span></span>                                       |
| <span data-ttu-id="e274e-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-188">Is Indexed</span></span>             | <span data-ttu-id="e274e-189">否</span><span class="sxs-lookup"><span data-stu-id="e274e-189">False</span></span>                                       |
| <span data-ttu-id="e274e-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-190">In Global Catalog</span></span>      | <span data-ttu-id="e274e-191">否</span><span class="sxs-lookup"><span data-stu-id="e274e-191">False</span></span>                                       |
| <span data-ttu-id="e274e-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-196">Search-Flags</span></span>           | <span data-ttu-id="e274e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-197">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-198">System-Flags</span></span>           | <span data-ttu-id="e274e-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-199">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-200">Classes used in</span></span>        | [<span data-ttu-id="e274e-201">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e274e-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e274e-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e274e-203">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-203">Entry</span></span> | <span data-ttu-id="e274e-204">值</span><span class="sxs-lookup"><span data-stu-id="e274e-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-207">System-Only</span></span>            | <span data-ttu-id="e274e-208">對</span><span class="sxs-lookup"><span data-stu-id="e274e-208">True</span></span>                                        |
| <span data-ttu-id="e274e-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-210">否</span><span class="sxs-lookup"><span data-stu-id="e274e-210">False</span></span>                                       |
| <span data-ttu-id="e274e-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-211">Is Indexed</span></span>             | <span data-ttu-id="e274e-212">否</span><span class="sxs-lookup"><span data-stu-id="e274e-212">False</span></span>                                       |
| <span data-ttu-id="e274e-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-213">In Global Catalog</span></span>      | <span data-ttu-id="e274e-214">否</span><span class="sxs-lookup"><span data-stu-id="e274e-214">False</span></span>                                       |
| <span data-ttu-id="e274e-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-219">Search-Flags</span></span>           | <span data-ttu-id="e274e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-220">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-221">System-Flags</span></span>           | <span data-ttu-id="e274e-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-222">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-223">Classes used in</span></span>        | [<span data-ttu-id="e274e-224">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e274e-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e274e-225">Windows Server 2008</span></span>



| <span data-ttu-id="e274e-226">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-226">Entry</span></span> | <span data-ttu-id="e274e-227">值</span><span class="sxs-lookup"><span data-stu-id="e274e-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-230">System-Only</span></span>            | <span data-ttu-id="e274e-231">對</span><span class="sxs-lookup"><span data-stu-id="e274e-231">True</span></span>                                        |
| <span data-ttu-id="e274e-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-233">否</span><span class="sxs-lookup"><span data-stu-id="e274e-233">False</span></span>                                       |
| <span data-ttu-id="e274e-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-234">Is Indexed</span></span>             | <span data-ttu-id="e274e-235">否</span><span class="sxs-lookup"><span data-stu-id="e274e-235">False</span></span>                                       |
| <span data-ttu-id="e274e-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-236">In Global Catalog</span></span>      | <span data-ttu-id="e274e-237">否</span><span class="sxs-lookup"><span data-stu-id="e274e-237">False</span></span>                                       |
| <span data-ttu-id="e274e-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-242">Search-Flags</span></span>           | <span data-ttu-id="e274e-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-243">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-244">System-Flags</span></span>           | <span data-ttu-id="e274e-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-245">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-246">Classes used in</span></span>        | [<span data-ttu-id="e274e-247">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e274e-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e274e-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e274e-249">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-249">Entry</span></span> | <span data-ttu-id="e274e-250">值</span><span class="sxs-lookup"><span data-stu-id="e274e-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-253">System-Only</span></span>            | <span data-ttu-id="e274e-254">對</span><span class="sxs-lookup"><span data-stu-id="e274e-254">True</span></span>                                        |
| <span data-ttu-id="e274e-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-255">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-256">否</span><span class="sxs-lookup"><span data-stu-id="e274e-256">False</span></span>                                       |
| <span data-ttu-id="e274e-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-257">Is Indexed</span></span>             | <span data-ttu-id="e274e-258">否</span><span class="sxs-lookup"><span data-stu-id="e274e-258">False</span></span>                                       |
| <span data-ttu-id="e274e-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-259">In Global Catalog</span></span>      | <span data-ttu-id="e274e-260">否</span><span class="sxs-lookup"><span data-stu-id="e274e-260">False</span></span>                                       |
| <span data-ttu-id="e274e-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-265">Search-Flags</span></span>           | <span data-ttu-id="e274e-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-266">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-267">System-Flags</span></span>           | <span data-ttu-id="e274e-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-268">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-269">Classes used in</span></span>        | [<span data-ttu-id="e274e-270">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e274e-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e274e-271">Windows Server 2012</span></span>



| <span data-ttu-id="e274e-272">進入</span><span class="sxs-lookup"><span data-stu-id="e274e-272">Entry</span></span> | <span data-ttu-id="e274e-273">值</span><span class="sxs-lookup"><span data-stu-id="e274e-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e274e-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="e274e-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e274e-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="e274e-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="e274e-276">System-Only</span></span>            | <span data-ttu-id="e274e-277">對</span><span class="sxs-lookup"><span data-stu-id="e274e-277">True</span></span>                                        |
| <span data-ttu-id="e274e-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="e274e-278">Is-Single-Valued</span></span>       | <span data-ttu-id="e274e-279">否</span><span class="sxs-lookup"><span data-stu-id="e274e-279">False</span></span>                                       |
| <span data-ttu-id="e274e-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="e274e-280">Is Indexed</span></span>             | <span data-ttu-id="e274e-281">否</span><span class="sxs-lookup"><span data-stu-id="e274e-281">False</span></span>                                       |
| <span data-ttu-id="e274e-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="e274e-282">In Global Catalog</span></span>      | <span data-ttu-id="e274e-283">否</span><span class="sxs-lookup"><span data-stu-id="e274e-283">False</span></span>                                       |
| <span data-ttu-id="e274e-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="e274e-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="e274e-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="e274e-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="e274e-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e274e-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="e274e-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e274e-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="e274e-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-288">Search-Flags</span></span>           | <span data-ttu-id="e274e-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e274e-289">0x00000000</span></span>                                  |
| <span data-ttu-id="e274e-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e274e-290">System-Flags</span></span>           | <span data-ttu-id="e274e-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="e274e-291">0x08000014</span></span>                                  |
| <span data-ttu-id="e274e-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="e274e-292">Classes used in</span></span>        | [<span data-ttu-id="e274e-293">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="e274e-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





