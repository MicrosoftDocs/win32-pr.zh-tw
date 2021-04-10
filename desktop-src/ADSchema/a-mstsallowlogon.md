---
title: ms-TS-允許-登入屬性
description: 指定是否允許使用者登入終端機伺服器。 若允許登入，則此值為 1；若不允許，則此值為 0。
ms.assetid: 9cd6edbc-f8e7-4933-9f62-1e34e3d31fb7
ms.tgt_platform: multiple
keywords:
- ms-TS-允許-登入屬性 AD 架構
- msTSAllowLogon 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TS-Allow-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd78662167e281ea720f2ad5d98f25c2f5c4ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103845039"
---
# <a name="ms-ts-allow-logon-attribute"></a><span data-ttu-id="7bcf1-106">ms-TS-允許-登入屬性</span><span class="sxs-lookup"><span data-stu-id="7bcf1-106">ms-TS-Allow-Logon attribute</span></span>

<span data-ttu-id="7bcf1-107">指定是否允許使用者登入終端機伺服器。</span><span class="sxs-lookup"><span data-stu-id="7bcf1-107">Specifies whether the user is allowed to log on to the Terminal Server.</span></span> <span data-ttu-id="7bcf1-108">若允許登入，則此值為 1；若不允許，則此值為 0。</span><span class="sxs-lookup"><span data-stu-id="7bcf1-108">The value is 1 if logon is allowed, and 0 if logon is not allowed.</span></span>



| <span data-ttu-id="7bcf1-109">進入</span><span class="sxs-lookup"><span data-stu-id="7bcf1-109">Entry</span></span> | <span data-ttu-id="7bcf1-110">值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="7bcf1-111">CN</span><span class="sxs-lookup"><span data-stu-id="7bcf1-111">CN</span></span>                | <span data-ttu-id="7bcf1-112">ms-TS-Allow-Logon</span><span class="sxs-lookup"><span data-stu-id="7bcf1-112">ms-TS-Allow-Logon</span></span>                    |
| <span data-ttu-id="7bcf1-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="7bcf1-113">Ldap-Display-Name</span></span> | <span data-ttu-id="7bcf1-114">msTSAllowLogon</span><span class="sxs-lookup"><span data-stu-id="7bcf1-114">msTSAllowLogon</span></span>                       |
| <span data-ttu-id="7bcf1-115">大小</span><span class="sxs-lookup"><span data-stu-id="7bcf1-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="7bcf1-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="7bcf1-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="7bcf1-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="7bcf1-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="7bcf1-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bcf1-118">Attribute-Id</span></span>      | <span data-ttu-id="7bcf1-119">1.2.840.113556.1.4.1979</span><span class="sxs-lookup"><span data-stu-id="7bcf1-119">1.2.840.113556.1.4.1979</span></span>              |
| <span data-ttu-id="7bcf1-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="7bcf1-120">System-Id-Guid</span></span>    | <span data-ttu-id="7bcf1-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span><span class="sxs-lookup"><span data-stu-id="7bcf1-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span></span> |
| <span data-ttu-id="7bcf1-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bcf1-122">Syntax</span></span>            | [<span data-ttu-id="7bcf1-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="7bcf1-124">實作</span><span class="sxs-lookup"><span data-stu-id="7bcf1-124">Implementations</span></span>

-   [<span data-ttu-id="7bcf1-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bcf1-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bcf1-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="7bcf1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bcf1-128">Windows Server 2008</span></span>



| <span data-ttu-id="7bcf1-129">進入</span><span class="sxs-lookup"><span data-stu-id="7bcf1-129">Entry</span></span> | <span data-ttu-id="7bcf1-130">值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7bcf1-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7bcf1-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bcf1-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bcf1-133">System-Only</span></span>            | <span data-ttu-id="7bcf1-134">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-134">False</span></span>                             |
| <span data-ttu-id="7bcf1-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-135">Is-Single-Valued</span></span>       | <span data-ttu-id="7bcf1-136">對</span><span class="sxs-lookup"><span data-stu-id="7bcf1-136">True</span></span>                              |
| <span data-ttu-id="7bcf1-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7bcf1-137">Is Indexed</span></span>             | <span data-ttu-id="7bcf1-138">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-138">False</span></span>                             |
| <span data-ttu-id="7bcf1-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7bcf1-139">In Global Catalog</span></span>      | <span data-ttu-id="7bcf1-140">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-140">False</span></span>                             |
| <span data-ttu-id="7bcf1-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7bcf1-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bcf1-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7bcf1-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7bcf1-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bcf1-143">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bcf1-144">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-145">Search-Flags</span></span>           | <span data-ttu-id="7bcf1-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bcf1-146">0x00000000</span></span>                        |
| <span data-ttu-id="7bcf1-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-147">System-Flags</span></span>           | <span data-ttu-id="7bcf1-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bcf1-148">0x00000010</span></span>                        |
| <span data-ttu-id="7bcf1-149">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7bcf1-149">Classes used in</span></span>        | [<span data-ttu-id="7bcf1-150">**User**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bcf1-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bcf1-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bcf1-152">進入</span><span class="sxs-lookup"><span data-stu-id="7bcf1-152">Entry</span></span> | <span data-ttu-id="7bcf1-153">值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7bcf1-154">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7bcf1-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bcf1-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bcf1-156">System-Only</span></span>            | <span data-ttu-id="7bcf1-157">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-157">False</span></span>                             |
| <span data-ttu-id="7bcf1-158">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-158">Is-Single-Valued</span></span>       | <span data-ttu-id="7bcf1-159">對</span><span class="sxs-lookup"><span data-stu-id="7bcf1-159">True</span></span>                              |
| <span data-ttu-id="7bcf1-160">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7bcf1-160">Is Indexed</span></span>             | <span data-ttu-id="7bcf1-161">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-161">False</span></span>                             |
| <span data-ttu-id="7bcf1-162">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7bcf1-162">In Global Catalog</span></span>      | <span data-ttu-id="7bcf1-163">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-163">False</span></span>                             |
| <span data-ttu-id="7bcf1-164">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7bcf1-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bcf1-165">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7bcf1-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7bcf1-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bcf1-166">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bcf1-167">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-168">Search-Flags</span></span>           | <span data-ttu-id="7bcf1-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bcf1-169">0x00000000</span></span>                        |
| <span data-ttu-id="7bcf1-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-170">System-Flags</span></span>           | <span data-ttu-id="7bcf1-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bcf1-171">0x00000010</span></span>                        |
| <span data-ttu-id="7bcf1-172">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7bcf1-172">Classes used in</span></span>        | [<span data-ttu-id="7bcf1-173">**User**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-173">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bcf1-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bcf1-174">Windows Server 2012</span></span>



| <span data-ttu-id="7bcf1-175">進入</span><span class="sxs-lookup"><span data-stu-id="7bcf1-175">Entry</span></span> | <span data-ttu-id="7bcf1-176">值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-176">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="7bcf1-177">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="7bcf1-177">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bcf1-178">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="7bcf1-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bcf1-179">System-Only</span></span>            | <span data-ttu-id="7bcf1-180">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-180">False</span></span>                             |
| <span data-ttu-id="7bcf1-181">是-單一值</span><span class="sxs-lookup"><span data-stu-id="7bcf1-181">Is-Single-Valued</span></span>       | <span data-ttu-id="7bcf1-182">對</span><span class="sxs-lookup"><span data-stu-id="7bcf1-182">True</span></span>                              |
| <span data-ttu-id="7bcf1-183">已編制索引</span><span class="sxs-lookup"><span data-stu-id="7bcf1-183">Is Indexed</span></span>             | <span data-ttu-id="7bcf1-184">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-184">False</span></span>                             |
| <span data-ttu-id="7bcf1-185">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="7bcf1-185">In Global Catalog</span></span>      | <span data-ttu-id="7bcf1-186">否</span><span class="sxs-lookup"><span data-stu-id="7bcf1-186">False</span></span>                             |
| <span data-ttu-id="7bcf1-187">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="7bcf1-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bcf1-188">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="7bcf1-188">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="7bcf1-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bcf1-189">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bcf1-190">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="7bcf1-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-191">Search-Flags</span></span>           | <span data-ttu-id="7bcf1-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bcf1-192">0x00000000</span></span>                        |
| <span data-ttu-id="7bcf1-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bcf1-193">System-Flags</span></span>           | <span data-ttu-id="7bcf1-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bcf1-194">0x00000010</span></span>                        |
| <span data-ttu-id="7bcf1-195">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="7bcf1-195">Classes used in</span></span>        | [<span data-ttu-id="7bcf1-196">**User**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-196">**User**</span></span>](c-user.md)<br/> |



 

 





