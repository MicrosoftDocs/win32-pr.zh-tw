---
description: 指定 Advanced 系統格式的標記 (ASF) 檔。 這個屬性會對應至 ASF 標頭中定義于 ASF 規格中的標記物件。
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: 'MF_PD_ASF_MARKER 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985350"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="75389-104">MF \_ PD \_ ASF \_ 標記屬性</span><span class="sxs-lookup"><span data-stu-id="75389-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="75389-105">指定 Advanced 系統格式的標記 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="75389-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="75389-106">這個屬性會對應至 ASF 標頭中定義于 ASF 規格中的標記物件。</span><span class="sxs-lookup"><span data-stu-id="75389-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="75389-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="75389-107">Data type</span></span>

<span data-ttu-id="75389-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="75389-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="75389-109">備註</span><span class="sxs-lookup"><span data-stu-id="75389-109">Remarks</span></span>

<span data-ttu-id="75389-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="75389-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="75389-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從標記物件產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="75389-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="75389-112">下表顯示 blob 的格式：</span><span class="sxs-lookup"><span data-stu-id="75389-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="75389-113">標記物件欄位</span><span class="sxs-lookup"><span data-stu-id="75389-113">Marker Object field</span></span> | <span data-ttu-id="75389-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="75389-114">Data type</span></span>    | <span data-ttu-id="75389-115">大小</span><span class="sxs-lookup"><span data-stu-id="75389-115">Size</span></span>    | <span data-ttu-id="75389-116">Description</span><span class="sxs-lookup"><span data-stu-id="75389-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="75389-117">標記計數</span><span class="sxs-lookup"><span data-stu-id="75389-117">Markers Count</span></span>       | <span data-ttu-id="75389-118">**Dword**</span><span class="sxs-lookup"><span data-stu-id="75389-118">**DWORD**</span></span>    | <span data-ttu-id="75389-119">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="75389-119">4 bytes</span></span> | <span data-ttu-id="75389-120">標記數目</span><span class="sxs-lookup"><span data-stu-id="75389-120">Number of markers</span></span> |
| <span data-ttu-id="75389-121">標記</span><span class="sxs-lookup"><span data-stu-id="75389-121">Markers</span></span>             | <span data-ttu-id="75389-122">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="75389-122">**BYTE**\[\]</span></span> | <span data-ttu-id="75389-123">不定</span><span class="sxs-lookup"><span data-stu-id="75389-123">Varies</span></span>  | <span data-ttu-id="75389-124">標記的陣列</span><span class="sxs-lookup"><span data-stu-id="75389-124">Array of markers</span></span>  |



 

<span data-ttu-id="75389-125">第一個 **DWORD** 是標記的數目，後面接著標記的陣列。</span><span class="sxs-lookup"><span data-stu-id="75389-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="75389-126">每個標記都具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="75389-126">Each marker has the following format:</span></span>



| <span data-ttu-id="75389-127">標記物件欄位</span><span class="sxs-lookup"><span data-stu-id="75389-127">Marker Object field</span></span>       | <span data-ttu-id="75389-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="75389-128">Data type</span></span>     | <span data-ttu-id="75389-129">大小</span><span class="sxs-lookup"><span data-stu-id="75389-129">Size</span></span>    | <span data-ttu-id="75389-130">Description</span><span class="sxs-lookup"><span data-stu-id="75389-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="75389-131">標記描述長度</span><span class="sxs-lookup"><span data-stu-id="75389-131">Marker Description Length</span></span> | <span data-ttu-id="75389-132">**Dword**</span><span class="sxs-lookup"><span data-stu-id="75389-132">**DWORD**</span></span>     | <span data-ttu-id="75389-133">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="75389-133">4 bytes</span></span> | <span data-ttu-id="75389-134">描述字串的大小（以位元組為單位），包括 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="75389-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="75389-135">標記描述</span><span class="sxs-lookup"><span data-stu-id="75389-135">Marker Description</span></span>        | <span data-ttu-id="75389-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="75389-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="75389-137">不定</span><span class="sxs-lookup"><span data-stu-id="75389-137">Varies</span></span>  | <span data-ttu-id="75389-138">描述標記的以 Null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="75389-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="75389-139">呈現時間</span><span class="sxs-lookup"><span data-stu-id="75389-139">Presentation Time</span></span>         | <span data-ttu-id="75389-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="75389-140">**LONGLONG**</span></span>  | <span data-ttu-id="75389-141">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="75389-141">8 bytes</span></span> | <span data-ttu-id="75389-142">標記的呈現時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="75389-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="75389-143">傳送時間</span><span class="sxs-lookup"><span data-stu-id="75389-143">Send Time</span></span>                 | <span data-ttu-id="75389-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="75389-144">**LONGLONG**</span></span>  | <span data-ttu-id="75389-145">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="75389-145">8 bytes</span></span> | <span data-ttu-id="75389-146">標記專案的傳送時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="75389-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="75389-147">Offset</span><span class="sxs-lookup"><span data-stu-id="75389-147">Offset</span></span>                    | <span data-ttu-id="75389-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="75389-148">**UINT64**</span></span>    | <span data-ttu-id="75389-149">8 個位元組</span><span class="sxs-lookup"><span data-stu-id="75389-149">8 bytes</span></span> | <span data-ttu-id="75389-150">資料物件中的位移（以位元組為單位），指定市場的位置。</span><span class="sxs-lookup"><span data-stu-id="75389-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="75389-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="75389-151">Requirements</span></span>



| <span data-ttu-id="75389-152">需求</span><span class="sxs-lookup"><span data-stu-id="75389-152">Requirement</span></span> | <span data-ttu-id="75389-153">值</span><span class="sxs-lookup"><span data-stu-id="75389-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75389-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75389-154">Minimum supported client</span></span><br/> | <span data-ttu-id="75389-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75389-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75389-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75389-156">Minimum supported server</span></span><br/> | <span data-ttu-id="75389-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75389-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="75389-158">標頭</span><span class="sxs-lookup"><span data-stu-id="75389-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="75389-159"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="75389-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75389-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75389-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75389-161">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="75389-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="75389-162">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="75389-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="75389-163">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="75389-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="75389-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="75389-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="75389-165">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="75389-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="75389-166">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="75389-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="75389-167">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="75389-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




