---
description: 深入瞭解：索引參數
title: 索引參數
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027508"
---
# <a name="index-parameters"></a><span data-ttu-id="bab8f-103">索引參數</span><span class="sxs-lookup"><span data-stu-id="bab8f-103">Index Parameters</span></span>


<span data-ttu-id="bab8f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bab8f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="bab8f-105">索引參數</span><span class="sxs-lookup"><span data-stu-id="bab8f-105">Index Parameters</span></span>

<span data-ttu-id="bab8f-106">本主題包含用於索引的參數。</span><span class="sxs-lookup"><span data-stu-id="bab8f-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="bab8f-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="bab8f-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="bab8f-108">132</span><span class="sxs-lookup"><span data-stu-id="bab8f-108">132</span></span>  

<span data-ttu-id="bab8f-109">此參數會指定在產生每個元組時，用來逐步執行來源資料行值的位移增量的預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="bab8f-110">如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bab8f-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-111">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-112">1</span><span class="sxs-lookup"><span data-stu-id="bab8f-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-114">整數</span><span class="sxs-lookup"><span data-stu-id="bab8f-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-115">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="bab8f-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-117">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-118">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-119">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-120">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-121">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-122">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-123">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-124">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-125">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-126">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-127">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-128">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-129">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-130">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-131">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-132">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="bab8f-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab8f-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="bab8f-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="bab8f-134">133</span><span class="sxs-lookup"><span data-stu-id="bab8f-134">133</span></span>  

<span data-ttu-id="bab8f-135">此參數會指定來源資料行值中的位移的預設值，而產生元組產生。</span><span class="sxs-lookup"><span data-stu-id="bab8f-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="bab8f-136">如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bab8f-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-137">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-138">0</span><span class="sxs-lookup"><span data-stu-id="bab8f-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-139">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-140">整數</span><span class="sxs-lookup"><span data-stu-id="bab8f-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-141">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="bab8f-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-143">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-144">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-145">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-146">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-147">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-148">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-149">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-150">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-151">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-152">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-153">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-154">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-155">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-156">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-157">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-158">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="bab8f-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab8f-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="bab8f-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="bab8f-160">111</span><span class="sxs-lookup"><span data-stu-id="bab8f-160">111</span></span>  

<span data-ttu-id="bab8f-161">此參數會針對元組索引中的最大元組長度指定預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="bab8f-162">如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bab8f-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="bab8f-163">**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bab8f-164">若為 Windows Vista，則不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="bab8f-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-165">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-166">10</span><span class="sxs-lookup"><span data-stu-id="bab8f-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-167">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-168">整數</span><span class="sxs-lookup"><span data-stu-id="bab8f-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-169">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-170"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>  0、2-255</span><span class="sxs-lookup"><span data-stu-id="bab8f-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="bab8f-171"><strong>Windows Vista：</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="bab8f-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-172">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-173">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-174">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-175">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-176">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-177">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-178">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-179">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-180">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-181">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-182">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-183">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-184">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-185">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-186">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-187">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="bab8f-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab8f-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="bab8f-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="bab8f-189">110</span><span class="sxs-lookup"><span data-stu-id="bab8f-189">110</span></span>  

<span data-ttu-id="bab8f-190">此參數會針對元組索引中的最小元組長度指定預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="bab8f-191">如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="bab8f-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="bab8f-192">**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bab8f-193">若為 Windows Vista，則不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="bab8f-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-194">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-195">3</span><span class="sxs-lookup"><span data-stu-id="bab8f-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-196">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-197">整數</span><span class="sxs-lookup"><span data-stu-id="bab8f-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-198">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-199"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>  0、2-255</span><span class="sxs-lookup"><span data-stu-id="bab8f-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="bab8f-200"><strong>Windows Vista：</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="bab8f-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-201">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-202">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-203">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-204">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-205">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-206">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-207">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-208">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-209">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-210">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-211">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-212">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-213">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-214">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-215">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-216">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="bab8f-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab8f-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="bab8f-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="bab8f-218">112</span><span class="sxs-lookup"><span data-stu-id="bab8f-218">112</span></span>  

<span data-ttu-id="bab8f-219">此參數會指定要細分為元組索引之元組的來源字串最大長度的預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="bab8f-220">如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="bab8f-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="bab8f-221">**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。</span><span class="sxs-lookup"><span data-stu-id="bab8f-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="bab8f-222">若為 Windows Vista，則不再支援此功能。</span><span class="sxs-lookup"><span data-stu-id="bab8f-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-223">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-224">32767</span><span class="sxs-lookup"><span data-stu-id="bab8f-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-225">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-226">整數</span><span class="sxs-lookup"><span data-stu-id="bab8f-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-227">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-228"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  0 –32767</span><span class="sxs-lookup"><span data-stu-id="bab8f-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="bab8f-229"><strong>Windows Vista：</strong>  1-32767</span><span class="sxs-lookup"><span data-stu-id="bab8f-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-230">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-231">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-232">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-233">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-234">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-235">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-236">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-237">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-238">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-239">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-240">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-241">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-242">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-243">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-244">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-245">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="bab8f-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bab8f-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="bab8f-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="bab8f-247">72</span><span class="sxs-lookup"><span data-stu-id="bab8f-247">72</span></span>  

<span data-ttu-id="bab8f-248">此參數會控制 Unicode 索引鍵資料行上任何索引所使用的預設 Unicode 參數。</span><span class="sxs-lookup"><span data-stu-id="bab8f-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="bab8f-249">這個參數的型別是 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) 的，實際上是使用儲存在 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 和 [JetSetSystemParameter](./jetsetsystemparameter-function.md)的整數參數中的緩衝區指標來傳遞。</span><span class="sxs-lookup"><span data-stu-id="bab8f-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="bab8f-250">緩衝區的大小必須等於 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) 的大小，且必須使用字串緩衝區大小參數傳遞至 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="bab8f-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="bab8f-251">這顯然不一致，但這是此參數的行為。</span><span class="sxs-lookup"><span data-stu-id="bab8f-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="bab8f-252">此參數的預設值包含美國英文地區設定的 LCID，以及下列 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標： LCMAP_SORTKEY、NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="bab8f-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="bab8f-253">**Windows 2000：**  LCID 中的 SORTID 會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bab8f-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="bab8f-254">一律會使用 SORT_DEFAULT 的 SORTID。</span><span class="sxs-lookup"><span data-stu-id="bab8f-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="bab8f-255">**Windows 2000：** [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 旗標必須包含下列旗標： LCMAP_SORTKEY、NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="bab8f-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="bab8f-256">此外， [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標可能包含下列旗標： NORM_IGNORENONSPACE。</span><span class="sxs-lookup"><span data-stu-id="bab8f-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="bab8f-257">**注意**  如果您的應用程式希望儲存 Unicode 資料，強烈建議您不要依賴索引的預設 Unicode 參數。</span><span class="sxs-lookup"><span data-stu-id="bab8f-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="bab8f-258">使用美式英文的表示是使用不變的地區設定，而且已知的預設 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標會嚴重干擾某些語言。</span><span class="sxs-lookup"><span data-stu-id="bab8f-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="bab8f-259">您應該一律使用 [JET_INDEXCREATE](./jet-indexcreate-structure.md)，將 Unicode 參數的設定指定為 JetCreateIndex2。</span><span class="sxs-lookup"><span data-stu-id="bab8f-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-260">預設值：3</span><span class="sxs-lookup"><span data-stu-id="bab8f-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-261">特殊</span><span class="sxs-lookup"><span data-stu-id="bab8f-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-262">輸入：</span><span class="sxs-lookup"><span data-stu-id="bab8f-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX) </span><span class="sxs-lookup"><span data-stu-id="bab8f-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-264">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-265">特殊</span><span class="sxs-lookup"><span data-stu-id="bab8f-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-266">範圍：</span><span class="sxs-lookup"><span data-stu-id="bab8f-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-267">執行個體</span><span class="sxs-lookup"><span data-stu-id="bab8f-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-268">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-269">Yes</span><span class="sxs-lookup"><span data-stu-id="bab8f-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-270">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="bab8f-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-271">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-272">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="bab8f-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-273">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-274">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-275">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-276">影響效能：</span><span class="sxs-lookup"><span data-stu-id="bab8f-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-277">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-278">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="bab8f-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-279">No</span><span class="sxs-lookup"><span data-stu-id="bab8f-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-280">可用性：</span><span class="sxs-lookup"><span data-stu-id="bab8f-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="bab8f-281">全部</span><span class="sxs-lookup"><span data-stu-id="bab8f-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="bab8f-282">規格需求</span><span class="sxs-lookup"><span data-stu-id="bab8f-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-283"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="bab8f-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bab8f-284">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="bab8f-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bab8f-285"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="bab8f-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bab8f-286">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="bab8f-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bab8f-287"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="bab8f-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bab8f-288">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="bab8f-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bab8f-289">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bab8f-289">See Also</span></span>

[<span data-ttu-id="bab8f-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="bab8f-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="bab8f-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="bab8f-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="bab8f-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="bab8f-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="bab8f-293">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="bab8f-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="bab8f-294">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bab8f-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="bab8f-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="bab8f-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="bab8f-296">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bab8f-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
