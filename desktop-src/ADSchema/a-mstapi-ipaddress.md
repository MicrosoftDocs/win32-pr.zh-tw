---
title: ms-TAPI-Ip 位址屬性
description: 使用者登入之 TAPI 用戶端電腦的 IP 位址。 這個屬性可用來作為用來保存電腦 IP 位址的一般屬性。
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- ms-TAPI-Ip 位址屬性 AD 架構
- msTAPI-IpAddress 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103935391"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="f0464-106">ms-TAPI-Ip 位址屬性</span><span class="sxs-lookup"><span data-stu-id="f0464-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="f0464-107">使用者登入之 TAPI 用戶端電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f0464-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="f0464-108">這個屬性可用來作為用來保存電腦 IP 位址的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="f0464-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="f0464-109">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-109">Entry</span></span> | <span data-ttu-id="f0464-110">值</span><span class="sxs-lookup"><span data-stu-id="f0464-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="f0464-111">CN</span><span class="sxs-lookup"><span data-stu-id="f0464-111">CN</span></span>                | <span data-ttu-id="f0464-112">ms-TAPI-Ip 位址</span><span class="sxs-lookup"><span data-stu-id="f0464-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="f0464-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f0464-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f0464-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="f0464-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="f0464-115">大小</span><span class="sxs-lookup"><span data-stu-id="f0464-115">Size</span></span>              | <span data-ttu-id="f0464-116">每個 IP 位址會以字串的形式儲存在 b.. D 標記法中。</span><span class="sxs-lookup"><span data-stu-id="f0464-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="f0464-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f0464-117">Update Privilege</span></span>  | <span data-ttu-id="f0464-118">不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="f0464-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="f0464-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f0464-119">Update Frequency</span></span>  | <span data-ttu-id="f0464-120">通常很低。</span><span class="sxs-lookup"><span data-stu-id="f0464-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="f0464-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-121">Attribute-Id</span></span>      | <span data-ttu-id="f0464-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="f0464-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="f0464-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f0464-123">System-Id-Guid</span></span>    | <span data-ttu-id="f0464-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="f0464-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="f0464-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0464-125">Syntax</span></span>            | [<span data-ttu-id="f0464-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f0464-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="f0464-127">實作</span><span class="sxs-lookup"><span data-stu-id="f0464-127">Implementations</span></span>

-   [<span data-ttu-id="f0464-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0464-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0464-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0464-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0464-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0464-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0464-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0464-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0464-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0464-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f0464-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0464-133">Windows Server 2003</span></span>



| <span data-ttu-id="f0464-134">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-134">Entry</span></span> | <span data-ttu-id="f0464-135">值</span><span class="sxs-lookup"><span data-stu-id="f0464-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f0464-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0464-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0464-138">System-Only</span></span>            | <span data-ttu-id="f0464-139">否</span><span class="sxs-lookup"><span data-stu-id="f0464-139">False</span></span>                                                     |
| <span data-ttu-id="f0464-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0464-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f0464-141">否</span><span class="sxs-lookup"><span data-stu-id="f0464-141">False</span></span>                                                     |
| <span data-ttu-id="f0464-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0464-142">Is Indexed</span></span>             | <span data-ttu-id="f0464-143">否</span><span class="sxs-lookup"><span data-stu-id="f0464-143">False</span></span>                                                     |
| <span data-ttu-id="f0464-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0464-144">In Global Catalog</span></span>      | <span data-ttu-id="f0464-145">否</span><span class="sxs-lookup"><span data-stu-id="f0464-145">False</span></span>                                                     |
| <span data-ttu-id="f0464-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0464-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0464-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0464-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f0464-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0464-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0464-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-150">Search-Flags</span></span>           | <span data-ttu-id="f0464-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0464-151">0x00000000</span></span>                                                |
| <span data-ttu-id="f0464-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-152">System-Flags</span></span>           | <span data-ttu-id="f0464-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0464-153">0x00000010</span></span>                                                |
| <span data-ttu-id="f0464-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0464-154">Classes used in</span></span>        | [<span data-ttu-id="f0464-155">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="f0464-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0464-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0464-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0464-157">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-157">Entry</span></span> | <span data-ttu-id="f0464-158">值</span><span class="sxs-lookup"><span data-stu-id="f0464-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f0464-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0464-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0464-161">System-Only</span></span>            | <span data-ttu-id="f0464-162">否</span><span class="sxs-lookup"><span data-stu-id="f0464-162">False</span></span>                                                     |
| <span data-ttu-id="f0464-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0464-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f0464-164">否</span><span class="sxs-lookup"><span data-stu-id="f0464-164">False</span></span>                                                     |
| <span data-ttu-id="f0464-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0464-165">Is Indexed</span></span>             | <span data-ttu-id="f0464-166">否</span><span class="sxs-lookup"><span data-stu-id="f0464-166">False</span></span>                                                     |
| <span data-ttu-id="f0464-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0464-167">In Global Catalog</span></span>      | <span data-ttu-id="f0464-168">否</span><span class="sxs-lookup"><span data-stu-id="f0464-168">False</span></span>                                                     |
| <span data-ttu-id="f0464-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0464-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0464-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0464-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f0464-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0464-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0464-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-173">Search-Flags</span></span>           | <span data-ttu-id="f0464-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0464-174">0x00000000</span></span>                                                |
| <span data-ttu-id="f0464-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-175">System-Flags</span></span>           | <span data-ttu-id="f0464-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0464-176">0x00000010</span></span>                                                |
| <span data-ttu-id="f0464-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0464-177">Classes used in</span></span>        | [<span data-ttu-id="f0464-178">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="f0464-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0464-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0464-179">Windows Server 2008</span></span>



| <span data-ttu-id="f0464-180">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-180">Entry</span></span> | <span data-ttu-id="f0464-181">值</span><span class="sxs-lookup"><span data-stu-id="f0464-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f0464-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0464-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0464-184">System-Only</span></span>            | <span data-ttu-id="f0464-185">否</span><span class="sxs-lookup"><span data-stu-id="f0464-185">False</span></span>                                                     |
| <span data-ttu-id="f0464-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0464-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f0464-187">否</span><span class="sxs-lookup"><span data-stu-id="f0464-187">False</span></span>                                                     |
| <span data-ttu-id="f0464-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0464-188">Is Indexed</span></span>             | <span data-ttu-id="f0464-189">否</span><span class="sxs-lookup"><span data-stu-id="f0464-189">False</span></span>                                                     |
| <span data-ttu-id="f0464-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0464-190">In Global Catalog</span></span>      | <span data-ttu-id="f0464-191">否</span><span class="sxs-lookup"><span data-stu-id="f0464-191">False</span></span>                                                     |
| <span data-ttu-id="f0464-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0464-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0464-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0464-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f0464-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0464-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0464-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-196">Search-Flags</span></span>           | <span data-ttu-id="f0464-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0464-197">0x00000000</span></span>                                                |
| <span data-ttu-id="f0464-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-198">System-Flags</span></span>           | <span data-ttu-id="f0464-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0464-199">0x00000010</span></span>                                                |
| <span data-ttu-id="f0464-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0464-200">Classes used in</span></span>        | [<span data-ttu-id="f0464-201">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="f0464-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0464-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0464-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0464-203">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-203">Entry</span></span> | <span data-ttu-id="f0464-204">值</span><span class="sxs-lookup"><span data-stu-id="f0464-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f0464-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0464-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0464-207">System-Only</span></span>            | <span data-ttu-id="f0464-208">否</span><span class="sxs-lookup"><span data-stu-id="f0464-208">False</span></span>                                                     |
| <span data-ttu-id="f0464-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0464-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f0464-210">否</span><span class="sxs-lookup"><span data-stu-id="f0464-210">False</span></span>                                                     |
| <span data-ttu-id="f0464-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0464-211">Is Indexed</span></span>             | <span data-ttu-id="f0464-212">否</span><span class="sxs-lookup"><span data-stu-id="f0464-212">False</span></span>                                                     |
| <span data-ttu-id="f0464-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0464-213">In Global Catalog</span></span>      | <span data-ttu-id="f0464-214">否</span><span class="sxs-lookup"><span data-stu-id="f0464-214">False</span></span>                                                     |
| <span data-ttu-id="f0464-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0464-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0464-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0464-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f0464-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0464-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0464-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-219">Search-Flags</span></span>           | <span data-ttu-id="f0464-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0464-220">0x00000000</span></span>                                                |
| <span data-ttu-id="f0464-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-221">System-Flags</span></span>           | <span data-ttu-id="f0464-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0464-222">0x00000010</span></span>                                                |
| <span data-ttu-id="f0464-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0464-223">Classes used in</span></span>        | [<span data-ttu-id="f0464-224">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="f0464-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0464-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0464-225">Windows Server 2012</span></span>



| <span data-ttu-id="f0464-226">進入</span><span class="sxs-lookup"><span data-stu-id="f0464-226">Entry</span></span> | <span data-ttu-id="f0464-227">值</span><span class="sxs-lookup"><span data-stu-id="f0464-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f0464-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f0464-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0464-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="f0464-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0464-230">System-Only</span></span>            | <span data-ttu-id="f0464-231">否</span><span class="sxs-lookup"><span data-stu-id="f0464-231">False</span></span>                                                     |
| <span data-ttu-id="f0464-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f0464-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f0464-233">否</span><span class="sxs-lookup"><span data-stu-id="f0464-233">False</span></span>                                                     |
| <span data-ttu-id="f0464-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f0464-234">Is Indexed</span></span>             | <span data-ttu-id="f0464-235">否</span><span class="sxs-lookup"><span data-stu-id="f0464-235">False</span></span>                                                     |
| <span data-ttu-id="f0464-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f0464-236">In Global Catalog</span></span>      | <span data-ttu-id="f0464-237">否</span><span class="sxs-lookup"><span data-stu-id="f0464-237">False</span></span>                                                     |
| <span data-ttu-id="f0464-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f0464-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0464-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f0464-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="f0464-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0464-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0464-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="f0464-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-242">Search-Flags</span></span>           | <span data-ttu-id="f0464-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0464-243">0x00000000</span></span>                                                |
| <span data-ttu-id="f0464-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0464-244">System-Flags</span></span>           | <span data-ttu-id="f0464-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0464-245">0x00000010</span></span>                                                |
| <span data-ttu-id="f0464-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f0464-246">Classes used in</span></span>        | [<span data-ttu-id="f0464-247">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="f0464-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





