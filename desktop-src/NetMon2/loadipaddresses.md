---
description: 監視器會呼叫 LoadIPAddresses 函式，以填入取自 HTML 設定字串變數之位址的 IP 位址清單。
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: 'LoadIPAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998925"
---
# <a name="loadipaddresses-function"></a>LoadIPAddresses 函式

監視器會呼叫 **LoadIPAddresses** 函式，以填入取自 HTML 設定字串變數之位址的 IP 位址清單。

## <a name="syntax"></a>語法


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>-pconfig* \[在\]
</dt> <dd>

[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。

</dd> <dt>

*pVarName* \[在\]
</dt> <dd>

設定字串中變數名稱的指標。

</dd> <dt>

*ppAddresses* \[擴展\]
</dt> <dd>

指向位址陣列指標的指標。 如果找到在 *pVarName* 中指定的變數，而且其長度為非零，則此函式會配置足夠的空間，並將所有 IP 位址儲存為數組。

</dd> <dt>

*pNumAddresses* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標，此變數會設定為取自設定字串的 IP 位址數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (已找到變數名稱，且具有表示 IP 位址) 的非零長度字串，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

IP 位址必須是 x.x 格式 (例如，127.0.0.1) ）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




