---
description: 將 CIM DATETIME 格式的日期和時間值轉換成 FILETIME 格式。
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: 'SWbemDateTime. GetFileTime 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739435"
---
# <a name="swbemdatetimegetfiletime-method"></a>SWbemDateTime. GetFileTime 方法

[**SWbemDateTime**](swbemdatetime.md)物件的 **GetFileTime** 方法會將 CIM [DATETIME](datetime.md)格式的日期和時間值轉換成 FILETIME 格式。

如果參數設定為 **TRUE**，則傳回值代表用戶端的本機時間。 否則，傳回值為國際標準時間 (UTC) 時間。 **FILETIME** [DATETIME](datetime.md)結構是64位的值，代表自1月 1 1601 日開始起算的 100-毫微秒單位數。 WindowsManagement Instrumentation (WMI) 會將 **FILETIME** 值視為不帶正負號64位數位的字串表示。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIsLocaL* \[在中，選擇性\]
</dt> <dd>

指出傳回的值是否會被視為當地時間。 UTC 屬性接著會包含轉換成正確國際標準時間的當地時間 (UTC) 位移。 如果值為 **FALSE**，則會將值視為 UTC，並將零 (0) 位移。

</dd> </dl>

## <a name="return-value"></a>傳回值

**FILETIME** 格式的日期和時間。

## <a name="error-codes"></a>錯誤碼

完成 **GetFileTime** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

呼叫失敗。

</dd> </dl>

## <a name="remarks"></a>備註

**VT \_日期** 和 **FILETIME** 值不能包含萬用字元欄位。

如果下列任何一個屬性為 **FALSE**，則 **GetFileTime** 方法會失敗 (wbemErrFailed) ：

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

從 [**SetFileTime**](swbemdatetime-setfiletime.md)成功傳回時，這些屬性全都會設定為 **TRUE**。

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

[**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

