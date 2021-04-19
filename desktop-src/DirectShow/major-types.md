---
description: 下表說明主要的媒體類型。
ms.assetid: 718a07f6-e2e4-4670-b9cf-982b53abffd2
title: '主要類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5722cbad713f2fb9ae876e58941bde44c2e110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000781"
---
# <a name="major-types"></a>主要類型

下表說明主要的媒體類型。



| GUID                                                                                                                                                                                                                                  | Description                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="MEDIATYPE_AnalogAudio"></span><span id="mediatype_analogaudio"></span><span id="MEDIATYPE_ANALOGAUDIO"></span><dl> <dt>**媒體 \_ AnalogAudio**</dt> </dl>         | 類比音訊。<br/>                                                                                  |
| <span id="MEDIATYPE_AnalogVideo"></span><span id="mediatype_analogvideo"></span><span id="MEDIATYPE_ANALOGVIDEO"></span><dl> <dt>**媒體 \_ AnalogVideo**</dt> </dl>         | 類比影片。<br/>                                                                                  |
| <span id="MEDIATYPE_Audio"></span><span id="mediatype_audio"></span><span id="MEDIATYPE_AUDIO"></span><dl> <dt>**媒體 \_ 媒體**</dt> </dl>                                 | 音訊。 請參閱 [音訊子類型](audio-subtypes.md)。<br/>                                               |
| <span id="MEDIATYPE_AUXLine21Data"></span><span id="mediatype_auxline21data"></span><span id="MEDIATYPE_AUXLINE21DATA"></span><dl> <dt>**媒體 \_ AUXLine21Data**</dt> </dl> | 第21行資料。 由隱藏式輔助字幕使用。 請參閱 [**第21行的媒體類型**](line-21-media-types.md)。<br/> |
| <span id="MEDIATYPE_File"></span><span id="mediatype_file"></span><span id="MEDIATYPE_FILE"></span><dl> <dt>**媒體 \_ 檔**</dt> </dl>                                     | 檔案  (淘汰) <br/>                                                                               |
| <span id="MEDIATYPE_Interleaved"></span><span id="mediatype_interleaved"></span><span id="MEDIATYPE_INTERLEAVED"></span><dl> <dt>**媒體的 \_ 交錯**</dt> </dl>         | 交錯音訊和影片。 用於數位視訊 (DV) 。<br/>                                      |
| <span id="MEDIATYPE_LMRT"></span><span id="mediatype_lmrt"></span><dl> <dt>**媒體 \_ LMRT**</dt> </dl>                                                                      | 已過時。 請勿使用。<br/>                                                                          |
| <span id="MEDIATYPE_Midi"></span><span id="mediatype_midi"></span><span id="MEDIATYPE_MIDI"></span><dl> <dt>**媒體 \_ 媒體**</dt> </dl>                                     | MIDI 格式。<br/>                                                                                   |
| <span id="MEDIATYPE_MPEG2_PES"></span><span id="mediatype_mpeg2_pes"></span><dl> <dt>**媒體媒體的 \_ MPEG2 \_ pe**</dt> </dl>                                                      | MPEG-2 PE 封包。 請參閱 [Mpeg-2 媒體類型](mpeg-2-media-types.md)。<br/>                          |
| <span id="MEDIATYPE_MPEG2_SECTIONS"></span><span id="mediatype_mpeg2_sections"></span><dl> <dt>**媒體的 \_ MPEG2 \_ 區段**</dt> </dl>                                       | MPEG-2 區段資料。 請參閱 [Mpeg-2 媒體類型](mpeg-2-media-types.md)。<br/>                         |
| <span id="MEDIATYPE_ScriptCommand"></span><span id="mediatype_scriptcommand"></span><span id="MEDIATYPE_SCRIPTCOMMAND"></span><dl> <dt>**媒體 \_ ScriptCommand**</dt> </dl> | 資料是由隱藏式輔助字幕使用的指令碼命令。<br/>                                             |
| <span id="MEDIATYPE_Stream"></span><span id="mediatype_stream"></span><span id="MEDIATYPE_STREAM"></span><dl> <dt>**媒體媒體的 \_ 串流**</dt> </dl>                             | 沒有時間戳記的位元組資料流程。 請參閱 [**資料流程子類型**](stream-subtypes.md)。<br/>               |
| <span id="MEDIATYPE_Text"></span><span id="mediatype_text"></span><span id="MEDIATYPE_TEXT"></span><dl> <dt>**媒體 \_ 文字**</dt> </dl>                                     | Text。<br/>                                                                                          |
| <span id="MEDIATYPE_Timecode"></span><span id="mediatype_timecode"></span><span id="MEDIATYPE_TIMECODE"></span><dl> <dt>**媒體時間 \_ 碼**</dt> </dl>                     | 時間碼資料。 注意： DirectShow 不提供任何支援此媒體類型的篩選。<br/>     |
| <span id="MEDIATYPE_URL_STREAM"></span><span id="mediatype_url_stream"></span><dl> <dt>**媒體 \_ URL \_ 資料流程**</dt> </dl>                                                   | 已過時。 請勿使用。<br/>                                                                          |
| <span id="MEDIATYPE_VBI"></span><span id="mediatype_vbi"></span><dl> <dt>**媒體 \_ VBI**</dt> </dl>                                                                         | 垂直空白間隔 (VBI 電視) 的) 資料 (。 與 KSDATAFORMAT \_ 類型 \_ VBI 相同。<br/>       |
| <span id="MEDIATYPE_Video"></span><span id="mediatype_video"></span><span id="MEDIATYPE_VIDEO"></span><dl> <dt>**媒體 \_ 媒體**</dt> </dl>                                 | 影片。 請參閱 [影片子類型](video-subtypes.md)。<br/>                                               |



## <a name="remarks"></a>備註

子類型 GUID 會進一步定義格式。 針對某些格式，子類型 GUID 可能是 MEDIASUBTYPE \_ 無，這表示格式不需要子類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 




