---
description: 監視器會呼叫 LoadDWORD 函式，以使用取自 HTML 設定字串變數的值來設定 DWORD 變數。
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: 'LoadDWORD 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979419"
---
# <a name="loaddword-function"></a>LoadDWORD 函式

監視器會呼叫 **LoadDWORD** 函式，以使用取自 HTML 設定字串變數的值來設定 **DWORD** 變數。

## <a name="syntax"></a>語法


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
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

*pValue* \[在\]
</dt> <dd>

**DWORD** 變數的指標，此變數會設定為設定字串變數的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (如果找到變數名稱，且) 長度為非零長度的字串，則會插入 **DWORD** ，且傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




