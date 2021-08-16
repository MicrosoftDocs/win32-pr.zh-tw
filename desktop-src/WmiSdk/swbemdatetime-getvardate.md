---
description: 將 CIM DATETIME 格式的日期和時間值轉換成 VT \_ 日期格式。
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: 'SWbemDateTime. GetVarDate 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314753"
---
# <a name="swbemdatetimegetvardate-method"></a>SWbemDateTime. GetVarDate 方法

[**SWbemDateTime**](swbemdatetime.md)物件的 **GetVarDate** 方法會將 CIM [**DATETIME**](datetime.md)格式的日期和時間值轉換成 **VT \_ 日期** 格式。

**VT \_ 日期** 格式是 Visual Basic 和 ActiveX 使用的自動化變異日期 [**時間**](datetime.md)值。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIsLocal* \[在中，選擇性\]
</dt> <dd>

指出傳回的值是否會被視為當地時間。 國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的本地時間。 如果值為 **FALSE**，則會將值視為 UTC，並將零 (0) 位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

以 **VT \_ 日期** 格式的日期和時間值。

## <a name="remarks"></a>備註

**VT \_日期** 和 **FILETIME** 值不能包含萬用字元欄位。

如果下列任何一個屬性為 **FALSE**，則 **GetVarDate** 方法會失敗 (**wbemErrFailed**) ：

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

從 [**SetVarDate**](swbemdatetime-setvardate.md)成功傳回時，這些屬性全都會設定為 **TRUE**。

在成功呼叫 [**SetVarDate**](swbemdatetime-setvardate.md)之後， [**日期時間**](datetime.md) 值一律會被視為絕對 **日期時間** 值，而不是間隔，而 [**IsInterval**](swbemdatetime-isinterval.md) 會設定為 **FALSE**。

如果 [**IsInterval**](swbemdatetime-isinterval.md) 設定為 **TRUE**，則呼叫 **GetVarDate** 會導致 **wbemErrFailed** 錯誤。

當您呼叫 **GetVarDate** 時，會遺失精確度，因為 [日期時間](datetime.md) 值的 ( s 為一微秒) 解析， **而 \_ VT 日期** 值的解析度是500毫秒。

## <a name="examples"></a>範例

如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。 如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。

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

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




