---
description: 比較兩個 Unicode 字串，以判斷某個字串是否為另一個字串的前置詞。
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: 'RtlPrefixUnicodeString 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 28997f3bc85dedb9a18139cec13b9a76a8dd975e4ff57f1380053178bfaab328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076002"
---
# <a name="rtlprefixunicodestring-function"></a>RtlPrefixUnicodeString 函式

比較兩個 Unicode 字串，以判斷某個字串是否為另一個字串的前置詞。

## <a name="syntax"></a>語法


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*String1* \[在\]
</dt> <dd>

第一個字串的指標，可能是位於 *String2* 之已緩衝處理的 Unicode 字串的前置詞。

</dd> <dt>

*String2* \[在\]
</dt> <dd>

第二個字串的指標。

</dd> <dt>

*CaseInSensitive* \[在\]
</dt> <dd>

若 **為 TRUE**，則在進行比較時應該忽略大小寫。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *String1* 是 *string2* 的前置詞，**則為 TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                    |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| 標頭<br/>                   | <dl> <dt>Ntddk (包含 Ntddk) </dt> </dl>                                    |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




