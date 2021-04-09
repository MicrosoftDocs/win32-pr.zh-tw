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
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="70e34-105">DIT-Content 規則屬性</span><span class="sxs-lookup"><span data-stu-id="70e34-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="70e34-106">這會藉由使用一組選擇性的輔助物件類別，以及必要的、選擇性和排除屬性，來指定特定結構物件類別的專案所允許的內容。</span><span class="sxs-lookup"><span data-stu-id="70e34-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="70e34-107">集體屬性包含在 DIT 內容規則中，如 RFC 2251 中所定義。</span><span class="sxs-lookup"><span data-stu-id="70e34-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="70e34-108">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-108">Entry</span></span> | <span data-ttu-id="70e34-109">值</span><span class="sxs-lookup"><span data-stu-id="70e34-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="70e34-110">CN</span><span class="sxs-lookup"><span data-stu-id="70e34-110">CN</span></span>                | <span data-ttu-id="70e34-111">DIT-內容-規則</span><span class="sxs-lookup"><span data-stu-id="70e34-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="70e34-112">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="70e34-112">Ldap-Display-Name</span></span> | <span data-ttu-id="70e34-113">dITContentRules</span><span class="sxs-lookup"><span data-stu-id="70e34-113">dITContentRules</span></span>                             |
| <span data-ttu-id="70e34-114">大小</span><span class="sxs-lookup"><span data-stu-id="70e34-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="70e34-115">更新許可權</span><span class="sxs-lookup"><span data-stu-id="70e34-115">Update Privilege</span></span>  | <span data-ttu-id="70e34-116">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="70e34-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="70e34-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="70e34-117">Update Frequency</span></span>  | <span data-ttu-id="70e34-118">每次建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="70e34-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="70e34-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-119">Attribute-Id</span></span>      | <span data-ttu-id="70e34-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="70e34-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="70e34-121">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="70e34-121">System-Id-Guid</span></span>    | <span data-ttu-id="70e34-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="70e34-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="70e34-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="70e34-123">Syntax</span></span>            | [<span data-ttu-id="70e34-124">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="70e34-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="70e34-125">實作</span><span class="sxs-lookup"><span data-stu-id="70e34-125">Implementations</span></span>

-   [<span data-ttu-id="70e34-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="70e34-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="70e34-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="70e34-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="70e34-128">**亞當**</span><span class="sxs-lookup"><span data-stu-id="70e34-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="70e34-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="70e34-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="70e34-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="70e34-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="70e34-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="70e34-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="70e34-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="70e34-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="70e34-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="70e34-133">Windows 2000 Server</span></span>



| <span data-ttu-id="70e34-134">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-134">Entry</span></span> | <span data-ttu-id="70e34-135">值</span><span class="sxs-lookup"><span data-stu-id="70e34-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-138">System-Only</span></span>            | <span data-ttu-id="70e34-139">對</span><span class="sxs-lookup"><span data-stu-id="70e34-139">True</span></span>                                        |
| <span data-ttu-id="70e34-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-140">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-141">否</span><span class="sxs-lookup"><span data-stu-id="70e34-141">False</span></span>                                       |
| <span data-ttu-id="70e34-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-142">Is Indexed</span></span>             | <span data-ttu-id="70e34-143">否</span><span class="sxs-lookup"><span data-stu-id="70e34-143">False</span></span>                                       |
| <span data-ttu-id="70e34-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-144">In Global Catalog</span></span>      | <span data-ttu-id="70e34-145">否</span><span class="sxs-lookup"><span data-stu-id="70e34-145">False</span></span>                                       |
| <span data-ttu-id="70e34-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-150">Search-Flags</span></span>           | <span data-ttu-id="70e34-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-151">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-152">System-Flags</span></span>           | <span data-ttu-id="70e34-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-153">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-154">Classes used in</span></span>        | [<span data-ttu-id="70e34-155">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="70e34-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="70e34-156">Windows Server 2003</span></span>



| <span data-ttu-id="70e34-157">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-157">Entry</span></span> | <span data-ttu-id="70e34-158">值</span><span class="sxs-lookup"><span data-stu-id="70e34-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-161">System-Only</span></span>            | <span data-ttu-id="70e34-162">對</span><span class="sxs-lookup"><span data-stu-id="70e34-162">True</span></span>                                        |
| <span data-ttu-id="70e34-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-163">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-164">否</span><span class="sxs-lookup"><span data-stu-id="70e34-164">False</span></span>                                       |
| <span data-ttu-id="70e34-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-165">Is Indexed</span></span>             | <span data-ttu-id="70e34-166">否</span><span class="sxs-lookup"><span data-stu-id="70e34-166">False</span></span>                                       |
| <span data-ttu-id="70e34-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-167">In Global Catalog</span></span>      | <span data-ttu-id="70e34-168">否</span><span class="sxs-lookup"><span data-stu-id="70e34-168">False</span></span>                                       |
| <span data-ttu-id="70e34-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-173">Search-Flags</span></span>           | <span data-ttu-id="70e34-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-174">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-175">System-Flags</span></span>           | <span data-ttu-id="70e34-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-176">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-177">Classes used in</span></span>        | [<span data-ttu-id="70e34-178">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="70e34-179">亞當</span><span class="sxs-lookup"><span data-stu-id="70e34-179">ADAM</span></span>



| <span data-ttu-id="70e34-180">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-180">Entry</span></span> | <span data-ttu-id="70e34-181">值</span><span class="sxs-lookup"><span data-stu-id="70e34-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-184">System-Only</span></span>            | <span data-ttu-id="70e34-185">對</span><span class="sxs-lookup"><span data-stu-id="70e34-185">True</span></span>                                        |
| <span data-ttu-id="70e34-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-186">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-187">否</span><span class="sxs-lookup"><span data-stu-id="70e34-187">False</span></span>                                       |
| <span data-ttu-id="70e34-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-188">Is Indexed</span></span>             | <span data-ttu-id="70e34-189">否</span><span class="sxs-lookup"><span data-stu-id="70e34-189">False</span></span>                                       |
| <span data-ttu-id="70e34-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-190">In Global Catalog</span></span>      | <span data-ttu-id="70e34-191">否</span><span class="sxs-lookup"><span data-stu-id="70e34-191">False</span></span>                                       |
| <span data-ttu-id="70e34-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-196">Search-Flags</span></span>           | <span data-ttu-id="70e34-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-197">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-198">System-Flags</span></span>           | <span data-ttu-id="70e34-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-199">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-200">Classes used in</span></span>        | [<span data-ttu-id="70e34-201">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="70e34-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="70e34-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="70e34-203">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-203">Entry</span></span> | <span data-ttu-id="70e34-204">值</span><span class="sxs-lookup"><span data-stu-id="70e34-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-207">System-Only</span></span>            | <span data-ttu-id="70e34-208">對</span><span class="sxs-lookup"><span data-stu-id="70e34-208">True</span></span>                                        |
| <span data-ttu-id="70e34-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-209">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-210">否</span><span class="sxs-lookup"><span data-stu-id="70e34-210">False</span></span>                                       |
| <span data-ttu-id="70e34-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-211">Is Indexed</span></span>             | <span data-ttu-id="70e34-212">否</span><span class="sxs-lookup"><span data-stu-id="70e34-212">False</span></span>                                       |
| <span data-ttu-id="70e34-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-213">In Global Catalog</span></span>      | <span data-ttu-id="70e34-214">否</span><span class="sxs-lookup"><span data-stu-id="70e34-214">False</span></span>                                       |
| <span data-ttu-id="70e34-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-219">Search-Flags</span></span>           | <span data-ttu-id="70e34-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-220">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-221">System-Flags</span></span>           | <span data-ttu-id="70e34-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-222">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-223">Classes used in</span></span>        | [<span data-ttu-id="70e34-224">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="70e34-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70e34-225">Windows Server 2008</span></span>



| <span data-ttu-id="70e34-226">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-226">Entry</span></span> | <span data-ttu-id="70e34-227">值</span><span class="sxs-lookup"><span data-stu-id="70e34-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-230">System-Only</span></span>            | <span data-ttu-id="70e34-231">對</span><span class="sxs-lookup"><span data-stu-id="70e34-231">True</span></span>                                        |
| <span data-ttu-id="70e34-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-232">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-233">否</span><span class="sxs-lookup"><span data-stu-id="70e34-233">False</span></span>                                       |
| <span data-ttu-id="70e34-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-234">Is Indexed</span></span>             | <span data-ttu-id="70e34-235">否</span><span class="sxs-lookup"><span data-stu-id="70e34-235">False</span></span>                                       |
| <span data-ttu-id="70e34-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-236">In Global Catalog</span></span>      | <span data-ttu-id="70e34-237">否</span><span class="sxs-lookup"><span data-stu-id="70e34-237">False</span></span>                                       |
| <span data-ttu-id="70e34-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-242">Search-Flags</span></span>           | <span data-ttu-id="70e34-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-243">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-244">System-Flags</span></span>           | <span data-ttu-id="70e34-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-245">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-246">Classes used in</span></span>        | [<span data-ttu-id="70e34-247">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="70e34-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70e34-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="70e34-249">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-249">Entry</span></span> | <span data-ttu-id="70e34-250">值</span><span class="sxs-lookup"><span data-stu-id="70e34-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-251">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-253">System-Only</span></span>            | <span data-ttu-id="70e34-254">對</span><span class="sxs-lookup"><span data-stu-id="70e34-254">True</span></span>                                        |
| <span data-ttu-id="70e34-255">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-255">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-256">否</span><span class="sxs-lookup"><span data-stu-id="70e34-256">False</span></span>                                       |
| <span data-ttu-id="70e34-257">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-257">Is Indexed</span></span>             | <span data-ttu-id="70e34-258">否</span><span class="sxs-lookup"><span data-stu-id="70e34-258">False</span></span>                                       |
| <span data-ttu-id="70e34-259">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-259">In Global Catalog</span></span>      | <span data-ttu-id="70e34-260">否</span><span class="sxs-lookup"><span data-stu-id="70e34-260">False</span></span>                                       |
| <span data-ttu-id="70e34-261">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-262">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-265">Search-Flags</span></span>           | <span data-ttu-id="70e34-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-266">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-267">System-Flags</span></span>           | <span data-ttu-id="70e34-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-268">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-269">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-269">Classes used in</span></span>        | [<span data-ttu-id="70e34-270">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="70e34-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70e34-271">Windows Server 2012</span></span>



| <span data-ttu-id="70e34-272">進入</span><span class="sxs-lookup"><span data-stu-id="70e34-272">Entry</span></span> | <span data-ttu-id="70e34-273">值</span><span class="sxs-lookup"><span data-stu-id="70e34-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="70e34-274">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="70e34-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="70e34-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="70e34-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="70e34-276">System-Only</span></span>            | <span data-ttu-id="70e34-277">對</span><span class="sxs-lookup"><span data-stu-id="70e34-277">True</span></span>                                        |
| <span data-ttu-id="70e34-278">是-單一值</span><span class="sxs-lookup"><span data-stu-id="70e34-278">Is-Single-Valued</span></span>       | <span data-ttu-id="70e34-279">否</span><span class="sxs-lookup"><span data-stu-id="70e34-279">False</span></span>                                       |
| <span data-ttu-id="70e34-280">已編制索引</span><span class="sxs-lookup"><span data-stu-id="70e34-280">Is Indexed</span></span>             | <span data-ttu-id="70e34-281">否</span><span class="sxs-lookup"><span data-stu-id="70e34-281">False</span></span>                                       |
| <span data-ttu-id="70e34-282">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="70e34-282">In Global Catalog</span></span>      | <span data-ttu-id="70e34-283">否</span><span class="sxs-lookup"><span data-stu-id="70e34-283">False</span></span>                                       |
| <span data-ttu-id="70e34-284">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="70e34-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="70e34-285">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="70e34-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="70e34-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="70e34-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="70e34-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="70e34-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="70e34-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-288">Search-Flags</span></span>           | <span data-ttu-id="70e34-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="70e34-289">0x00000000</span></span>                                  |
| <span data-ttu-id="70e34-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="70e34-290">System-Flags</span></span>           | <span data-ttu-id="70e34-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="70e34-291">0x08000014</span></span>                                  |
| <span data-ttu-id="70e34-292">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="70e34-292">Classes used in</span></span>        | [<span data-ttu-id="70e34-293">**Ubschema**</span><span class="sxs-lookup"><span data-stu-id="70e34-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





