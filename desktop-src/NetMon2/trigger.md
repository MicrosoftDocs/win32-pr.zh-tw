---
description: 觸發程式結構指出驅動程式在指定時間所要採取的動作。
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: '觸發程式結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 99404c8e9fc48e0ab85b956dd84af39b11eb87b22c87b4f9a232bd5b72d32143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363016"
---
# <a name="trigger-structure"></a>觸發程式結構

**觸發** 程式結構指出驅動程式在指定時間所要採取的動作。

## <a name="syntax"></a>語法


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>成員

<dl> <dt>

**TriggerActive**
</dt> <dd>

布林值，決定是否要由驅動程式來注意觸發程式。

</dd> <dt>

**TriggerType**
</dt> <dd>

觸發程式的 op 程式碼。

</dd> <dt>

**TriggerAction**
</dt> <dd>

觸發程式在引發時所要採取的動作。

</dd> <dt>

**TriggerFlags**
</dt> <dd>

觸發程式旗標。

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

觸發程式模式相符。

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

觸發緩衝區大小。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




