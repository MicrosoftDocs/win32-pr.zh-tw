---
description: 下列函式會搭配系統時間使用。
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: 時間函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988924"
---
# <a name="time-functions"></a>時間函數

下列函式會搭配系統時間使用。



| 函式                                                                   | 描述                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | 以 UTC 格式抓取目前的系統日期和時間。                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | 判斷系統是否要將定期時間調整套用至其當天時間時鐘。          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | 將系統時間格式化為指定地區設定的時間字串。                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | 傳回系統時間。                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | 將指定的當地時間轉換為系統時間。                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | 將指定的系統時間轉換成從1970年1月1日開始的秒數。 |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | 設定目前系統的時間和日期。                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | 啟用或停用定期調整系統時間時鐘的時間。                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | 將系統時間轉換成檔案時間。                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | 將 UTC 時間轉換為指定的時區相對應本地時間。                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | 將當地時間轉換為 UTC 時間。                                                                   |



 

下列函式會搭配本地時間使用。



| 函式                                                                                           | 描述                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | 列舉儲存在登錄中的動態日光節約時間資訊專案。                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | 將 UTC 檔案時間轉換為本機檔案時間。                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | 抓取目前的時區和動態日光節約時間設定。                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | 抓取 [**動態 \_ 時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) 具有有效專案的範圍（以年為單位）。 |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | 抓取目前的本機日期和時間。                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | 抓取目前的時區設定。                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | 抓取指定年份和時區的時區設定。                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | 將指定的當地時間轉換為系統時間。                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | 設定目前的時區和動態日光節約時間設定。                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | 設定目前的當地時間和日期。                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | 設定目前的時區設定。                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | 將 UTC 時間轉換為指定的時區相對應本地時間。                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | 使用動態日光節約時間設定，將 UTC 時間轉換為指定時區的相對應本地時間。                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | 將當地時間轉換為 UTC 時間。                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | 使用動態日光節約時間設定，將當地時間轉換為 UTC 時間。                                                                   |



 

下列函式會搭配檔案時間使用。



| 函式                                                   | 描述                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | 比較兩個檔案時間。                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | 將 UTC 檔案時間轉換為本機檔案時間。                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | 將檔案時間轉換為系統時間格式。                                                                     |
| [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | 抓取所指定檔案或目錄的建立日期和時間、上次存取的日期和時間，以及上次修改的日期和時間。 |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | 以 UTC 格式抓取目前的系統日期和時間。                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | 根據 UTC 將本機檔案的時間轉換為檔案時間。                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | 設定指定檔案或目錄的建立日期和時間、上次存取時間或上次修改時間。       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | 將系統時間轉換成檔案時間。                                                                          |



 

下列函式會搭配 MS-DOS 日期和時間使用。



| 函式                                               | 描述                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | 將 MS-DOS 日期和時間值轉換成檔案時間。 |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | 將檔案時間轉換為 MS-DOS 日期和時間值。 |



 

下列函式會搭配 Windows 時間使用。



| 函式                                 | 描述                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | 捕獲系統計時資訊。                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | 抓取自系統啟動以來經過的毫秒數（最多49.7 天）。 |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | 捕獲自系統啟動以來經過的毫秒數。                  |



 

下列函式會搭配使用高解析度效能計數器。



| 函式                                                              | 描述                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | 抓取高解析度效能計數器的目前值。 |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | 捕獲高解析度效能計數器的頻率。     |



 

下列函式會搭配使用輔助效能計數器。



| 函式                                                                                           | 描述                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryAuxiliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | 查詢輔助計數器頻率。                                                                                                                                                                      |
| [**ConvertAuxiliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | 將指定的輔助計數器值轉換為對應的效能計數器值;（選擇性）在因延遲和最大可能漂移的情況下，于毫微秒內提供估計的轉換錯誤。 |
| [**ConvertPerformanceCounterToAuxiliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | 將指定的效能計數器值轉換為對應的輔助計數器值;（選擇性）在因延遲和最大可能漂移的情況下，于毫微秒內提供估計的轉換錯誤。 |



 

下列函式會搭配停機時間使用。



| 函式                                                                       | 描述                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | 取得目前的停機時間計數。                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | 以比 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) 更精確的形式取得目前的停機時間計數。                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | 取得目前的非偏誤停機時間計數。 非偏誤停機時間計數不包括系統花在睡眠或休眠狀態的時間。                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | 以比 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 更精確的形式取得目前的非偏誤停機時間計數。 非偏誤停機時間計數不包括系統花在睡眠或休眠狀態的時間。 |



 

 

 
