---
description: 指定 h.264 影片資料流程的速率控制模式。
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: 'MF_MT_H264_RATE_CONTROL_MODES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34fac6f047b8454ea6ddd79dfd26659fa7751fd1a6a14e01c7ea9457a5f7dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104434"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a>MF \_ MT \_ H264 \_ 速率 \_ 控制 \_ 模式屬性

指定 h.264 影片資料流程的速率控制模式。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。 值會對應至 UVC 1.2 h.264 探查/commit 控制項中的 **bmRateControlModes** 欄位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




