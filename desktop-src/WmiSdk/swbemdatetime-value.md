---
description: 取得或設定 DMTF (分散式管理工作強制) 格式的原始 CIM 日期。
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: 'SWbemDateTime： Value 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114876"
---
# <a name="swbemdatetimevalue-property"></a>SWbemDateTime。 Value 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **Value** 屬性會取得或設定 DMTF (分散式管理工作強制) 格式的原始 CIM 日期。 DMTF 格式是 [**日期時間**](datetime.md) 值的字串表示。 這個屬性是 **SWbemDateTime** 物件的預設屬性。 **Value** 屬性的預設值為 00000101000000.000000 + 000。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

當您取得或設定 **Value** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021) 
</dt> <dd>

*StrValue* 的格式無效。

</dd> </dl>

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

