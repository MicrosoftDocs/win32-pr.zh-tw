---
description: 識別資料流程接收的拓撲節點。
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: 'MF_EVENT_OUTPUT_NODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998266"
---
# <a name="mf_event_output_node-attribute"></a>MF \_ 事件 \_ 輸出 \_ 節點屬性

識別資料流程接收的拓撲節點。

## <a name="data-type"></a>資料類型

**UINT64**

視為 [**TOPOID**](topoid.md)。

## <a name="remarks"></a>備註

這個屬性的值是目前拓撲上輸出節點的節點識別碼。 若要取得相關聯節點的指標，請在拓撲上呼叫 [**IMFTopology：： GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) 。

這個屬性會搭配下列事件使用：

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

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

[事件屬性](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




