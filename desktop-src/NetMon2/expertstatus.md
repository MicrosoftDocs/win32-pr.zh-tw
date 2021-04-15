---
description: 指出正在執行之專家的目前狀態。
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: 'EXPERTSTATUS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510981"
---
# <a name="expertstatus-structure"></a>EXPERTSTATUS 結構

**EXPERTSTATUS** 結構指出正在執行之專家的目前狀態。

## <a name="syntax"></a>語法


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>成員

<dl> <dt>

**狀態**
</dt> <dd>

[**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md)列舉所定義的目前專家狀態值。

</dd> <dt>

**狀態值**
</dt> <dd>

子狀態值。

</dd> <dt>

**PercentDone**
</dt> <dd>

已完成的網路資料專家分析完成百分比。

</dd> <dt>

**Frame**
</dt> <dd>

畫面格編號。

</dd> <dt>

**szStatusText**
</dt> <dd>

描述專家狀態的文字。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




