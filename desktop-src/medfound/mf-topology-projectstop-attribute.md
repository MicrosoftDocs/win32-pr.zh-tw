---
description: 指定拓撲的開始時間（相對於序列中第一個拓撲的開頭）。
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: 'MF_TOPOLOGY_PROJECTSTOP 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512816"
---
# <a name="mf_topology_projectstop-attribute"></a>MF \_ 拓撲 \_ PROJECTSTOP 屬性

指定拓撲的開始時間（相對於序列中第一個拓撲的開頭）。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="remarks"></a>備註

此值是以100毫微秒的單位來提供。

如果媒體會話是使用等於 **TRUE** 的 [**mf \_ 會話 \_ GLOBAL \_ TIME**](mf-session-global-time-attribute.md)屬性所建立，則所有拓撲都必須包含 **MF \_ 拓撲 \_ PROJECTSTOP** 屬性。 否則，拓撲不得包含 **MF \_ 拓撲 \_ PROJECTSTOP** 屬性。 如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。

這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。

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

[順序呈現時間](sequence-presentation-times.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




