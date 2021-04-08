---
title: 'Windows 事件記錄檔資料類型 (\System32\winevt\logs\application.evtx .h) '
description: Windows 事件記錄檔會定義下列資料類型
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685879"
---
# <a name="windows-event-log-data-types"></a>Windows 事件記錄檔資料類型

Windows 事件記錄檔會定義下列資料類型：


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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>\System32\winevt\logs\application.evtx。h</dt> </dl> |



 

 





