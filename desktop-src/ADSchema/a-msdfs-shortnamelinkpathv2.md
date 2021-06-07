---
title: ms-DFS-簡短名稱-連結路徑-v2 屬性
description: 相對於 DFS 根目標共用的簡短名稱 DFS 連結路徑 (也就是沒有伺服器/網域和 DFS 命名空間名稱元件) 。 使用正斜線 (/) ，而不是反斜線 (\) ，因此可以完成 LDAP 搜尋，而不需要使用 esc。
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- ms-DFS-簡短名稱-連結路徑-v2 屬性 AD 架構
- msDFS-ShortNameLinkPathv2 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386847"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="f947f-106">ms-DFS-簡短名稱-連結路徑-v2 屬性</span><span class="sxs-lookup"><span data-stu-id="f947f-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="f947f-107">相對於 DFS 根目標共用的簡短名稱 DFS 連結路徑 (也就是沒有伺服器/網域和 DFS 命名空間名稱元件) 。</span><span class="sxs-lookup"><span data-stu-id="f947f-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="f947f-108">使用正斜線 (/) ，而不是反斜線 (\\) ，如此就可以完成 LDAP 搜尋，而不需要使用 esc。</span><span class="sxs-lookup"><span data-stu-id="f947f-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="f947f-109">進入</span><span class="sxs-lookup"><span data-stu-id="f947f-109">Entry</span></span> | <span data-ttu-id="f947f-110">值</span><span class="sxs-lookup"><span data-stu-id="f947f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f947f-111">CN</span><span class="sxs-lookup"><span data-stu-id="f947f-111">CN</span></span>                | <span data-ttu-id="f947f-112">ms-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="f947f-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="f947f-113">Ldap-顯示名稱</span><span class="sxs-lookup"><span data-stu-id="f947f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f947f-114">msDFS-ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="f947f-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="f947f-115">大小</span><span class="sxs-lookup"><span data-stu-id="f947f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f947f-116">更新許可權</span><span class="sxs-lookup"><span data-stu-id="f947f-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f947f-117">更新頻率</span><span class="sxs-lookup"><span data-stu-id="f947f-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f947f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f947f-118">Attribute-Id</span></span>      | <span data-ttu-id="f947f-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="f947f-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="f947f-120">系統識別碼-Guid</span><span class="sxs-lookup"><span data-stu-id="f947f-120">System-Id-Guid</span></span>    | <span data-ttu-id="f947f-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="f947f-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="f947f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f947f-122">Syntax</span></span>            | [<span data-ttu-id="f947f-123">**String(Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f947f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f947f-124">實作</span><span class="sxs-lookup"><span data-stu-id="f947f-124">Implementations</span></span>

-   [<span data-ttu-id="f947f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f947f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f947f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f947f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f947f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f947f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="f947f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f947f-128">Windows Server 2008</span></span>



| <span data-ttu-id="f947f-129">進入</span><span class="sxs-lookup"><span data-stu-id="f947f-129">Entry</span></span> | <span data-ttu-id="f947f-130">值</span><span class="sxs-lookup"><span data-stu-id="f947f-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f947f-131">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f947f-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f947f-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="f947f-133">System-Only</span></span>            | <span data-ttu-id="f947f-134">False</span><span class="sxs-lookup"><span data-stu-id="f947f-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-135">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f947f-135">Is-Single-Valued</span></span>       | <span data-ttu-id="f947f-136">True</span><span class="sxs-lookup"><span data-stu-id="f947f-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="f947f-137">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f947f-137">Is Indexed</span></span>             | <span data-ttu-id="f947f-138">False</span><span class="sxs-lookup"><span data-stu-id="f947f-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-139">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f947f-139">In Global Catalog</span></span>      | <span data-ttu-id="f947f-140">False</span><span class="sxs-lookup"><span data-stu-id="f947f-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-141">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f947f-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="f947f-142">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f947f-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f947f-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f947f-143">Range-Lower</span></span>            | <span data-ttu-id="f947f-144">0</span><span class="sxs-lookup"><span data-stu-id="f947f-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="f947f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f947f-145">Range-Upper</span></span>            | <span data-ttu-id="f947f-146">32766</span><span class="sxs-lookup"><span data-stu-id="f947f-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-147">Search-Flags</span></span>           | <span data-ttu-id="f947f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f947f-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f947f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-149">System-Flags</span></span>           | <span data-ttu-id="f947f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f947f-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f947f-151">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f947f-151">Classes used in</span></span>        | [<span data-ttu-id="f947f-152">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f947f-153">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f947f-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f947f-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f947f-155">進入</span><span class="sxs-lookup"><span data-stu-id="f947f-155">Entry</span></span> | <span data-ttu-id="f947f-156">值</span><span class="sxs-lookup"><span data-stu-id="f947f-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f947f-157">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f947f-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f947f-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f947f-159">System-Only</span></span>            | <span data-ttu-id="f947f-160">False</span><span class="sxs-lookup"><span data-stu-id="f947f-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-161">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f947f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f947f-162">True</span><span class="sxs-lookup"><span data-stu-id="f947f-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="f947f-163">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f947f-163">Is Indexed</span></span>             | <span data-ttu-id="f947f-164">False</span><span class="sxs-lookup"><span data-stu-id="f947f-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-165">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f947f-165">In Global Catalog</span></span>      | <span data-ttu-id="f947f-166">False</span><span class="sxs-lookup"><span data-stu-id="f947f-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-167">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f947f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f947f-168">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f947f-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f947f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f947f-169">Range-Lower</span></span>            | <span data-ttu-id="f947f-170">0</span><span class="sxs-lookup"><span data-stu-id="f947f-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="f947f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f947f-171">Range-Upper</span></span>            | <span data-ttu-id="f947f-172">32766</span><span class="sxs-lookup"><span data-stu-id="f947f-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-173">Search-Flags</span></span>           | <span data-ttu-id="f947f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f947f-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f947f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-175">System-Flags</span></span>           | <span data-ttu-id="f947f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f947f-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f947f-177">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f947f-177">Classes used in</span></span>        | [<span data-ttu-id="f947f-178">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f947f-179">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f947f-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f947f-180">Windows Server 2012</span></span>



| <span data-ttu-id="f947f-181">進入</span><span class="sxs-lookup"><span data-stu-id="f947f-181">Entry</span></span> | <span data-ttu-id="f947f-182">值</span><span class="sxs-lookup"><span data-stu-id="f947f-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f947f-183">連結識別碼</span><span class="sxs-lookup"><span data-stu-id="f947f-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f947f-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="f947f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f947f-185">System-Only</span></span>            | <span data-ttu-id="f947f-186">False</span><span class="sxs-lookup"><span data-stu-id="f947f-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-187">是-單一值</span><span class="sxs-lookup"><span data-stu-id="f947f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f947f-188">True</span><span class="sxs-lookup"><span data-stu-id="f947f-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="f947f-189">已編制索引</span><span class="sxs-lookup"><span data-stu-id="f947f-189">Is Indexed</span></span>             | <span data-ttu-id="f947f-190">False</span><span class="sxs-lookup"><span data-stu-id="f947f-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-191">在通用類別目錄中</span><span class="sxs-lookup"><span data-stu-id="f947f-191">In Global Catalog</span></span>      | <span data-ttu-id="f947f-192">False</span><span class="sxs-lookup"><span data-stu-id="f947f-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-193">NT-Security-描述元</span><span class="sxs-lookup"><span data-stu-id="f947f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f947f-194">O:BAG：不正確： S：</span><span class="sxs-lookup"><span data-stu-id="f947f-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="f947f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f947f-195">Range-Lower</span></span>            | <span data-ttu-id="f947f-196">0</span><span class="sxs-lookup"><span data-stu-id="f947f-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="f947f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f947f-197">Range-Upper</span></span>            | <span data-ttu-id="f947f-198">32766</span><span class="sxs-lookup"><span data-stu-id="f947f-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="f947f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-199">Search-Flags</span></span>           | <span data-ttu-id="f947f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f947f-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="f947f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f947f-201">System-Flags</span></span>           | <span data-ttu-id="f947f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f947f-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="f947f-203">中使用的類別</span><span class="sxs-lookup"><span data-stu-id="f947f-203">Classes used in</span></span>        | [<span data-ttu-id="f947f-204">**ms-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="f947f-205">**ms-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="f947f-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





