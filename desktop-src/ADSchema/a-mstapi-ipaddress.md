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
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="49a19-106">ms-TAPI-Ip 位址屬性</span><span class="sxs-lookup"><span data-stu-id="49a19-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="49a19-107">使用者登入之 TAPI 用戶端電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="49a19-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="49a19-108">這個屬性可用來作為用來保存電腦 IP 位址的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="49a19-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="49a19-109">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-109">Entry</span></span> | <span data-ttu-id="49a19-110">值</span><span class="sxs-lookup"><span data-stu-id="49a19-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="49a19-111">CN</span><span class="sxs-lookup"><span data-stu-id="49a19-111">CN</span></span>                | <span data-ttu-id="49a19-112">ms-TAPI-Ip 位址</span><span class="sxs-lookup"><span data-stu-id="49a19-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="49a19-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="49a19-113">Ldap-Display-Name</span></span> | <span data-ttu-id="49a19-114">msTAPI-IpAddress</span><span class="sxs-lookup"><span data-stu-id="49a19-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="49a19-115">大小</span><span class="sxs-lookup"><span data-stu-id="49a19-115">Size</span></span>              | <span data-ttu-id="49a19-116">每個 IP 位址會以字串的形式儲存在 b.. D 標記法中。</span><span class="sxs-lookup"><span data-stu-id="49a19-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="49a19-117">更新許可權</span><span class="sxs-lookup"><span data-stu-id="49a19-117">Update Privilege</span></span>  | <span data-ttu-id="49a19-118">不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="49a19-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="49a19-119">更新頻率</span><span class="sxs-lookup"><span data-stu-id="49a19-119">Update Frequency</span></span>  | <span data-ttu-id="49a19-120">通常很低。</span><span class="sxs-lookup"><span data-stu-id="49a19-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="49a19-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-121">Attribute-Id</span></span>      | <span data-ttu-id="49a19-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="49a19-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="49a19-123">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="49a19-123">System-Id-Guid</span></span>    | <span data-ttu-id="49a19-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="49a19-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="49a19-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a19-125">Syntax</span></span>            | [<span data-ttu-id="49a19-126">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="49a19-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="49a19-127">實作</span><span class="sxs-lookup"><span data-stu-id="49a19-127">Implementations</span></span>

-   [<span data-ttu-id="49a19-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49a19-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49a19-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49a19-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49a19-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49a19-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49a19-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49a19-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49a19-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49a19-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="49a19-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49a19-133">Windows Server 2003</span></span>



| <span data-ttu-id="49a19-134">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-134">Entry</span></span> | <span data-ttu-id="49a19-135">值</span><span class="sxs-lookup"><span data-stu-id="49a19-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="49a19-136">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49a19-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="49a19-138">System-Only</span></span>            | <span data-ttu-id="49a19-139">否</span><span class="sxs-lookup"><span data-stu-id="49a19-139">False</span></span>                                                     |
| <span data-ttu-id="49a19-140">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49a19-140">Is-Single-Valued</span></span>       | <span data-ttu-id="49a19-141">否</span><span class="sxs-lookup"><span data-stu-id="49a19-141">False</span></span>                                                     |
| <span data-ttu-id="49a19-142">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49a19-142">Is Indexed</span></span>             | <span data-ttu-id="49a19-143">否</span><span class="sxs-lookup"><span data-stu-id="49a19-143">False</span></span>                                                     |
| <span data-ttu-id="49a19-144">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49a19-144">In Global Catalog</span></span>      | <span data-ttu-id="49a19-145">否</span><span class="sxs-lookup"><span data-stu-id="49a19-145">False</span></span>                                                     |
| <span data-ttu-id="49a19-146">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49a19-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="49a19-147">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49a19-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="49a19-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49a19-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49a19-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-150">Search-Flags</span></span>           | <span data-ttu-id="49a19-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49a19-151">0x00000000</span></span>                                                |
| <span data-ttu-id="49a19-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-152">System-Flags</span></span>           | <span data-ttu-id="49a19-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49a19-153">0x00000010</span></span>                                                |
| <span data-ttu-id="49a19-154">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49a19-154">Classes used in</span></span>        | [<span data-ttu-id="49a19-155">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="49a19-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49a19-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49a19-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49a19-157">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-157">Entry</span></span> | <span data-ttu-id="49a19-158">值</span><span class="sxs-lookup"><span data-stu-id="49a19-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="49a19-159">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49a19-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="49a19-161">System-Only</span></span>            | <span data-ttu-id="49a19-162">否</span><span class="sxs-lookup"><span data-stu-id="49a19-162">False</span></span>                                                     |
| <span data-ttu-id="49a19-163">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49a19-163">Is-Single-Valued</span></span>       | <span data-ttu-id="49a19-164">否</span><span class="sxs-lookup"><span data-stu-id="49a19-164">False</span></span>                                                     |
| <span data-ttu-id="49a19-165">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49a19-165">Is Indexed</span></span>             | <span data-ttu-id="49a19-166">否</span><span class="sxs-lookup"><span data-stu-id="49a19-166">False</span></span>                                                     |
| <span data-ttu-id="49a19-167">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49a19-167">In Global Catalog</span></span>      | <span data-ttu-id="49a19-168">否</span><span class="sxs-lookup"><span data-stu-id="49a19-168">False</span></span>                                                     |
| <span data-ttu-id="49a19-169">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49a19-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="49a19-170">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49a19-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="49a19-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49a19-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49a19-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-173">Search-Flags</span></span>           | <span data-ttu-id="49a19-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49a19-174">0x00000000</span></span>                                                |
| <span data-ttu-id="49a19-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-175">System-Flags</span></span>           | <span data-ttu-id="49a19-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49a19-176">0x00000010</span></span>                                                |
| <span data-ttu-id="49a19-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49a19-177">Classes used in</span></span>        | [<span data-ttu-id="49a19-178">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="49a19-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49a19-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49a19-179">Windows Server 2008</span></span>



| <span data-ttu-id="49a19-180">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-180">Entry</span></span> | <span data-ttu-id="49a19-181">值</span><span class="sxs-lookup"><span data-stu-id="49a19-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="49a19-182">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49a19-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="49a19-184">System-Only</span></span>            | <span data-ttu-id="49a19-185">否</span><span class="sxs-lookup"><span data-stu-id="49a19-185">False</span></span>                                                     |
| <span data-ttu-id="49a19-186">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49a19-186">Is-Single-Valued</span></span>       | <span data-ttu-id="49a19-187">否</span><span class="sxs-lookup"><span data-stu-id="49a19-187">False</span></span>                                                     |
| <span data-ttu-id="49a19-188">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49a19-188">Is Indexed</span></span>             | <span data-ttu-id="49a19-189">否</span><span class="sxs-lookup"><span data-stu-id="49a19-189">False</span></span>                                                     |
| <span data-ttu-id="49a19-190">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49a19-190">In Global Catalog</span></span>      | <span data-ttu-id="49a19-191">否</span><span class="sxs-lookup"><span data-stu-id="49a19-191">False</span></span>                                                     |
| <span data-ttu-id="49a19-192">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49a19-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="49a19-193">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49a19-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="49a19-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49a19-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49a19-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-196">Search-Flags</span></span>           | <span data-ttu-id="49a19-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49a19-197">0x00000000</span></span>                                                |
| <span data-ttu-id="49a19-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-198">System-Flags</span></span>           | <span data-ttu-id="49a19-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49a19-199">0x00000010</span></span>                                                |
| <span data-ttu-id="49a19-200">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49a19-200">Classes used in</span></span>        | [<span data-ttu-id="49a19-201">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="49a19-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49a19-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49a19-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49a19-203">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-203">Entry</span></span> | <span data-ttu-id="49a19-204">值</span><span class="sxs-lookup"><span data-stu-id="49a19-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="49a19-205">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49a19-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="49a19-207">System-Only</span></span>            | <span data-ttu-id="49a19-208">否</span><span class="sxs-lookup"><span data-stu-id="49a19-208">False</span></span>                                                     |
| <span data-ttu-id="49a19-209">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49a19-209">Is-Single-Valued</span></span>       | <span data-ttu-id="49a19-210">否</span><span class="sxs-lookup"><span data-stu-id="49a19-210">False</span></span>                                                     |
| <span data-ttu-id="49a19-211">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49a19-211">Is Indexed</span></span>             | <span data-ttu-id="49a19-212">否</span><span class="sxs-lookup"><span data-stu-id="49a19-212">False</span></span>                                                     |
| <span data-ttu-id="49a19-213">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49a19-213">In Global Catalog</span></span>      | <span data-ttu-id="49a19-214">否</span><span class="sxs-lookup"><span data-stu-id="49a19-214">False</span></span>                                                     |
| <span data-ttu-id="49a19-215">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49a19-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="49a19-216">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49a19-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="49a19-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49a19-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49a19-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-219">Search-Flags</span></span>           | <span data-ttu-id="49a19-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49a19-220">0x00000000</span></span>                                                |
| <span data-ttu-id="49a19-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-221">System-Flags</span></span>           | <span data-ttu-id="49a19-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49a19-222">0x00000010</span></span>                                                |
| <span data-ttu-id="49a19-223">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49a19-223">Classes used in</span></span>        | [<span data-ttu-id="49a19-224">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="49a19-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49a19-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49a19-225">Windows Server 2012</span></span>



| <span data-ttu-id="49a19-226">進入</span><span class="sxs-lookup"><span data-stu-id="49a19-226">Entry</span></span> | <span data-ttu-id="49a19-227">值</span><span class="sxs-lookup"><span data-stu-id="49a19-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="49a19-228">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="49a19-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49a19-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="49a19-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="49a19-230">System-Only</span></span>            | <span data-ttu-id="49a19-231">否</span><span class="sxs-lookup"><span data-stu-id="49a19-231">False</span></span>                                                     |
| <span data-ttu-id="49a19-232">是-單一值</span><span class="sxs-lookup"><span data-stu-id="49a19-232">Is-Single-Valued</span></span>       | <span data-ttu-id="49a19-233">否</span><span class="sxs-lookup"><span data-stu-id="49a19-233">False</span></span>                                                     |
| <span data-ttu-id="49a19-234">已編制索引</span><span class="sxs-lookup"><span data-stu-id="49a19-234">Is Indexed</span></span>             | <span data-ttu-id="49a19-235">否</span><span class="sxs-lookup"><span data-stu-id="49a19-235">False</span></span>                                                     |
| <span data-ttu-id="49a19-236">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="49a19-236">In Global Catalog</span></span>      | <span data-ttu-id="49a19-237">否</span><span class="sxs-lookup"><span data-stu-id="49a19-237">False</span></span>                                                     |
| <span data-ttu-id="49a19-238">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="49a19-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="49a19-239">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="49a19-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="49a19-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49a19-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49a19-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="49a19-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-242">Search-Flags</span></span>           | <span data-ttu-id="49a19-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49a19-243">0x00000000</span></span>                                                |
| <span data-ttu-id="49a19-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49a19-244">System-Flags</span></span>           | <span data-ttu-id="49a19-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49a19-245">0x00000010</span></span>                                                |
| <span data-ttu-id="49a19-246">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="49a19-246">Classes used in</span></span>        | [<span data-ttu-id="49a19-247">**ms-TAPI-Rt-Person**</span><span class="sxs-lookup"><span data-stu-id="49a19-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





