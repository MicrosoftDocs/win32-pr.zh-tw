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
# <a name="tapimediatype_-constants"></a>TAPIMEDIATYPE \_ 常數

以下是定義的媒體類型：



| 常數/值                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_音訊**</dt> <dt>0x8</dt> </dl>                    | 進入或離開電腦的音訊媒體資料流程。 進入媒體資料流程通常會在喇叭上播放，或傳送到話筒裝置，而離開的串流通常會透過麥克風或話筒裝置來捕捉。<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_VIDEO**</dt> <dt>0x8000</dt> </dl>                 | 進入或離開電腦的影片媒體資料流程。 進入媒體資料流程通常會在影片視窗中轉譯，而離開媒體資料流程通常會使用攝影機來捕捉。<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_DATAMODEM**</dt> <dt>0x10</dt> </dl>       | 與資料數據機相關聯的資料媒體資料流程。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_G3FAX**</dt> <dt>0x20</dt> </dl>                   | 與 G3 通訊協定傳真相關聯的資料媒體資料流程。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_MULTITRACK**</dt> <dt>0x10000</dt> </dl> | 資料流程位於 multitrack 終端機上。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**媒體媒體 \_ RTP \_ 單一 \_ 資料流程**</dt> </dl>     | 此 GUID 會在應用程式提供的終端機和 MSP 的串流之間使用。 如果終端機的 pin 支援此媒體類型，則串流會與終端機交換原始的 RTP 資料。 只有 H323 MSP 和 IPConf MSP （適用于 Windows 2000 SP1 或更新版本）的影片串流才支援此模式。<br/> **標頭：** 在 ipmsp 中宣告。 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用標頭 ipmsp。 <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                              |
| 標頭<br/>       | <dl> <dt>Tapi3。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITQOSEvent：：取得 \_ 媒體媒體**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat：： get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat：:p 的 \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport：： get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

