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
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="b6f24-106">ms-DFS-連結-路徑-v2 屬性</span><span class="sxs-lookup"><span data-stu-id="b6f24-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="b6f24-107">相對於 DFS 根目標共用的 DFS 連結路徑 (也就是，沒有伺服器/網域和 DFS 命名空間名稱元件) 。</span><span class="sxs-lookup"><span data-stu-id="b6f24-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="b6f24-108">使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。</span><span class="sxs-lookup"><span data-stu-id="b6f24-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="b6f24-109">進入</span><span class="sxs-lookup"><span data-stu-id="b6f24-109">Entry</span></span> | <span data-ttu-id="b6f24-110">值</span><span class="sxs-lookup"><span data-stu-id="b6f24-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b6f24-111">CN</span><span class="sxs-lookup"><span data-stu-id="b6f24-111">CN</span></span>                | <span data-ttu-id="b6f24-112">ms-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="b6f24-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="b6f24-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="b6f24-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b6f24-114">msDFS-LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="b6f24-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="b6f24-115">大小</span><span class="sxs-lookup"><span data-stu-id="b6f24-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="b6f24-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="b6f24-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="b6f24-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="b6f24-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="b6f24-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b6f24-118">Attribute-Id</span></span>      | <span data-ttu-id="b6f24-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="b6f24-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="b6f24-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="b6f24-120">System-Id-Guid</span></span>    | <span data-ttu-id="b6f24-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="b6f24-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="b6f24-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6f24-122">Syntax</span></span>            | [<span data-ttu-id="b6f24-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="b6f24-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b6f24-124">實作</span><span class="sxs-lookup"><span data-stu-id="b6f24-124">Implementations</span></span>

-   [<span data-ttu-id="b6f24-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b6f24-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b6f24-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b6f24-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b6f24-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="b6f24-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6f24-128">Windows Server 2008</span></span>



| <span data-ttu-id="b6f24-129">進入</span><span class="sxs-lookup"><span data-stu-id="b6f24-129">Entry</span></span> | <span data-ttu-id="b6f24-130">值</span><span class="sxs-lookup"><span data-stu-id="b6f24-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f24-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b6f24-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6f24-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6f24-133">System-Only</span></span>            | <span data-ttu-id="b6f24-134">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b6f24-135">Is-Single-Valued</span></span>       | <span data-ttu-id="b6f24-136">對</span><span class="sxs-lookup"><span data-stu-id="b6f24-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="b6f24-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b6f24-137">Is Indexed</span></span>             | <span data-ttu-id="b6f24-138">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b6f24-139">In Global Catalog</span></span>      | <span data-ttu-id="b6f24-140">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b6f24-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6f24-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b6f24-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="b6f24-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6f24-143">Range-Lower</span></span>            | <span data-ttu-id="b6f24-144">0</span><span class="sxs-lookup"><span data-stu-id="b6f24-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="b6f24-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6f24-145">Range-Upper</span></span>            | <span data-ttu-id="b6f24-146">32766</span><span class="sxs-lookup"><span data-stu-id="b6f24-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-147">Search-Flags</span></span>           | <span data-ttu-id="b6f24-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6f24-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-149">System-Flags</span></span>           | <span data-ttu-id="b6f24-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6f24-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b6f24-151">Classes used in</span></span>        | [<span data-ttu-id="b6f24-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="b6f24-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b6f24-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b6f24-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b6f24-155">進入</span><span class="sxs-lookup"><span data-stu-id="b6f24-155">Entry</span></span> | <span data-ttu-id="b6f24-156">值</span><span class="sxs-lookup"><span data-stu-id="b6f24-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f24-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b6f24-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6f24-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6f24-159">System-Only</span></span>            | <span data-ttu-id="b6f24-160">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b6f24-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b6f24-162">對</span><span class="sxs-lookup"><span data-stu-id="b6f24-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="b6f24-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b6f24-163">Is Indexed</span></span>             | <span data-ttu-id="b6f24-164">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b6f24-165">In Global Catalog</span></span>      | <span data-ttu-id="b6f24-166">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b6f24-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6f24-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b6f24-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="b6f24-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6f24-169">Range-Lower</span></span>            | <span data-ttu-id="b6f24-170">0</span><span class="sxs-lookup"><span data-stu-id="b6f24-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="b6f24-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6f24-171">Range-Upper</span></span>            | <span data-ttu-id="b6f24-172">32766</span><span class="sxs-lookup"><span data-stu-id="b6f24-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-173">Search-Flags</span></span>           | <span data-ttu-id="b6f24-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6f24-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-175">System-Flags</span></span>           | <span data-ttu-id="b6f24-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6f24-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b6f24-177">Classes used in</span></span>        | [<span data-ttu-id="b6f24-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="b6f24-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b6f24-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6f24-180">Windows Server 2012</span></span>



| <span data-ttu-id="b6f24-181">進入</span><span class="sxs-lookup"><span data-stu-id="b6f24-181">Entry</span></span> | <span data-ttu-id="b6f24-182">值</span><span class="sxs-lookup"><span data-stu-id="b6f24-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f24-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="b6f24-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6f24-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="b6f24-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6f24-185">System-Only</span></span>            | <span data-ttu-id="b6f24-186">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="b6f24-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b6f24-188">對</span><span class="sxs-lookup"><span data-stu-id="b6f24-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="b6f24-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="b6f24-189">Is Indexed</span></span>             | <span data-ttu-id="b6f24-190">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="b6f24-191">In Global Catalog</span></span>      | <span data-ttu-id="b6f24-192">否</span><span class="sxs-lookup"><span data-stu-id="b6f24-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="b6f24-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6f24-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="b6f24-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="b6f24-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6f24-195">Range-Lower</span></span>            | <span data-ttu-id="b6f24-196">0</span><span class="sxs-lookup"><span data-stu-id="b6f24-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="b6f24-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6f24-197">Range-Upper</span></span>            | <span data-ttu-id="b6f24-198">32766</span><span class="sxs-lookup"><span data-stu-id="b6f24-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="b6f24-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-199">Search-Flags</span></span>           | <span data-ttu-id="b6f24-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6f24-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6f24-201">System-Flags</span></span>           | <span data-ttu-id="b6f24-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6f24-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="b6f24-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="b6f24-203">Classes used in</span></span>        | [<span data-ttu-id="b6f24-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="b6f24-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="b6f24-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





