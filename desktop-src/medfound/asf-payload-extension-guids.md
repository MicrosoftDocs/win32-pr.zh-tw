---
description: 下列 Guid 會定義 Advanced 系統格式 (ASF) 資料流程的承載延伸模組。
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: 'ASF 承載延伸模組 Guid (Wmcontainer .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6478c024d3e79b0f8035f03b6e893e2e5d0308037242f9ac3013450b57f83242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959568"
---
# <a name="asf-payload-extension-guids"></a>ASF 承載延伸模組 Guid

下列 Guid 會定義 Advanced 系統格式 (ASF) 資料流程的承載延伸模組。



| 常數                                                                                                                                                                                                                                                                                      | 描述                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <dt>**MFASFSampleExtension \_ SampleDuration**</dt> </dl>         | 資料表示緩衝區物件中所含樣本的持續時間（以毫秒為單位）。<br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <dt>**MFASFSampleExtension \_ OutputCleanPoint**</dt> </dl> | 資料會指出此範例是否為主要畫面格。 值為零表示此範例不是主要畫面格。 非零值表示它是主要畫面格。<br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <dt>**MFASFSampleExtension \_ SMPTE**</dt> </dl>                                             | 資料是 SMPTE 時間代碼。<br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <dt>**MFASFSampleExtension \_ 檔案名**</dt> </dl>                                 | 範例延伸模組中的資料會指定從中取得範例內容的檔案名。<br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <dt>**MFASFSampleExtension \_ ContentType**</dt> </dl>                     | 資料會識別此範例所包含的內容類型。<br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <dt>**MFASFSampleExtension \_ PixelAspectRatio**</dt> </dl> | 資料會指出範例中內容的圖元外觀比例。<br/>                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFASFStreamConfig::AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[**IMFASFStreamConfig::GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> </dl>

 

 




