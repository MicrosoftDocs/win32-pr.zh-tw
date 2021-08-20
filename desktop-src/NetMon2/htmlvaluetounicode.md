---
description: HTMLValueToUnicode 函式會將 HTML CP \_ UTF8 字串轉換成 Unicode 字串。
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: 'HTMLValueToUnicode 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39b7c05a20e07f406f4036659008ad68a40d25ecc6bca3f0600d121cf6557a32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981384"
---
# <a name="htmlvaluetounicode-function"></a>HTMLValueToUnicode 函式

**HTMLValueToUnicode** 函式會將 HTML CP \_ UTF8 字串轉換成 Unicode 字串。

## <a name="syntax"></a>語法


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValue* \[in、out\]
</dt> <dd>

在輸入時，指向 MCSVC 所提供之 HTML 字串的指標。

在輸出時，指向已轉換之 Unicode 字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回字串的 Unicode 對等專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




