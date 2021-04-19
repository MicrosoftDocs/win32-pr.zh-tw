---
description: 判斷共用名稱是否使用適當的語法。
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: 'NDdeIsValidShareName 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973807"
---
# <a name="nddeisvalidsharename-function"></a>NDdeIsValidShareName 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

判斷共用名稱是否使用適當的語法。

## <a name="syntax"></a>語法


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*共用名稱* \[在\]
</dt> <dd>

要驗證的共用名稱。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果共用名稱具有有效的語法，則傳回值為非零值。

如果共用名稱的語法無效，則傳回值為零。

## <a name="remarks"></a>備註

[**NDdeShareAdd**](nddeshareadd.md)在建立 DDE 共用時，也會呼叫這個函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeIsValidShareNameW** (Unicode) 和 **NDdeIsValidShareNameA** (ANSI) <br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




