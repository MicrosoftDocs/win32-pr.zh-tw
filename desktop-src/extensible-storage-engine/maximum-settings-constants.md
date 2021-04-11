---
description: 深入瞭解：設定常數上限
title: 最大設定常數
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848177"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="074a1-103">最大設定常數</span><span class="sxs-lookup"><span data-stu-id="074a1-103">Maximum Settings Constants</span></span>


<span data-ttu-id="074a1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="074a1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="074a1-105">最大設定常數</span><span class="sxs-lookup"><span data-stu-id="074a1-105">Maximum Settings Constants</span></span>

<span data-ttu-id="074a1-106">這些常數會提供 ESE 資料庫中專案上所允許的最大設定。</span><span class="sxs-lookup"><span data-stu-id="074a1-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="074a1-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="074a1-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="074a1-108">Description</span><span class="sxs-lookup"><span data-stu-id="074a1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="074a1-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="074a1-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="074a1-110">3</span><span class="sxs-lookup"><span data-stu-id="074a1-110">3</span></span></p></td>
<td><p><span data-ttu-id="074a1-111">設定用來命名資料庫引擎所使用之檔案的前置詞長度。</span><span class="sxs-lookup"><span data-stu-id="074a1-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="074a1-112">此長度適用于為 <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> 系統參數設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="074a1-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="074a1-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="074a1-114">15</span><span class="sxs-lookup"><span data-stu-id="074a1-114">15</span></span></p></td>
<td><p><span data-ttu-id="074a1-115">設定 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>的最大長度。</span><span class="sxs-lookup"><span data-stu-id="074a1-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="074a1-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="074a1-117">256</span><span class="sxs-lookup"><span data-stu-id="074a1-117">256</span></span></p></td>
<td><p><span data-ttu-id="074a1-118">書簽的預設大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="074a1-119">當金鑰大小保留為其預設值時，這會是有效的。</span><span class="sxs-lookup"><span data-stu-id="074a1-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="074a1-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="074a1-121">2000</span><span class="sxs-lookup"><span data-stu-id="074a1-121">2000</span></span></p></td>
<td><p><span data-ttu-id="074a1-122">當 esent 設定為具有最大的可用索引鍵時，書簽的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="074a1-123"><strong>Windows 7：</strong> JET_cbBookmarkMostMost 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="074a1-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="074a1-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="074a1-125">64</span><span class="sxs-lookup"><span data-stu-id="074a1-125">64</span></span></p></td>
<td><p><span data-ttu-id="074a1-126">物件、資料行、索引或屬性名稱的最大長度。</span><span class="sxs-lookup"><span data-stu-id="074a1-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="074a1-127"><strong>注意</strong>  若為 Unicode，則值為128。</span><span class="sxs-lookup"><span data-stu-id="074a1-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="074a1-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="074a1-129">255</span><span class="sxs-lookup"><span data-stu-id="074a1-129">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-130">&quot;Name.name.name ... 結構的最大長度。 &quot;</span><span class="sxs-lookup"><span data-stu-id="074a1-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="074a1-131"><strong>注意</strong>  若為 Unicode，則值為510。</span><span class="sxs-lookup"><span data-stu-id="074a1-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="074a1-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="074a1-133">82</span><span class="sxs-lookup"><span data-stu-id="074a1-133">82</span></span></p></td>
<td><p><span data-ttu-id="074a1-134">此數位可用來計算資料庫引擎可在單一資料庫頁面上儲存之 BLOB 的最大數量。</span><span class="sxs-lookup"><span data-stu-id="074a1-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="074a1-135">公式的大小上限 = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead。</span><span class="sxs-lookup"><span data-stu-id="074a1-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="074a1-136">此值現在已過時。</span><span class="sxs-lookup"><span data-stu-id="074a1-136">This value is now obsolete.</span></span> <span data-ttu-id="074a1-137">應該使用 JET_paramLVChunkSizeMost 參數來取出長值的區塊大小。</span><span class="sxs-lookup"><span data-stu-id="074a1-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="074a1-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="074a1-139">255</span><span class="sxs-lookup"><span data-stu-id="074a1-139">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-140">非 long 值資料行資料的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="074a1-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="074a1-142">255</span><span class="sxs-lookup"><span data-stu-id="074a1-142">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-143">長值 (LongBinary 或 LongText) 資料行預設值的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="074a1-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="074a1-145">255</span><span class="sxs-lookup"><span data-stu-id="074a1-145">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-146">排序或索引鍵的預設大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="074a1-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="074a1-148">2000</span><span class="sxs-lookup"><span data-stu-id="074a1-148">2000</span></span></p></td>
<td><p><span data-ttu-id="074a1-149">任何頁面大小之排序或索引鍵可設定的最大大小。</span><span class="sxs-lookup"><span data-stu-id="074a1-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="074a1-150"> (參閱 JET_INDEXCREATE2 cbKeyMost) </span><span class="sxs-lookup"><span data-stu-id="074a1-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="074a1-151"><strong>Windows 7：</strong> JET_cbKeyMostMost 是在 Windows 7 作業系統中引進。</span><span class="sxs-lookup"><span data-stu-id="074a1-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="074a1-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="074a1-153">500</span><span class="sxs-lookup"><span data-stu-id="074a1-153">500</span></span></p></td>
<td><p><span data-ttu-id="074a1-154">使用2048位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="074a1-155">如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="074a1-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="074a1-156"><strong>Windows Vista：</strong> JET_cbKeyMost2KBytePage 是在 Windows Vista 作業系統中引進。</span><span class="sxs-lookup"><span data-stu-id="074a1-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="074a1-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="074a1-158">1000</span><span class="sxs-lookup"><span data-stu-id="074a1-158">1000</span></span></p></td>
<td><p><span data-ttu-id="074a1-159">使用4096位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="074a1-160">如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="074a1-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="074a1-161"><strong>Windows Vista：</strong> JET_cbKeyMost4KBytePage 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="074a1-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="074a1-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="074a1-163">2000</span><span class="sxs-lookup"><span data-stu-id="074a1-163">2000</span></span></p></td>
<td><p><span data-ttu-id="074a1-164">使用8192位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="074a1-165">如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="074a1-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="074a1-166"><strong>Windows Vista：  </strong>Windows Vista 引進 JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="074a1-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="074a1-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="074a1-168">255</span><span class="sxs-lookup"><span data-stu-id="074a1-168">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-169">索引鍵的最小允許大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="074a1-170">如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="074a1-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="074a1-171"><strong>Windows Vista：  </strong>JET_cbKeyMostMin 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="074a1-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="074a1-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="074a1-173">256</span><span class="sxs-lookup"><span data-stu-id="074a1-173">256</span></span></p></td>
<td><p><span data-ttu-id="074a1-174">使用限制 <em>grbit</em>（例如在 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 函數中使用的 JET_bitStrLimit）來形成索引鍵時的最大索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="074a1-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="074a1-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="074a1-176">255</span><span class="sxs-lookup"><span data-stu-id="074a1-176">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-177">主要索引的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-177">The maximum size of the primary index.</span></span> <span data-ttu-id="074a1-178">這項功能現在已過時。</span><span class="sxs-lookup"><span data-stu-id="074a1-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="074a1-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="074a1-180">255</span><span class="sxs-lookup"><span data-stu-id="074a1-180">255</span></span></p></td>
<td><p><span data-ttu-id="074a1-181">次要索引的大小上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="074a1-182">這項功能現在已過時。</span><span class="sxs-lookup"><span data-stu-id="074a1-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="074a1-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="074a1-184">12</span><span class="sxs-lookup"><span data-stu-id="074a1-184">12</span></span></p></td>
<td><p><span data-ttu-id="074a1-185">排序或索引鍵中元件的最大數目。</span><span class="sxs-lookup"><span data-stu-id="074a1-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="074a1-186"><strong>Windows Vista：  </strong>在 Windows Vista 和更新版本的 Windows 中，此值為16。</span><span class="sxs-lookup"><span data-stu-id="074a1-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="074a1-187">JET_ccolMost</span></span><br />
<span data-ttu-id="074a1-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="074a1-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="074a1-189">資料表中允許的資料行數目上限。</span><span class="sxs-lookup"><span data-stu-id="074a1-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="074a1-190"><strong>WINDOWS XP：  </strong>0x0000fee0 值用於 Windows XP 及更新版本的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="074a1-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="074a1-191"><strong>Windows 2000：  </strong>0x00007ffe 值是在 Windows 2000 中使用。</span><span class="sxs-lookup"><span data-stu-id="074a1-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="074a1-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="074a1-193">0x0000007f</span><span class="sxs-lookup"><span data-stu-id="074a1-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="074a1-194">資料表中允許的固定資料行數目上限（目前為127）。</span><span class="sxs-lookup"><span data-stu-id="074a1-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="074a1-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="074a1-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="074a1-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="074a1-197">可包含在資料表中之可變長度資料行的最大數目，目前為128。</span><span class="sxs-lookup"><span data-stu-id="074a1-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="074a1-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="074a1-199"> ( JET_ccolMost 0x000000ff ) </span><span class="sxs-lookup"><span data-stu-id="074a1-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="074a1-200">可包含在資料表中的標記資料行數目上限，目前為64993。</span><span class="sxs-lookup"><span data-stu-id="074a1-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="074a1-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="074a1-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="074a1-202"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="074a1-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="074a1-203">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="074a1-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="074a1-204"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="074a1-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="074a1-205">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="074a1-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="074a1-206"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="074a1-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="074a1-207">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="074a1-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

