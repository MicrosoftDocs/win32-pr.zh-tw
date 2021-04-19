---
description: 指定編碼檔案的容器類型。
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: 'MF_TRANSCODE_CONTAINERTYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972688"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="8c0c7-103">MF \_ 轉碼 \_ CONTAINERTYPE 屬性</span><span class="sxs-lookup"><span data-stu-id="8c0c7-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="8c0c7-104">指定編碼檔案的容器類型。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="8c0c7-105">媒體基礎支援容器類型。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c0c7-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="8c0c7-106">Data type</span></span>

<span data-ttu-id="8c0c7-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8c0c7-107">**GUID**</span></span>

<span data-ttu-id="8c0c7-108">下表說明媒體基礎所提供之容器類型的可能值。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="8c0c7-109">值</span><span class="sxs-lookup"><span data-stu-id="8c0c7-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="8c0c7-110">意義</span><span class="sxs-lookup"><span data-stu-id="8c0c7-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="8c0c7-111"><dt>**MFTranscodeContainerType \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-112">ASF 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="8c0c7-113"><dt>**MFTranscodeContainerType \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="8c0c7-114">檔容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="8c0c7-115"><dt>**MFTranscodeContainerType \_ MP3**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-116">MP3 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="8c0c7-117"><dt>**MFTranscodeContainerType \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-118">3GP 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="8c0c7-119"><dt>**MFTranscodeContainerType \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-120">AC3 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="8c0c7-121"><dt>**MFTranscodeContainerType \_ ADTS**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="8c0c7-122">ADTS 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="8c0c7-123"><dt>**MFTranscodeContainerType \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="8c0c7-124">MPEG2 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="8c0c7-125"><dt>**MFTranscodeContainerType \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="8c0c7-126">FMPEG4 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="8c0c7-127"><dt>**MFTranscodeContainerType \_ WAVE**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="8c0c7-128">WAVE 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-128">WAVE file container.</span></span><br/> <span data-ttu-id="8c0c7-129">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="8c0c7-130"><dt>**MFTranscodeContainerType \_ AVI**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-131">AVI 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-131">AVI file container.</span></span><br/> <span data-ttu-id="8c0c7-132">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="8c0c7-133"><dt>**MFTranscodeContainerType \_ AMR**</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="8c0c7-134">AMR 檔案容器。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="8c0c7-135">取得/設定</span><span class="sxs-lookup"><span data-stu-id="8c0c7-135">Get/set</span></span>

<span data-ttu-id="8c0c7-136">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="8c0c7-137">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0c7-138">備註</span><span class="sxs-lookup"><span data-stu-id="8c0c7-138">Remarks</span></span>

<span data-ttu-id="8c0c7-139">這個屬性會搭配 Fast 轉碼功能和接收寫入器物件一起使用。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="8c0c7-140">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="8c0c7-141">快速轉碼</span><span class="sxs-lookup"><span data-stu-id="8c0c7-141">Fast Transcode</span></span>

<span data-ttu-id="8c0c7-142">應用程式必須先設定轉碼設定檔上的容器屬性，才能建立轉碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="8c0c7-143">拓撲產生器會分析此屬性，並在管線中載入適當的媒體接收。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="8c0c7-144">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="8c0c7-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8c0c7-145">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="8c0c7-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="8c0c7-146">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="8c0c7-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="8c0c7-147">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="8c0c7-147">Sink Writer</span></span>

<span data-ttu-id="8c0c7-148">這個屬性可以用來設定接收寫入器的檔案容器型別。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="8c0c7-149">如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c0c7-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0c7-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0c7-150">Requirements</span></span>



| <span data-ttu-id="8c0c7-151">需求</span><span class="sxs-lookup"><span data-stu-id="8c0c7-151">Requirement</span></span> | <span data-ttu-id="8c0c7-152">值</span><span class="sxs-lookup"><span data-stu-id="8c0c7-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0c7-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c0c7-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0c7-154">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0c7-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c0c7-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c0c7-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0c7-156">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0c7-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8c0c7-157">標頭</span><span class="sxs-lookup"><span data-stu-id="8c0c7-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0c7-158"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c7-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0c7-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c0c7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0c7-160">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8c0c7-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c0c7-161">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="8c0c7-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




