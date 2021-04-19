---
title: ms-TAPI-會議-Blob 屬性
description: 描述 TAPI 多播會議各項屬性之資料的二進位 BLOB。 其格式和內容是由相同物件中 Protocol-Id 屬性值所決定。 一般而言，此 BLOB 中的資料會符合 RFC2327。
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- ms-TAPI-會議-Blob 屬性 AD 架構
- msTAPI-ConferenceBlob 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106973722"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="ce06f-107">ms-TAPI-會議-Blob 屬性</span><span class="sxs-lookup"><span data-stu-id="ce06f-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="ce06f-108">描述 TAPI 多播會議各項屬性之資料的二進位 BLOB。</span><span class="sxs-lookup"><span data-stu-id="ce06f-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="ce06f-109">其格式和內容是由相同物件中 Protocol-Id 屬性值所決定。</span><span class="sxs-lookup"><span data-stu-id="ce06f-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="ce06f-110">一般而言，此 BLOB 中的資料會符合 RFC2327。</span><span class="sxs-lookup"><span data-stu-id="ce06f-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="ce06f-111">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-111">Entry</span></span> | <span data-ttu-id="ce06f-112">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce06f-113">CN</span><span class="sxs-lookup"><span data-stu-id="ce06f-113">CN</span></span>                | <span data-ttu-id="ce06f-114">ms-TAPI-會議-Blob</span><span class="sxs-lookup"><span data-stu-id="ce06f-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="ce06f-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="ce06f-115">Ldap-Display-Name</span></span> | <span data-ttu-id="ce06f-116">msTAPI-ConferenceBlob</span><span class="sxs-lookup"><span data-stu-id="ce06f-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="ce06f-117">大小</span><span class="sxs-lookup"><span data-stu-id="ce06f-117">Size</span></span>              | <span data-ttu-id="ce06f-118">可以是任意長度。</span><span class="sxs-lookup"><span data-stu-id="ce06f-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="ce06f-119">更新許可權</span><span class="sxs-lookup"><span data-stu-id="ce06f-119">Update Privilege</span></span>  | <span data-ttu-id="ce06f-120">不需要任何特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="ce06f-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="ce06f-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="ce06f-121">Update Frequency</span></span>  | <span data-ttu-id="ce06f-122">當會議的一些資料需要變更時，可能會因為 TAPI 會議擁有者而變更。</span><span class="sxs-lookup"><span data-stu-id="ce06f-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="ce06f-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-123">Attribute-Id</span></span>      | <span data-ttu-id="ce06f-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="ce06f-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="ce06f-125">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="ce06f-125">System-Id-Guid</span></span>    | <span data-ttu-id="ce06f-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="ce06f-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="ce06f-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce06f-127">Syntax</span></span>            | [<span data-ttu-id="ce06f-128">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="ce06f-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="ce06f-129">實作</span><span class="sxs-lookup"><span data-stu-id="ce06f-129">Implementations</span></span>

-   [<span data-ttu-id="ce06f-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ce06f-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ce06f-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ce06f-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ce06f-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ce06f-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ce06f-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ce06f-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ce06f-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ce06f-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="ce06f-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce06f-135">Windows Server 2003</span></span>



| <span data-ttu-id="ce06f-136">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-136">Entry</span></span> | <span data-ttu-id="ce06f-137">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ce06f-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce06f-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce06f-140">System-Only</span></span>            | <span data-ttu-id="ce06f-141">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-141">False</span></span>                                                             |
| <span data-ttu-id="ce06f-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce06f-142">Is-Single-Valued</span></span>       | <span data-ttu-id="ce06f-143">對</span><span class="sxs-lookup"><span data-stu-id="ce06f-143">True</span></span>                                                              |
| <span data-ttu-id="ce06f-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce06f-144">Is Indexed</span></span>             | <span data-ttu-id="ce06f-145">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-145">False</span></span>                                                             |
| <span data-ttu-id="ce06f-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce06f-146">In Global Catalog</span></span>      | <span data-ttu-id="ce06f-147">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-147">False</span></span>                                                             |
| <span data-ttu-id="ce06f-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce06f-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce06f-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce06f-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ce06f-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce06f-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce06f-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-152">Search-Flags</span></span>           | <span data-ttu-id="ce06f-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce06f-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="ce06f-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-154">System-Flags</span></span>           | <span data-ttu-id="ce06f-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce06f-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="ce06f-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce06f-156">Classes used in</span></span>        | [<span data-ttu-id="ce06f-157">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ce06f-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ce06f-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ce06f-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ce06f-159">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-159">Entry</span></span> | <span data-ttu-id="ce06f-160">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ce06f-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce06f-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce06f-163">System-Only</span></span>            | <span data-ttu-id="ce06f-164">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-164">False</span></span>                                                             |
| <span data-ttu-id="ce06f-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce06f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ce06f-166">對</span><span class="sxs-lookup"><span data-stu-id="ce06f-166">True</span></span>                                                              |
| <span data-ttu-id="ce06f-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce06f-167">Is Indexed</span></span>             | <span data-ttu-id="ce06f-168">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-168">False</span></span>                                                             |
| <span data-ttu-id="ce06f-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce06f-169">In Global Catalog</span></span>      | <span data-ttu-id="ce06f-170">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-170">False</span></span>                                                             |
| <span data-ttu-id="ce06f-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce06f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce06f-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce06f-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ce06f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce06f-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce06f-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-175">Search-Flags</span></span>           | <span data-ttu-id="ce06f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce06f-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="ce06f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-177">System-Flags</span></span>           | <span data-ttu-id="ce06f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce06f-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="ce06f-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce06f-179">Classes used in</span></span>        | [<span data-ttu-id="ce06f-180">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ce06f-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ce06f-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce06f-181">Windows Server 2008</span></span>



| <span data-ttu-id="ce06f-182">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-182">Entry</span></span> | <span data-ttu-id="ce06f-183">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ce06f-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce06f-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce06f-186">System-Only</span></span>            | <span data-ttu-id="ce06f-187">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-187">False</span></span>                                                             |
| <span data-ttu-id="ce06f-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce06f-188">Is-Single-Valued</span></span>       | <span data-ttu-id="ce06f-189">對</span><span class="sxs-lookup"><span data-stu-id="ce06f-189">True</span></span>                                                              |
| <span data-ttu-id="ce06f-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce06f-190">Is Indexed</span></span>             | <span data-ttu-id="ce06f-191">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-191">False</span></span>                                                             |
| <span data-ttu-id="ce06f-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce06f-192">In Global Catalog</span></span>      | <span data-ttu-id="ce06f-193">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-193">False</span></span>                                                             |
| <span data-ttu-id="ce06f-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce06f-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce06f-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce06f-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ce06f-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce06f-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce06f-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-198">Search-Flags</span></span>           | <span data-ttu-id="ce06f-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce06f-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="ce06f-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-200">System-Flags</span></span>           | <span data-ttu-id="ce06f-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce06f-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="ce06f-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce06f-202">Classes used in</span></span>        | [<span data-ttu-id="ce06f-203">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ce06f-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ce06f-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce06f-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ce06f-205">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-205">Entry</span></span> | <span data-ttu-id="ce06f-206">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ce06f-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce06f-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce06f-209">System-Only</span></span>            | <span data-ttu-id="ce06f-210">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-210">False</span></span>                                                             |
| <span data-ttu-id="ce06f-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce06f-211">Is-Single-Valued</span></span>       | <span data-ttu-id="ce06f-212">對</span><span class="sxs-lookup"><span data-stu-id="ce06f-212">True</span></span>                                                              |
| <span data-ttu-id="ce06f-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce06f-213">Is Indexed</span></span>             | <span data-ttu-id="ce06f-214">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-214">False</span></span>                                                             |
| <span data-ttu-id="ce06f-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce06f-215">In Global Catalog</span></span>      | <span data-ttu-id="ce06f-216">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-216">False</span></span>                                                             |
| <span data-ttu-id="ce06f-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce06f-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce06f-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce06f-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ce06f-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce06f-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce06f-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-221">Search-Flags</span></span>           | <span data-ttu-id="ce06f-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce06f-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="ce06f-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-223">System-Flags</span></span>           | <span data-ttu-id="ce06f-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce06f-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="ce06f-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce06f-225">Classes used in</span></span>        | [<span data-ttu-id="ce06f-226">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ce06f-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ce06f-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ce06f-227">Windows Server 2012</span></span>



| <span data-ttu-id="ce06f-228">進入</span><span class="sxs-lookup"><span data-stu-id="ce06f-228">Entry</span></span> | <span data-ttu-id="ce06f-229">值</span><span class="sxs-lookup"><span data-stu-id="ce06f-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="ce06f-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="ce06f-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ce06f-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="ce06f-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="ce06f-232">System-Only</span></span>            | <span data-ttu-id="ce06f-233">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-233">False</span></span>                                                             |
| <span data-ttu-id="ce06f-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="ce06f-234">Is-Single-Valued</span></span>       | <span data-ttu-id="ce06f-235">對</span><span class="sxs-lookup"><span data-stu-id="ce06f-235">True</span></span>                                                              |
| <span data-ttu-id="ce06f-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="ce06f-236">Is Indexed</span></span>             | <span data-ttu-id="ce06f-237">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-237">False</span></span>                                                             |
| <span data-ttu-id="ce06f-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="ce06f-238">In Global Catalog</span></span>      | <span data-ttu-id="ce06f-239">否</span><span class="sxs-lookup"><span data-stu-id="ce06f-239">False</span></span>                                                             |
| <span data-ttu-id="ce06f-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="ce06f-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="ce06f-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="ce06f-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="ce06f-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ce06f-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ce06f-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="ce06f-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-244">Search-Flags</span></span>           | <span data-ttu-id="ce06f-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ce06f-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="ce06f-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ce06f-246">System-Flags</span></span>           | <span data-ttu-id="ce06f-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce06f-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="ce06f-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="ce06f-248">Classes used in</span></span>        | [<span data-ttu-id="ce06f-249">**ms-TAPI-Rt-會議**</span><span class="sxs-lookup"><span data-stu-id="ce06f-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





