---
description: 代表控制流程防護 (CFG) 的呼叫目標相關資訊。
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: 'CFG_CALL_TARGET_INFO 結構 (Ntmmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974267"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ 呼叫 \_ 目標 \_ 資訊結構

代表控制流程防護 (CFG) 的呼叫目標相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**Offset**
</dt> <dd>

相對於所提供之 (開始) 虛擬位址的位移。 此位移應為16位元組對齊。

</dd> <dt>

**旗標**
</dt> <dd>

描述要在位址上執行之作業的旗標。 如果已設定 **cfg \_ 呼叫 \_ 目標 \_ 有效** ，則會將位址標示為適用于 CFG。 否則，它會標示為不正確呼叫目標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Ntmmapi。h</dt> </dl> |



 

 




