---
description: 深入瞭解：資源參數
title: 資源參數
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983675"
---
# <a name="resource-parameters"></a><span data-ttu-id="62013-103">資源參數</span><span class="sxs-lookup"><span data-stu-id="62013-103">Resource Parameters</span></span>


<span data-ttu-id="62013-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="62013-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="62013-105">資源參數</span><span class="sxs-lookup"><span data-stu-id="62013-105">Resource Parameters</span></span>

<span data-ttu-id="62013-106">本主題包含用於資源的參數。</span><span class="sxs-lookup"><span data-stu-id="62013-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="62013-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="62013-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="62013-108">125</span><span class="sxs-lookup"><span data-stu-id="62013-108">125</span></span>  

<span data-ttu-id="62013-109">此參數會控制應用程式已關閉實例所代表的資料表之後，該實例所快取的 B + 樹系資源數目。</span><span class="sxs-lookup"><span data-stu-id="62013-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="62013-110">此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。</span><span class="sxs-lookup"><span data-stu-id="62013-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="62013-111">對於具有極大量資料表之架構的應用程式而言，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="62013-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-112">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-113">64</span><span class="sxs-lookup"><span data-stu-id="62013-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-114">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-115">整數</span><span class="sxs-lookup"><span data-stu-id="62013-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-116">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-117">1–2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-118">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-119">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-120">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-121">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-122">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-123">No</span><span class="sxs-lookup"><span data-stu-id="62013-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-124">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-125">No</span><span class="sxs-lookup"><span data-stu-id="62013-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-126">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-127">No</span><span class="sxs-lookup"><span data-stu-id="62013-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-128">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-129">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-130">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-131">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-132">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-133">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="62013-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="62013-135">107</span><span class="sxs-lookup"><span data-stu-id="62013-135">107</span></span>  

<span data-ttu-id="62013-136">此參數可用來防止資料庫引擎將其效能的相關資料發佈至 Windows。</span><span class="sxs-lookup"><span data-stu-id="62013-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="62013-137">這樣做可以減少資料庫引擎的服務執行緒活動。</span><span class="sxs-lookup"><span data-stu-id="62013-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-138">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-139">否</span><span class="sxs-lookup"><span data-stu-id="62013-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-140">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="62013-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-142">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-143">False, True</span><span class="sxs-lookup"><span data-stu-id="62013-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-144">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-145">全球</span><span class="sxs-lookup"><span data-stu-id="62013-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-146">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-147">No</span><span class="sxs-lookup"><span data-stu-id="62013-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-148">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-149">No</span><span class="sxs-lookup"><span data-stu-id="62013-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-150">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-151">No</span><span class="sxs-lookup"><span data-stu-id="62013-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-152">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-153">No</span><span class="sxs-lookup"><span data-stu-id="62013-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-154">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-155">No</span><span class="sxs-lookup"><span data-stu-id="62013-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-156">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-157">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-158">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-159">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="62013-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="62013-161">81</span><span class="sxs-lookup"><span data-stu-id="62013-161">81</span></span>  

<span data-ttu-id="62013-162">此參數可讓在多重實例模式中運作的應用程式預先配置記憶體給全域集區中的版本頁面，以模擬較舊的行為。</span><span class="sxs-lookup"><span data-stu-id="62013-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="62013-163">如果應用程式想要保證特定大小的交易稍後可能會成功，即使記憶體變得很少，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="62013-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="62013-164">**Windows 2000：**  在 [JetInit](./jetinit-function.md) 時，一律會保留足夠的記憶體來備份所有版本頁面。</span><span class="sxs-lookup"><span data-stu-id="62013-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="62013-165">**WINDOWS XP：**  在 Windows XP 中，這在單一實例模式中仍為 true。</span><span class="sxs-lookup"><span data-stu-id="62013-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="62013-166">不過，在多重實例模式中時，會以動態方式配置版本頁面記憶體。</span><span class="sxs-lookup"><span data-stu-id="62013-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-167">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-168">64</span><span class="sxs-lookup"><span data-stu-id="62013-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-169">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-170">整數</span><span class="sxs-lookup"><span data-stu-id="62013-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-171">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-172">1–2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-173">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-174">全球</span><span class="sxs-lookup"><span data-stu-id="62013-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-175">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-176">No</span><span class="sxs-lookup"><span data-stu-id="62013-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-177">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-178">No</span><span class="sxs-lookup"><span data-stu-id="62013-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-179">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-180">No</span><span class="sxs-lookup"><span data-stu-id="62013-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-181">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-182">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-183">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-184">No</span><span class="sxs-lookup"><span data-stu-id="62013-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-185">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-186">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-187">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-188">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="62013-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="62013-190">8</span><span class="sxs-lookup"><span data-stu-id="62013-190">8</span></span>  

<span data-ttu-id="62013-191">此參數會保留所要求的資料指標資源數目，供實例使用。</span><span class="sxs-lookup"><span data-stu-id="62013-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="62013-192">資料指標資源直接對應至 [JET_TABLEID](./jet-tableid.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="62013-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="62013-193">此設定會影響可同時使用的資料指標數目。</span><span class="sxs-lookup"><span data-stu-id="62013-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="62013-194">不同的會話無法共用資料指標資源，因此這個參數必須設定為夠大的值，讓每個會話可以使用所需的資料指標數目。</span><span class="sxs-lookup"><span data-stu-id="62013-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="62013-195">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="62013-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-196">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-197">1024</span><span class="sxs-lookup"><span data-stu-id="62013-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-198">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-199">整數</span><span class="sxs-lookup"><span data-stu-id="62013-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-200">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-201">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-202">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-203">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-204">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-205">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-206">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-207">No</span><span class="sxs-lookup"><span data-stu-id="62013-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-208">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-209">No</span><span class="sxs-lookup"><span data-stu-id="62013-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-210">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-211">No</span><span class="sxs-lookup"><span data-stu-id="62013-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-212">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-213">No</span><span class="sxs-lookup"><span data-stu-id="62013-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-214">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-215">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-216">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-217">全部</span><span class="sxs-lookup"><span data-stu-id="62013-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="62013-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="62013-219">104</span><span class="sxs-lookup"><span data-stu-id="62013-219">104</span></span>  

<span data-ttu-id="62013-220">此參數會控制可在單一進程中建立的實例數目上限。</span><span class="sxs-lookup"><span data-stu-id="62013-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-221">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-222">16</span><span class="sxs-lookup"><span data-stu-id="62013-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-223">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-224">整數</span><span class="sxs-lookup"><span data-stu-id="62013-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-225">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="62013-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-227">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-228">全球</span><span class="sxs-lookup"><span data-stu-id="62013-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-229">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-230">No</span><span class="sxs-lookup"><span data-stu-id="62013-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-231">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-232">No</span><span class="sxs-lookup"><span data-stu-id="62013-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-233">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-234">No</span><span class="sxs-lookup"><span data-stu-id="62013-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-235">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-236">No</span><span class="sxs-lookup"><span data-stu-id="62013-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-237">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-238">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-239">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-240">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-241">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-242">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="62013-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="62013-244">6</span><span class="sxs-lookup"><span data-stu-id="62013-244">6</span></span>  

<span data-ttu-id="62013-245">此參數會保留要求的 B + 樹狀結構資源數目，以供實例使用。</span><span class="sxs-lookup"><span data-stu-id="62013-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="62013-246">此設定會影響可同時使用的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="62013-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="62013-247">此參數必須相對於資料庫引擎所使用之資料庫的實體架構進行設定，如此一來，這項設定就不會像它一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="62013-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="62013-248">一般情況下，每個資料表的每個次要索引都需要兩個資源，再加上一個資源，同時應用程式同時使用。</span><span class="sxs-lookup"><span data-stu-id="62013-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="62013-249">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="62013-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-250">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-251">300</span><span class="sxs-lookup"><span data-stu-id="62013-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-252">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-253">整數</span><span class="sxs-lookup"><span data-stu-id="62013-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-254">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-255">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-256">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-257">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-258">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-259">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-260">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-261">No</span><span class="sxs-lookup"><span data-stu-id="62013-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-262">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-263">No</span><span class="sxs-lookup"><span data-stu-id="62013-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-264">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-265">No</span><span class="sxs-lookup"><span data-stu-id="62013-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-266">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-267">No</span><span class="sxs-lookup"><span data-stu-id="62013-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-268">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-269">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-270">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-271">全部</span><span class="sxs-lookup"><span data-stu-id="62013-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="62013-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="62013-273">5</span><span class="sxs-lookup"><span data-stu-id="62013-273">5</span></span>  

<span data-ttu-id="62013-274">此參數會保留實例所用的要求會話資源數目。</span><span class="sxs-lookup"><span data-stu-id="62013-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="62013-275">會話資源直接對應至 [JET_SESID](./jet-sesid.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="62013-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="62013-276">此設定會影響可同時使用的會話數目。</span><span class="sxs-lookup"><span data-stu-id="62013-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="62013-277">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="62013-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-278">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-279">16</span><span class="sxs-lookup"><span data-stu-id="62013-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-280">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-281">整數</span><span class="sxs-lookup"><span data-stu-id="62013-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-282">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-283">0-30000</span><span class="sxs-lookup"><span data-stu-id="62013-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-284">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-285">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-286">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-287">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-288">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-289">No</span><span class="sxs-lookup"><span data-stu-id="62013-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-290">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-291">No</span><span class="sxs-lookup"><span data-stu-id="62013-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-292">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-293">No</span><span class="sxs-lookup"><span data-stu-id="62013-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-294">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-295">No</span><span class="sxs-lookup"><span data-stu-id="62013-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-296">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-297">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-298">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-299">全部</span><span class="sxs-lookup"><span data-stu-id="62013-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="62013-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="62013-301">10</span><span class="sxs-lookup"><span data-stu-id="62013-301">10</span></span>  

<span data-ttu-id="62013-302">此參數會保留所要求的臨時表資源數目，供實例使用。</span><span class="sxs-lookup"><span data-stu-id="62013-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="62013-303">此設定會影響可同時使用的臨時表數目。</span><span class="sxs-lookup"><span data-stu-id="62013-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="62013-304">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="62013-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="62013-305">**WINDOWS XP 和更新版本：**  如果這個系統參數設定為零，則不會建立暫存資料庫，而且任何需要使用暫存資料庫的活動都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="62013-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="62013-306">這項設定有助於避免建立暫存資料庫所需的 i/o （如果已知不會使用）。</span><span class="sxs-lookup"><span data-stu-id="62013-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="62013-307">**注意**  使用臨時表也需要資料指標資源。</span><span class="sxs-lookup"><span data-stu-id="62013-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-308">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-309">20</span><span class="sxs-lookup"><span data-stu-id="62013-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-310">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-311">整數</span><span class="sxs-lookup"><span data-stu-id="62013-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-312">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-313">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-314">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-315">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-316">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-317">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-318">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-319">No</span><span class="sxs-lookup"><span data-stu-id="62013-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-320">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-321">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-322">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-323">No</span><span class="sxs-lookup"><span data-stu-id="62013-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-324">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-325">No</span><span class="sxs-lookup"><span data-stu-id="62013-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-326">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-327">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-328">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-329">全部</span><span class="sxs-lookup"><span data-stu-id="62013-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="62013-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="62013-331">9</span><span class="sxs-lookup"><span data-stu-id="62013-331">9</span></span>  

<span data-ttu-id="62013-332">此參數會保留實例所使用的版本存放區頁面所要求的數目。</span><span class="sxs-lookup"><span data-stu-id="62013-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="62013-333">版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。</span><span class="sxs-lookup"><span data-stu-id="62013-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="62013-334">這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。</span><span class="sxs-lookup"><span data-stu-id="62013-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="62013-335">這項設定會影響一次可以保留在記憶體中的更新數目。</span><span class="sxs-lookup"><span data-stu-id="62013-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="62013-336">這將會影響單一交易可執行檔更新數目上限、交易可保持開啟的最大持續時間、在系統上更新交易的最大並行載入，或是這些的組合。</span><span class="sxs-lookup"><span data-stu-id="62013-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="62013-337">此參數所設定的每個版本存放區頁面，在32位電腦上的大小為16KB，而在64位電腦上則為32KB。</span><span class="sxs-lookup"><span data-stu-id="62013-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="62013-338">**Windows Vista 和更新版本：**  版本存放區頁面大小可透過 JET_paramVerPageSize 讀取及變更。</span><span class="sxs-lookup"><span data-stu-id="62013-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="62013-339">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  此參數的大數值會耗用位址空間，而且可能會增加記憶體使用量。</span><span class="sxs-lookup"><span data-stu-id="62013-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="62013-340">**注意**  這是最常用於資料庫引擎的資源。</span><span class="sxs-lookup"><span data-stu-id="62013-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="62013-341">請注意，必須將系統參數的設定以及應用程式的交易式負載的設定付費，以避免在正常操作下耗盡此資源。</span><span class="sxs-lookup"><span data-stu-id="62013-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="62013-342">當此資源耗盡時，資料庫的更新將會遭到拒絕，並 JET_errVersionStoreOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="62013-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="62013-343">若要釋放其中一些資源，最舊的未完成交易必須中止。</span><span class="sxs-lookup"><span data-stu-id="62013-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-344">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-345">64</span><span class="sxs-lookup"><span data-stu-id="62013-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-346">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-347">整數</span><span class="sxs-lookup"><span data-stu-id="62013-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-348">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-349">1–2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-350">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-351">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-352">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-353">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-354">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-355">No</span><span class="sxs-lookup"><span data-stu-id="62013-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-356">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-357">No</span><span class="sxs-lookup"><span data-stu-id="62013-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-358">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-359">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-360">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-361">No</span><span class="sxs-lookup"><span data-stu-id="62013-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-362">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-363">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-364">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-365">全部</span><span class="sxs-lookup"><span data-stu-id="62013-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="62013-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="62013-367">101</span><span class="sxs-lookup"><span data-stu-id="62013-367">101</span></span>  

<span data-ttu-id="62013-368">此參數會控制特殊快取的大小，用來加速查閱資料庫頁面快取中 B + 樹狀目錄的子頁面指標。</span><span class="sxs-lookup"><span data-stu-id="62013-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="62013-369">快取的大小是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="62013-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-370">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-371">262144</span><span class="sxs-lookup"><span data-stu-id="62013-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-372">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-373">整數</span><span class="sxs-lookup"><span data-stu-id="62013-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-374">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-375">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-376">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-377">全球</span><span class="sxs-lookup"><span data-stu-id="62013-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-378">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-379">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-380">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-381">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-382">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-383">No</span><span class="sxs-lookup"><span data-stu-id="62013-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-384">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-385">No</span><span class="sxs-lookup"><span data-stu-id="62013-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-386">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-387">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-388">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-389">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-390">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-391">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="62013-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="62013-393">7</span><span class="sxs-lookup"><span data-stu-id="62013-393">7</span></span>  

<span data-ttu-id="62013-394">此參數會嘗試將 B + 樹系資源的數目維持在低於指定的臨界值。</span><span class="sxs-lookup"><span data-stu-id="62013-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="62013-395">如果此參數設定為零，則會預設為100% 的 **JET_paramMaxOpenTables**。</span><span class="sxs-lookup"><span data-stu-id="62013-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="62013-396">**Windows Vista 和更新版本：**  此參數已過時，且不會影響資料庫引擎的操作。</span><span class="sxs-lookup"><span data-stu-id="62013-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="62013-397">應用程式應該改用 JET_paramMaxCachedClosedTables。</span><span class="sxs-lookup"><span data-stu-id="62013-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-398">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-399">0 (100% 的 <strong>JET_paramMaxOpenTables</strong>) </span><span class="sxs-lookup"><span data-stu-id="62013-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-400">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-401">整數</span><span class="sxs-lookup"><span data-stu-id="62013-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-402">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-403">0-2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-404">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-405">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-406">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-407">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-408">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-409">No</span><span class="sxs-lookup"><span data-stu-id="62013-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-410">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-411">No</span><span class="sxs-lookup"><span data-stu-id="62013-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-412">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-413">No</span><span class="sxs-lookup"><span data-stu-id="62013-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-414">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-415">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-416">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-417">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-418">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-419">全部</span><span class="sxs-lookup"><span data-stu-id="62013-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="62013-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="62013-421">63</span><span class="sxs-lookup"><span data-stu-id="62013-421">63</span></span>  

<span data-ttu-id="62013-422">此參數代表一個相對於 **JET_paramMaxVerPages** 的臨界值，可控制 database engine 任意使用版本頁面。</span><span class="sxs-lookup"><span data-stu-id="62013-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="62013-423">如果版本存放區的大小超過此臨界值，則只會針對選擇性的背景工作（例如回收資料庫中已刪除的空間）使用任何資訊，而不會犧牲保存交易資訊的空間。</span><span class="sxs-lookup"><span data-stu-id="62013-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="62013-424">**Windows 2000、WINDOWS XP 及 Windows Server 2003：**  將此參數設定為零會將臨界值設定為90% 的 **JET_paramMaxVerPages**。</span><span class="sxs-lookup"><span data-stu-id="62013-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="62013-425">**Windows Vista 和更新版本：**  已不再支援此參數，且此參數的預設值已變更，以闡明其行為。</span><span class="sxs-lookup"><span data-stu-id="62013-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="62013-426">此參數所設定的每個版本存放區頁面，在32位電腦上的大小為16KB，而在64位電腦上則為32KB。</span><span class="sxs-lookup"><span data-stu-id="62013-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="62013-427">**Windows Vista 和更新版本：**  版本存放區頁面大小可透過 JET_paramVerPageSize 讀取及變更。</span><span class="sxs-lookup"><span data-stu-id="62013-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="62013-428">**注意**  如果資料庫引擎太過頻繁地操作此閾值，則資料庫可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="62013-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="62013-429">發生這種情況的原因是，清除資料庫的背景進程無法正常運作，而不需要在此案例中擲回的選擇性資訊。</span><span class="sxs-lookup"><span data-stu-id="62013-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="62013-430">線上或離線磁碟重組將會阻礙此效果。</span><span class="sxs-lookup"><span data-stu-id="62013-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-431">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-432"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  0 (90% 的 JET_paramMaxVerPages) </span><span class="sxs-lookup"><span data-stu-id="62013-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="62013-433"><strong>Windows Vista：</strong>  58</span><span class="sxs-lookup"><span data-stu-id="62013-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-434">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-435">整數</span><span class="sxs-lookup"><span data-stu-id="62013-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-436">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-437">1–2147483647</span><span class="sxs-lookup"><span data-stu-id="62013-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-438">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-439">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-440">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-441">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-442">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-443">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-444">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-445">No</span><span class="sxs-lookup"><span data-stu-id="62013-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-446">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-447">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-448">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-449">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-450">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-451">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-452">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-453">全部</span><span class="sxs-lookup"><span data-stu-id="62013-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="62013-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="62013-455">128</span><span class="sxs-lookup"><span data-stu-id="62013-455">128</span></span>  

<span data-ttu-id="62013-456">此參數可控制 database engine 用來保存交易資訊的版本存放區頁面大小。</span><span class="sxs-lookup"><span data-stu-id="62013-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="62013-457">此參數的值是版本頁面的所有其他系統參數的單位大小 (例如 JET_paramMaxVerPages) 。</span><span class="sxs-lookup"><span data-stu-id="62013-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="62013-458">資料庫引擎可能會選擇使用比要求更大的版本存放區頁面大小。</span><span class="sxs-lookup"><span data-stu-id="62013-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-459">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-460">16384</span><span class="sxs-lookup"><span data-stu-id="62013-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-461">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-462">整數</span><span class="sxs-lookup"><span data-stu-id="62013-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-463">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-464">1024、2048、4096、8192、16384、32768、65536</span><span class="sxs-lookup"><span data-stu-id="62013-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-465">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-466">全球</span><span class="sxs-lookup"><span data-stu-id="62013-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-467">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-468">No</span><span class="sxs-lookup"><span data-stu-id="62013-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-469">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-470">No</span><span class="sxs-lookup"><span data-stu-id="62013-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-471">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-472">No</span><span class="sxs-lookup"><span data-stu-id="62013-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-473">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-474">No</span><span class="sxs-lookup"><span data-stu-id="62013-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-475">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-476">No</span><span class="sxs-lookup"><span data-stu-id="62013-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-477">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-478">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-479">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-480">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="62013-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="62013-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="62013-482">105</span><span class="sxs-lookup"><span data-stu-id="62013-482">105</span></span>  

<span data-ttu-id="62013-483">此參數會控制可以在任何時間佇列至 database engine 執行緒集區的背景清除工作專案數目。</span><span class="sxs-lookup"><span data-stu-id="62013-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-484">預設值：3</span><span class="sxs-lookup"><span data-stu-id="62013-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="62013-485">32</span><span class="sxs-lookup"><span data-stu-id="62013-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-486">輸入：</span><span class="sxs-lookup"><span data-stu-id="62013-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="62013-487">整數</span><span class="sxs-lookup"><span data-stu-id="62013-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-488">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="62013-489"><strong>WINDOWS XP 和 Windows Server 2003：  </strong>  1 –63</span><span class="sxs-lookup"><span data-stu-id="62013-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="62013-490"><strong>Windows Vista：</strong>  1-127</span><span class="sxs-lookup"><span data-stu-id="62013-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-491">範圍：</span><span class="sxs-lookup"><span data-stu-id="62013-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="62013-492">執行個體</span><span class="sxs-lookup"><span data-stu-id="62013-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-493">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-494">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-495">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="62013-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="62013-496"><strong>WINDOWS XP 和 Windows Server 2003：  </strong>  不</span><span class="sxs-lookup"><span data-stu-id="62013-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="62013-497"><strong>Windows Vista：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="62013-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-498">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="62013-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="62013-499">No</span><span class="sxs-lookup"><span data-stu-id="62013-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-500">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="62013-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="62013-501">No</span><span class="sxs-lookup"><span data-stu-id="62013-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-502">影響效能：</span><span class="sxs-lookup"><span data-stu-id="62013-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="62013-503">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-504">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="62013-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="62013-505">Yes</span><span class="sxs-lookup"><span data-stu-id="62013-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-506">可用性：</span><span class="sxs-lookup"><span data-stu-id="62013-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="62013-507">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="62013-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="62013-508">規格需求</span><span class="sxs-lookup"><span data-stu-id="62013-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62013-509"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="62013-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="62013-510">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="62013-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62013-511"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="62013-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="62013-512">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="62013-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62013-513"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="62013-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="62013-514">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="62013-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="62013-515">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62013-515">See Also</span></span>

[<span data-ttu-id="62013-516">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="62013-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="62013-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="62013-517">JetInit</span></span>](./jetinit-function.md)
