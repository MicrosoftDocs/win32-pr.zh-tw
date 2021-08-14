---
description: 取得或設定日期時間值的國際標準時間 (UTC) 標記法。
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: 'SWbemDateTime. UTC 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c1bb3307116042a61aae06489bec7d8eabbf7859f3e8770811b50680dcfe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314691"
---
# <a name="swbemdatetimeutc-property"></a>SWbemDateTime UTC 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **utc** 屬性會取得或設定 **日期時間** 值的國際標準時間 (utc) 標記法。 UTC 是由世界時間標準所設定的時間。 UTC 已更換格林尼治平均時間 (GMT) 。 具有零位移的 UTC 值與 GMT 的值相同，且具有零位移。 帶正負號的數位必須在-720 到720的範圍內，否則會傳回錯誤 **wbemErrValueOutOfRange** 。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

取得或設定 **UTC** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B) 
</dt> <dd>

值不在-720 到720的範圍內。

</dd> </dl>

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemDateTime.UTCSpecified**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

