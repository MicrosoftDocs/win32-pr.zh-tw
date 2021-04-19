---
description: SWbemDateTime 物件是一個協助程式物件，用來剖析和設定通用訊息模型 (CIM) 日期時間值。
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: 'SWbemDateTime 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986975"
---
# <a name="swbemdatetime-object"></a>SWbemDateTime 物件

**SWbemDateTime** 物件是一個協助程式物件，用來剖析和設定通用訊息模型 (CIM) [日期時間](datetime.md)值。 它扮演類似于 [**SWbemObjectPath**](swbemobjectpath.md)的角色，可協助您格式化及解讀物件路徑。 您可以使用 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫來建立 **SWbemDateTime** 物件。

您可以使用物件上的方法，從 **VT \_ 日期** 或 **FILETIME** 值初始化 **SWbemDateTime** 物件，並將其格式化。 使用物件的屬性，可將值剖析為 component year、month、day、hour、分、秒或微秒。 **SWbemDateTime** 物件可以格式化為 local 或國際標準時間 (UTC) 值。 如需詳細資訊，請參閱 [日期和時間格式](date-and-time-format.md)。

**SWbemDateTime** 是唯一的 WINDOWS MANAGEMENT INSTRUMENTATION (WMI) 腳本物件，該物件標示為安全的初始化和在 Internet Explorer 中的 HTML 網頁上執行的腳本。

## <a name="members"></a>成員

**SWbemDateTime** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemDateTime** 物件有這些方法。



| 方法                                           | 描述                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | 將 **FILETIME** 日期和時間（以 **BSTR** 表示）轉換為 WMI [日期時間](datetime.md) 格式。<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | 將 WMI [DATETIME](datetime.md) 格式化日期和時間值轉換成 **VT \_ 日期**。<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | 將 WMI [DATETIME](datetime.md) 格式轉換為 **FILETIME** 日期和時間，以 **BSTR** 表示。<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | 將 **VT \_ 日期** 格式的日期和時間轉換為 WMI 日期 [時間](datetime.md)。<br/>                        |



 

### <a name="properties"></a>屬性

**SWbemDateTime** 物件具有這些屬性。



| 屬性                                                                        | 存取類型           | Description                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**天**](swbemdatetime-day.md)<br/>                                     | 讀取/寫入<br/> | CIM [日期時間](datetime.md) 值的日元件。<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | 讀取/寫入<br/> | 指出日期是否指定或保留為萬用字元。<br/>                                                        |
| [**小時**](swbemdatetime-hours.md)<br/>                                 | 讀取/寫入<br/> | CIM [datetime](datetime.md) 值之 day 元件的時數。<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | 讀取/寫入<br/> | 指出小時是否指定或保留為萬用字元。<br/>                                                       |
| [**IsInterval**](swbemdatetime-isinterval.md)<br/>                       | 讀取/寫入<br/> | 指出至少有一個 CIM [datetime](datetime.md) 的元件代表間隔，而不是日期。<br/> |
| [**微秒**](swbemdatetime-microseconds.md)<br/>                   | 讀取/寫入<br/> | CIM [datetime](datetime.md) 值的微秒部分。<br/>                                                  |
| [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)<br/> | 讀取/寫入<br/> | 指出是否將微秒元件指定或保留為萬用字元。<br/>                                     |
| [**分鐘**](swbemdatetime-minutes.md)<br/>                             | 讀取/寫入<br/> | CIM [日期時間](datetime.md) 值的分鐘元件。<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | 讀取/寫入<br/> | 指出分鐘元件是否指定或保留為萬用字元。<br/>                                          |
| [**月**](swbemdatetime-month.md)<br/>                                 | 讀取/寫入<br/> | CIM [日期時間](datetime.md) 值的月份元件。<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | 讀取/寫入<br/> | 指出月份是否已指定或保留為萬用字元。<br/>                                                      |
| [**秒**](swbemdatetime-seconds.md)<br/>                             | 讀取/寫入<br/> | CIM [日期時間](datetime.md) 值的秒陣列件。<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | 讀取/寫入<br/> | 指出秒元件是否指定或保留為萬用字元。<br/>                                          |
| [**Utc**](swbemdatetime-utc.md)<br/>                                     | 讀取/寫入<br/> | CIM [datetime](datetime.md) 值的 UTC 元件。<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | 讀取/寫入<br/> | 指出 UTC 元件是否指定或保留為萬用字元。<br/>                                              |
| [**值**](swbemdatetime-value.md)<br/>                                 | 讀取/寫入<br/> | 完整的 CIM [日期時間](datetime.md) 值。<br/>                                                                         |
| [**年**](swbemdatetime-year.md)<br/>                                   | 讀取/寫入<br/> | CIM [日期時間](datetime.md) 值的年份元件。<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | 讀取/寫入<br/> | 指出年份是否指定或保留為萬用字元。<br/>                                                |



 

## <a name="remarks"></a>備註

以國際標準時間座標 (UTC) 格式的 WMI 記錄時間戳記。 UTC 並非大部分開發人員和 IT 系統管理員使用的格式。 因此，常見的問題是決定如何將 UTC 轉譯成更容易讀取的內容。 如需如何使用 UTC 的詳細資訊，請參閱 [wmi 工作：日期和時間](wmi-tasks--dates-and-times.md) ，以及 [使用 wmi 處理日期和時間](/previous-versions/tn-archive/ee198928(v=technet.10))。 您也可以閱讀 (喔的 [相關時間，以及有關日期的) ](/previous-versions/technet-magazine/cc160973(v=msdn.10)) ，以及 [如何從 UTC 值減去指定的天數？](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog 文章以取得詳細資訊。

如果 [**IsInterval**](swbemdatetime-isinterval.md) 屬性設定為 **FALSE**，任何數值欄位都可以有萬用字元值。 具有萬用字元值的欄位包含整個欄位中的星號。

每個屬性（例如 [**Day**](swbemdatetime-day.md)）都有對應的指定布林值，例如 [**DaySpecified**](swbemdatetime-dayspecified.md)。 當 **DaySpecified** 為 **FALSE** 時，會將值視為間隔，而不是1到31之間的數位。 如果在 CIM [datetime](datetime.md) 值的任何地方使用間隔，則 [**IsInterval**](swbemdatetime-isinterval.md) 也會設定為 **TRUE**。 預設值是讓 CIM datetime 值包含日期，而不是一或多個間隔。

例如，如果 [**SWbemDateTime**](swbemdatetime-dayspecified.md) 為 **TRUE**，則 [**SWbemDateTime。值**](swbemdatetime-value.md) 會包含 [**SWbemDateTime**](swbemdatetime-day.md)的目前值，否則為萬用字元值。 在任何一種情況下， [**IsInterval**](swbemdatetime-isinterval.md) 屬性都是 **FALSE** 。

## <a name="examples"></a>範例

下列腳本範例示範如何使用 **SWbemDateTime** 物件來剖析從 WMI 儲存機制讀取的 datetime 屬性值（ [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)中的 **InstallDate** 屬性）。


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



下列範例示範如何建立 **SWbemDateTime** 物件、將日期值儲存在物件中、將日期顯示為本機和國際標準時間 (UTC) ，然後將值儲存在新建立的類別和屬性中。 如需有關常數 **wbemCimtypeDatetime** 的詳細資訊，請參閱 [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)。


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



下列腳本程式碼範例示範如何使用 **SWbemDateTime** 物件來修改從 WMI 儲存機制讀取之屬性的間隔值。


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



下列腳本程式碼範例示範如何使用 **SWbemDate** 物件來讀取 **FILETIME** 值。


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



下列 PowerShell 程式碼會建立 SWbemDateTime 物件的實例、捕獲 OS 安裝日期，並將日期轉換成不同的格式


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



下列 Powershell 程式碼會將程式碼轉譯成可供 CIM 提供者使用的格式。


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



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

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[Datetime](datetime.md)
</dt> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

