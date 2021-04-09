---
description: 比較兩個 Unicode 字串。
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: 'RtlCompareUnicodeString 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847260"
---
# <a name="rtlcompareunicodestring-function"></a>RtlCompareUnicodeString 函式

比較兩個 Unicode 字串。

## <a name="syntax"></a>語法


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*String1* \[在\]
</dt> <dd>

第一個字串的指標。

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

提供比較結果的帶正負號值：



| 傳回碼                                                                               | Description                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**零個**</dt> </dl>       | *String2* 等於 *String2*。<br/>          |
| <dl> <dt>**< 零**</dt> </dl>  | *String1* 小於 *string2*。<br/>    |
| <dl> <dt>**> 零**</dt> </dl> | *String1* 大於 *string2*。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                    |
| 目標平台<br/>          | <dl> <dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| 標頭<br/>                   | <dl> <dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt> </dl>                   |
| 程式庫<br/>                  | <dl> <dt>Ntdll.dll .lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RtlCompareString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**RtlEqualString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
