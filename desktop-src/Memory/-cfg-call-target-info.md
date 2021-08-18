---
description: 表示控制 Flow 防護 (CFG) 的呼叫目標相關資訊。
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
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040278"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ 呼叫 \_ 目標 \_ 資訊結構

表示控制 Flow 防護 (CFG) 的呼叫目標相關資訊。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Ntmmapi。h</dt> </dl> |



 

 




