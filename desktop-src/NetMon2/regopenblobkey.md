---
description: RegOpenBlobKey 函式會在指定的登錄機碼上，抓取儲存的 BLOB。
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: 'RegOpenBlobKey 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5d372d6cc69c4e80691f96075aaa0d9030c90d06fc8256f85a7ed2dc894f3fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364147"
---
# <a name="regopenblobkey-function"></a>RegOpenBlobKey 函式

**RegOpenBlobKey** 函式會在指定的登錄機碼上，抓取儲存的 BLOB。

## <a name="syntax"></a>語法


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hkey* \[在\]
</dt> <dd>

包含 BLOB 之登錄機碼的控制碼。

</dd> <dt>

*szBlobName* \[在\]
</dt> <dd>

識別登錄中指定之 BLOB 的名稱。

</dd> <dt>

*phBlob* \[擴展\]
</dt> <dd>

要抓取之 BLOB 的指標。

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

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




