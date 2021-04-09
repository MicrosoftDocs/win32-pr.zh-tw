---
description: 指定嘗試解析拓撲的狀態。
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: 'MF_TOPOLOGY_RESOLUTION_STATUS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848521"
---
# <a name="mf_topology_resolution_status-attribute"></a>MF \_ 拓撲 \_ 解析 \_ 狀態屬性

指定嘗試解析拓撲的狀態。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

拓撲載入器或媒體會話可能會在拓撲上設定此屬性。 這個屬性的值是來自于 [**MF \_ 拓撲 \_ 解析 \_ 狀態 \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags)列舉的位 **or** of 旗標。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




