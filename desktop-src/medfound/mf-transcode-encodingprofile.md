---
description: 指定用於編碼 Advanced 串流格式 (ASF) 檔案的裝置一致性設定檔。
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: 'MF_TRANSCODE_ENCODINGPROFILE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b44a923abc563a84f3536fd6353ac2a3dd2352e472344edf7053d647674908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244229"
---
# <a name="mf_transcode_encodingprofile-attribute"></a>MF \_ 轉碼 \_ ENCODINGPROFILE 屬性

指定用於編碼 Advanced 串流格式 (ASF) 檔案的裝置一致性設定檔。

## <a name="data-type"></a>資料類型

**LPWSTR**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

當轉碼至支援 Windows 媒體的裝置時，請使用此屬性。 如果設定此屬性，則編碼器會使用 Windows 媒體編解碼器的裝置一致性設定檔或範本。 建立轉碼拓撲之前，請先在轉碼設定檔上設定屬性。

這個屬性的值可以是下列主題中所列的任何一個一致性範本字串：

-   [音訊裝置一致性範本](../wmformat/audio-device-conformance-templates.md)
-   [影片裝置一致性範本](../wmformat/video-device-conformance-templates.md)

針對 Windows Media 視訊編碼，拓撲產生器會使用此屬性來設定編碼器上的 [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md)屬性。 編碼器將嘗試使用指定的範本將內容編碼。 若要取得實際的範本，請遍歷轉碼拓撲的節點以取得編碼器節點的指標。 然後從編碼器取得 [**MFPKEY \_ DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) 屬性的值。

拓撲產生器也會使用此屬性的值來設定 ASF 媒體接收器上的 "DeviceConformanceTemplate" 屬性。

如果設定此屬性，則不論 [MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸](mf-transcode-skip-metadata-transfer.md) 屬性的應用程式指定值，一律會產生 ASF 檔案的中繼資料物件。

這個屬性的一般值包括下列各項：



| 值   | 描述                      |
|---------|----------------------------------|
| AP    | Advanced profile 影片           |
| 多功能    | 主要設定檔影片               |
| SP-1    | 簡單的個人資料影片             |
| "MP@LL" | 主要設定檔，中等級影片 |
| L2    | 音訊設定檔，<= 160 Kbps    |



 

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉碼 API](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[**IMFTranscodeProfile::GetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
