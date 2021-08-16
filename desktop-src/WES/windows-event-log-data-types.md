---
title: 'Windows事件記錄檔資料類型 (\System32\winevt\logs\application.evtx .h) '
description: Windows事件記錄檔會定義下列資料類型
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619988"
---
# <a name="windows-event-log-data-types"></a>Windows事件記錄檔資料類型

Windows事件記錄檔會定義下列資料類型：


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**.EVT \_ 控制碼**
</dt> <dd>

Windows 事件記錄檔物件的控制碼。

</dd> <dt>

**PEVT \_ 控制碼**
</dt> <dd>

Windows 事件記錄檔物件的控制碼指標。

</dd> <dt>

**.EVT \_ 物件 \_ 陣列 \_ 屬性 \_ 控制碼**
</dt> <dd>

Windows 事件記錄檔物件陣列的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>\System32\winevt\logs\application.evtx。h</dt> </dl> |



 

 





