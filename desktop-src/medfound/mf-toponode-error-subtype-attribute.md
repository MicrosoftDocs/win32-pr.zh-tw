---
description: 包含拓撲節點的媒體子類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: 'MF_TOPONODE_ERROR_SUBTYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992008"
---
# <a name="mf_toponode_error_subtype-attribute"></a>MF \_ TOPONODE \_ 錯誤 \_ 子類型屬性

包含拓撲節點的媒體子類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。

拓撲載入器可能會設定屬性。 應用程式通常會讀取此屬性，但不會設定它。

如需可能值的清單，請參閱 [媒體類型 guid](media-type-guids.md)。

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

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




