---
description: GetProtocolFromName 函式會將控制碼傳回給指定名稱的通訊協定。
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: 'GetProtocolFromName 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689715"
---
# <a name="getprotocolfromname-function"></a>GetProtocolFromName 函式

**GetProtocolFromName** 函式會將控制碼傳回給指定名稱的通訊協定。

## <a name="syntax"></a>語法


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolName* \[在\]
</dt> <dd>

通訊協定名稱 (例如 IP) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為通訊協定控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProtocolFromName** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




