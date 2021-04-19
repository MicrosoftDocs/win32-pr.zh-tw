---
description: 媒體類型常數定義如下。
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: 'TAPIMEDIATYPE_ 常數 (Tapi3) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991171"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="cf362-103">TAPIMEDIATYPE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="cf362-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="cf362-104">以下是定義的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="cf362-104">The following media types are defined:</span></span>



| <span data-ttu-id="cf362-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="cf362-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="cf362-106">Description</span><span class="sxs-lookup"><span data-stu-id="cf362-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="cf362-107"><dt>**TAPIMEDIATYPE \_音訊**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="cf362-108">進入或離開電腦的音訊媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="cf362-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="cf362-109">進入媒體資料流程通常會在喇叭上播放，或傳送到話筒裝置，而離開的串流通常會透過麥克風或話筒裝置來捕捉。</span><span class="sxs-lookup"><span data-stu-id="cf362-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="cf362-110"><dt>**TAPIMEDIATYPE \_VIDEO**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="cf362-111">進入或離開電腦的影片媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="cf362-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="cf362-112">進入媒體資料流程通常會在影片視窗中轉譯，而離開媒體資料流程通常會使用攝影機來捕捉。</span><span class="sxs-lookup"><span data-stu-id="cf362-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="cf362-113"><dt>**TAPIMEDIATYPE \_DATAMODEM**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="cf362-114">與資料數據機相關聯的資料媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="cf362-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="cf362-115"><dt>**TAPIMEDIATYPE \_G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="cf362-116">與 G3 通訊協定傳真相關聯的資料媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="cf362-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="cf362-117"><dt>**TAPIMEDIATYPE \_MULTITRACK**</dt> <dt>0x10000</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="cf362-118">資料流程位於 multitrack 終端機上。</span><span class="sxs-lookup"><span data-stu-id="cf362-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="cf362-119"><dt>**媒體媒體 \_ RTP \_ 單一 \_ 資料流程**</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="cf362-120">此 GUID 會在應用程式提供的終端機和 MSP 的串流之間使用。</span><span class="sxs-lookup"><span data-stu-id="cf362-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="cf362-121">如果終端機的 pin 支援此媒體類型，則串流會與終端機交換原始的 RTP 資料。</span><span class="sxs-lookup"><span data-stu-id="cf362-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="cf362-122">只有 H323 MSP 和 IPConf MSP （適用于 Windows 2000 SP1 或更新版本）的影片串流才支援此模式。</span><span class="sxs-lookup"><span data-stu-id="cf362-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="cf362-123">**標頭：** 在 ipmsp 中宣告。</span><span class="sxs-lookup"><span data-stu-id="cf362-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="cf362-124">在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用標頭 ipmsp。</span><span class="sxs-lookup"><span data-stu-id="cf362-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cf362-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf362-125">Requirements</span></span>



| <span data-ttu-id="cf362-126">需求</span><span class="sxs-lookup"><span data-stu-id="cf362-126">Requirement</span></span> | <span data-ttu-id="cf362-127">值</span><span class="sxs-lookup"><span data-stu-id="cf362-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf362-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cf362-128">TAPI version</span></span><br/> | <span data-ttu-id="cf362-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cf362-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="cf362-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cf362-130">Header</span></span><br/>       | <dl> <span data-ttu-id="cf362-131"><dt>Tapi3。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf362-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf362-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf362-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf362-133">**ITQOSEvent：：取得 \_ 媒體媒體**</span><span class="sxs-lookup"><span data-stu-id="cf362-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="cf362-134">**ITAMMediaFormat：： get \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="cf362-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="cf362-135">**ITAMMediaFormat：:p 的 \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="cf362-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="cf362-136">**ITCallInfo：： get \_ CallInfoLong**</span><span class="sxs-lookup"><span data-stu-id="cf362-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="cf362-137">**ITMediaSupport：： get \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="cf362-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="cf362-138">**ITTerminalSupport::CreateTerminal**</span><span class="sxs-lookup"><span data-stu-id="cf362-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

