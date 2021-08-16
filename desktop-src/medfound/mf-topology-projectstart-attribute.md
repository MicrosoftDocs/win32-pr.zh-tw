---
description: 指定拓撲的停止時間（相對於序列中第一個拓撲的開頭）。
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: 'MF_TOPOLOGY_PROJECTSTART 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f295f68b3ac94bf29fa4607eb2b5ba00ea8eab19774bcaa0af150ef6d3fbe1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875405"
---
# <a name="mf_topology_projectstart-attribute"></a>MF \_ 拓撲 \_ PROJECTSTART 屬性

指定拓撲的停止時間（相對於序列中第一個拓撲的開頭）。

## <a name="data-type"></a>資料類型

**UINT64**

視為 **LONGLONG** 值。

## <a name="remarks"></a>備註

此值是以100毫微秒的單位來提供。

如果媒體會話是使用等於 **TRUE** 的 [**mf \_ 會話 \_ GLOBAL \_ TIME**](mf-session-global-time-attribute.md)屬性所建立，則所有拓撲都必須包含 **MF \_ 拓撲 \_ PROJECTSTART** 屬性。 否則，拓撲不得包含 **MF \_ 拓撲 \_ PROJECTSTART** 屬性。 如需詳細資訊，請參閱 [順序呈現時間](sequence-presentation-times.md)。

這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
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

[**MF \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




