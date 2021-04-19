---
description: 指定拓撲是否有全域開始和停止時間。
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: 'MF_SESSION_GLOBAL_TIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981009"
---
# <a name="mf_session_global_time-attribute"></a>MF \_ 會話 \_ GLOBAL \_ TIME 屬性

指定拓撲是否有全域開始和停止時間。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

當您使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數建立媒體 sesison 時，可以設定這個屬性。

如果此屬性存在且為非零值，則傳遞至媒體會話的所有拓撲都必須有 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 和 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性。 這些屬性會指定拓撲的開始和停止時間（相對於整個展示）。

如果這個屬性不存在或 **為 FALSE**，則拓撲不能有 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 或 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性。

使用這個屬性來建立編輯順序。 如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體會話屬性](media-session-attributes.md)
</dt> <dt>

[順序呈現時間](sequence-presentation-times.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**MF \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




