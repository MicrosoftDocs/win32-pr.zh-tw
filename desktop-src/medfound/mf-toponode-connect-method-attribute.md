---
description: 指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: 'MF_TOPONODE_CONNECT_METHOD 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194587"
---
# <a name="mf_toponode_connect_method-attribute"></a>MF \_ TOPONODE \_ CONNECT \_ METHOD 屬性

指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。

此屬性值是來自 [**MF \_ CONNECT \_ 方法**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method)列舉的位 **or** of 旗標。 如果未設定此屬性，則預設值為 [ **MF \_ CONNECT \_ 允許 \_ 解碼器]**。

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

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[拓撲節點屬性](topology-node-attributes.md)
</dt> </dl>

 

 




