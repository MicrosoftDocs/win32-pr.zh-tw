---
description: 監視器會呼叫 LoadTCHAR 函式，將字串變數設定為取自 HTML 設定字串的字串。
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: 'LoadTCHAR 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972065"
---
# <a name="loadtchar-function"></a>LoadTCHAR 函式

監視器會呼叫 **LoadTCHAR** 函式，將字串變數設定為取自 HTML 設定字串的字串。

## <a name="syntax"></a>語法


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
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

*ppszString* \[擴展\]
</dt> <dd>

字串指標的指標。 如果找到要求的變數名稱，則會配置字串並將其指派給這個指標。 使用者會以負責任的方式釋放與字串相關聯的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (如果找到變數名稱，且) 長度為非零長度的字串，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




