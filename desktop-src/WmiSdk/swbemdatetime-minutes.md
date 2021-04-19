---
description: 取得或設定值，這個值表示 datetime 值的分鐘元件。
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: 'SWbemDateTime：分鐘屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975319"
---
# <a name="swbemdatetimeminutes-property"></a>SWbemDateTime 分鐘屬性

[**SWbemDateTime**](swbemdatetime.md)物件的 **分鐘** 屬性會取得或設定值，這個值表示 datetime 值的分鐘元件。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

取得或設定 **分鐘** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。

<dl> <dt>

**wbemErrValueOutOfRange** -2147749931 (0x8004102B) 
</dt> <dd>

值不在0到59的範圍內。

</dd> </dl>

## <a name="remarks"></a>備註

如果 [ **SWbemDateTime** ] 屬性設定為1，則 [ [**SWbemDateTime**](swbemdatetime-seconds.md) ] 屬性所包含的值會以一秒位移，這是當 CIM 日期 **時間** 值轉譯成 **VT \_ 日期** 值時所發生的舍入錯誤。 如果 [ **分鐘** ] 屬性是設定為0，則 [ **秒** ] 屬性會傳回正確的值。

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

[**SWbemDateTime.MinutesSpecified**](swbemdatetime-minutesspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

