---
title: 'MPSTATUS_DATAEX_UNUSED 結構 (MpClient .h) '
description: 非 SRP 的虛擬結構。
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED 結構舊版 Windows 環境功能
- PMPSTATUS_DATAEX_UNUSED 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245315d12b5fbe76ec2f552e510336aa3974753678e04f87c33546737f180c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961088"
---
# <a name="mpstatus_dataex_unused-structure"></a>MPSTATUS \_ DATAEX \_ 未使用的結構

非 SRP 的虛擬結構。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a>成員

<dl> <dt>

**dwNone**
</dt> <dd>

類型： **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





