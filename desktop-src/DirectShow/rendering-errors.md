---
description: 轉譯錯誤
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: 轉譯錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467820"
---
# <a name="rendering-errors"></a><span data-ttu-id="19731-103">轉譯錯誤</span><span class="sxs-lookup"><span data-stu-id="19731-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="19731-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="19731-104">\[Deprecated.</span></span> <span data-ttu-id="19731-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="19731-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="19731-106">Microsoft® DirectShow®編輯服務 (DES) 定義各種用來記錄轉譯錯誤的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="19731-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="19731-107">如果專案未正確轉譯，轉譯引擎會呼叫 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="19731-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="19731-108">下表摘要說明 **LogError** 提供的參數：</span><span class="sxs-lookup"><span data-stu-id="19731-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="19731-109">錯誤碼包含在 *ErrorCode* 參數中。</span><span class="sxs-lookup"><span data-stu-id="19731-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="19731-110">描述包含在 ErrorString 參數中。</span><span class="sxs-lookup"><span data-stu-id="19731-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="19731-111">描述包含在 *ErrorString* 參數中。</span><span class="sxs-lookup"><span data-stu-id="19731-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="19731-112">如果有額外的資訊， **variant** 型別就會包含在 *pExtraInfo* 所指向之 **變異** 的 **vt** 成員中。</span><span class="sxs-lookup"><span data-stu-id="19731-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="19731-113">此處所述的錯誤碼不是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="19731-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="19731-114">如需 DES 特定的 **HRESULT** 傳回值清單，請參閱 [錯誤和成功碼](error-and-success-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="19731-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19731-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="19731-115">Error code</span></span></th>
<th><span data-ttu-id="19731-116">描述</span><span class="sxs-lookup"><span data-stu-id="19731-116">Description</span></span></th>
<th><span data-ttu-id="19731-117">額外資訊</span><span class="sxs-lookup"><span data-stu-id="19731-117">Extra information</span></span></th>
<th><span data-ttu-id="19731-118">Variant 型別</span><span class="sxs-lookup"><span data-stu-id="19731-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19731-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="19731-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="19731-120">檔案名不存在，或 DirectShow 無法辨識副檔名。</span><span class="sxs-lookup"><span data-stu-id="19731-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="19731-121">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="19731-121">File name</span></span></td>
<td><span data-ttu-id="19731-122"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="19731-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="19731-124">檔案類型與副檔名不符，或檔案已損毀。</span><span class="sxs-lookup"><span data-stu-id="19731-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="19731-125">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="19731-125">File name</span></span></td>
<td><span data-ttu-id="19731-126"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="19731-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="19731-128">檔案名是必要的，但未提供。</span><span class="sxs-lookup"><span data-stu-id="19731-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="19731-129">無</span><span class="sxs-lookup"><span data-stu-id="19731-129">None</span></span></td>
<td><span data-ttu-id="19731-130">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="19731-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="19731-132">無法剖析此來源所提供的資料來源。</span><span class="sxs-lookup"><span data-stu-id="19731-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="19731-133">無</span><span class="sxs-lookup"><span data-stu-id="19731-133">None</span></span></td>
<td><span data-ttu-id="19731-134">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="19731-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="19731-136">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-136">Unexpected error.</span></span> <span data-ttu-id="19731-137">某些 DirectShow 元件未正確安裝。</span><span class="sxs-lookup"><span data-stu-id="19731-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="19731-138">無</span><span class="sxs-lookup"><span data-stu-id="19731-138">None</span></span></td>
<td><span data-ttu-id="19731-139">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="19731-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="19731-141">來源篩選不接受檔案名。</span><span class="sxs-lookup"><span data-stu-id="19731-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="19731-142">無</span><span class="sxs-lookup"><span data-stu-id="19731-142">None</span></span></td>
<td><span data-ttu-id="19731-143">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="19731-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="19731-145">不支援群組的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="19731-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="19731-146">群組編號</span><span class="sxs-lookup"><span data-stu-id="19731-146">Group number</span></span></td>
<td><span data-ttu-id="19731-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="19731-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="19731-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="19731-149">此來源的資料流程號碼無效。</span><span class="sxs-lookup"><span data-stu-id="19731-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="19731-150">串流號碼</span><span class="sxs-lookup"><span data-stu-id="19731-150">Stream number</span></span></td>
<td><span data-ttu-id="19731-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="19731-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="19731-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="19731-153">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="19731-153">Out of memory.</span></span></td>
<td><span data-ttu-id="19731-154">無</span><span class="sxs-lookup"><span data-stu-id="19731-154">None</span></span></td>
<td><span data-ttu-id="19731-155">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="19731-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="19731-157">序列中的一個點陣圖與其他點陣圖的類型不同。</span><span class="sxs-lookup"><span data-stu-id="19731-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="19731-158">點陣圖名稱</span><span class="sxs-lookup"><span data-stu-id="19731-158">Bitmap name</span></span></td>
<td><span data-ttu-id="19731-159"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="19731-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="19731-161">剪輯的媒體時間無效，或與裝置無關的點陣圖 (DIB) 順序太短。</span><span class="sxs-lookup"><span data-stu-id="19731-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="19731-162">如果發生其他轉譯錯誤，雖然媒體時間有效，仍可能發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="19731-163">無</span><span class="sxs-lookup"><span data-stu-id="19731-163">None</span></span></td>
<td><span data-ttu-id="19731-164">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="19731-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="19731-166">效果或轉換 (CLSID) 的類別識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="19731-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="19731-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="19731-167">CLSID</span></span></td>
<td><span data-ttu-id="19731-168"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="19731-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="19731-170">預設效果或轉換的 CLSID 無效。</span><span class="sxs-lookup"><span data-stu-id="19731-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="19731-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="19731-171">CLSID</span></span></td>
<td><span data-ttu-id="19731-172"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="19731-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="19731-174">您的 DirectX 版本不支援三維轉換。</span><span class="sxs-lookup"><span data-stu-id="19731-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="19731-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="19731-175">CLSID</span></span></td>
<td><span data-ttu-id="19731-176"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="19731-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="19731-178">此效果不是正確的類型或已中斷。</span><span class="sxs-lookup"><span data-stu-id="19731-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="19731-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="19731-179">CLSID</span></span></td>
<td><span data-ttu-id="19731-180"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="19731-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="19731-182">物件上不存在這類屬性。</span><span class="sxs-lookup"><span data-stu-id="19731-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="19731-183">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="19731-183">Property name</span></span></td>
<td><span data-ttu-id="19731-184"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="19731-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="19731-186">這個屬性的值不合法。</span><span class="sxs-lookup"><span data-stu-id="19731-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="19731-187">指定的值</span><span class="sxs-lookup"><span data-stu-id="19731-187">Value specified</span></span></td>
<td><span data-ttu-id="19731-188"><strong>變異</strong></span><span class="sxs-lookup"><span data-stu-id="19731-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="19731-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="19731-190">XML 檔案中有語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="19731-191">行號</span><span class="sxs-lookup"><span data-stu-id="19731-191">Line number</span></span></td>
<td><span data-ttu-id="19731-192">VT_I4 (4 位元組整數) </span><span class="sxs-lookup"><span data-stu-id="19731-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="19731-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="19731-194">在 XML 中找不到依類別和實例指定的篩選。</span><span class="sxs-lookup"><span data-stu-id="19731-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="19731-195"> (實例) 的易記名稱</span><span class="sxs-lookup"><span data-stu-id="19731-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="19731-196"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="19731-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="19731-198">將 XML 檔案寫入磁片時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="19731-199">無</span><span class="sxs-lookup"><span data-stu-id="19731-199">None</span></span></td>
<td><span data-ttu-id="19731-200">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19731-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="19731-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="19731-202">CLSID 不是有效的 DirectShow 音訊效果篩選。</span><span class="sxs-lookup"><span data-stu-id="19731-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="19731-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="19731-203">CLSID</span></span></td>
<td><span data-ttu-id="19731-204"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="19731-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19731-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="19731-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="19731-206">找不到壓縮檔以產生指定的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="19731-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="19731-207">無</span><span class="sxs-lookup"><span data-stu-id="19731-207">None</span></span></td>
<td><span data-ttu-id="19731-208">不適用</span><span class="sxs-lookup"><span data-stu-id="19731-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="19731-209">永遠不會發生下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-209">The following errors should never occur.</span></span> <span data-ttu-id="19731-210">如果您遇到上述其中一個錯誤，請將錯誤報表傳送給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="19731-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="19731-211">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="19731-211">Error code</span></span>                 | <span data-ttu-id="19731-212">描述</span><span class="sxs-lookup"><span data-stu-id="19731-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="19731-213">DEX \_ 識別碼 \_ 時間軸 \_ 剖析</span><span class="sxs-lookup"><span data-stu-id="19731-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="19731-214">剖析時間軸時發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="19731-215">DEX \_ 識別碼 \_ 圖形 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="19731-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="19731-216">建立篩選圖形時發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="19731-217">DEX \_ 識別碼 \_ 方格 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="19731-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="19731-218">內部方格發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="19731-219">DEX \_ 識別碼 \_ 介面 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="19731-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="19731-220">取得介面時發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19731-220">Unexpected error getting an interface.</span></span>      |



 

 

 




