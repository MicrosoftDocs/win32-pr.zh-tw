---
description: PROTOCOLINFO 結構描述通訊協定。
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: 'PROTOCOLINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996863"
---
# <a name="protocolinfo-structure"></a>PROTOCOLINFO 結構

**PROTOCOLINFO** 結構描述通訊協定。

## <a name="syntax"></a>語法


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**ProtocolID**
</dt> <dd>

指定之執行會話的系統指派通訊協定識別碼。

</dd> <dt>

**PropertyDatabase**
</dt> <dd>

指定之通訊協定的屬性資料庫。

</dd> <dt>

**ProtocolName**
</dt> <dd>

縮寫的通訊協定名稱。

</dd> <dt>

**HelpFile**
</dt> <dd>

與通訊協定相關聯的選擇性說明檔名稱。

</dd> <dt>

**註解**
</dt> <dd>

描述通訊協定的批註。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




