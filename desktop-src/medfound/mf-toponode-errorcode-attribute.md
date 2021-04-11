---
description: 包含此拓撲節點最近連接失敗的錯誤碼。
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: 'MF_TOPONODE_ERRORCODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114028"
---
# <a name="mf_toponode_errorcode-attribute"></a>MF \_ TOPONODE \_ ERRORCODE 屬性

包含此拓撲節點最近連接失敗的錯誤碼。

## <a name="data-type"></a>資料類型

**UINT32**

Ttreat 為 **HRESULT** 值。

## <a name="remarks"></a>備註

這個屬性會套用至所有節點類型。

這個屬性的值是 **HRESULT** 值。

媒體會話或拓撲載入器可能會設定屬性。 應用程式通常會讀取此屬性，但不會設定它。

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

 

 




