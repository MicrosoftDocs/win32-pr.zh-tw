---
description: MP3 檔案來源會剖析 MP3 檔案。
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: MP3 檔案來源
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114381"
---
# <a name="mp3-file-source"></a><span data-ttu-id="97ad0-103">MP3 檔案來源</span><span class="sxs-lookup"><span data-stu-id="97ad0-103">MP3 File Source</span></span>

<span data-ttu-id="97ad0-104">MP3 檔案來源會剖析 MP3 檔案。</span><span class="sxs-lookup"><span data-stu-id="97ad0-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="97ad0-105">MP3 檔案來源會輸出包含 MPEG-2 音訊框架的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="97ad0-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="97ad0-106">它不會解碼音訊。</span><span class="sxs-lookup"><span data-stu-id="97ad0-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="97ad0-107">副檔名和 MIME 類型</span><span class="sxs-lookup"><span data-stu-id="97ad0-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="97ad0-108">MP3 檔案來源是下列副檔名的預設媒體來源：</span><span class="sxs-lookup"><span data-stu-id="97ad0-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="97ad0-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="97ad0-109">.mp3</span></span>

<span data-ttu-id="97ad0-110">它也是下列 MIME 類型的預設媒體來源。</span><span class="sxs-lookup"><span data-stu-id="97ad0-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="97ad0-111">音訊/mpeg</span><span class="sxs-lookup"><span data-stu-id="97ad0-111">audio/mpeg</span></span>
-   <span data-ttu-id="97ad0-112">音訊/x-mp3</span><span class="sxs-lookup"><span data-stu-id="97ad0-112">audio/x-mp3</span></span>
-   <span data-ttu-id="97ad0-113">音訊/x-mpeg</span><span class="sxs-lookup"><span data-stu-id="97ad0-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="97ad0-114">媒體類型</span><span class="sxs-lookup"><span data-stu-id="97ad0-114">Media Types</span></span>

<span data-ttu-id="97ad0-115">MP3 檔案來源所提供的媒體類型包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="97ad0-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="97ad0-116">屬性</span><span class="sxs-lookup"><span data-stu-id="97ad0-116">Attribute</span></span>                                                                                    | <span data-ttu-id="97ad0-117">描述</span><span class="sxs-lookup"><span data-stu-id="97ad0-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97ad0-118">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="97ad0-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="97ad0-119">等於 **MFMediaType \_ 音訊**。</span><span class="sxs-lookup"><span data-stu-id="97ad0-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="97ad0-120">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="97ad0-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="97ad0-121">等於 **MFAudioFormat \_ MP3** 或 **MFAudioFormat \_ MPEG**。</span><span class="sxs-lookup"><span data-stu-id="97ad0-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="97ad0-122">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97ad0-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="97ad0-123">每秒的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="97ad0-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="97ad0-124">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="97ad0-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="97ad0-125">等於1。</span><span class="sxs-lookup"><span data-stu-id="97ad0-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="97ad0-126">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="97ad0-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="97ad0-127">音訊聲道數目。</span><span class="sxs-lookup"><span data-stu-id="97ad0-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="97ad0-128">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97ad0-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="97ad0-129">每秒音訊樣本數。</span><span class="sxs-lookup"><span data-stu-id="97ad0-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="97ad0-130">**MF \_ MT \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="97ad0-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="97ad0-131">包含在結構的 **wfx** 成員後面出現的 [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat)結構部分。</span><span class="sxs-lookup"><span data-stu-id="97ad0-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="97ad0-132">介面</span><span class="sxs-lookup"><span data-stu-id="97ad0-132">Interfaces</span></span>

<span data-ttu-id="97ad0-133">MP3 檔案來源會透過 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="97ad0-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="97ad0-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="97ad0-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="97ad0-135">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="97ad0-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="97ad0-136">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="97ad0-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="97ad0-137">此外，它會透過 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="97ad0-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97ad0-138">服務 GUID</span><span class="sxs-lookup"><span data-stu-id="97ad0-138">Service GUID</span></span></th>
<th><span data-ttu-id="97ad0-139">介面</span><span class="sxs-lookup"><span data-stu-id="97ad0-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97ad0-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="97ad0-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="97ad0-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="97ad0-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97ad0-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="97ad0-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="97ad0-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="97ad0-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="97ad0-144">請參閱 <a href="shell-metadata-providers.md">Shell 中繼資料提供者</a>。</span><span class="sxs-lookup"><span data-stu-id="97ad0-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97ad0-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="97ad0-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="97ad0-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="97ad0-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97ad0-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="97ad0-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="97ad0-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="97ad0-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="97ad0-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="97ad0-149">Requirements</span></span>



| <span data-ttu-id="97ad0-150">需求</span><span class="sxs-lookup"><span data-stu-id="97ad0-150">Requirement</span></span> | <span data-ttu-id="97ad0-151">值</span><span class="sxs-lookup"><span data-stu-id="97ad0-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97ad0-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97ad0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="97ad0-153">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ad0-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97ad0-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97ad0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="97ad0-155">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ad0-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="97ad0-156">DLL</span><span class="sxs-lookup"><span data-stu-id="97ad0-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97ad0-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97ad0-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ad0-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97ad0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ad0-159">媒體來源和接收</span><span class="sxs-lookup"><span data-stu-id="97ad0-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="97ad0-160">媒體來源</span><span class="sxs-lookup"><span data-stu-id="97ad0-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="97ad0-161">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="97ad0-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="97ad0-162">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="97ad0-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
