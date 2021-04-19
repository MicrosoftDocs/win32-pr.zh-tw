---
title: 'TS_AS_ 常數 (Textstor) '
description: 下列旗標會指定呼叫 AdviseSink 方法的事件。
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998022"
---
# <a name="ts_as_-constants"></a>TS \_ 作為 \_ \* 常數

下列旗標會指定呼叫 **AdviseSink** 方法的事件。



| 常數/值                                                                                                                                                                                                                                                                                                                                         | Description                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <dt>**TS \_\_文字 \_ 變更**</dt> <dt> ( 0x1 )</dt> </dl>                                                                                                               | 檔中的文字已變更。<br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <dt>**TS \_作為 \_ SEL \_ 變更**</dt> <dt> ( 0x2 )</dt> </dl>                                                                                                                  | 在檔中選取文字。<br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <dt>**TS \_當 \_ 版面配置 \_ 變更**</dt> <dt> ( 0x4 )</dt> </dl>                                                                                                         | 檔的版面配置已變更。<br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <dt>**TS \_ ( 0x8 ) 的 \_ ATTR \_ 變更**</dt> <dt></dt> </dl>                                                                                                               | 檔的屬性已變更。<br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <dt>**TS \_\_狀態 \_ 變更**</dt> <dt> ( 0x10 )</dt> </dl>                                                                                                        | 檔的狀態已變更。<br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <dt>**TS \_因為 \_ 所有 \_ 接收都**</dt> <dt> ( ts \_ 作為 \_ 文字 \_ 變更 \| ts \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_</dt>作為「變更 ts」做為「配置變更 ts」作為變更 ts 作為狀態變更 )  </dl> | 檔中發生先前四個事件的其中一個。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



 

 





