---
description: 指定管線是否可以從拓撲節點卸載範例。
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: 'MF_TOPONODE_DISCARDABLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989001"
---
# <a name="mf_toponode_discardable-attribute"></a>MF \_ TOPONODE \_ DISCARDABLE 屬性

指定管線是否可以從拓撲節點卸載範例。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。 一般而言，您會在 t 節點上設定此屬性，以指出次要輸出並不重要。

屬性的值是在節點上輸出資料流程的索引陣列。

如果設定這個屬性，則如果資料流程落後，管線可能會從指定的輸出資料流程中卸載樣本。

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

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




