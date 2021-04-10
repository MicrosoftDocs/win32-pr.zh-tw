---
title: ms-chap-通訊協定識別碼屬性
description: 此屬性工作表示 TAPI 會議類型。
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- ms-chap-通訊協定識別碼屬性 AD 架構
- msTAPI-ProtocolId 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10538f66b98988fafa69d4fe2f3e70b47348c999
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108057"
---
# <a name="ms-tapi-protocol-id-attribute"></a><span data-ttu-id="ddf56-105">ms-chap-通訊協定識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="ddf56-105">ms-TAPI-Protocol-Id attribute</span></span>

<span data-ttu-id="ddf56-106">此屬性工作表示 TAPI 會議類型。</span><span class="sxs-lookup"><span data-stu-id="ddf56-106">This attribute indicates the TAPI conference type.</span></span> <span data-ttu-id="ddf56-107">這個屬性是用來決定要如何解讀 [**MS TAPI 會議 blob**](a-mstapi-conferenceblob.md) 屬性中的二進位 BLOB。</span><span class="sxs-lookup"><span data-stu-id="ddf56-107">This attribute is used to determine how the binary BLOB in the [**ms-TAPI-Conference-Blob**](a-mstapi-conferenceblob.md) attribute is to be interpreted.</span></span> <span data-ttu-id="ddf56-108">這個屬性是任一字元串，其長度通常少於100個字元。</span><span class="sxs-lookup"><span data-stu-id="ddf56-108">This attribute is an arbitrary string, typically less than 100 characters in length.</span></span>



| <span data-ttu-id="ddf56-109">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-109">Entry</span></span> | <span data-ttu-id="ddf56-110">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="ddf56-111">CN</span><span class="sxs-lookup"><span data-stu-id="ddf56-111">CN</span></span>                | <span data-ttu-id="ddf56-112">ms-chap-通訊協定-識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-112">ms-TAPI-Protocol-Id</span></span>                                        |
| <span data-ttu-id="ddf56-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ddf56-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ddf56-114">msTAPI-ProtocolId</span><span class="sxs-lookup"><span data-stu-id="ddf56-114">msTAPI-ProtocolId</span></span>                                          |
| <span data-ttu-id="ddf56-115">大小</span><span class="sxs-lookup"><span data-stu-id="ddf56-115">Size</span></span>              | \-                                                         |
| <span data-ttu-id="ddf56-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ddf56-116">Update Privilege</span></span>  | <span data-ttu-id="ddf56-117">不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="ddf56-117">No special privileges required.</span></span>                            |
| <span data-ttu-id="ddf56-118">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ddf56-118">Update Frequency</span></span>  | <span data-ttu-id="ddf56-119">在建立 Rt-Conference 物件時設定一次。</span><span class="sxs-lookup"><span data-stu-id="ddf56-119">Set once at the time of creating the Rt-Conference object.</span></span> |
| <span data-ttu-id="ddf56-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-120">Attribute-Id</span></span>      | <span data-ttu-id="ddf56-121">1.2.840.113556.1.4.1699</span><span class="sxs-lookup"><span data-stu-id="ddf56-121">1.2.840.113556.1.4.1699</span></span>                                    |
| <span data-ttu-id="ddf56-122">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ddf56-122">System-Id-Guid</span></span>    | <span data-ttu-id="ddf56-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span><span class="sxs-lookup"><span data-stu-id="ddf56-123">89c1ebcf-7a5f-41fd-99ca-c900b32299ab</span></span>                       |
| <span data-ttu-id="ddf56-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddf56-124">Syntax</span></span>            | [<span data-ttu-id="ddf56-125">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="ddf56-125">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="ddf56-126">實作</span><span class="sxs-lookup"><span data-stu-id="ddf56-126">Implementations</span></span>

-   [<span data-ttu-id="ddf56-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ddf56-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ddf56-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf56-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ddf56-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ddf56-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ddf56-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ddf56-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ddf56-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ddf56-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ddf56-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ddf56-132">Windows Server 2003</span></span>



| <span data-ttu-id="ddf56-133">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-133">Entry</span></span> | <span data-ttu-id="ddf56-134">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-134">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ddf56-135">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-135">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-136">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf56-137">System-Only</span></span>            | <span data-ttu-id="ddf56-138">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-138">False</span></span>                                                             |
| <span data-ttu-id="ddf56-139">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ddf56-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf56-140">對</span><span class="sxs-lookup"><span data-stu-id="ddf56-140">True</span></span>                                                              |
| <span data-ttu-id="ddf56-141">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ddf56-141">Is Indexed</span></span>             | <span data-ttu-id="ddf56-142">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-142">False</span></span>                                                             |
| <span data-ttu-id="ddf56-143">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ddf56-143">In Global Catalog</span></span>      | <span data-ttu-id="ddf56-144">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-144">False</span></span>                                                             |
| <span data-ttu-id="ddf56-145">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ddf56-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf56-146">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ddf56-146">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ddf56-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf56-147">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf56-148">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-149">Search-Flags</span></span>           | <span data-ttu-id="ddf56-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf56-150">0x00000000</span></span>                                                        |
| <span data-ttu-id="ddf56-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-151">System-Flags</span></span>           | <span data-ttu-id="ddf56-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf56-152">0x00000010</span></span>                                                        |
| <span data-ttu-id="ddf56-153">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ddf56-153">Classes used in</span></span>        | [<span data-ttu-id="ddf56-154">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ddf56-154">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ddf56-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ddf56-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ddf56-156">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-156">Entry</span></span> | <span data-ttu-id="ddf56-157">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ddf56-158">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-158">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-159">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf56-160">System-Only</span></span>            | <span data-ttu-id="ddf56-161">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-161">False</span></span>                                                             |
| <span data-ttu-id="ddf56-162">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ddf56-162">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf56-163">對</span><span class="sxs-lookup"><span data-stu-id="ddf56-163">True</span></span>                                                              |
| <span data-ttu-id="ddf56-164">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ddf56-164">Is Indexed</span></span>             | <span data-ttu-id="ddf56-165">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-165">False</span></span>                                                             |
| <span data-ttu-id="ddf56-166">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ddf56-166">In Global Catalog</span></span>      | <span data-ttu-id="ddf56-167">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-167">False</span></span>                                                             |
| <span data-ttu-id="ddf56-168">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ddf56-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf56-169">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ddf56-169">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ddf56-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf56-170">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf56-171">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-172">Search-Flags</span></span>           | <span data-ttu-id="ddf56-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf56-173">0x00000000</span></span>                                                        |
| <span data-ttu-id="ddf56-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-174">System-Flags</span></span>           | <span data-ttu-id="ddf56-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf56-175">0x00000010</span></span>                                                        |
| <span data-ttu-id="ddf56-176">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ddf56-176">Classes used in</span></span>        | [<span data-ttu-id="ddf56-177">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ddf56-177">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ddf56-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddf56-178">Windows Server 2008</span></span>



| <span data-ttu-id="ddf56-179">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-179">Entry</span></span> | <span data-ttu-id="ddf56-180">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ddf56-181">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-181">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-182">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf56-183">System-Only</span></span>            | <span data-ttu-id="ddf56-184">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-184">False</span></span>                                                             |
| <span data-ttu-id="ddf56-185">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ddf56-185">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf56-186">對</span><span class="sxs-lookup"><span data-stu-id="ddf56-186">True</span></span>                                                              |
| <span data-ttu-id="ddf56-187">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ddf56-187">Is Indexed</span></span>             | <span data-ttu-id="ddf56-188">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-188">False</span></span>                                                             |
| <span data-ttu-id="ddf56-189">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ddf56-189">In Global Catalog</span></span>      | <span data-ttu-id="ddf56-190">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-190">False</span></span>                                                             |
| <span data-ttu-id="ddf56-191">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ddf56-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf56-192">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ddf56-192">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ddf56-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf56-193">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf56-194">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-195">Search-Flags</span></span>           | <span data-ttu-id="ddf56-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf56-196">0x00000000</span></span>                                                        |
| <span data-ttu-id="ddf56-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-197">System-Flags</span></span>           | <span data-ttu-id="ddf56-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf56-198">0x00000010</span></span>                                                        |
| <span data-ttu-id="ddf56-199">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ddf56-199">Classes used in</span></span>        | [<span data-ttu-id="ddf56-200">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ddf56-200">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ddf56-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ddf56-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ddf56-202">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-202">Entry</span></span> | <span data-ttu-id="ddf56-203">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ddf56-204">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-204">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-205">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf56-206">System-Only</span></span>            | <span data-ttu-id="ddf56-207">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-207">False</span></span>                                                             |
| <span data-ttu-id="ddf56-208">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ddf56-208">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf56-209">對</span><span class="sxs-lookup"><span data-stu-id="ddf56-209">True</span></span>                                                              |
| <span data-ttu-id="ddf56-210">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ddf56-210">Is Indexed</span></span>             | <span data-ttu-id="ddf56-211">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-211">False</span></span>                                                             |
| <span data-ttu-id="ddf56-212">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ddf56-212">In Global Catalog</span></span>      | <span data-ttu-id="ddf56-213">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-213">False</span></span>                                                             |
| <span data-ttu-id="ddf56-214">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ddf56-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf56-215">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ddf56-215">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ddf56-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf56-216">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf56-217">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-218">Search-Flags</span></span>           | <span data-ttu-id="ddf56-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf56-219">0x00000000</span></span>                                                        |
| <span data-ttu-id="ddf56-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-220">System-Flags</span></span>           | <span data-ttu-id="ddf56-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf56-221">0x00000010</span></span>                                                        |
| <span data-ttu-id="ddf56-222">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ddf56-222">Classes used in</span></span>        | [<span data-ttu-id="ddf56-223">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ddf56-223">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ddf56-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddf56-224">Windows Server 2012</span></span>



| <span data-ttu-id="ddf56-225">進入</span><span class="sxs-lookup"><span data-stu-id="ddf56-225">Entry</span></span> | <span data-ttu-id="ddf56-226">值</span><span class="sxs-lookup"><span data-stu-id="ddf56-226">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ddf56-227">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ddf56-227">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ddf56-228">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ddf56-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="ddf56-229">System-Only</span></span>            | <span data-ttu-id="ddf56-230">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-230">False</span></span>                                                             |
| <span data-ttu-id="ddf56-231">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ddf56-231">Is-Single-Valued</span></span>       | <span data-ttu-id="ddf56-232">對</span><span class="sxs-lookup"><span data-stu-id="ddf56-232">True</span></span>                                                              |
| <span data-ttu-id="ddf56-233">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ddf56-233">Is Indexed</span></span>             | <span data-ttu-id="ddf56-234">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-234">False</span></span>                                                             |
| <span data-ttu-id="ddf56-235">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ddf56-235">In Global Catalog</span></span>      | <span data-ttu-id="ddf56-236">否</span><span class="sxs-lookup"><span data-stu-id="ddf56-236">False</span></span>                                                             |
| <span data-ttu-id="ddf56-237">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ddf56-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="ddf56-238">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ddf56-238">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ddf56-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ddf56-239">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ddf56-240">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ddf56-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-241">Search-Flags</span></span>           | <span data-ttu-id="ddf56-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ddf56-242">0x00000000</span></span>                                                        |
| <span data-ttu-id="ddf56-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ddf56-243">System-Flags</span></span>           | <span data-ttu-id="ddf56-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ddf56-244">0x00000010</span></span>                                                        |
| <span data-ttu-id="ddf56-245">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ddf56-245">Classes used in</span></span>        | [<span data-ttu-id="ddf56-246">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ddf56-246">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





