---
description: 深入瞭解：回呼參數
title: 回呼參數
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114096"
---
# <a name="callback-parameters"></a><span data-ttu-id="e52e6-103">回呼參數</span><span class="sxs-lookup"><span data-stu-id="e52e6-103">Callback Parameters</span></span>


<span data-ttu-id="e52e6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e52e6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="callback-parameters"></a><span data-ttu-id="e52e6-105">回呼參數</span><span class="sxs-lookup"><span data-stu-id="e52e6-105">Callback Parameters</span></span>

<span data-ttu-id="e52e6-106">本主題包含用於回呼的參數。</span><span class="sxs-lookup"><span data-stu-id="e52e6-106">This topic contains parameters that are used for callbacks.</span></span>

<span data-ttu-id="e52e6-107">*JET_paramDisableCallbacks*</span><span class="sxs-lookup"><span data-stu-id="e52e6-107">*JET_paramDisableCallbacks*</span></span>  
<span data-ttu-id="e52e6-108">65</span><span class="sxs-lookup"><span data-stu-id="e52e6-108">65</span></span>  

<span data-ttu-id="e52e6-109">此參數會停用應用程式提供之函式的所有 database engine 回呼。</span><span class="sxs-lookup"><span data-stu-id="e52e6-109">This parameter disables all database engine callbacks to application provided functions.</span></span> <span data-ttu-id="e52e6-110">它的主要目的是要支援資料庫引擎公用程式，而不是要在應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="e52e6-110">It is primarily intended to support the database engine utilities and is not intended to be used in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-111">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e52e6-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-112">否</span><span class="sxs-lookup"><span data-stu-id="e52e6-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="e52e6-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="e52e6-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-115">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-116">False, True</span><span class="sxs-lookup"><span data-stu-id="e52e6-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-117">範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-118">執行個體</span><span class="sxs-lookup"><span data-stu-id="e52e6-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-119">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-120">Yes</span><span class="sxs-lookup"><span data-stu-id="e52e6-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-121">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-122">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-123">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e52e6-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-124">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-125">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-126">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-127">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e52e6-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-128">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-129">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e52e6-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-130">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-131">可用性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-132">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="e52e6-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e52e6-133">*JET_paramEnablePersistedCallbacks*</span><span class="sxs-lookup"><span data-stu-id="e52e6-133">*JET_paramEnablePersistedCallbacks*</span></span>  
<span data-ttu-id="e52e6-134">156</span><span class="sxs-lookup"><span data-stu-id="e52e6-134">156</span></span>  

<span data-ttu-id="e52e6-135">此參數可讓您在資料庫中使用持續性回呼。</span><span class="sxs-lookup"><span data-stu-id="e52e6-135">This parameter enables the use of persistent callbacks in the database.</span></span> <span data-ttu-id="e52e6-136">在 Windows Vista 之前的版本中，預設會啟用持續性回呼的使用。</span><span class="sxs-lookup"><span data-stu-id="e52e6-136">In releases prior to Windows Vista, the use of persistent callbacks was enabled by default.</span></span> <span data-ttu-id="e52e6-137">應用程式現在必須使用這個參數，在執行時間明確地啟用持續性回呼。</span><span class="sxs-lookup"><span data-stu-id="e52e6-137">Applications must now explicitly enable the use of persistent callbacks at runtime using this parameter.</span></span> <span data-ttu-id="e52e6-138">如果未設定此參數，則任何需要回呼回呼的資料庫作業都會失敗，並 JET_errCallbackFailed。</span><span class="sxs-lookup"><span data-stu-id="e52e6-138">If this parameter is not set, then any database operation that requires the invocation of a callback will fail with JET_errCallbackFailed.</span></span> <span data-ttu-id="e52e6-139">此參數不會影響在執行時間使用下列機制指定的任何回呼： JET_paramRuntimeCallback、 [JetRegisterCallback](./jetregistercallback-function.md)或對 JET API 的明確回呼參數。</span><span class="sxs-lookup"><span data-stu-id="e52e6-139">This parameter does not affect any callbacks that are specified at runtime with the following mechanisms: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md), or an explicit callback parameter to a JET API.</span></span> <span data-ttu-id="e52e6-140">即使不允許使用這些持續性回呼，仍可能建立包含持續性回呼的架構元素。</span><span class="sxs-lookup"><span data-stu-id="e52e6-140">It is still possible to create schema elements that contain persistent callbacks even when the use of those persistent callbacks is disallowed.</span></span> <span data-ttu-id="e52e6-141">當此參數設定為 false 時，它會覆寫 JET_paramDisableCallbacks。</span><span class="sxs-lookup"><span data-stu-id="e52e6-141">When this parameter is set to false it overrides JET_paramDisableCallbacks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-142">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e52e6-142">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-143">否</span><span class="sxs-lookup"><span data-stu-id="e52e6-143">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-144">輸入：</span><span class="sxs-lookup"><span data-stu-id="e52e6-144">Type:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="e52e6-145">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-146">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-146">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-147">False, True</span><span class="sxs-lookup"><span data-stu-id="e52e6-147">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-148">範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-148">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-149">執行個體</span><span class="sxs-lookup"><span data-stu-id="e52e6-149">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-150">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-150">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-151">Yes</span><span class="sxs-lookup"><span data-stu-id="e52e6-151">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-152">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-152">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-153">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-154">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e52e6-154">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-155">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-156">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-156">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-157">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-158">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e52e6-158">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-159">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-159">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-160">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e52e6-160">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-161">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-161">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-162">可用性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-162">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-163">Windows Vista 和更新版本</span><span class="sxs-lookup"><span data-stu-id="e52e6-163">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e52e6-164">*JET_paramRuntimeCallback*</span><span class="sxs-lookup"><span data-stu-id="e52e6-164">*JET_paramRuntimeCallback*</span></span>  
<span data-ttu-id="e52e6-165">73</span><span class="sxs-lookup"><span data-stu-id="e52e6-165">73</span></span>  

<span data-ttu-id="e52e6-166">此參數會使用執行 [JET_CALLBACK](./jet-callback-callback-function.md) 介面的執行時間回呼函式來設定引擎。</span><span class="sxs-lookup"><span data-stu-id="e52e6-166">This parameter configures the engine with a runtime callback function implementing the [JET_CALLBACK](./jet-callback-callback-function.md) interface.</span></span> <span data-ttu-id="e52e6-167">基於下列原因，可能會呼叫這個回呼： [JET_cbtypFreeCursorLS](./jet-cbtyp.md)、 [JET_cbtypFreeTableLS](./jet-cbtyp.md)或 [JET_cbtypNull](./jet-cbtyp.md)。</span><span class="sxs-lookup"><span data-stu-id="e52e6-167">This callback may be called for the following reasons: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md), or [JET_cbtypNull](./jet-cbtyp.md).</span></span> <span data-ttu-id="e52e6-168">如需詳細資訊，請參閱 [JetSetLS](./jetsetls-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="e52e6-168">Please see [JetSetLS](./jetsetls-function.md) for more information.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-169">預設值：3</span><span class="sxs-lookup"><span data-stu-id="e52e6-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-170">NULL</span><span class="sxs-lookup"><span data-stu-id="e52e6-170">NULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-171">輸入：</span><span class="sxs-lookup"><span data-stu-id="e52e6-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-172">函數指標 (JET_API_PTR) </span><span class="sxs-lookup"><span data-stu-id="e52e6-172">Function Pointer (JET_API_PTR)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-173">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-174">Null、 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span><span class="sxs-lookup"><span data-stu-id="e52e6-174">NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>\*</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-175">範圍：</span><span class="sxs-lookup"><span data-stu-id="e52e6-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-176">執行個體</span><span class="sxs-lookup"><span data-stu-id="e52e6-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-177">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-178">Yes</span><span class="sxs-lookup"><span data-stu-id="e52e6-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-179">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="e52e6-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-180">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-181">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="e52e6-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-182">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-183">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-184">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-185">影響效能：</span><span class="sxs-lookup"><span data-stu-id="e52e6-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-186">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-187">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="e52e6-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-188">No</span><span class="sxs-lookup"><span data-stu-id="e52e6-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-189">可用性：</span><span class="sxs-lookup"><span data-stu-id="e52e6-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="e52e6-190">Windows XP 和更新版本</span><span class="sxs-lookup"><span data-stu-id="e52e6-190">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e52e6-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="e52e6-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e52e6-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e52e6-193">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e52e6-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e52e6-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e52e6-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e52e6-195">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="e52e6-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e52e6-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e52e6-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e52e6-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e52e6-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e52e6-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e52e6-198">See Also</span></span>

[<span data-ttu-id="e52e6-199">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="e52e6-199">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="e52e6-200">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="e52e6-200">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="e52e6-201">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="e52e6-201">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="e52e6-202">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="e52e6-202">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="e52e6-203">JetInit</span><span class="sxs-lookup"><span data-stu-id="e52e6-203">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="e52e6-204">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="e52e6-204">JetSetLS</span></span>](./jetsetls-function.md)
