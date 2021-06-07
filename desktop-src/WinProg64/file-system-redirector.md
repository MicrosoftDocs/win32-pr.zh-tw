---
title: 檔案系統重新導向程式
description: Windir \\ System32 目錄是保留給64位 Windows 上的64位應用程式。
ms.assetid: b4d36fe8-8bbb-469b-8ad1-650d559a4c75
keywords:
- 檔案系統重新導向程式 64-位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，檔案系統重新導向程式
- WOW64 64 位 Windows 程式設計，檔案系統重新導向程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568ddde85d18f90b951051251774c3509081dfdd
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443629"
---
# <a name="file-system-redirector"></a>檔案系統重新導向程式

% Windir% \\ System32 目錄是保留給64位 Windows 上的64位應用程式。 當建立64位版本的 dll 時，大部分的 DLL 檔案名都不會變更，因此32位版本的 Dll 會儲存在不同的目錄中。 WOW64 會使用 *檔案系統* 重新導向器來隱藏這項差異。

在大部分情況下，只要32位應用程式嘗試存取% windir% \\ System32、% windir% \\ lastgood \\ System32 或% windir% \\regedit.exe，就會將存取重新導向至特定架構的路徑。

> [!Note]  
> 這些路徑僅提供供參考之用。 為了相容，應用程式不應該直接使用這些路徑。 相反地，它們應該呼叫如下所述的 Api。

 



| 原始路徑                | 32位 x86 進程的重新導向路徑 | 32位 ARM 進程的重新導向路徑 |
|------------------------------|------------------------------------------|------------------------------------------|
| % windir% \\ System32           | % windir% \\ SysWOW64                       | % windir% \\ SysArm32                       |
| % windir% \\ lastgood \\ system32 | % windir% \\ lastgood \\ SysWOW64             | % windir% \\ lastgood \\ SysArm32             |
| % windir% \\regedit.exe        | % windir% \\ SysWOW64 \\regedit.exe          | % windir% \\ SysArm32 \\regedit.exe         |



 

如果存取導致系統顯示 UAC 提示，則不會發生重新導向。 相反地，會啟動所要求檔案的64位版本。 若要避免這個問題，請指定 SysWOW64 目錄以避免重新導向，並確保存取32位版本的檔案，或以系統管理員許可權執行32位應用程式，如此就不會顯示 UAC 提示。

* * Windows Server 2003 和 Windows XP： * * 不支援 UAC。

某些子目錄豁免于重新導向。 這些子目錄的存取權不會重新導向至% windir% \\ SysWOW64： <dl> % windir% \\ system32 \\ catroot  
% windir% \\ system32 \\ catroot2  
% windir% \\ system32 \\ driverstore  
% windir% \\ system32 \\ 驅動程式 \\ 等  
% windir% \\ system32 記錄檔 \\  
% windir% \\ system32 多工 \\ 緩衝處理  
</dl>

* * Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP： * *% windir% \\ system32 \\ driverstore 已重新導向。

若要取出32位系統目錄的名稱，64位應用程式應該使用 [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a) 函式 (Windows 10、1511版) 或 [**GetSystemWow64Directory**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函數。

應用程式應該使用 [**SHGetKnownFolderPath**](https://www.bing.com/search?q=**SHGetKnownFolderPath**) 函式來判斷% ProgramFiles% 的目錄名稱。

**Windows Server 2003 和 WINDOWS XP：** 應用程式應該使用 [**SHGetSpecialFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) 函式來判斷% ProgramFiles% 的目錄名稱。

應用程式可以使用 [**Wow64DisableWow64FsRedirection**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection)、 [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)和 [**WOW64REVERTWOW64FSREDIRECTION**](/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection) 函式來控制 WOW64 檔案系統重新導向器。 停用檔案系統重新導向會影響呼叫執行緒所執行的所有檔案作業，因此只有在單一 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 呼叫需要時才會停用，並且在函式傳回之後立即重新啟用。 停用較長期間的檔案系統重新導向可能會導致32位應用程式無法載入系統 Dll，導致應用程式失敗。

32位應用程式可以藉由將% windir% \\ Sysnative 取代為% windir% System32 來存取原生系統目錄 \\ 。 WOW64 會將 Sysnative 辨識為特殊別名，用來指出檔案系統不應重新導向存取。 這項機制很有彈性且容易使用，因此建議您最好使用此機制來略過檔案系統重新導向。 請注意，64位應用程式無法使用 Sysnative 別名，因為它是虛擬目錄，而不是真正的目錄。

**Windows Server 2003 和 WINDOWS XP：** 從 Windows Vista 開始，已新增 Sysnative 別名。

 

 