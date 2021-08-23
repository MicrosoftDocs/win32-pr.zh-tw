---
title: 'ADSI 單一資料型別 (Iads .h) '
description: ADSI)  (Active Directory 服務介面會定義和使用下列簡單的資料類型。
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422fc0e20195e576f3ade8b39948992d61a376b58fd22f399ca1009db79cbdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023696"
---
# <a name="adsi-simple-data-types"></a>ADSI 單一資料型別

ADSI)  (Active Directory 服務介面會定義和使用下列簡單的資料類型。


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**ADS \_ 布林值**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ 案例 \_ 精確 \_ 字串**
</dt> <dd>

LPWSTR

</dd> <dt>

**廣告 \_ 案例 \_ 忽略 \_ 字串**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ DN \_ 字串**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ 整數**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ 大型 \_ 整數**
</dt> <dd>

[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**ADS \_ 數值 \_ 字串**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ 物件 \_ 類別**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ 可列印 \_ 字串**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ 搜尋 \_ 控制碼**
</dt> <dd>

HANDLE

</dd> <dt>

**ADS \_ UTC \_ 時間**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>備註

當 ADSI 讀取已定義為 LDAP 架構中之 **整數** 的屬性時，它一律會將整數處理為32位值，而且可能會截斷資料。 這只是允許任意大小的整數值之 LDAP 伺服器的考慮。 如果屬性是延伸架構所定義的自訂屬性，則可將自訂屬性定義為字串來避免此問題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl> |



 

