---
description: 包含 IP 或 IPX 通訊協定所使用的埠號碼。
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: 'GENERIC_PORT 聯集 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936631"
---
# <a name="generic_port-union"></a>泛型 \_ 埠聯集

**一般 \_ 埠** 結構包含 IP 或 IPX 通訊協定所使用的埠號碼。

## <a name="syntax"></a>語法


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a>成員

<dl> <dt>

**IPPort**
</dt> <dd>

填入的 IP 埠號碼。

</dd> <dt>

**ByteSwappedIPXPort**
</dt> <dd>

填入的 IPX 埠號碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




