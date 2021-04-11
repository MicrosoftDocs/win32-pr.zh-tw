---
description: 深入瞭解：資訊參數
title: 資訊參數
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691336"
---
# <a name="informational-parameters"></a><span data-ttu-id="4137e-103">資訊參數</span><span class="sxs-lookup"><span data-stu-id="4137e-103">Informational Parameters</span></span>


<span data-ttu-id="4137e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4137e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="4137e-105">資訊參數</span><span class="sxs-lookup"><span data-stu-id="4137e-105">Informational Parameters</span></span>

<span data-ttu-id="4137e-106">本主題包含用來公開資料庫引擎相關資訊的參數。</span><span class="sxs-lookup"><span data-stu-id="4137e-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="4137e-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="4137e-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="4137e-108">134</span><span class="sxs-lookup"><span data-stu-id="4137e-108">134</span></span>  

<span data-ttu-id="4137e-109">這個唯讀參數表示可針對目前資料庫頁面大小選取的最大可允許索引鍵長度， (如 JET_paramDatabasePageSize) 所設定。</span><span class="sxs-lookup"><span data-stu-id="4137e-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4137e-110">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4137e-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4137e-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="4137e-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-112">輸入：</span><span class="sxs-lookup"><span data-stu-id="4137e-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="4137e-113">整數</span><span class="sxs-lookup"><span data-stu-id="4137e-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-114">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4137e-115">255–65535</span><span class="sxs-lookup"><span data-stu-id="4137e-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-116">範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4137e-117">全球</span><span class="sxs-lookup"><span data-stu-id="4137e-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-118">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4137e-119">N/A</span><span class="sxs-lookup"><span data-stu-id="4137e-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-120">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4137e-121">N/A</span><span class="sxs-lookup"><span data-stu-id="4137e-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-122">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4137e-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4137e-123">No</span><span class="sxs-lookup"><span data-stu-id="4137e-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-124">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4137e-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4137e-125">No</span><span class="sxs-lookup"><span data-stu-id="4137e-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-126">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4137e-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4137e-127">No</span><span class="sxs-lookup"><span data-stu-id="4137e-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-128">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4137e-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4137e-129">No</span><span class="sxs-lookup"><span data-stu-id="4137e-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-130">可用性：</span><span class="sxs-lookup"><span data-stu-id="4137e-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4137e-131">從 Windows Server 2008 和 Windows Vista 開始</span><span class="sxs-lookup"><span data-stu-id="4137e-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4137e-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="4137e-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="4137e-133">131</span><span class="sxs-lookup"><span data-stu-id="4137e-133">131</span></span>  

<span data-ttu-id="4137e-134">這個唯讀參數會傳回該版本資料庫引擎的最大 [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) 。</span><span class="sxs-lookup"><span data-stu-id="4137e-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="4137e-135">這個值可以用來測試特定 [JET_COLTYP](./jet-coltyp.md)的支援。</span><span class="sxs-lookup"><span data-stu-id="4137e-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="4137e-136">如果給定的 [JET_COLTYP](./jet-coltyp.md) 小於這個參數的值，database engine 就會支援它。</span><span class="sxs-lookup"><span data-stu-id="4137e-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4137e-137">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4137e-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4137e-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="4137e-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-139">輸入：</span><span class="sxs-lookup"><span data-stu-id="4137e-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="4137e-140">整數</span><span class="sxs-lookup"><span data-stu-id="4137e-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-141">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4137e-142">0-255</span><span class="sxs-lookup"><span data-stu-id="4137e-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-143">範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="4137e-144">全球</span><span class="sxs-lookup"><span data-stu-id="4137e-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-145">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="4137e-146">N/A</span><span class="sxs-lookup"><span data-stu-id="4137e-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-147">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="4137e-148">N/A</span><span class="sxs-lookup"><span data-stu-id="4137e-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-149">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4137e-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="4137e-150">No</span><span class="sxs-lookup"><span data-stu-id="4137e-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-151">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4137e-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="4137e-152">No</span><span class="sxs-lookup"><span data-stu-id="4137e-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-153">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4137e-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="4137e-154">No</span><span class="sxs-lookup"><span data-stu-id="4137e-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-155">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4137e-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="4137e-156">No</span><span class="sxs-lookup"><span data-stu-id="4137e-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-157">可用性：</span><span class="sxs-lookup"><span data-stu-id="4137e-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="4137e-158">從 Windows Server 2008 和 Windows Vista 開始</span><span class="sxs-lookup"><span data-stu-id="4137e-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4137e-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="4137e-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="4137e-160">163</span><span class="sxs-lookup"><span data-stu-id="4137e-160">163</span></span>  

<span data-ttu-id="4137e-161">唯讀參數，會根據設定的頁面大小傳回長值的區塊大小。</span><span class="sxs-lookup"><span data-stu-id="4137e-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="4137e-162">如果要使用多個 Jet {Set，抓取} 資料行呼叫來讀取或寫入較長的值，則使用大小是區塊大小倍數的緩衝區會更有效率。</span><span class="sxs-lookup"><span data-stu-id="4137e-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4137e-163">預設值：3</span><span class="sxs-lookup"><span data-stu-id="4137e-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="4137e-164">2kb 頁面 = 1966 位元組</span><span class="sxs-lookup"><span data-stu-id="4137e-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="4137e-165">4 kb 頁面 = 4014 個位元組</span><span class="sxs-lookup"><span data-stu-id="4137e-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="4137e-166">8kb 頁面 = 8110 位元組</span><span class="sxs-lookup"><span data-stu-id="4137e-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="4137e-167">16kb 頁面 = 4050 位元組</span><span class="sxs-lookup"><span data-stu-id="4137e-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="4137e-168">32kb 頁面 = 8150 位元組</span><span class="sxs-lookup"><span data-stu-id="4137e-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-169">輸入：</span><span class="sxs-lookup"><span data-stu-id="4137e-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="4137e-170">整數</span><span class="sxs-lookup"><span data-stu-id="4137e-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-171">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="4137e-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="4137e-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-173">範圍：</span><span class="sxs-lookup"><span data-stu-id="4137e-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-174">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-175">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="4137e-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-176">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="4137e-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-177">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="4137e-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-178">影響效能：</span><span class="sxs-lookup"><span data-stu-id="4137e-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-179">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="4137e-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-180">可用性：</span><span class="sxs-lookup"><span data-stu-id="4137e-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="4137e-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="4137e-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4137e-182"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4137e-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4137e-183">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="4137e-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4137e-184"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4137e-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4137e-185">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="4137e-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4137e-186"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4137e-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4137e-187">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4137e-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4137e-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4137e-188">See Also</span></span>

[<span data-ttu-id="4137e-189">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4137e-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4137e-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="4137e-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="4137e-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="4137e-191">JET_COLTYP</span></span>](./jet-coltyp.md)
