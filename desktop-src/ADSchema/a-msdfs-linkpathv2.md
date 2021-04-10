---
title: ms-DFS-連結-路徑-v2 屬性
description: 相對於 DFS 根目標共用的 DFS 連結路徑 (也就是，沒有伺服器/網域和 DFS 命名空間名稱元件) 。 使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- ms-DFS-連結-路徑-v2 屬性 AD 架構
- msDFS-LinkPathv2 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108180"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="65843-106">ms-DFS-連結-路徑-v2 屬性</span><span class="sxs-lookup"><span data-stu-id="65843-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="65843-107">相對於 DFS 根目標共用的 DFS 連結路徑 (也就是，沒有伺服器/網域和 DFS 命名空間名稱元件) 。</span><span class="sxs-lookup"><span data-stu-id="65843-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="65843-108">使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。</span><span class="sxs-lookup"><span data-stu-id="65843-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="65843-109">進入</span><span class="sxs-lookup"><span data-stu-id="65843-109">Entry</span></span> | <span data-ttu-id="65843-110">值</span><span class="sxs-lookup"><span data-stu-id="65843-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="65843-111">CN</span><span class="sxs-lookup"><span data-stu-id="65843-111">CN</span></span>                | <span data-ttu-id="65843-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="65843-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="65843-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="65843-113">Ldap-Display-Name</span></span> | <span data-ttu-id="65843-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="65843-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="65843-115">大小</span><span class="sxs-lookup"><span data-stu-id="65843-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="65843-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="65843-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="65843-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="65843-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="65843-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65843-118">Attribute-Id</span></span>      | <span data-ttu-id="65843-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="65843-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="65843-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="65843-120">System-Id-Guid</span></span>    | <span data-ttu-id="65843-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="65843-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="65843-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="65843-122">Syntax</span></span>            | [<span data-ttu-id="65843-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="65843-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="65843-124">實作</span><span class="sxs-lookup"><span data-stu-id="65843-124">Implementations</span></span>

-   [<span data-ttu-id="65843-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65843-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65843-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65843-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65843-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65843-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="65843-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65843-128">Windows Server 2008</span></span>



| <span data-ttu-id="65843-129">進入</span><span class="sxs-lookup"><span data-stu-id="65843-129">Entry</span></span> | <span data-ttu-id="65843-130">值</span><span class="sxs-lookup"><span data-stu-id="65843-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65843-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65843-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65843-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="65843-133">System-Only</span></span>            | <span data-ttu-id="65843-134">否</span><span class="sxs-lookup"><span data-stu-id="65843-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65843-135">Is-Single-Valued</span></span>       | <span data-ttu-id="65843-136">對</span><span class="sxs-lookup"><span data-stu-id="65843-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="65843-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65843-137">Is Indexed</span></span>             | <span data-ttu-id="65843-138">否</span><span class="sxs-lookup"><span data-stu-id="65843-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65843-139">In Global Catalog</span></span>      | <span data-ttu-id="65843-140">否</span><span class="sxs-lookup"><span data-stu-id="65843-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65843-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="65843-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65843-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="65843-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65843-143">Range-Lower</span></span>            | <span data-ttu-id="65843-144">0</span><span class="sxs-lookup"><span data-stu-id="65843-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="65843-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65843-145">Range-Upper</span></span>            | <span data-ttu-id="65843-146">32766</span><span class="sxs-lookup"><span data-stu-id="65843-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="65843-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-147">Search-Flags</span></span>           | <span data-ttu-id="65843-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65843-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="65843-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-149">System-Flags</span></span>           | <span data-ttu-id="65843-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65843-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="65843-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65843-151">Classes used in</span></span>        | [<span data-ttu-id="65843-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="65843-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65843-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65843-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65843-155">進入</span><span class="sxs-lookup"><span data-stu-id="65843-155">Entry</span></span> | <span data-ttu-id="65843-156">值</span><span class="sxs-lookup"><span data-stu-id="65843-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65843-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65843-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65843-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="65843-159">System-Only</span></span>            | <span data-ttu-id="65843-160">否</span><span class="sxs-lookup"><span data-stu-id="65843-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65843-161">Is-Single-Valued</span></span>       | <span data-ttu-id="65843-162">對</span><span class="sxs-lookup"><span data-stu-id="65843-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="65843-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65843-163">Is Indexed</span></span>             | <span data-ttu-id="65843-164">否</span><span class="sxs-lookup"><span data-stu-id="65843-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65843-165">In Global Catalog</span></span>      | <span data-ttu-id="65843-166">否</span><span class="sxs-lookup"><span data-stu-id="65843-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65843-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="65843-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65843-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="65843-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65843-169">Range-Lower</span></span>            | <span data-ttu-id="65843-170">0</span><span class="sxs-lookup"><span data-stu-id="65843-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="65843-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65843-171">Range-Upper</span></span>            | <span data-ttu-id="65843-172">32766</span><span class="sxs-lookup"><span data-stu-id="65843-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="65843-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-173">Search-Flags</span></span>           | <span data-ttu-id="65843-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65843-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="65843-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-175">System-Flags</span></span>           | <span data-ttu-id="65843-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65843-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="65843-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65843-177">Classes used in</span></span>        | [<span data-ttu-id="65843-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="65843-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65843-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65843-180">Windows Server 2012</span></span>



| <span data-ttu-id="65843-181">進入</span><span class="sxs-lookup"><span data-stu-id="65843-181">Entry</span></span> | <span data-ttu-id="65843-182">值</span><span class="sxs-lookup"><span data-stu-id="65843-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65843-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="65843-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65843-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="65843-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="65843-185">System-Only</span></span>            | <span data-ttu-id="65843-186">否</span><span class="sxs-lookup"><span data-stu-id="65843-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="65843-187">Is-Single-Valued</span></span>       | <span data-ttu-id="65843-188">對</span><span class="sxs-lookup"><span data-stu-id="65843-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="65843-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="65843-189">Is Indexed</span></span>             | <span data-ttu-id="65843-190">否</span><span class="sxs-lookup"><span data-stu-id="65843-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="65843-191">In Global Catalog</span></span>      | <span data-ttu-id="65843-192">否</span><span class="sxs-lookup"><span data-stu-id="65843-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="65843-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="65843-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="65843-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="65843-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="65843-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65843-195">Range-Lower</span></span>            | <span data-ttu-id="65843-196">0</span><span class="sxs-lookup"><span data-stu-id="65843-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="65843-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65843-197">Range-Upper</span></span>            | <span data-ttu-id="65843-198">32766</span><span class="sxs-lookup"><span data-stu-id="65843-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="65843-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-199">Search-Flags</span></span>           | <span data-ttu-id="65843-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65843-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="65843-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65843-201">System-Flags</span></span>           | <span data-ttu-id="65843-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65843-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="65843-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="65843-203">Classes used in</span></span>        | [<span data-ttu-id="65843-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="65843-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="65843-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





