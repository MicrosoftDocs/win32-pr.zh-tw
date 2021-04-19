---
description: 包含目前簡報中使用的 RFC 1766 語言清單。
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: 'MF_PD_ASF_LANGLIST_LEGACYORDER 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980398"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="634a6-103">MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER 屬性</span><span class="sxs-lookup"><span data-stu-id="634a6-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="634a6-104">包含目前簡報中使用的 RFC 1766 語言清單。</span><span class="sxs-lookup"><span data-stu-id="634a6-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="634a6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="634a6-105">Data type</span></span>

<span data-ttu-id="634a6-106">**位元組 \[\]**</span><span class="sxs-lookup"><span data-stu-id="634a6-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="634a6-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="634a6-107">Get/set</span></span>

<span data-ttu-id="634a6-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="634a6-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="634a6-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="634a6-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="634a6-110">適用於</span><span class="sxs-lookup"><span data-stu-id="634a6-110">Applies to</span></span>

[<span data-ttu-id="634a6-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="634a6-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="634a6-112">備註</span><span class="sxs-lookup"><span data-stu-id="634a6-112">Remarks</span></span>

<span data-ttu-id="634a6-113">這個屬性會套用至透過呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)從 [ASF ContentInfo 物件](asf-contentinfo-object.md)產生的呈現描述項。</span><span class="sxs-lookup"><span data-stu-id="634a6-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="634a6-114">位元組陣列的格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="634a6-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="634a6-115">語言清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="634a6-115">Language List Object field</span></span> | <span data-ttu-id="634a6-116">資料類型</span><span class="sxs-lookup"><span data-stu-id="634a6-116">Data type</span></span>    | <span data-ttu-id="634a6-117">大小</span><span class="sxs-lookup"><span data-stu-id="634a6-117">Size</span></span>    | <span data-ttu-id="634a6-118">Description</span><span class="sxs-lookup"><span data-stu-id="634a6-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="634a6-119">語言識別項記錄計數</span><span class="sxs-lookup"><span data-stu-id="634a6-119">Language ID Records Count</span></span>  | <span data-ttu-id="634a6-120">**Dword**</span><span class="sxs-lookup"><span data-stu-id="634a6-120">**DWORD**</span></span>    | <span data-ttu-id="634a6-121">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="634a6-121">4 bytes</span></span> | <span data-ttu-id="634a6-122">語言數目</span><span class="sxs-lookup"><span data-stu-id="634a6-122">Number of languages</span></span>                    |
| <span data-ttu-id="634a6-123">語言識別項記錄</span><span class="sxs-lookup"><span data-stu-id="634a6-123">Language ID Records</span></span>        | <span data-ttu-id="634a6-124">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="634a6-124">**BYTE**\[\]</span></span> | <span data-ttu-id="634a6-125">不定</span><span class="sxs-lookup"><span data-stu-id="634a6-125">Varies</span></span>  | <span data-ttu-id="634a6-126">語言字串的陣列 (請參閱下面的) 。</span><span class="sxs-lookup"><span data-stu-id="634a6-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="634a6-127">第一個 **DWORD** 是語言的數目，後面接著語言識別項字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="634a6-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="634a6-128">每個字串的格式如下：</span><span class="sxs-lookup"><span data-stu-id="634a6-128">Each string has the following format:</span></span>



| <span data-ttu-id="634a6-129">語言清單物件欄位</span><span class="sxs-lookup"><span data-stu-id="634a6-129">Language List Object field</span></span> | <span data-ttu-id="634a6-130">資料類型</span><span class="sxs-lookup"><span data-stu-id="634a6-130">Data type</span></span>     | <span data-ttu-id="634a6-131">大小</span><span class="sxs-lookup"><span data-stu-id="634a6-131">Size</span></span>    | <span data-ttu-id="634a6-132">Description</span><span class="sxs-lookup"><span data-stu-id="634a6-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="634a6-133">語言識別項長度</span><span class="sxs-lookup"><span data-stu-id="634a6-133">Language ID Length</span></span>         | <span data-ttu-id="634a6-134">**Dword**</span><span class="sxs-lookup"><span data-stu-id="634a6-134">**DWORD**</span></span>     | <span data-ttu-id="634a6-135">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="634a6-135">4 bytes</span></span> | <span data-ttu-id="634a6-136">字串的長度（以位元組為單位），包括尾端 **Null** 字元的大小。</span><span class="sxs-lookup"><span data-stu-id="634a6-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="634a6-137">語言識別碼</span><span class="sxs-lookup"><span data-stu-id="634a6-137">Language ID</span></span>                | <span data-ttu-id="634a6-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="634a6-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="634a6-139">不定</span><span class="sxs-lookup"><span data-stu-id="634a6-139">Varies</span></span>  | <span data-ttu-id="634a6-140">以 null 終止的字串，包含 RFC 1766 語言名稱。</span><span class="sxs-lookup"><span data-stu-id="634a6-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="634a6-141">每個字串都是符合 RFC 1766 的語言標記。</span><span class="sxs-lookup"><span data-stu-id="634a6-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="634a6-142">使用這個屬性的目的，只是為了與 Windows Media 格式 SDK 中 [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) 介面的列舉順序進行回溯相容。</span><span class="sxs-lookup"><span data-stu-id="634a6-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="634a6-143">語言字串會以不同的順序儲存在 [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="634a6-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="634a6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="634a6-144">Requirements</span></span>



| <span data-ttu-id="634a6-145">需求</span><span class="sxs-lookup"><span data-stu-id="634a6-145">Requirement</span></span> | <span data-ttu-id="634a6-146">值</span><span class="sxs-lookup"><span data-stu-id="634a6-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="634a6-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="634a6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="634a6-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="634a6-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="634a6-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="634a6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="634a6-150">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="634a6-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="634a6-151">標頭</span><span class="sxs-lookup"><span data-stu-id="634a6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="634a6-152"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="634a6-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="634a6-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="634a6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="634a6-154">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="634a6-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="634a6-155">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="634a6-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
