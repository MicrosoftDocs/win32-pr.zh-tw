---
title: SPN-Mappings 屬性
description: 這個多重值屬性包含服務主體名稱的清單 (SPN) 來顯示 SPN 類型的等價。
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings 屬性 AD 架構
- sPNMappings 屬性 AD 架構
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509658"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="27e81-105">SPN-Mappings 屬性</span><span class="sxs-lookup"><span data-stu-id="27e81-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="27e81-106">這個多重值屬性包含服務主體名稱的清單 (SPN) 來顯示 SPN 類型的等價。</span><span class="sxs-lookup"><span data-stu-id="27e81-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="27e81-107">SPN 是用戶端用來唯一識別服務實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="27e81-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="27e81-108">若您透過樹系在電腦上安裝多個服務執行個體，則每個執行個體都須有自己的 SPN。</span><span class="sxs-lookup"><span data-stu-id="27e81-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="27e81-109">若用戶端需使用多個名稱進行驗證，則指定的服務執行個體可擁有多個 SPN。</span><span class="sxs-lookup"><span data-stu-id="27e81-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="27e81-110">例如，"ldap/..."Spn 可以對應，使其相當於「主機/...」Spn。</span><span class="sxs-lookup"><span data-stu-id="27e81-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="27e81-111">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-111">Entry</span></span> | <span data-ttu-id="27e81-112">值</span><span class="sxs-lookup"><span data-stu-id="27e81-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e81-113">CN</span><span class="sxs-lookup"><span data-stu-id="27e81-113">CN</span></span>                | <span data-ttu-id="27e81-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="27e81-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="27e81-115">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="27e81-115">Ldap-Display-Name</span></span> | <span data-ttu-id="27e81-116">sPNMappings</span><span class="sxs-lookup"><span data-stu-id="27e81-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="27e81-117">大小</span><span class="sxs-lookup"><span data-stu-id="27e81-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="27e81-118">更新許可權</span><span class="sxs-lookup"><span data-stu-id="27e81-118">Update Privilege</span></span>  | <span data-ttu-id="27e81-119">此值會在產品安裝期間設定。</span><span class="sxs-lookup"><span data-stu-id="27e81-119">This value is set during the product installation.</span></span> <span data-ttu-id="27e81-120">系統管理員可以在稍後修改它。</span><span class="sxs-lookup"><span data-stu-id="27e81-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="27e81-121">更新頻率</span><span class="sxs-lookup"><span data-stu-id="27e81-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="27e81-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-122">Attribute-Id</span></span>      | <span data-ttu-id="27e81-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="27e81-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="27e81-124">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="27e81-124">System-Id-Guid</span></span>    | <span data-ttu-id="27e81-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="27e81-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="27e81-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="27e81-126">Syntax</span></span>            | [<span data-ttu-id="27e81-127">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="27e81-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="27e81-128">實作</span><span class="sxs-lookup"><span data-stu-id="27e81-128">Implementations</span></span>

-   [<span data-ttu-id="27e81-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27e81-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27e81-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27e81-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27e81-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27e81-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27e81-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27e81-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27e81-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27e81-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27e81-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27e81-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27e81-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27e81-135">Windows 2000 Server</span></span>



| <span data-ttu-id="27e81-136">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-136">Entry</span></span> | <span data-ttu-id="27e81-137">值</span><span class="sxs-lookup"><span data-stu-id="27e81-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-138">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-140">System-Only</span></span>            | <span data-ttu-id="27e81-141">否</span><span class="sxs-lookup"><span data-stu-id="27e81-141">False</span></span>                                            |
| <span data-ttu-id="27e81-142">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-142">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-143">否</span><span class="sxs-lookup"><span data-stu-id="27e81-143">False</span></span>                                            |
| <span data-ttu-id="27e81-144">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-144">Is Indexed</span></span>             | <span data-ttu-id="27e81-145">否</span><span class="sxs-lookup"><span data-stu-id="27e81-145">False</span></span>                                            |
| <span data-ttu-id="27e81-146">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-146">In Global Catalog</span></span>      | <span data-ttu-id="27e81-147">否</span><span class="sxs-lookup"><span data-stu-id="27e81-147">False</span></span>                                            |
| <span data-ttu-id="27e81-148">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-149">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-152">Search-Flags</span></span>           | <span data-ttu-id="27e81-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-153">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-154">System-Flags</span></span>           | <span data-ttu-id="27e81-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-155">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-156">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-156">Classes used in</span></span>        | [<span data-ttu-id="27e81-157">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27e81-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27e81-158">Windows Server 2003</span></span>



| <span data-ttu-id="27e81-159">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-159">Entry</span></span> | <span data-ttu-id="27e81-160">值</span><span class="sxs-lookup"><span data-stu-id="27e81-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-161">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-163">System-Only</span></span>            | <span data-ttu-id="27e81-164">否</span><span class="sxs-lookup"><span data-stu-id="27e81-164">False</span></span>                                            |
| <span data-ttu-id="27e81-165">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-165">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-166">否</span><span class="sxs-lookup"><span data-stu-id="27e81-166">False</span></span>                                            |
| <span data-ttu-id="27e81-167">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-167">Is Indexed</span></span>             | <span data-ttu-id="27e81-168">否</span><span class="sxs-lookup"><span data-stu-id="27e81-168">False</span></span>                                            |
| <span data-ttu-id="27e81-169">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-169">In Global Catalog</span></span>      | <span data-ttu-id="27e81-170">否</span><span class="sxs-lookup"><span data-stu-id="27e81-170">False</span></span>                                            |
| <span data-ttu-id="27e81-171">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-172">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-175">Search-Flags</span></span>           | <span data-ttu-id="27e81-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-176">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-177">System-Flags</span></span>           | <span data-ttu-id="27e81-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-178">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-179">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-179">Classes used in</span></span>        | [<span data-ttu-id="27e81-180">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27e81-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27e81-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27e81-182">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-182">Entry</span></span> | <span data-ttu-id="27e81-183">值</span><span class="sxs-lookup"><span data-stu-id="27e81-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-184">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-186">System-Only</span></span>            | <span data-ttu-id="27e81-187">否</span><span class="sxs-lookup"><span data-stu-id="27e81-187">False</span></span>                                            |
| <span data-ttu-id="27e81-188">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-188">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-189">否</span><span class="sxs-lookup"><span data-stu-id="27e81-189">False</span></span>                                            |
| <span data-ttu-id="27e81-190">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-190">Is Indexed</span></span>             | <span data-ttu-id="27e81-191">否</span><span class="sxs-lookup"><span data-stu-id="27e81-191">False</span></span>                                            |
| <span data-ttu-id="27e81-192">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-192">In Global Catalog</span></span>      | <span data-ttu-id="27e81-193">否</span><span class="sxs-lookup"><span data-stu-id="27e81-193">False</span></span>                                            |
| <span data-ttu-id="27e81-194">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-195">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-198">Search-Flags</span></span>           | <span data-ttu-id="27e81-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-199">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-200">System-Flags</span></span>           | <span data-ttu-id="27e81-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-201">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-202">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-202">Classes used in</span></span>        | [<span data-ttu-id="27e81-203">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27e81-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27e81-204">Windows Server 2008</span></span>



| <span data-ttu-id="27e81-205">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-205">Entry</span></span> | <span data-ttu-id="27e81-206">值</span><span class="sxs-lookup"><span data-stu-id="27e81-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-207">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-209">System-Only</span></span>            | <span data-ttu-id="27e81-210">否</span><span class="sxs-lookup"><span data-stu-id="27e81-210">False</span></span>                                            |
| <span data-ttu-id="27e81-211">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-211">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-212">否</span><span class="sxs-lookup"><span data-stu-id="27e81-212">False</span></span>                                            |
| <span data-ttu-id="27e81-213">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-213">Is Indexed</span></span>             | <span data-ttu-id="27e81-214">否</span><span class="sxs-lookup"><span data-stu-id="27e81-214">False</span></span>                                            |
| <span data-ttu-id="27e81-215">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-215">In Global Catalog</span></span>      | <span data-ttu-id="27e81-216">否</span><span class="sxs-lookup"><span data-stu-id="27e81-216">False</span></span>                                            |
| <span data-ttu-id="27e81-217">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-218">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-221">Search-Flags</span></span>           | <span data-ttu-id="27e81-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-222">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-223">System-Flags</span></span>           | <span data-ttu-id="27e81-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-224">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-225">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-225">Classes used in</span></span>        | [<span data-ttu-id="27e81-226">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27e81-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27e81-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27e81-228">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-228">Entry</span></span> | <span data-ttu-id="27e81-229">值</span><span class="sxs-lookup"><span data-stu-id="27e81-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-230">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-232">System-Only</span></span>            | <span data-ttu-id="27e81-233">否</span><span class="sxs-lookup"><span data-stu-id="27e81-233">False</span></span>                                            |
| <span data-ttu-id="27e81-234">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-234">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-235">否</span><span class="sxs-lookup"><span data-stu-id="27e81-235">False</span></span>                                            |
| <span data-ttu-id="27e81-236">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-236">Is Indexed</span></span>             | <span data-ttu-id="27e81-237">否</span><span class="sxs-lookup"><span data-stu-id="27e81-237">False</span></span>                                            |
| <span data-ttu-id="27e81-238">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-238">In Global Catalog</span></span>      | <span data-ttu-id="27e81-239">否</span><span class="sxs-lookup"><span data-stu-id="27e81-239">False</span></span>                                            |
| <span data-ttu-id="27e81-240">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-241">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-244">Search-Flags</span></span>           | <span data-ttu-id="27e81-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-245">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-246">System-Flags</span></span>           | <span data-ttu-id="27e81-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-247">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-248">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-248">Classes used in</span></span>        | [<span data-ttu-id="27e81-249">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27e81-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27e81-250">Windows Server 2012</span></span>



| <span data-ttu-id="27e81-251">進入</span><span class="sxs-lookup"><span data-stu-id="27e81-251">Entry</span></span> | <span data-ttu-id="27e81-252">值</span><span class="sxs-lookup"><span data-stu-id="27e81-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27e81-253">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="27e81-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27e81-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27e81-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="27e81-255">System-Only</span></span>            | <span data-ttu-id="27e81-256">否</span><span class="sxs-lookup"><span data-stu-id="27e81-256">False</span></span>                                            |
| <span data-ttu-id="27e81-257">是-單一值</span><span class="sxs-lookup"><span data-stu-id="27e81-257">Is-Single-Valued</span></span>       | <span data-ttu-id="27e81-258">否</span><span class="sxs-lookup"><span data-stu-id="27e81-258">False</span></span>                                            |
| <span data-ttu-id="27e81-259">已編制索引</span><span class="sxs-lookup"><span data-stu-id="27e81-259">Is Indexed</span></span>             | <span data-ttu-id="27e81-260">否</span><span class="sxs-lookup"><span data-stu-id="27e81-260">False</span></span>                                            |
| <span data-ttu-id="27e81-261">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="27e81-261">In Global Catalog</span></span>      | <span data-ttu-id="27e81-262">否</span><span class="sxs-lookup"><span data-stu-id="27e81-262">False</span></span>                                            |
| <span data-ttu-id="27e81-263">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="27e81-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="27e81-264">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="27e81-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27e81-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27e81-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27e81-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27e81-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27e81-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-267">Search-Flags</span></span>           | <span data-ttu-id="27e81-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27e81-268">0x00000000</span></span>                                       |
| <span data-ttu-id="27e81-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27e81-269">System-Flags</span></span>           | <span data-ttu-id="27e81-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27e81-270">0x00000010</span></span>                                       |
| <span data-ttu-id="27e81-271">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="27e81-271">Classes used in</span></span>        | [<span data-ttu-id="27e81-272">**NTDS 服務**</span><span class="sxs-lookup"><span data-stu-id="27e81-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





