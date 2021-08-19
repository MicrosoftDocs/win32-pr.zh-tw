---
description: 取得或設定值，這個值表示 datetime 值的秒陣列件。
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: 'SWbemDateTime： Seconds 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4d30095e5464736b3db984b71f94a216c29f4327227a5e5b99becfbcae5e1a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816181"
---
# <a name="swbemdatetimeseconds-property"></a>SWbemDateTime. Seconds 屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **seconds** 屬性會取得或設定值，這個值表示 datetime 值的秒陣列件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

當您取得或設定 **Seconds** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B) 
</dt> <dd>

值不在0到59的範圍內。

</dd> </dl>

## <a name="remarks"></a>備註

如果 [**SWbemDateTime. 分鐘**](swbemdatetime-minutes.md)屬性已設定為1，則 **SWbemDateTime** 的屬性可能會包含不正確的值。 它包含的值會位移1秒，因為 CIM [**DATETIME**](datetime.md) 值轉譯成 **VT \_ 日期** 值時，會發生舍入錯誤。 如果 [ **分鐘** ] 屬性設定為 0 (零) ，則 [ **秒** ] 屬性會傳回正確的值。

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

[**SWbemDateTime.SecondsSpecified**](swbemdatetime-secondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

