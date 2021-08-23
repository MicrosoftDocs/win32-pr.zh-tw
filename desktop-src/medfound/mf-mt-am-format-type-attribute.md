---
description: 包含媒體類型的 DirectShow 格式 GUID。
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: 'MF_MT_AM_FORMAT_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973627"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT \_ \_ 格式 \_ 類型屬性

包含媒體類型的 DirectShow 格式 GUID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

當 DirectShow 媒體類型轉換成媒體基礎媒體類型時，可能會設定此屬性。 屬性工作表示原始 DirectShow 格式類型。 值會對應至 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的 formattype 成員。

若是音訊格式，如果無法辨識 DirectShow 格式類型，則 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md)屬性可能會包含原始的格式區塊。

除非您要轉換 DirectShow 格式結構，否則請勿在媒體類型上設定此屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[媒體類型轉換](media-type-conversions.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
