---
description: RegCreateBlobKey 函式會在指定的登錄機碼上儲存 BLOB。
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: 'RegCreateBlobKey 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975545"
---
# <a name="regcreateblobkey-function"></a>RegCreateBlobKey 函式

**RegCreateBlobKey** 函式會在指定的登錄機碼上儲存 BLOB。

## <a name="syntax"></a>語法


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hkey* \[擴展\]
</dt> <dd>

將儲存 BLOB 之登錄機碼的控制碼。

</dd> <dt>

*szBlobName* \[在\]
</dt> <dd>

代表登錄中 BLOB 的 (應用程式定義) 名稱。

</dd> <dt>

*hBlob* \[在\]
</dt> <dd>

儲存之 BLOB 的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




