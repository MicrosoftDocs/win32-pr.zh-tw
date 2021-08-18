---
description: 指定管線是否在此節點套用標記。
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: 'MF_TOPONODE_MARKIN_HERE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c105dae6792e995e281309d2b693b78a0ec01e67c4412dc6d62056df09ebe9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874875"
---
# <a name="mf_toponode_markin_here-attribute"></a>MF \_ TOPONODE \_ MARKIN \_ 這裡屬性

指定管線是否在此節點套用標記。 [標記] 是簡報開始的起點。 如果管線元件在標記點之前產生資料，則不會呈現資料。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

> [!Note]  
> 大部分的應用程式不需要使用此屬性。 [媒體會話](media-session.md)會自動設定此屬性（如有需要）。

 

這個屬性會套用至所有節點類型。 如果屬性為 **TRUE**，媒體基礎管線會修剪這個節點的輸出範例，以符合簡報的開始時間。 拓撲載入器會在解析拓撲時設定這個屬性。

建議將此屬性設定為 **TRUE** 時，拓撲的每個分支中必須只有一個節點。 拓撲分支會定義為從來源節點到輸出節點的路徑。 在分支中，您 [ \_ \_ \_ ](mf-toponode-markout-here-attribute.md) \_ \_ \_ 必須在分支中的相同節點上設定 [TOPONODE MARKOUT] 和 [mf TOPONODE MARKIN] 屬性。 它們無法在相同分支內的不同節點上設定。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ 這裡**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




