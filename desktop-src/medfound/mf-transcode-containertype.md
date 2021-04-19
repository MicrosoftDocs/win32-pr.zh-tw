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
# <a name="mf_transcode_containertype-attribute"></a>MF \_ 轉碼 \_ CONTAINERTYPE 屬性

指定編碼檔案的容器類型。 媒體基礎支援容器類型。

## <a name="data-type"></a>資料類型

**GUID**

下表說明媒體基礎所提供之容器類型的可能值。



| 值                                                                                                                                                                                                                                                                 | 意義                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <dt>**MFTranscodeContainerType \_ ASF**</dt> </dl>             | ASF 檔案容器。<br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG4**</dt> </dl>     | 檔容器。<br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <dt>**MFTranscodeContainerType \_ MP3**</dt> </dl>             | MP3 檔案容器。<br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <dt>**MFTranscodeContainerType \_ 3GP**</dt> </dl>             | 3GP 檔案容器。 <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <dt>**MFTranscodeContainerType \_ AC3**</dt> </dl>             | AC3 檔案容器。 <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <dt>**MFTranscodeContainerType \_ ADTS**</dt> </dl>         | ADTS 檔案容器。 <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <dt>**MFTranscodeContainerType \_ MPEG2**</dt> </dl>     | MPEG2 檔案容器。 <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <dt>**MFTranscodeContainerType \_ FMPEG4**</dt> </dl> | FMPEG4 檔案容器。 <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <dt>**MFTranscodeContainerType \_ WAVE**</dt> </dl>         | WAVE 檔案容器。<br/> 在 Windows 8.1 和更新版本中支援。<br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <dt>**MFTranscodeContainerType \_ AVI**</dt> </dl>             | AVI 檔案容器。<br/> 在 Windows 8.1 和更新版本中支援。<br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <dt>**MFTranscodeContainerType \_ AMR**</dt> </dl>             | AMR 檔案容器。 <br/>                                                    |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。

## <a name="remarks"></a>備註

這個屬性會搭配 Fast 轉碼功能和接收寫入器物件一起使用。

這個屬性的 GUID 常數是從 mfuuid 匯出。

### <a name="fast-transcode"></a>快速轉碼

應用程式必須先設定轉碼設定檔上的容器屬性，才能建立轉碼拓撲。 拓撲產生器會分析此屬性，並在管線中載入適當的媒體接收。 如需詳細資訊，請參閱下列主題：

-   [**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a>接收寫入器

這個屬性可以用來設定接收寫入器的檔案容器型別。 如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉碼 API](transcode-api.md)
</dt> </dl>

 

 




