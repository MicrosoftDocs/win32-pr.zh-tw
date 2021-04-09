---
description: 本主題包含 Windows 用戶端基礎結構所使用之低層級 Api 的相關資訊。
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: 其他 Low-Level 用戶端支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846916"
---
# <a name="miscellaneous-low-level-client-support"></a>其他 Low-Level 用戶端支援

本主題包含 Windows 用戶端基礎結構所使用之低層級 Api 的相關資訊。

### <a name="functions"></a>函式



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>目錄</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>_Lclose 函式會關閉指定的檔案，使其無法再供讀取或寫入。 這個函式是為了與16位版本的 Windows 相容而提供。 以 Win32 為基礎的應用程式應該使用 CloseHandle 函數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>_Lopen 函式會開啟現有的檔案，並將檔案指標設定為檔案的開頭。 這個函式是為了與16位版本的 Windows 相容而提供。 以 Win32 為基礎的應用程式應該使用 CreateFile 函數。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>_Lread 函數會從指定的檔案讀取資料。 這個函式是為了與16位版本的 Windows 相容而提供。 以 Win32 為基礎的應用程式應該使用 ReadFile 函數。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></td>
<td>傳回值，這個值表示是否已在目前的裝置上啟用 DVD 編解碼器。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></td>
<td>停用呼叫 GUI 進程的視窗重影功能。 視窗重影是 Windows Manager 的功能，可讓使用者將沒有回應的應用程式主視窗最小化、移動或關閉。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></td>
<td>針對安裝在符合指定需求之系統上的所有媒體編解碼器，傳回屬性的清單。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></td>
<td>建立用來註冊媒體擴充功能的通訊 factory。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></td>
<td>在應用程式封裝中建立類別的實例。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></td>
<td>取得值，這個值表示是否已啟用與指定 GUID 相關聯的媒體行為。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></td>
<td>已取代。 此函數可用來關閉指定的控制碼。 <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> 被 <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>取代。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></td>
<td>已取代。 為提供的緩衝區 (的) 建立描述項，並將不具類型的資料傳遞至與檔案控制代碼相關聯的設備磁碟機。 <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> 被 <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>取代。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></td>
<td>已取代。 等到指定的物件並達到狀態為止 <code>signaled</code> 。 <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> 被 <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>取代。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></td>
<td>將指定的 ANSI 來源字串轉換成 Unicode 字串。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></td>
<td>將字元字串轉換成整數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></td>
<td>使用目前使用者之 SID 的字串表示，初始化提供的緩衝區。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></td>
<td>釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>所配置的字串緩衝區。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></td>
<td>釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>所配置的字串緩衝區。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></td>
<td>釋放 <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> 或 <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>所配置的字串緩衝區。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></td>
<td>初始化已計算的字串。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></td>
<td>初始化已計算的 Unicode 字串。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></td>
<td>將指定的 Unicode 來源字串轉換成 ANSI 字串。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></td>
<td>此函數會將指定的 Unicode 來源字串轉換成 OEM 字串。 這項翻譯是與 OEM 字碼頁 (OCP) 相關。 <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></td>
<td>決定將 Unicode 字串表示為 ANSI 字串所需的位元組數目。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a>函式會使用8位 Unicode 轉換格式 (utf-8) 字碼頁，將指定的 unicode 字串轉譯成新的字元字串。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a>函式會使用 utf-8 字碼頁，將指定的來源字串轉譯成 Unicode 字串。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></td>
<td>透過指定的子，指定輸入方法編輯器 (IME) 的動作或處理。
<blockquote>
[!Note]<br />
此函式已過時，不應該使用。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></td>
<td>暫時啟用或停用 IME，同時開啟或關閉 IME 所擁有之所有視窗的顯示。
<blockquote>
[!Note]<br />
此函式已過時，不應該使用。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>結構



| 主題                                 | 目錄                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa)用來指定要在 IME 訊息及其參數中執行的子。 此結構也用來接收來自這些稱為的傳回值。<br/> |
| [**字串**](/windows/desktop/api/Winternl/ns-winternl-string)       | 此結構會與 [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) 函數搭配使用。 <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>編譯器常式



| 主題                                                             | 目錄                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_C \_ 特定 \_ 處理常式常式**](--c-specific-handler2.md) | [**\_ \_ C \_ 特定 \_ 處理常式**](--c-specific-handler2.md)是 c 編譯器的 helper 常式。<br/> |
| [\_alldiv 常式](-win32-alldiv.md)                             | [ \_ alldiv 常式](-win32-alldiv.md)是 C 編譯器的 helper 常式。<br/>                     |
| [\_allmul](-win32-allmul.md) | 將兩個 **LONGLONG** 或 **ULONGLONG** 相乘。 |
| [\_aulldiv](-win32-aulldiv.md) | 將兩個 **ULONGLONG** 整數相除。 |
| [\_chkstk 常式](-win32-chkstk.md)                             | [ \_ chkstk 常式](-win32-chkstk.md)是 C 編譯器的 helper 常式。<br/>                     |
