---
description: 指定用於編碼 Advanced 串流格式 (ASF) 檔案的裝置一致性設定檔。
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: 'MF_TRANSCODE_ENCODINGPROFILE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512265"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="ff5cc-103">MF \_ 轉碼 \_ ENCODINGPROFILE 屬性</span><span class="sxs-lookup"><span data-stu-id="ff5cc-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="ff5cc-104">指定用於編碼 Advanced 串流格式 (ASF) 檔案的裝置一致性設定檔。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="ff5cc-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ff5cc-105">Data type</span></span>

<span data-ttu-id="ff5cc-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ff5cc-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="ff5cc-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="ff5cc-107">Get/set</span></span>

<span data-ttu-id="ff5cc-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring)。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="ff5cc-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff5cc-110">備註</span><span class="sxs-lookup"><span data-stu-id="ff5cc-110">Remarks</span></span>

<span data-ttu-id="ff5cc-111">當轉碼至支援 Windows Media 的裝置時，請使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="ff5cc-112">如果設定此屬性，則編碼器會使用 Windows Media 編解碼器的裝置一致性設定檔或範本。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="ff5cc-113">建立轉碼拓撲之前，請先在轉碼設定檔上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="ff5cc-114">這個屬性的值可以是下列主題中所列的任何一個一致性範本字串：</span><span class="sxs-lookup"><span data-stu-id="ff5cc-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="ff5cc-115">音訊裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="ff5cc-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="ff5cc-116">影片裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="ff5cc-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="ff5cc-117">針對 Windows Media 視訊編碼，拓撲產生器會使用此屬性來設定編碼器上的 [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="ff5cc-118">編碼器將嘗試使用指定的範本將內容編碼。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="ff5cc-119">若要取得實際的範本，請遍歷轉碼拓撲的節點以取得編碼器節點的指標。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="ff5cc-120">然後從編碼器取得 [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="ff5cc-121">拓撲產生器也會使用此屬性的值來設定 ASF 媒體接收器上的 "DeviceConformanceTemplate" 屬性。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="ff5cc-122">如果設定此屬性，則不論 [MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸](mf-transcode-skip-metadata-transfer.md) 屬性的應用程式指定值，一律會產生 ASF 檔案的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="ff5cc-123">這個屬性的一般值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="ff5cc-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="ff5cc-124">值</span><span class="sxs-lookup"><span data-stu-id="ff5cc-124">Value</span></span>   | <span data-ttu-id="ff5cc-125">描述</span><span class="sxs-lookup"><span data-stu-id="ff5cc-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="ff5cc-126">AP</span><span class="sxs-lookup"><span data-stu-id="ff5cc-126">"AP"</span></span>    | <span data-ttu-id="ff5cc-127">Advanced profile 影片</span><span class="sxs-lookup"><span data-stu-id="ff5cc-127">Advanced profile video</span></span>           |
| <span data-ttu-id="ff5cc-128">多功能</span><span class="sxs-lookup"><span data-stu-id="ff5cc-128">"MP"</span></span>    | <span data-ttu-id="ff5cc-129">主要設定檔影片</span><span class="sxs-lookup"><span data-stu-id="ff5cc-129">Main profile video</span></span>               |
| <span data-ttu-id="ff5cc-130">SP-1</span><span class="sxs-lookup"><span data-stu-id="ff5cc-130">"SP"</span></span>    | <span data-ttu-id="ff5cc-131">簡單的個人資料影片</span><span class="sxs-lookup"><span data-stu-id="ff5cc-131">Simple profile video</span></span>             |
| <span data-ttu-id="ff5cc-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="ff5cc-132">"MP@LL"</span></span> | <span data-ttu-id="ff5cc-133">主要設定檔，中等級影片</span><span class="sxs-lookup"><span data-stu-id="ff5cc-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="ff5cc-134">L2</span><span class="sxs-lookup"><span data-stu-id="ff5cc-134">"L2"</span></span>    | <span data-ttu-id="ff5cc-135">音訊設定檔，<= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="ff5cc-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="ff5cc-136">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ff5cc-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5cc-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff5cc-137">Requirements</span></span>



| <span data-ttu-id="ff5cc-138">需求</span><span class="sxs-lookup"><span data-stu-id="ff5cc-138">Requirement</span></span> | <span data-ttu-id="ff5cc-139">值</span><span class="sxs-lookup"><span data-stu-id="ff5cc-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5cc-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff5cc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ff5cc-141">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff5cc-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff5cc-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff5cc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ff5cc-143">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff5cc-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ff5cc-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ff5cc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff5cc-145"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5cc-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5cc-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff5cc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5cc-147">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ff5cc-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ff5cc-148">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="ff5cc-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="ff5cc-149">**IMFTranscodeProfile::GetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="ff5cc-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="ff5cc-150">**IMFTranscodeProfile::SetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="ff5cc-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="ff5cc-151">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="ff5cc-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="ff5cc-152">**IMFTranscodeProfile::GetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="ff5cc-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
