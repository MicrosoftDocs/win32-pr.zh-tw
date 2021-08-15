---
description: 指定拓撲節點的基礎物件是否為解碼器。
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: 'MF_TOPONODE_DECODER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8946e9de4131ce62a7ab76119b4a409cea03b1d05000a5c28c3cbab4bdcf3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875182"
---
# <a name="mf_toponode_decoder-attribute"></a>MF \_ TOPONODE \_ 解碼器屬性

指定拓撲節點的基礎物件是否為解碼器。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。

如果這個屬性的值為非零值，則節點的基礎物件為一個解碼器。

拓撲載入器會在建立一個解碼器節點時設定這個屬性。 如果應用程式手動將解碼器加入拓撲中，應用程式應該設定這個屬性。

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

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




