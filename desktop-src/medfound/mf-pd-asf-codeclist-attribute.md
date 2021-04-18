---
description: 包含編解碼器和格式的相關資訊，這些編解碼器和格式是用來將 Advanced 系統格式的內容編碼 (ASF) 檔。 這個屬性會對應到 ASF 標頭中所定義的編解碼器清單物件（在 ASF 規格中定義）。
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: 'MF_PD_ASF_CODECLIST 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971538"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="2ae7c-104">MF \_ PD \_ ASF \_ CODECLIST 屬性</span><span class="sxs-lookup"><span data-stu-id="2ae7c-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="2ae7c-105">包含編解碼器和格式的相關資訊，這些編解碼器和格式是用來將 Advanced 系統格式的內容編碼 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2ae7c-106">這個屬性會對應到 ASF 標頭中所定義的編解碼器清單物件（在 ASF 規格中定義）。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ae7c-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2ae7c-107">Data type</span></span>

<span data-ttu-id="2ae7c-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="2ae7c-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae7c-109">備註</span><span class="sxs-lookup"><span data-stu-id="2ae7c-109">Remarks</span></span>

<span data-ttu-id="2ae7c-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2ae7c-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從 ASF 標頭中的編解碼器清單物件產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="2ae7c-112">使用 [ASF 媒體來源](asf-media-source.md) 的應用程式可以藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，然後從呈現描述項取得屬性，來取得這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="2ae7c-113">下表顯示內容 blob 的版面配置。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="2ae7c-114">編解碼器清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="2ae7c-114">Codec List Object field</span></span> | <span data-ttu-id="2ae7c-115">資料類型</span><span class="sxs-lookup"><span data-stu-id="2ae7c-115">Data type</span></span>    | <span data-ttu-id="2ae7c-116">大小</span><span class="sxs-lookup"><span data-stu-id="2ae7c-116">Size</span></span>    | <span data-ttu-id="2ae7c-117">Description</span><span class="sxs-lookup"><span data-stu-id="2ae7c-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="2ae7c-118">編解碼器專案計數</span><span class="sxs-lookup"><span data-stu-id="2ae7c-118">Codec Entries Count</span></span>     | <span data-ttu-id="2ae7c-119">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-119">**DWORD**</span></span>    | <span data-ttu-id="2ae7c-120">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ae7c-120">4 bytes</span></span> | <span data-ttu-id="2ae7c-121">編解碼器數目</span><span class="sxs-lookup"><span data-stu-id="2ae7c-121">Number of codecs</span></span>                      |
| <span data-ttu-id="2ae7c-122">編解碼器專案</span><span class="sxs-lookup"><span data-stu-id="2ae7c-122">Codec Entries</span></span>           | <span data-ttu-id="2ae7c-123">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-123">**BYTE**\[\]</span></span> | <span data-ttu-id="2ae7c-124">不定</span><span class="sxs-lookup"><span data-stu-id="2ae7c-124">Varies</span></span>  | <span data-ttu-id="2ae7c-125">編解碼器資訊結構的陣列</span><span class="sxs-lookup"><span data-stu-id="2ae7c-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="2ae7c-126">[程式碼專案] 欄位是結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="2ae7c-127">下表顯示每個專案的格式：</span><span class="sxs-lookup"><span data-stu-id="2ae7c-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ae7c-128">編解碼器清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="2ae7c-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="2ae7c-129">資料類型</span><span class="sxs-lookup"><span data-stu-id="2ae7c-129">Data type</span></span></th>
<th><span data-ttu-id="2ae7c-130">大小</span><span class="sxs-lookup"><span data-stu-id="2ae7c-130">Size</span></span></th>
<th><span data-ttu-id="2ae7c-131">描述</span><span class="sxs-lookup"><span data-stu-id="2ae7c-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ae7c-132">類型</span><span class="sxs-lookup"><span data-stu-id="2ae7c-132">Type</span></span></td>
<td><span data-ttu-id="2ae7c-133"><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="2ae7c-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="2ae7c-134">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ae7c-134">4 bytes</span></span></td>
<td><span data-ttu-id="2ae7c-135">編解碼器類型。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-135">Codec type.</span></span> <span data-ttu-id="2ae7c-136">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2ae7c-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="2ae7c-137">0x0001：音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="2ae7c-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="2ae7c-138">0x0002：影片編解碼器</span><span class="sxs-lookup"><span data-stu-id="2ae7c-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="2ae7c-139">0xFFFF：未知</span><span class="sxs-lookup"><span data-stu-id="2ae7c-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ae7c-140">編解碼器名稱長度</span><span class="sxs-lookup"><span data-stu-id="2ae7c-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="2ae7c-141"><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="2ae7c-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="2ae7c-142">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ae7c-142">4 bytes</span></span></td>
<td><span data-ttu-id="2ae7c-143">編解碼器名稱字串的大小（以位元組為單位），包括 <strong>Null</strong> 字元。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ae7c-144">編解碼器名稱</span><span class="sxs-lookup"><span data-stu-id="2ae7c-144">Codec Name</span></span></td>
<td><span data-ttu-id="2ae7c-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="2ae7c-146">不定</span><span class="sxs-lookup"><span data-stu-id="2ae7c-146">Varies</span></span></td>
<td><span data-ttu-id="2ae7c-147">以 Null 終止的 Unicode 字串，其中包含編解碼器的名稱，例如 &quot; Windows Media 視訊 9 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ae7c-148">編解碼器描述長度</span><span class="sxs-lookup"><span data-stu-id="2ae7c-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="2ae7c-149"><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="2ae7c-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="2ae7c-150">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ae7c-150">4 bytes</span></span></td>
<td><span data-ttu-id="2ae7c-151">編解碼器描述字串的大小（以位元組為單位），包括 <strong>Null</strong> 字元。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ae7c-152">編解碼器描述</span><span class="sxs-lookup"><span data-stu-id="2ae7c-152">Codec Description</span></span></td>
<td><span data-ttu-id="2ae7c-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="2ae7c-154">不定</span><span class="sxs-lookup"><span data-stu-id="2ae7c-154">Varies</span></span></td>
<td><span data-ttu-id="2ae7c-155">以 null 終止的 Unicode 字串，其中包含編解碼器的描述。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ae7c-156">編解碼器資訊長度</span><span class="sxs-lookup"><span data-stu-id="2ae7c-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="2ae7c-157"><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="2ae7c-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="2ae7c-158">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="2ae7c-158">4 bytes</span></span></td>
<td><span data-ttu-id="2ae7c-159">編解碼器資訊欄位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ae7c-160">編解碼器資訊</span><span class="sxs-lookup"><span data-stu-id="2ae7c-160">Codec Information</span></span></td>
<td><span data-ttu-id="2ae7c-161"><strong>BYTE</strong>[]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="2ae7c-162">不定</span><span class="sxs-lookup"><span data-stu-id="2ae7c-162">Varies</span></span></td>
<td><span data-ttu-id="2ae7c-163">編解碼器資料。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-163">Codec data.</span></span> <span data-ttu-id="2ae7c-164">這項資料的意義取決於編解碼器。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="2ae7c-165">一般而言，此資料會指出格式。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="2ae7c-166">屬性 blob 的配置與 ASF 標頭中編解碼器清單物件的版面配置不完全相符。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="2ae7c-167">特別是，字串長度會以位元組為單位提供，並包含 **Null** 結束字元的大小。</span><span class="sxs-lookup"><span data-stu-id="2ae7c-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ae7c-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ae7c-168">Requirements</span></span>



| <span data-ttu-id="2ae7c-169">需求</span><span class="sxs-lookup"><span data-stu-id="2ae7c-169">Requirement</span></span> | <span data-ttu-id="2ae7c-170">值</span><span class="sxs-lookup"><span data-stu-id="2ae7c-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae7c-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ae7c-171">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae7c-172">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ae7c-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ae7c-173">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae7c-174">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2ae7c-175">標頭</span><span class="sxs-lookup"><span data-stu-id="2ae7c-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae7c-176"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae7c-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae7c-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ae7c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae7c-178">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2ae7c-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ae7c-179">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="2ae7c-180">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="2ae7c-181">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2ae7c-182">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="2ae7c-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ae7c-183">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="2ae7c-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2ae7c-184">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="2ae7c-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




