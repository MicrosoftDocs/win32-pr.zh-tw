---
description: 指定捕捉引擎是否要捕獲影片，而非音訊。
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: 'MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973967"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 使用 \_ \_ \_ 僅限影片裝置屬性

指定捕捉引擎是否要捕獲影片，而非音訊。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則表示捕獲引擎不會選取或使用音訊捕獲裝置。 如果您想要在沒有音訊的情況下捕獲影片，請將此屬性設定為 **TRUE** 。 預設值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




