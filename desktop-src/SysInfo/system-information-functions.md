---
description: 下列函式可用來取出或設定系統資訊。
ms.assetid: aa7deebf-7dce-4147-8a15-1d7411aea0fa
title: 系統資訊功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 675c2e5dfc9df9029a8ca7f5d4dc9468dd16a9d65cbd9ffa91edf6dc618e0e11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763457"
---
# <a name="system-information-functions"></a>系統資訊功能

下列函式可用來取出或設定系統資訊。



| 函式                                                                     | 描述                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CeipIsOptedIn**](/windows/desktop/api/Windowsceip/nf-windowsceip-ceipisoptedin)                                       | 檢查使用者是否已選擇將 SQM 資料收集作為客戶經驗改進計畫 (CEIP) 的一部分。                                                                                                       |
| [**DnsHostnameToComputerName**](/windows/desktop/api/Winbase/nf-winbase-dnshostnametocomputernamea)               | 將 DNS 名稱轉換成 NetBIOS 名稱。                                                                                                                                                                                            |
| [**EnumSystemFirmwareTables**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)                 | 列舉指定類型的所有系統固件資料表。                                                                                                                                                                      |
| [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa)                 | 以其定義的值取代環境變數字串。                                                                                                                                                                  |
| [**GetComputerName**](/windows/desktop/api/Winbase/nf-winbase-getcomputernamea)                                   | 抓取本機電腦的 NetBIOS 名稱。                                                                                                                                                                                 |
| [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)                               | 抓取本機電腦的 NetBIOS 或 DNS 名稱。                                                                                                                                                                          |
| [**GetComputerObjectName**](/windows/desktop/api/Secext/nf-secext-getcomputerobjectnamea)                       | 以指定的格式抓取本機電腦的名稱。                                                                                                                                                                        |
| [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea)                           | 抓取本機電腦目前的硬體設定檔。                                                                                                                                                                    |
| [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)     | 從 NVRAM 抓取指定之固件環境變數的值。                                                                                                                                                    |
| [**GetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa) | 抓取指定的固件環境變數及其屬性值。                                                                                                                                            |
| [**GetFirmwareType**](/windows/desktop/api/Winbase/nf-winbase-getfirmwaretype)                                   | 抓取本機電腦的固件類型。                                                                                                                                                                                |
| [**GetIntegratedDisplaySize**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getintegrateddisplaysize)                 | 抓取內建螢幕對角線大小的最佳估計值（以英寸為單位）。                                                                                                                                               |
| [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)                           | 針對在 WOW64 下執行的應用程式，捕獲目前系統的相關資訊。                                                                                                                                            |
| [**GetProductInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo)                                     | 抓取本機電腦上作業系統的產品類型，並將類型對應到指定作業系統所支援的產品類型。                                                                    |
| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)                             | 捕獲系統目錄的路徑。                                                                                                                                                                                       |
| [**GetSystemFirmwareTable**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)                     | 從「固件資料表」提供者抓取指定的固件資料表。                                                                                                                                                          |
| [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)                                       | 抓取目前系統的相關資訊。                                                                                                                                                                                   |
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)                     | 抓取目前的登錄大小，以及允許登錄在系統上達到的大小上限。                                                                                                             |
| [**GetSystemWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemwindowsdirectorya)               | 抓取多使用者系統上共用 Windows 目錄的路徑。                                                                                                                                                        |
| [**GetSystemWow64Directory**](/windows/win32/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)                   | 抓取 WOW64 所使用之系統目錄的路徑。                                                                                                                                                                         |
| [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a)                 | 使用指定的影像檔電腦類型，抓取 WOW64 所使用之系統目錄的路徑。                                                                                                                            |
| [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea)                                           | 抓取目前線程的使用者名稱。                                                                                                                                                                                    |
| [**GetUserNameEx**](/windows/desktop/api/Secext/nf-secext-getusernameexa)                                       | 抓取與呼叫執行緒相關聯的使用者或其他安全性主體的名稱。 您可以指定傳回名稱的格式。                                                                                   |
| [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion)                                             | 抓取目前作業系統的版本號碼。                                                                                                                                                                     |
| [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)                                         | 抓取目前作業系統的相關資訊。                                                                                                                                                                         |
| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)                           | 抓取 Windows 目錄的路徑。                                                                                                                                                                                      |
| [**IsNativeVhdBoot**](/windows/desktop/api/Winbase/nf-winbase-isnativevhdboot)                                   | 指出作業系統是否從 VHD 容器啟動。                                                                                                                                                                              |
| [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported)         |                                                                                                                                                                                                                                   |
| [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)               | 判斷目前的電腦是否支援處理器功能。                                                                                                                                                      |
| [**IsWow64Message**](/windows/desktop/api/winuser/nf-winuser-iswow64message)                                    | 判斷從目前進程的佇列讀取的最後一個訊息是從 WOW64 進程產生的。                                                                                                                   |
| [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)                                    | 判斷進程是否正在 WOW64 下執行。                                                                                                                                                                              |
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)                   | 抓取高解析度效能計數器的目前值。                                                                                                                                                           |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)               | 捕獲高解析度效能計數器的頻率。                                                                                                                                                               |
| [**RtlGetSuiteMask**](rtlgetsuitemask.md)                                   | 抓取識別系統上可用之產品套件的位元遮罩。 如果在伺服器接收器內容中執行的應用程式中呼叫此函式，則會改為抓取伺服器定址接收器的套件遮罩。 |
| [**SetComputerName**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernamea)                                   | 設定本機電腦的新 NetBIOS 名稱。                                                                                                                                                                                   |
| [**SetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa)                               | 設定本機電腦的新 NetBIOS 或 DNS 名稱。                                                                                                                                                                            |
| [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)     | 設定指定之固件環境變數的值。                                                                                                                                                                    |
| [**SetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa) | 設定指定之固件環境變數及其屬性的值。                                                                                                                                                 |
| [**TranslateName**](/windows/desktop/api/Secext/nf-secext-translatenamea)                                       | 將目錄服務物件名稱從一種格式轉換成另一種格式。                                                                                                                                                              |
| [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa)                               | 將一組版本需求與目前作業系統的值進行比較。                                                                                                                                            |
| [**VerSetConditionMask**](/windows/desktop/api/Winnt/nf-winnt-versetconditionmask)                           | 建立 [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) 函數的條件遮罩。                                                                                                                                        |
| [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection)    | 停用呼叫執行緒的檔案系統重新導向。                                                                                                                                                                          |
| [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)      | 啟用或停用呼叫執行緒的檔案系統重新導向。                                                                                                                                                               |
| [**Wow64RevertWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection)      | 還原呼叫執行緒的檔案系統重新導向。                                                                                                                                                                          |



 

## <a name="obsolete-functions"></a>過時的函式

-   [**NtQuerySystemInformation**](/windows/desktop/api/Winternl/nf-winternl-ntquerysysteminformation)
-   [**ZwQuerySystemInformation**](zwquerysysteminformation.md)

 

 
