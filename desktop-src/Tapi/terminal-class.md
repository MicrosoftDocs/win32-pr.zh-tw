---
description: 終端機類別 Guid 會依功能識別特定的終端機。
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: 'Terminal 類別 (Tapi3if .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d67d7668f9e4e16ad357408c8e9087fce870a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983171"
---
# <a name="terminal-class"></a>Terminal 類別

終端機類別 Guid 會依功能識別特定的終端機。

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**CLSID \_ FilePlaybackTerminal**
</dt> <dd> <dl> <dt>



檔案播放終端機。


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**CLSID \_ FileRecordingTerminal**
</dt> <dd> <dl> <dt>



檔案記錄終端機。


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**CLSID \_ FileRecordingTrack**
</dt> <dd> <dl> <dt>



檔案錄製播放軌。


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**CLSID \_ HandsetTerminal**
</dt> <dd> <dl> <dt>



電話聽筒。


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID \_ HeadsetTerminal**
</dt> <dd> <dl> <dt>



前端集。


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



媒體資料流程終端機，以動態方式建立。


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID \_ MicrophoneTerminal**
</dt> <dd> <dl> <dt>



麥克風。


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



喇叭電話。


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**CLSID \_ SpeakersTerminal**
</dt> <dd> <dl> <dt>



揚聲器。


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



影片輸入終端機。


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ VideoWindowTerm**
</dt> <dd> <dl> <dt>



以動態方式建立的影片顯示視窗。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

終端機類別的 **BSTR** 版本主要是針對使用 Visual Basic 應用程式而指定。 例如， (會以 [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)取得的集合元素傳回。 ) 

-   BSTR CLSID \_ 字串 \_ HandsetTerminal
-   BSTR CLSID \_ 字串 \_ HeadsetTerminal
-   BSTR CLSID \_ 字串 \_ MediaStreamTerminal
-   BSTR CLSID \_ 字串 \_ MicrophoneTerminal
-   BSTR CLSID \_ 字串 \_ SpeakerphoneTerminal
-   BSTR CLSID \_ 字串 \_ SpeakersTerminal
-   BSTR CLSID \_ 字串 \_ VideoInputTerminal
-   BSTR CLSID \_ 字串 \_ VideoWindowTerm

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                |
| 標頭<br/>       | <dl> <dt>Tapi3if。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal：： get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

