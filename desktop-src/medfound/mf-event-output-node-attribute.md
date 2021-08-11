---
description: 識別資料流程接收的拓撲節點。
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: 'MF_EVENT_OUTPUT_NODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cbcbc243c195deb1061417adb6d93271b328fa242b497a7fdb232f5f7695e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244707"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
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

 

 




