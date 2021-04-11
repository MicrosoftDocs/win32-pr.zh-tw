---
description: 深入瞭解：錯誤處理參數
title: 錯誤處理參數
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852619"
---
# <a name="error-handling-parameters"></a><span data-ttu-id="20807-103">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="20807-103">Error Handling Parameters</span></span>


<span data-ttu-id="20807-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20807-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-parameters"></a><span data-ttu-id="20807-105">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="20807-105">Error Handling Parameters</span></span>

<span data-ttu-id="20807-106">本主題包含用於錯誤處理的參數。</span><span class="sxs-lookup"><span data-stu-id="20807-106">This topic contains parameters that are used for error handling.</span></span>

<span data-ttu-id="20807-107">*JET_paramErrorToString* 70</span><span class="sxs-lookup"><span data-stu-id="20807-107">*JET_paramErrorToString* 70</span></span>  

<span data-ttu-id="20807-108">這個參數可以用來將 [JET_ERR](./jet-err.md) 轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="20807-108">This parameter can be used to convert a [JET_ERR](./jet-err.md) into a string.</span></span> <span data-ttu-id="20807-109">這是使用 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 的特殊呼叫來完成，其中整數輸出緩衝區包含要轉換 (為輸入參數的 [JET_ERR](./jet-err.md) 值) 而且字串輸出緩衝區會傳回相符的錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="20807-109">This is done using a special call to [JetGetSystemParameter](./jetgetsystemparameter-function.md) where the integer output buffer contains the [JET_ERR](./jet-err.md) value to be converted (as an input parameter) and the string output buffer returns the matching error string.</span></span> <span data-ttu-id="20807-110">字串看起來會像這樣：「JET_errSuccess，成功的作業」。</span><span class="sxs-lookup"><span data-stu-id="20807-110">The string will look something like this: "JET_errSuccess,Successful Operation".</span></span> <span data-ttu-id="20807-111">字串是由字串的符號名稱、逗號，以及錯誤的簡單文字描述所組成。</span><span class="sxs-lookup"><span data-stu-id="20807-111">The string is composed of the symbolic name for the string, then a comma, and then a simple text description of the error.</span></span> <span data-ttu-id="20807-112">描述字串本身可以包含逗號。</span><span class="sxs-lookup"><span data-stu-id="20807-112">The description string may itself contain commas.</span></span> <span data-ttu-id="20807-113">如果無法辨識錯誤，則字串會是「未知的錯誤，未知的錯誤」。</span><span class="sxs-lookup"><span data-stu-id="20807-113">If the error is not recognized then the string will be "Unknown Error,Unknown Error".</span></span>

<span data-ttu-id="20807-114">**注意**  此參數是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="20807-114">**Note**  This parameter is read only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20807-115">預設值：3</span><span class="sxs-lookup"><span data-stu-id="20807-115">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="20807-116">特殊</span><span class="sxs-lookup"><span data-stu-id="20807-116">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-117">輸入：</span><span class="sxs-lookup"><span data-stu-id="20807-117">Type:</span></span></p></td>
<td><p><span data-ttu-id="20807-118">特殊</span><span class="sxs-lookup"><span data-stu-id="20807-118">Special</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-119">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="20807-119">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="20807-120">特殊</span><span class="sxs-lookup"><span data-stu-id="20807-120">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-121">範圍：</span><span class="sxs-lookup"><span data-stu-id="20807-121">Scope:</span></span></p></td>
<td><p><span data-ttu-id="20807-122">全球</span><span class="sxs-lookup"><span data-stu-id="20807-122">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-123">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="20807-123">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="20807-124">No</span><span class="sxs-lookup"><span data-stu-id="20807-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-125">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="20807-125">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="20807-126">No</span><span class="sxs-lookup"><span data-stu-id="20807-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-127">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="20807-127">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="20807-128">No</span><span class="sxs-lookup"><span data-stu-id="20807-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-129">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="20807-129">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="20807-130">No</span><span class="sxs-lookup"><span data-stu-id="20807-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-131">影響效能：</span><span class="sxs-lookup"><span data-stu-id="20807-131">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="20807-132">No</span><span class="sxs-lookup"><span data-stu-id="20807-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-133">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="20807-133">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="20807-134">No</span><span class="sxs-lookup"><span data-stu-id="20807-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-135">可用性：</span><span class="sxs-lookup"><span data-stu-id="20807-135">Availability:</span></span></p></td>
<td><p><span data-ttu-id="20807-136">全部</span><span class="sxs-lookup"><span data-stu-id="20807-136">All</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="20807-137">*JET_paramExceptionAction*</span><span class="sxs-lookup"><span data-stu-id="20807-137">*JET_paramExceptionAction*</span></span>  
<span data-ttu-id="20807-138">98</span><span class="sxs-lookup"><span data-stu-id="20807-138">98</span></span>  

<span data-ttu-id="20807-139">此參數會控制資料庫引擎擲回例外狀況時所發生的狀況，或資料庫引擎所呼叫的程式碼。</span><span class="sxs-lookup"><span data-stu-id="20807-139">This parameter controls what happens when an exception is thrown by the database engine or code that is called by the database engine.</span></span> <span data-ttu-id="20807-140">當設定為 JET_ExceptionMsgBox 時，將會擲回任何例外狀況至 Windows 未處理的例外狀況篩選準則。</span><span class="sxs-lookup"><span data-stu-id="20807-140">When set to JET_ExceptionMsgBox, any exception will be thrown to the Windows unhandled exception filter.</span></span> <span data-ttu-id="20807-141">這會導致應用程式失敗時處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="20807-141">This will result in the exception being handled as an application failure.</span></span> <span data-ttu-id="20807-142">其目的是要避免應用程式程式碼錯誤地嘗試攔截並忽略 database engine 所產生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="20807-142">The intent is to prevent application code from erroneously trying to catch and ignore an exception generated by the database engine.</span></span> <span data-ttu-id="20807-143">因為可能發生資料庫損毀，所以無法允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="20807-143">This cannot be allowed because database corruption could occur.</span></span> <span data-ttu-id="20807-144">如果應用程式希望適當地處理這些例外狀況，則可以將此參數設定為 JET_ExceptionNone 來停用保護。</span><span class="sxs-lookup"><span data-stu-id="20807-144">If the application wishes to properly handle these exceptions then the protection can be disabled by setting this parameter to JET_ExceptionNone.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20807-145">預設值：3</span><span class="sxs-lookup"><span data-stu-id="20807-145">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="20807-146">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="20807-146">JET_ExceptionMsgBox</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-147">輸入：</span><span class="sxs-lookup"><span data-stu-id="20807-147">Type:</span></span></p></td>
<td><p><span data-ttu-id="20807-148">整數</span><span class="sxs-lookup"><span data-stu-id="20807-148">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-149">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="20807-149">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="20807-150">JET_ExceptionMsgBox，JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="20807-150">JET_ExceptionMsgBox, JET_ExceptionNone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-151">範圍：</span><span class="sxs-lookup"><span data-stu-id="20807-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="20807-152">全球</span><span class="sxs-lookup"><span data-stu-id="20807-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-153">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="20807-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="20807-154"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：  </strong>  不</span><span class="sxs-lookup"><span data-stu-id="20807-154"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="20807-155"><strong>Windows Vista：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="20807-155"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-156">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="20807-156">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="20807-157"><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：  </strong>  不</span><span class="sxs-lookup"><span data-stu-id="20807-157"><strong>Windows 2000, Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="20807-158"><strong>Windows Vista：</strong>  是的</span><span class="sxs-lookup"><span data-stu-id="20807-158"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-159">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="20807-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="20807-160">No</span><span class="sxs-lookup"><span data-stu-id="20807-160">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-161">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="20807-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="20807-162">Yes</span><span class="sxs-lookup"><span data-stu-id="20807-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-163">影響效能：</span><span class="sxs-lookup"><span data-stu-id="20807-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="20807-164">No</span><span class="sxs-lookup"><span data-stu-id="20807-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-165">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="20807-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="20807-166">No</span><span class="sxs-lookup"><span data-stu-id="20807-166">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-167">可用性：</span><span class="sxs-lookup"><span data-stu-id="20807-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="20807-168">全部</span><span class="sxs-lookup"><span data-stu-id="20807-168">All</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="requirements"></a><span data-ttu-id="20807-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="20807-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20807-170"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="20807-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20807-171">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="20807-171">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20807-172"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="20807-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20807-173">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="20807-173">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20807-174"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="20807-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20807-175">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="20807-175">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a><span data-ttu-id="20807-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20807-176">See Also</span></span>

[<span data-ttu-id="20807-177">錯誤處理常數</span><span class="sxs-lookup"><span data-stu-id="20807-177">Error Handling Constants</span></span>](./error-handling-constants.md)  
[<span data-ttu-id="20807-178">可擴充儲存引擎錯誤碼</span><span class="sxs-lookup"><span data-stu-id="20807-178">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="20807-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="20807-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="20807-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="20807-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="20807-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="20807-181">JetInit</span></span>](./jetinit-function.md)
