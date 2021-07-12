---
description: 本檔中的表格列出 Shlwapi.dll 的包裝函式，提供有限的 Unicode 功能給 Windows 95、Windows 98 和 Windows Millennium Edition (Windows Me) 。
title: SHLWAPI 包裝函式
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c166e005c9bcc9efe68fee926c9fa9c2a4f4e7e
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581766"
---
# <a name="shlwapi-wrapper-functions"></a>SHLWAPI 包裝函式

\[這些函數可透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 取得。 它們可能會在 Windows 的後續版本中變更或無法使用。\]

本檔中的表格列出 Shlwapi.dll 的包裝函式，提供有限的 Unicode 功能給 Windows 95、Windows 98 和 Windows Millennium Edition (Windows Me) 。

Windows 95、Windows 98 和 Windows Millennium Edition (Windows Me) 在此稱為「原生 ANSI 平臺」。 在原生 ANSI 平臺上，這些包裝函式會將 Unicode 輸入字串參數轉換成 ANSI，並在 [ **轉送到** ] 資料行中呼叫 ansi 版本的函式。 例如， **AppendMenuWrapW** 會呼叫 **AppendMenuA**，也就是 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)的 ANSI 版本。 其他函式會遵循相同的模式。 ANSI 函數所傳回的任何字串都會轉換成 Unicode，並傳回給呼叫的應用程式。 除了 [ **備註** ] 資料行中所述的例外之外，包裝函式的語法也相同，而且提供的功能與 [ **轉送至** ] 資料行中的函數相同。 您應該參考該參考頁面，以取得詳細的使用資訊。

**安全性警告：** 多個 Unicode 字串可以轉換成相同的 ANSI 字串。 轉換後未預期的衝突可能會導致非預期的行為。 例如，如果使用 **CreateEventWrapW** 來建立兩個名稱不同的名稱事件，而這些事件的名稱在從 Unicode 轉換為 ANSI 之後是相符的，則第二個呼叫會將控制碼傳回至與第一個呼叫相同的事件，即使原始 Unicode 字串不同也是一樣。

Microsoft Windows NT、Windows 2000、Windows XP、Windows Server 2003 和更新版本的作業系統，在此稱為「原生 Unicode 平臺」。 大部分的情況下，在原生 Unicode 平臺上，這些包裝函式只會將輸入字串參數轉寄至轉送 **至** 資料行中函式的 Unicode 版本。 例如， **AppendMenuWrapW** 轉送至 **AppendMenuW**，這是 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)的 Unicode 版本。 其他函式會遵循相同的模式。 Unicode 函數所傳回的任何字串都會傳回給呼叫的應用程式。 除了 [ **備註** ] 資料行中所述的例外之外，包裝函式的語法也相同，而且提供的功能與 [ **轉送至** ] 資料行中的函數相同。 您應該參考該參考頁面，以取得詳細的使用資訊。

**安全性警告：** 針對 [ **轉送至** ] 資料行中的函式所述的安全性問題，也會套用至對應的包裝函式。 如需詳細資訊，請參閱 **轉送至** 資料行中函數的參考檔。

此資料表中的包裝函數全都包含在 Shlwapi.dll 中。 若要呼叫它們，您必須使用資料表中所列的序數。

> [!Note]  
> 這些包裝函式可在 Windows xp 上取得，但不提供 Windows XP Service Pack 2 (SP2) 和更新版本中的任何包裝函式功能。 它們也不會提供 Windows Server 2003 中的包裝函式功能。 您應該改用 [ **轉寄至** ] 資料行中所列的函數。

 



| 函式                  | 序數 | 轉寄至                                             | DLL      | 備註                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)、 [ (f) ](#dragqueryfile)、 [ (功能表) ](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32.DLL   | [ (我) ](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32.DLL | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32.DLL | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32.DLL | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32.DLL | [ (CompareString) ](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32.DLL   | [ (我) ](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32.DLL   | [ (f) ](#dragqueryfile)， [ () ](#shlwapi-wrapper-functions)， [ (DialogBoxParam) ](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32.DLL   | [ (我) ](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [ (b) ](#dialogboxparam)、 [ (c) ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)、 [ (DragQueryFile) ](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)， [ (d) ](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [ (d) ](#shlwapi-wrapper-functions)、 [ (f) ](#dragqueryfile)、 [ (ExtTextOut) ](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)、 [ (FormatMessage) ](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32.DLL   | [ (GetClassInfo) ](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)、 [ (DateTime) ](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32.DLL   | [ (g) ](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32.DLL | [ (g) ](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32.DLL   | [ (f) ](#dragqueryfile)、 [ (g) ](#compareexchange)、 [ (MenuItemInfo) ](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32.DLL | [ (c) ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32.DLL | [ (c) ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [ (g) ](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32.LIB | [ () ](#shlwapi-wrapper-functions)、 [ (b) ](#dialogboxparam)、 [ (g) ](#compareexchange)、 [ (OpenFileName) ](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32.LIB | [ () ](#shlwapi-wrapper-functions)、 [ (b) ](#dialogboxparam)、 [ (g) ](#compareexchange)、 [ (OpenFileName) ](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32.DLL | [ (c) ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)、 [ (DateTime) ](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32.DLL   | [ (WindowLong) ](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32.DLL | [ (c) ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32.DLL   | [ (j) ](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32.DLL   | [ (f) ](#dragqueryfile)、 [ (g) ](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)、 [ (f) ](#dragqueryfile)、 [ (功能表) ](#menu) ([ MenuItemInfo) ](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32.DLL   | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32.DLL | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32.DLL   | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**Loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32.DLL | [ (e) ](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)， [ (c) ](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32.DLL | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32.DLL   | [ (PeekMessage 和 PostMessage) ](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32.DLL   | [ (PeekMessage 和 PostMessage) ](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32.DLL | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32.DLL   | [ () ](#shlwapi-wrapper-functions) [ (RegisterClass) ](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32.DLL | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32.DLL | [ () ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)、 [ (ValueEx) ](#regqueryvalueexw)、 [ (RegQueryValueExW) ](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32.DLL | [ () ](#shlwapi-wrapper-functions)、 [ (g) ](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32.DLL | [ () ](#shlwapi-wrapper-functions) [ (ValueEx) ](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32.DLL   | [ (SendMessage) ](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32.DLL   | [ (WindowLong) ](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [ () ](#shlwapi-wrapper-functions)、 [ (b) ](#dialogboxparam)、 [ (ShellExecuteEx) ](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [ () ](#shlwapi-wrapper-functions) [ (FormatMessage) ](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [ () ](#shlwapi-wrapper-functions)、 [ (b) ](#dialogboxparam)、 [ (g) ](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32.DLL   | [ (g) ](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32.DLL   | [ (我) ](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32.DLL   | [ () ](#shlwapi-wrapper-functions)                                                                                                   |



 

下表中的包裝函式不會執行任何字元集轉換。 相反地，它們會針對舊版平臺上無法使用的作業系統功能提供有限的支援。



| 函式                     | 序數 | 轉寄至                                                                     | DLL      | 備註                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32.DLL | [ (h) ](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32.DLL | [ (h) ](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue)                                   | KERNEL32.DLL | [ (h) ](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32.DLL | [ (CompareExchange) ](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32.DLL | [ (QueueUserWorkItem) ](#queueuserworkitem)， [ (h) ](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32.DLL | [ (SetTimerQueueTimer) ](#settimerqueuetimer)， [ (h) ](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>備註

### <a name="a"></a> () 

如果需要字串轉換，所有字串都會透過 CP \_ ACP 字碼頁進行轉換。

這些函式會採用最適合的字元，而且在從 Unicode 轉換為 ANSI 時，不會執行預設檢查。 此外，如果字串無法從 Unicode 轉換為 ANSI，則包裝函數會將 **Null** 字串傳遞至基礎 ANSI 函數。 例如，記憶體不足時，就會發生這種情況。 傳遞 **null** 字串可能會導致某些函式失敗，並產生不正確參數錯誤，但其他函式會接受 **Null** 字串，並將它視為預期的參數。 例如，當 **CreateWindowExWrapW** 函式嘗試將 *lpWindowName* 參數轉換為 ANSI，而 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 建立具有空白標題的視窗時，就會發生錯誤。 當發生這些問題時，包裝函式不會通知您。

適用于 Unicode 的 Microsoft 層 (MSLU) 在從 Unicode 轉換為 ANSI 時檢查錯誤，並傳回適當的錯誤值。 例如，如果未成功附加專案，MSLU 中的 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) 包裝函式函數會傳回0。

### <a name="b"></a> (b) 

這些函式會針對適當的函式使用延遲載入的連結。 這表示除非呼叫該 DLL 中的函式，否則 Shlwapi.dll 不會載入包含「轉送至」資料行中之函式的 DLL。 Microsoft Visual C++ 連結器可透過/DELAYLOAD 選項更一般地支援這項功能。

### <a name="c"></a> (c) 

此函數會操作檔案名。 如 [ () ](#shlwapi-wrapper-functions)所述，函式會透過 CP \_ ACP 字碼頁轉換所有字串。 它們不會檢查檔案 i/o 函數是否已設定為 ANSI 模式。 如果檔案 i/o 函式處於 OEM 模式，字串就會轉換成錯誤字元集或從錯誤字元集轉換。 應用程式可以藉由呼叫 [**可透過 setfileapistooem**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) 函式，來明確地將檔案 i/o 函數設定為 OEM 模式。

* * 安全性警告： * * 針對檔案名使用這些包裝函式可能會危及應用程式的安全性。 由於不會執行任何預設檢查，而且採用最適合的字元，因此檔案名字元可以用非預期的方式進行轉換。 這可能會導致檔案系統詐騙攻擊。 此外，從 Unicode 轉換成 ANSI 期間可能會發生無訊息資料遺失。

MSLU 沒有這些限制。

### <a name="d"></a> (d) 

如果所繪製的字串需要的字元集無法在選取到裝置內容中的字型使用，則這些包裝函式會使用[MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85))程式庫的[字型連結](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85))功能，以適當的字型轉譯每個字元。 與其他大部分的包裝函式不同的是，除了原生 ANSI 平臺之外，這些函數也可在 Microsoft Windows NT 4.0 上運作。

### <a name="e"></a> (e) 

這些函式的完整 Unicode 實作為原生 ANSI 平臺提供。 這些函式不會呼叫相關的 ANSI 函數。

### <a name="f"></a> (f) 

如果使用者預設的 UI 語言使用的字元集與系統預設的 UI 語言不同，系統會嘗試重寫對話方塊範本和子類別控制項，並將功能表項目轉換為主控描繪，讓使用者預設 UI 語言中的字串繼續正確地顯示。 對話方塊範本重寫規則所支援的控制項只有靜態、按鈕、listbox 和 combobox 控制項。 這些控制項有子類別化，因此 **SendMessageWrapW** 函式可以取得原始的 Unicode 字串，而不需要透過 ANSI 字元集進行轉譯。 與大部分其他包裝函式不同的是，這些函式在 Microsoft Windows NT 4.0 以及原生 ANSI 平臺上都有作用。 請參閱 [**MLLoadLibrary**](./callbacks.md) 函式檔中的備註，以進一步討論使用者預設 ui 語言和系統預設 ui 語言的判斷方式。

### <a name="g"></a> (g) 

如果需要字串轉換，所有字串都會透過 CP \_ ACP 字碼頁進行轉換。

從 ANSI 轉換成 Unicode 以進行輸出時，如果傳回的字串不符合所提供的緩衝區，則包裝函數會截斷字串。 這些函式會傳回復制到緩衝區的字元數或避免截斷所需的字元數，不會傳回從包裝函式的呼叫端所提供或需要的 Unicode 字元數。 它們會傳回復制到緩衝區或基礎 ANSI 函數所需的 ANSI 字元數目。 MSLU 沒有這些限制。

### <a name="h"></a> (h) 

在 Windows XP 之前的系統上，這些函式會執行簡化的執行緒集區和計時器佇列。 在 Windows XP 和更新版本上，這些函數會使用系統執行緒集區和系統計時器佇列。 若為計時器佇列函數， *hQueue* 參數必須設定為 **Null** ，以表示要在預設計時器佇列上執行作業。

### <a name="i"></a> (我) 

在 Unicode 平臺上，如果目的地視窗是 ANSI，則這些函式會將訊息從 Unicode 轉譯為 ANSI。 這些函式不會在原生 ANSI 平臺上執行訊息轉譯。 因此，呼叫此函式的應用程式必須確保訊息在 Unicode 平臺上是 Unicode 格式，而 ANSI 平臺上的 ANSI 格式必須如此。 例如，在下列函式呼叫中，如果程式是在 Unicode 平臺上執行，則 *wParam* 必須是 unicode 程式碼點，而且如果程式是在 ansi 平臺上執行，則必須是 ansi 字元。

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

MSLU 會追蹤目的地視窗程式的字元集，並視需要轉換訊息。

### <a name="j"></a> (j) 

在 ANSI 平臺上，這些函式會傳回基礎 ANSI 字串的長度，而不是翻譯的 Unicode 字串長度。 MSLU 沒有這些限制。

### <a name="compareexchange"></a> (CompareExchange) 

**SHInterlockedCompareExchange** 的語法與 [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)的語法有點不同，但其功能相同。

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a> (CompareString) 

請記住，在原生 ANSI 平臺上，這兩個字串都會轉換成 ANSI，並比較為 ANSI 字串。 如果 Unicode 字串包含無法在 ANSI 中表示的字元，則結果可能不是預期的。 例如，如果預設的 ANSI 字碼頁不支援 CJK 字元，則字串 L " \\ x66F0" 和 l " \\ x6708" 會在原生 ANSI 平臺上比較為相等，因為它們都對應至 ANSI 字串 "？"。

### <a name="datetime"></a> (DateTime) 

在 Windows 2000 隨附的 Shlwapi.dll 5.0 版中，您以 **GetDateFormatWrapW** 和 **GetTimeFormatWrapW** 的第一個參數傳遞之地區設定識別碼的字碼頁必須符合目前的 ANSI 字碼頁。 否則，傳回的字串可能會不正確地轉換。 這項限制不適用於 Shlwapi.dll 5.5 或更高版本。 這表示 Windows XP 及更新版本的系統不受限於這項限制。 MSLU 沒有這項限制。

### <a name="dialogboxparam"></a> (DialogBoxParam) 

**DialogBoxParamWrapW** 函數的 *lpTemplateName* 參數不可以是字串。 它必須是 [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) 宏所建立的序數。 *LpDialogFunc* 參數所指定的對話方塊程式會接收原生 ansi 平臺上的 ansi 訊息，以及原生 unicode 平臺上的 unicode 訊息。 對話程式必須準備好處理這兩種情況。 MSLU 沒有這些限制。

### <a name="exttextout"></a> (ExtTextOut) 

原生 ANSI 平臺會採用 [**ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 函式以及原生 Unicode 平臺。 **ExtTextOutWrapW** 的目的是要執行字型連結，如個別的備註所述。

### <a name="dragqueryfile"></a> (DragQueryFile) 

**DragQueryFileWrapW** 函式不允許您傳遞 **Null** 做為 *lpszFile* 參數，查詢 drop 控制碼中的檔案長度。 MSLU 沒有這些限制。

### <a name="formatmessage"></a> (FormatMessage) 

在原生 ANSI 平臺上，字串中的格式不會從 Unicode 轉換為 ANSI。 例如，下列程式碼範例為錯誤。


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



這個程式碼範例會使用 "！ s！" format。 在原生 ANSI 平臺上，這個字串會傳遞至 ANSI 版本的 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數。 因此，預期的是 ANSI 字串，而不是 Unicode 字串。 同樣地，"%2" 格式意指字串引數。 傳遞至 ANSI **FormatMessage** 函式時，它會被解釋為 ansi 字串，而不是 Unicode 字串。 正確的格式字串為 L "%1！ ws！ %2！ ws！ "。 這會在 ANSI 和 Unicode 平臺上正確列印字串。

函數不支援 "%0"特殊的格式字串。

MSLU 沒有這些限制。

### <a name="getclassinfo"></a> (GetClassInfo) 

在原生 ANSI 平臺上， [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **lpszMenuName** 和 **lpszClassName** 成員不會轉譯成 Unicode，而且一律會設定為 **Null**。 此外，在 **WNDCLASS** 結構的 **lpfnWndProc** 成員中傳回的視窗程式不會轉譯成 Unicode，而是參考 ANSI 視窗程式。 MSLU 沒有這些限制。

### <a name="menu"></a> (] 功能表) 

在 Windows 2000 隨附的 Shlwapi.dll 5.0 版中，包含定位字元 (t) 的功能表項目字串 \\ 可能無法正確顯示。 這項限制不適用於 Shlwapi.dll 5.5 或更高版本。 這表示 Windows XP 及更新版本的系統不受限於這項限制。 MSLU 沒有這項限制。

### <a name="menuiteminfo"></a> (MenuItemInfo) 

此函數僅支援 Microsoft Windows NT 4.0 版的 [**MENUITEMINFOW**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構。 此結構缺少 **hbmpItem** 成員。 此外，此函數不支援 MIIM \_ 點陣圖旗標。 MSLU 沒有這些限制。

### <a name="openfilename"></a> (OpenFileName) 

[**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **cbSize** 成員必須設定為 sizeof (OPENFILENAME \_ NT4W) 。

[**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpstrCustomFilter** 成員必須設定為 **Null**。

[**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **nMaxFile** 和 **nMaxFileTitle** 成員值不能超過最大 \_ 路徑。

如果 [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **lpfnHook** 成員不是 **Null**，它就必須參考原生 ANSI 平臺上的 ANSI 勾點程式，以及原生 unicode 平臺上的 unicode 攔截程式。

MSLU 沒有這些限制。

### <a name="peekmessage-and-postmessage"></a> (PeekMessage 和 PostMessage) 

在原生 ANSI 平臺上，不會在傳輸或抓取的訊息上執行轉譯。 在原生 ANSI 平臺上，傳輸/抓取的訊息是 ANSI，在原生 Unicode 平臺上則是 Unicode。 呼叫的應用程式必須準備好處理這兩種情況。 例如，如果取出的訊息是 WM \_ CHAR，則 *wParam* 是原生 ansi 平臺上的 ansi 字元碼，但在原生 unicode 平臺上是 unicode 程式碼點。 MSLU 沒有這些限制。

### <a name="queueuserworkitem"></a> (QueueUserWorkItem) 

**SHQueueUserWorkItem** 函數與對應的 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)函式稍有不同。 **SHQueueUserWorkItem** 的語法如下所示。

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

參數應設定如下：

-   *PfnCallback* 和 *pCoNtext* 參數的意義與 *函數* 和 *內容* 參數的意義相同，分別為 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)。
-   *DwTag* 參數未使用，且必須設定為0。
-   *Pdwld* 參數未使用，且必須設定為 **Null**。
-   *PszModule* 參數指向以 null 終止的選擇性 ANSI 字串，這個字串會指定在工作專案完成後，工作專案開始和卸載之前要載入的程式庫名稱。 此參數可以是 **Null**。
-   *DwFlags* 參數僅支援 [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)支援的值子集。 可辨識下列旗標。

    

    | Name              | 值      | 意義                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | 與 WT. \_ EXECUTEINIOTHREAD 相同。   |
    | TPS \_ LONGEXECTIME | 0x00000008 | 與 WT. \_ EXECUTELONGFUNCTION 相同。 |

    

     

    > [!Note]  
    > TP LONGEXECTIME 旗標沒有與 \_ Wt. EXECUTELONGFUNCTION 旗標相同的數值 \_ 。 使用 **SHQueueUserWorkItem** 時，dwFlags 參數必須是 tp 值的組合 \_ \* ，而不是 wt. 的 \_ \* 值。

     

如果工作專案已成功排入佇列， **SHQueueUserWorkItem** 會傳回非零值，否則會傳回0。 如果函式失敗，您可以使用 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得其他資訊。

### <a name="registerclass"></a> (RegisterClass) 

在原生 ANSI 平臺上，不會在 [**WNDCLASSW**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **lpfnWndProc** 成員上執行任何轉譯。 視窗將會在原生 ANSI 平臺上接收 ANSI 視窗訊息，並在原生 Unicode 平臺上收到 Unicode 視窗訊息。 視窗程式必須準備好處理這兩種情況。 MSLU 沒有這些限制。

### <a name="regqueryvalueexw"></a> (RegQueryValueExW) 

**RegQueryValueExWrapW** 也是在名稱 **RegQueryValueExW** 下呼叫。 如同任何以序數完全匯出的未命名函式，您可以在程式碼中選擇函式的已知名稱。

### <a name="sendmessage"></a> (SendMessage) 

在原生 Unicode 平臺上， **SendMessageWrapW** 函式會轉送至 [**SendMessageW**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。 在原生 ANSI 平臺上， **SendMessageWrapW** 提供將 Unicode 訊息翻譯為 ANSI 的有限支援。 下表提供支援的訊息清單。 函數不會轉譯任何其他訊息。

MSLU 沒有這些限制。



| 訊息              | 描述                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ ADDSTRING        |  (b)  (f)  (c)                                                                                                |
| CB \_ FINDSTRING       |  (b)  (f)  (c)                                                                                                |
| CB \_ FINDSTRINGEXACT  |  ()  (f)  (c)                                                                                                |
| CB \_ GETLBTEXT        |  (b)  (f)  (c)  (o) 傳入 *lParam* 參數的緩衝區必須有至少256個字元的空間。   |
| CB \_ GETLBTEXTLEN     |  ()                                                                                                        |
| CB \_ INSERTSTRING     |  (b)  (f)  (c)                                                                                                |
| CB \_ SELECTSTRING     |  (b)  (f)  (c)                                                                                                |
| EM \_ CHARFROMPOS      |                                                                                                           |
| EM \_ GETLINE          |  (e) 傳回值是複製的 ANSI 字元數目。                                             |
| EM \_ GETSEL           |                                                                                                           |
| EM \_ REPLACESEL       |  (b)  (f)                                                                                                    |
| EM \_ SETPASSWORDCHAR  |  ()                                                                                                        |
| EM \_ SETSEL           |                                                                                                           |
| EM \_ SETWORDBREAKPROC | 此訊息沒有任何作用。 未設定斷詞程式。                                          |
| LB \_ ADDSTRING        |  (b)  (f)  (d)                                                                                                |
| LB \_ FINDSTRING       |  (b)  (f)  (d)                                                                                                |
| LB \_ FINDSTRINGEXACT  |  (b)  (f)  (磅)                                                                                              |
| LB \_ GETTEXT          |  (b)  (f)  (磅)  (o) 傳入 *lParam* 參數的緩衝區必須有至少256個字元的空間。 |
| LB \_ GETTEXTLEN       |  ()                                                                                                        |
| LB \_ INSERTSTRING     |  (b)  (f)  (d)                                                                                                |
| LB \_ SELECTSTRING     |  (b)  (f)  (d)                                                                                                |
| WM \_ GETTEXT          |  (b)  (f)                                                                                                    |
| WM \_ GETTEXTLENGTH    |  ()                                                                                                        |
| WM \_ SETTEXT          |  (b)  (f)                                                                                                    |
| WM \_ SETTINGCHANGE    |  () 訊息會以三秒的超時時間傳送。                                                  |



 


-    () 要測量或抓取的 ANSI 字串必須符合下列條件：字串相對應的 Unicode 版本長度不能超過 ANSI 版本的字串長度。 如果不符合此條件，傳回的長度將會很短。 如果記憶體不足，無法判斷 Unicode 字串的長度，則函式會傳回零，而不是 \_ 如預期般的 LB err 或 CB \_ err。
-    (b) 如果需要字串轉換，則所有字串都會透過 CP \_ ACP 字碼頁進行轉換。

    此函式會採用最適合的字元，而且在從 Unicode 轉換為 ANSI 時，不會執行預設檢查。 此外，如果字串無法從 Unicode 轉換為 ANSI，則函式會將 null 字串傳遞至基礎 ANSI 函數。 例如，記憶體不足時，就會發生這種情況。 傳遞 null 字串可能會導致某些函式失敗，並產生不正確參數錯誤，但其他函式會接受 null 字串，並將它視為預期的參數。 例如，如果當 WM \_ SETTEXT 包裝函式嘗試將視窗標題轉換成 ANSI 時發生錯誤，視窗將會有空白的標題。 當這些問題發生時，函數不會通知您。 MSLU 沒有這些限制。

-    (c) 指定的視窗控制碼必須是 [ComboBox](../controls/combo-boxes.md) 或 [ComboBoxEx](../controls/comboboxex-controls.md) 控制項的控制碼。 如果控制碼是做為主控描繪的 combobox 控制項，而且不是使用 [清單方塊樣式](../controls/list-box-styles.md) 樣式建立的，則此訊息的轉譯會失敗，甚至可能會損毀。
-    (d) 指定的視窗控制碼必須是 listbox 控制項的控制碼。 如果 listbox 是主控描繪，而且不是使用 [清單方塊樣式](../controls/list-box-styles.md) 樣式建立的，則此訊息的轉譯會失敗，甚至可能會損毀。
-    (e) 如果需要字串轉換，則所有字串都會透過 CP \_ ACP 字碼頁進行轉換。

    從 ANSI 轉換成 Unicode 以進行輸出時，如果在提供的緩衝區中無法容納傳回的字串，則包裝函式會將它截斷。 傳回復制到緩衝區的字元數目的函式傳回值，或為了避免截斷所需的字元數，是指複製到緩衝區或基礎 ANSI 函數所需的 ANSI 字元數目，而不是從呼叫的應用程式呼叫包裝函式所提供或所需的 Unicode 字元數。 MSLU 沒有這項限制。 如需詳細資訊，請參閱[Windows 95/98/Me 系統上的 Microsoft Layer for Unicode](/previous-versions/ms812865(v=msdn.10))。

### <a name="settimerqueuetimer"></a> (SetTimerQueueTimer) 

**SHSetTimerQueueTimer** 函數與對應的 [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)函式稍有不同。 其語法如下：

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

參數應設定如下：

-   *HQueue* 參數必須設定為 **Null**，指定預設計時器佇列。
-   *PfnCallback*、 *pCoNtext*、 *DwDueTime* 和 *dwPeriod* 參數與 [**DueTime**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)的 *回呼*、*參數*、 *CreateTimerQueueTimer* 和 *句號* 參數具有相同的意義。
-   *LpszLibrary* 參數未使用，且必須設定為 **Null**。
-   *Flags* 參數只支援 [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)支援的值子集。

    

    | Name              | 值      | 意義                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | 與 WT. \_ EXECUTEINIOTHREAD 相同   |
    | TPS \_ LONGEXECTIME | 0x00000008 | 與 WT. \_ EXECUTELONGFUNCTION 相同 |

    

     

    > [!Note]  
    > TP LONGEXECTIME 旗標沒有與 \_ Wt. EXECUTELONGFUNCTION 旗標相同的數值 \_ 。 使用 **SHSetTimerQueueTimer** 時， *dwFlags* 參數必須是 tp 值的組合 \_ \* ，而不是 wt. 的 \_ \* 值。

     

**SHSetTimerQueueTimer** 會在成功時傳回已建立之計時器的控制碼，否則會傳回 **Null** 。

### <a name="shellexecuteex"></a> (ShellExecuteEx) 

在此函式的唯一參數中傳遞之 [**SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa)結構的 **lpFile** 成員，可能不會超過網際網路 \_ URL 長度的最大 \_ \_ 字元數。 如果省略了 [請參閱 \_ MASK \_ CLASSNAME] 旗標，則 **lpClass** 成員必須初始化為 **Null**。

### <a name="valueex"></a> (ValueEx) 

僅支援下列登錄資料類型： REG \_ SZ、reg \_ EXPAND \_ SZ、REG \_ BINARY 和 reg \_ DWORD。 與這些包裝函式不同的是，MSLU 也支援 REG \_ 多重 \_ 展開 \_ SZ。

### <a name="windowlong"></a> (WindowLong) 

在原生 ANSI 平臺上，此函數不會在任何視窗長上執行任何轉譯。 例如，如果您傳遞 GWLP \_ WNDPROC，則函式會傳回 ANSI 視窗程式，而不是 Thunk。 MSLU 沒有這些限制。

 

 
