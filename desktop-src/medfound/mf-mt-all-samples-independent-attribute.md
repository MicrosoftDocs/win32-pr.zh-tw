---
description: 指定每個範例是否與資料流程中的其他範例無關的媒體類型。
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: 'MF_MT_ALL_SAMPLES_INDEPENDENT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986822"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>MF \_ MT \_ 所有 \_ 範例 \_ 獨立屬性

指定每個範例是否與資料流程中的其他範例無關的媒體類型。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

如果這個屬性為 **FALSE**，則無法使用某些範例，而不需要參考資料流中的其他範例。 例如，如果影片格式包含 delta 框架，則此屬性應為 **FALSE**。

這個屬性會對應至 DirectShow [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構中的 **bTemporalCompression** 欄位。

針對所有未壓縮的媒體類型，將這個屬性設定為 **TRUE** 。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 
