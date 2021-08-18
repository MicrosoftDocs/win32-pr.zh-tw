---
description: 包含拓撲節點的主要媒體類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: 'MF_TOPONODE_ERROR_MAJORTYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e32752f74708272c367e3f15b208ed66fb0d476baab75b8032ed028e1b9e4162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875144"
---
# <a name="mf_toponode_error_majortype-attribute"></a>MF \_ TOPONODE \_ ERROR \_ MAJORTYPE 屬性

包含拓撲節點的主要媒體類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。

拓撲載入器可能會設定屬性。 應用程式通常會讀取此屬性，但不會設定它。

如需可能值的清單，請參閱 [主要媒體類型](media-type-guids.md)。

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

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




