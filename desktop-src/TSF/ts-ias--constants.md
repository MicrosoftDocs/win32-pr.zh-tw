---
title: 'TS_IAS_ 常數 (Textstor) '
description: TS \_ IAS \_ \ 常數用來作為位旗標，以控制在選取範圍或插入點插入文字或内嵌物件。
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7de66a9fcfc6d1b64b3b94fa43f8acd7afdfefb4d1263fe8860b5b6ca3169b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873795"
---
# <a name="ts_ias_-constants"></a>TS \_ IAS \_ \* 常數

TS \_ IAS \_ \* 常數是用來做為位旗標，以控制在選取範圍或插入點插入文字或内嵌物件。



| 常數/值                                                                                                                                                                                                                       | 描述                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <dt>**TS \_IAS \_ NOQUERY**</dt> <dt> ( 0x1 )</dt> </dl>       | 在結束時插入文字，範圍指標會設定為 **Null** 。 無法與 TS \_ IAS \_ QUERYONLY 旗標合併。<br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <dt>**TS \_IAS \_ QUERYONLY**</dt> <dt> ( 0x2 )</dt> </dl> | 請勿執行插入。 呼叫端只需要設定範圍指標。 無法與 TS \_ IAS \_ NOQUERY 旗標合併。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



 

 





