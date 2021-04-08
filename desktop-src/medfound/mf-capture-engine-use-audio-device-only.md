---
description: 指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: 'MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943546"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 使用 \_ \_ \_ 僅限音訊裝置屬性

指定捕捉引擎是否會捕捉音訊，但不會捕捉影片。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則表示捕獲引擎不會選取或使用影片捕獲裝置。 如果您想要在沒有影片的情況下捕獲音訊，請將此屬性設定為 **TRUE** 。 預設值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




