---
description: 從 Setup.exe 讀取一行，並從字串中解壓縮指定的欄位。
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: 'ParseField 函式 (Util) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193351"
---
# <a name="parsefield-function"></a>ParseField 函式

\[**ParseField** 函式目前應可用於下一版的 Microsoft Windows 作業系統。 它可能會在後續版本中變更或無法使用。\]

從 Setup.exe 讀取一行，並從字串中解壓縮指定的欄位。

## <a name="syntax"></a>語法


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szData* \[在\]
</dt> <dd>

類型： **LPCTSTR \** _

Setup.exe 的行指標。

</dd> <dt>

_n * \[ in\]
</dt> <dd>

類型： **int**

**整數** ，表示要解壓縮的欄位。

<dt>



  (0)


</dt> <dd>

指出在等號 (=) 之前的欄位。

</dd> <dt>



 (1)


</dt> <dd>

表示第一個欄位。

</dd> </dl> </dd> <dt>

*szBuf* \[在\]
</dt> <dd>

類型： **LPTSTR \** _

接收已解壓縮之欄位之緩衝區的指標。

</dd> <dt>

_iBufLen * \[ in\]
</dt> <dd>

類型： **int**

**INT** ，可接收已解壓縮之欄位的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **bool**

如果函式成功，則傳回 **TRUE** ，如果失敗，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

字串中的欄位必須以逗號分隔。

移除前置和尾端空格。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Util。h</dt> </dl>                             |
| 程式庫<br/>                  | <dl> <dt>Shell32 .lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 




