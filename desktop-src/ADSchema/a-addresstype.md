---
title: Address-Type 屬性
description: 描述使用者位址格式的字元字串。 網址類別型會對應至位址格式。 也就是說，藉由查看收件者的網址類別型，用戶端應用程式可以決定如何格式化適合收件者的位址。
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Address-Type 屬性 AD 架構
- addressType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106972732"
---
# <a name="address-type-attribute"></a><span data-ttu-id="981fc-107">Address-Type 屬性</span><span class="sxs-lookup"><span data-stu-id="981fc-107">Address-Type attribute</span></span>

<span data-ttu-id="981fc-108">描述使用者位址格式的字元字串。</span><span class="sxs-lookup"><span data-stu-id="981fc-108">A character string that describes the format of the user's address.</span></span> <span data-ttu-id="981fc-109">網址類別型會對應至位址格式。</span><span class="sxs-lookup"><span data-stu-id="981fc-109">Address types map to address formats.</span></span> <span data-ttu-id="981fc-110">也就是說，藉由查看收件者的網址類別型，用戶端應用程式可以決定如何格式化適合收件者的位址。</span><span class="sxs-lookup"><span data-stu-id="981fc-110">That is, by looking at a recipient's address type, client applications can determine how to format an address that is appropriate for the recipient.</span></span>



| <span data-ttu-id="981fc-111">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-111">Entry</span></span> | <span data-ttu-id="981fc-112">值</span><span class="sxs-lookup"><span data-stu-id="981fc-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981fc-113">CN</span><span class="sxs-lookup"><span data-stu-id="981fc-113">CN</span></span>                | <span data-ttu-id="981fc-114">Address-Type</span><span class="sxs-lookup"><span data-stu-id="981fc-114">Address-Type</span></span>                                                                                                              |
| <span data-ttu-id="981fc-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="981fc-115">Ldap-Display-Name</span></span> | <span data-ttu-id="981fc-116">addressType</span><span class="sxs-lookup"><span data-stu-id="981fc-116">addressType</span></span>                                                                                                               |
| <span data-ttu-id="981fc-117">大小</span><span class="sxs-lookup"><span data-stu-id="981fc-117">Size</span></span>              | <span data-ttu-id="981fc-118">網址類別型：3COM、ATT、CCMAIL、COMPUSERVE、EX、FAX、MSFAX、MCI、MHS、MS、MSA、MSN、PROFS、SMTP、SNADS、電傳、X400、X500</span><span class="sxs-lookup"><span data-stu-id="981fc-118">Address types: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN,PROFS,SMTP, SNADS, TELEX, X400, X500</span></span> |
| <span data-ttu-id="981fc-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="981fc-119">Update Privilege</span></span>  | <span data-ttu-id="981fc-120">此值是由系統所設定。</span><span class="sxs-lookup"><span data-stu-id="981fc-120">This value is set by the system.</span></span>                                                                                          |
| <span data-ttu-id="981fc-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="981fc-121">Update Frequency</span></span>  | <span data-ttu-id="981fc-122">在建立物件時設定。</span><span class="sxs-lookup"><span data-stu-id="981fc-122">Set when the object is created.</span></span>                                                                                           |
| <span data-ttu-id="981fc-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-123">Attribute-Id</span></span>      | <span data-ttu-id="981fc-124">1.2.840.113556.1.2.350</span><span class="sxs-lookup"><span data-stu-id="981fc-124">1.2.840.113556.1.2.350</span></span>                                                                                                    |
| <span data-ttu-id="981fc-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="981fc-125">System-Id-Guid</span></span>    | <span data-ttu-id="981fc-126">5fd42464-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="981fc-126">5fd42464-1262-11d0-a060-00aa006c33ed</span></span>                                                                                      |
| <span data-ttu-id="981fc-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="981fc-127">Syntax</span></span>            | [<span data-ttu-id="981fc-128">**String(Teletex)**</span><span class="sxs-lookup"><span data-stu-id="981fc-128">**String(Teletex)**</span></span>](s-string-teletex.md)                                                                               |



## <a name="implementations"></a><span data-ttu-id="981fc-129">實作</span><span class="sxs-lookup"><span data-stu-id="981fc-129">Implementations</span></span>

-   [<span data-ttu-id="981fc-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="981fc-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="981fc-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="981fc-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="981fc-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="981fc-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="981fc-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="981fc-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="981fc-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="981fc-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="981fc-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="981fc-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="981fc-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="981fc-136">Windows 2000 Server</span></span>



| <span data-ttu-id="981fc-137">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-137">Entry</span></span> | <span data-ttu-id="981fc-138">值</span><span class="sxs-lookup"><span data-stu-id="981fc-138">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-139">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-139">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-140">MAPI-Id</span></span>                | <span data-ttu-id="981fc-141">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-141">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-142">System-Only</span></span>            | <span data-ttu-id="981fc-143">否</span><span class="sxs-lookup"><span data-stu-id="981fc-143">False</span></span>                                                    |
| <span data-ttu-id="981fc-144">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-144">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-145">對</span><span class="sxs-lookup"><span data-stu-id="981fc-145">True</span></span>                                                     |
| <span data-ttu-id="981fc-146">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-146">Is Indexed</span></span>             | <span data-ttu-id="981fc-147">否</span><span class="sxs-lookup"><span data-stu-id="981fc-147">False</span></span>                                                    |
| <span data-ttu-id="981fc-148">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-148">In Global Catalog</span></span>      | <span data-ttu-id="981fc-149">否</span><span class="sxs-lookup"><span data-stu-id="981fc-149">False</span></span>                                                    |
| <span data-ttu-id="981fc-150">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-151">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-151">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-152">Range-Lower</span></span>            | <span data-ttu-id="981fc-153">1</span><span class="sxs-lookup"><span data-stu-id="981fc-153">1</span></span>                                                        |
| <span data-ttu-id="981fc-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-154">Range-Upper</span></span>            | <span data-ttu-id="981fc-155">32</span><span class="sxs-lookup"><span data-stu-id="981fc-155">32</span></span>                                                       |
| <span data-ttu-id="981fc-156">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-156">Search-Flags</span></span>           | <span data-ttu-id="981fc-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-157">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-158">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-158">System-Flags</span></span>           | <span data-ttu-id="981fc-159">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-159">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-160">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-160">Classes used in</span></span>        | [<span data-ttu-id="981fc-161">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-161">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="981fc-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="981fc-162">Windows Server 2003</span></span>



| <span data-ttu-id="981fc-163">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-163">Entry</span></span> | <span data-ttu-id="981fc-164">值</span><span class="sxs-lookup"><span data-stu-id="981fc-164">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-165">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-165">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-166">MAPI-Id</span></span>                | <span data-ttu-id="981fc-167">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-167">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-168">System-Only</span></span>            | <span data-ttu-id="981fc-169">否</span><span class="sxs-lookup"><span data-stu-id="981fc-169">False</span></span>                                                    |
| <span data-ttu-id="981fc-170">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-170">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-171">對</span><span class="sxs-lookup"><span data-stu-id="981fc-171">True</span></span>                                                     |
| <span data-ttu-id="981fc-172">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-172">Is Indexed</span></span>             | <span data-ttu-id="981fc-173">否</span><span class="sxs-lookup"><span data-stu-id="981fc-173">False</span></span>                                                    |
| <span data-ttu-id="981fc-174">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-174">In Global Catalog</span></span>      | <span data-ttu-id="981fc-175">否</span><span class="sxs-lookup"><span data-stu-id="981fc-175">False</span></span>                                                    |
| <span data-ttu-id="981fc-176">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-177">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-177">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-178">Range-Lower</span></span>            | <span data-ttu-id="981fc-179">1</span><span class="sxs-lookup"><span data-stu-id="981fc-179">1</span></span>                                                        |
| <span data-ttu-id="981fc-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-180">Range-Upper</span></span>            | <span data-ttu-id="981fc-181">32</span><span class="sxs-lookup"><span data-stu-id="981fc-181">32</span></span>                                                       |
| <span data-ttu-id="981fc-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-182">Search-Flags</span></span>           | <span data-ttu-id="981fc-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-183">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-184">System-Flags</span></span>           | <span data-ttu-id="981fc-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-185">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-186">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-186">Classes used in</span></span>        | [<span data-ttu-id="981fc-187">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-187">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="981fc-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="981fc-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="981fc-189">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-189">Entry</span></span> | <span data-ttu-id="981fc-190">值</span><span class="sxs-lookup"><span data-stu-id="981fc-190">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-191">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-191">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-192">MAPI-Id</span></span>                | <span data-ttu-id="981fc-193">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-193">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-194">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-194">System-Only</span></span>            | <span data-ttu-id="981fc-195">否</span><span class="sxs-lookup"><span data-stu-id="981fc-195">False</span></span>                                                    |
| <span data-ttu-id="981fc-196">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-196">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-197">對</span><span class="sxs-lookup"><span data-stu-id="981fc-197">True</span></span>                                                     |
| <span data-ttu-id="981fc-198">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-198">Is Indexed</span></span>             | <span data-ttu-id="981fc-199">否</span><span class="sxs-lookup"><span data-stu-id="981fc-199">False</span></span>                                                    |
| <span data-ttu-id="981fc-200">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-200">In Global Catalog</span></span>      | <span data-ttu-id="981fc-201">否</span><span class="sxs-lookup"><span data-stu-id="981fc-201">False</span></span>                                                    |
| <span data-ttu-id="981fc-202">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-202">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-203">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-203">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-204">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-204">Range-Lower</span></span>            | <span data-ttu-id="981fc-205">1</span><span class="sxs-lookup"><span data-stu-id="981fc-205">1</span></span>                                                        |
| <span data-ttu-id="981fc-206">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-206">Range-Upper</span></span>            | <span data-ttu-id="981fc-207">32</span><span class="sxs-lookup"><span data-stu-id="981fc-207">32</span></span>                                                       |
| <span data-ttu-id="981fc-208">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-208">Search-Flags</span></span>           | <span data-ttu-id="981fc-209">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-209">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-210">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-210">System-Flags</span></span>           | <span data-ttu-id="981fc-211">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-211">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-212">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-212">Classes used in</span></span>        | [<span data-ttu-id="981fc-213">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-213">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="981fc-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="981fc-214">Windows Server 2008</span></span>



| <span data-ttu-id="981fc-215">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-215">Entry</span></span> | <span data-ttu-id="981fc-216">值</span><span class="sxs-lookup"><span data-stu-id="981fc-216">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-217">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-217">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-218">MAPI-Id</span></span>                | <span data-ttu-id="981fc-219">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-219">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-220">System-Only</span></span>            | <span data-ttu-id="981fc-221">否</span><span class="sxs-lookup"><span data-stu-id="981fc-221">False</span></span>                                                    |
| <span data-ttu-id="981fc-222">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-222">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-223">對</span><span class="sxs-lookup"><span data-stu-id="981fc-223">True</span></span>                                                     |
| <span data-ttu-id="981fc-224">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-224">Is Indexed</span></span>             | <span data-ttu-id="981fc-225">否</span><span class="sxs-lookup"><span data-stu-id="981fc-225">False</span></span>                                                    |
| <span data-ttu-id="981fc-226">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-226">In Global Catalog</span></span>      | <span data-ttu-id="981fc-227">否</span><span class="sxs-lookup"><span data-stu-id="981fc-227">False</span></span>                                                    |
| <span data-ttu-id="981fc-228">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-229">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-229">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-230">Range-Lower</span></span>            | <span data-ttu-id="981fc-231">1</span><span class="sxs-lookup"><span data-stu-id="981fc-231">1</span></span>                                                        |
| <span data-ttu-id="981fc-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-232">Range-Upper</span></span>            | <span data-ttu-id="981fc-233">32</span><span class="sxs-lookup"><span data-stu-id="981fc-233">32</span></span>                                                       |
| <span data-ttu-id="981fc-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-234">Search-Flags</span></span>           | <span data-ttu-id="981fc-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-235">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-236">System-Flags</span></span>           | <span data-ttu-id="981fc-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-237">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-238">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-238">Classes used in</span></span>        | [<span data-ttu-id="981fc-239">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-239">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="981fc-240">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="981fc-240">Windows Server 2008 R2</span></span>



| <span data-ttu-id="981fc-241">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-241">Entry</span></span> | <span data-ttu-id="981fc-242">值</span><span class="sxs-lookup"><span data-stu-id="981fc-242">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-243">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-243">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-244">MAPI-Id</span></span>                | <span data-ttu-id="981fc-245">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-245">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-246">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-246">System-Only</span></span>            | <span data-ttu-id="981fc-247">否</span><span class="sxs-lookup"><span data-stu-id="981fc-247">False</span></span>                                                    |
| <span data-ttu-id="981fc-248">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-248">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-249">對</span><span class="sxs-lookup"><span data-stu-id="981fc-249">True</span></span>                                                     |
| <span data-ttu-id="981fc-250">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-250">Is Indexed</span></span>             | <span data-ttu-id="981fc-251">否</span><span class="sxs-lookup"><span data-stu-id="981fc-251">False</span></span>                                                    |
| <span data-ttu-id="981fc-252">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-252">In Global Catalog</span></span>      | <span data-ttu-id="981fc-253">否</span><span class="sxs-lookup"><span data-stu-id="981fc-253">False</span></span>                                                    |
| <span data-ttu-id="981fc-254">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-254">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-255">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-255">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-256">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-256">Range-Lower</span></span>            | <span data-ttu-id="981fc-257">1</span><span class="sxs-lookup"><span data-stu-id="981fc-257">1</span></span>                                                        |
| <span data-ttu-id="981fc-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-258">Range-Upper</span></span>            | <span data-ttu-id="981fc-259">32</span><span class="sxs-lookup"><span data-stu-id="981fc-259">32</span></span>                                                       |
| <span data-ttu-id="981fc-260">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-260">Search-Flags</span></span>           | <span data-ttu-id="981fc-261">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-261">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-262">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-262">System-Flags</span></span>           | <span data-ttu-id="981fc-263">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-263">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-264">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-264">Classes used in</span></span>        | [<span data-ttu-id="981fc-265">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-265">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="981fc-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="981fc-266">Windows Server 2012</span></span>



| <span data-ttu-id="981fc-267">進入</span><span class="sxs-lookup"><span data-stu-id="981fc-267">Entry</span></span> | <span data-ttu-id="981fc-268">值</span><span class="sxs-lookup"><span data-stu-id="981fc-268">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="981fc-269">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="981fc-269">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="981fc-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981fc-270">MAPI-Id</span></span>                | <span data-ttu-id="981fc-271">0x8048</span><span class="sxs-lookup"><span data-stu-id="981fc-271">0x8048</span></span>                                                   |
| <span data-ttu-id="981fc-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="981fc-272">System-Only</span></span>            | <span data-ttu-id="981fc-273">否</span><span class="sxs-lookup"><span data-stu-id="981fc-273">False</span></span>                                                    |
| <span data-ttu-id="981fc-274">是-單一值</span><span class="sxs-lookup"><span data-stu-id="981fc-274">Is-Single-Valued</span></span>       | <span data-ttu-id="981fc-275">對</span><span class="sxs-lookup"><span data-stu-id="981fc-275">True</span></span>                                                     |
| <span data-ttu-id="981fc-276">已編制索引</span><span class="sxs-lookup"><span data-stu-id="981fc-276">Is Indexed</span></span>             | <span data-ttu-id="981fc-277">否</span><span class="sxs-lookup"><span data-stu-id="981fc-277">False</span></span>                                                    |
| <span data-ttu-id="981fc-278">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="981fc-278">In Global Catalog</span></span>      | <span data-ttu-id="981fc-279">否</span><span class="sxs-lookup"><span data-stu-id="981fc-279">False</span></span>                                                    |
| <span data-ttu-id="981fc-280">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="981fc-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="981fc-281">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="981fc-281">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="981fc-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981fc-282">Range-Lower</span></span>            | <span data-ttu-id="981fc-283">1</span><span class="sxs-lookup"><span data-stu-id="981fc-283">1</span></span>                                                        |
| <span data-ttu-id="981fc-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981fc-284">Range-Upper</span></span>            | <span data-ttu-id="981fc-285">32</span><span class="sxs-lookup"><span data-stu-id="981fc-285">32</span></span>                                                       |
| <span data-ttu-id="981fc-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-286">Search-Flags</span></span>           | <span data-ttu-id="981fc-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981fc-287">0x00000000</span></span>                                               |
| <span data-ttu-id="981fc-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981fc-288">System-Flags</span></span>           | <span data-ttu-id="981fc-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981fc-289">0x00000010</span></span>                                               |
| <span data-ttu-id="981fc-290">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="981fc-290">Classes used in</span></span>        | [<span data-ttu-id="981fc-291">**位址範本**</span><span class="sxs-lookup"><span data-stu-id="981fc-291">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 





