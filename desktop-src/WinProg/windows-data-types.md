---
title: Windows 資料類型 (BaseTsd.h)
description: Windows 所支援的資料類型是用來定義函數傳回值、函數和訊息參數，以及結構成員。
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- 資料類型
- 資料類型，Windows
- Windows 應用程式開發介面
- WindowsAPI，資料類型
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- 回檔
- CCHAR
- CHAR
- COLORREF
- 常量
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- HACCEL
- HALF_PTR
- HANDLE
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- HDC
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- HGDIOBJ
- HGLOBAL
- HHOOK
- HICON
- HINSTANCE
- HKEY
- HKL
- HLOCAL
- HMENU
- HMETAFILE
- HMODULE
- HMONITOR
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- LANGID
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- 品脫
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- PSTR
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- PVOID
- PWCHAR
- PWORD
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- USN
- 無效
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3002912cafbdf2dd4fe62c19fe3faef302da8c9b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626334"
---
# <a name="windows-data-types"></a>Windows 資料類型

Windows 所支援的資料類型是用來定義函數傳回值、函數和訊息參數，以及結構成員。 它們會定義這些元素的大小和意義。 如需基礎 C/c + + 資料類型的詳細資訊，請參閱 [資料類型範圍](/cpp/cpp/data-type-ranges?view=vs-2019)。

下表包含下列類型：字元、整數、布林值、指標和控制碼。 字元、整數和布林值類型通用於大部分的 C 編譯器。 大部分的指標類型名稱都是以 P 或 LP 的前置詞開頭。 控制碼指的是已載入記憶體的資源。

如需有關處理64位整數的詳細資訊，請參閱 [大型整數](large-integers.md)。



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>資料類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>系統函數的呼叫慣例。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>原子</strong></td>
<td>Atom。 如需詳細資訊，請參閱 <a href="/windows/desktop/dataxchg/about-atom-tables">關於 Atom 資料表</a>。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></td>
<td>布林值變數 (應該是 <strong>TRUE</strong> 或 <strong>FALSE</strong>) 。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>布林</strong></td>
<td>布林值變數 (應該是 <strong>TRUE</strong> 或 <strong>FALSE</strong>) 。<br/> 此類型會在 WinNT 中宣告，如下所示：<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>位元組</strong></td>
<td>)  (8 個位的位元組。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>回檔</strong></td>
<td>回呼函數的呼叫慣例。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>#define CALLBACK __stdcall</code><br/> <strong>回呼</strong>、 <strong>WINAPI</strong>和 <strong>APIENTRY</strong> 全都用來定義具有 __stdcall 呼叫慣例的函式。 Windows API 中的大部分函式都是使用<strong>WINAPI</strong>來宣告。 您可能會想要針對您所執行的回呼函式使用 <strong>回呼</strong> ，以協助將函式識別為回呼函數。<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>8位 Windows (ANSI) 字元。<br/> 此類型會在 WinNT 中宣告，如下所示：<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>字元</strong></td>
<td>8位 Windows (ANSI) 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。<br/> 此類型會在 WinNT 中宣告，如下所示：<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>紅色、綠色、藍色 (RGB) 色彩值 (32 個位) 。 如需此類型的詳細資訊，請參閱 <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> 。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>常量</strong></td>
<td>值在執行期間保持不變的變數。 <br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></td>
<td>32 位元不帶正負號的整數。 範圍是0到4294967295的十進位數。<br/> 此類型是在 IntSafe 中宣告，如下所示：<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>64 位元不帶正負號的整數。 範圍是0到 18446744073709551615 decimal。<br/> 此類型是在 IntSafe 中宣告，如下所示：<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>指標有效位數不帶正負號的 long 類型。 在將指標轉換為 long 類型以執行指標算術時使用。  (也常用於已在64位 Windows 延伸至64位的一般32位參數。 ) <br/> 此類型是在 BaseTsd 中宣告，如下所示：<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>32 位元不帶正負號的整數。<br/> 此類型是在 BaseTsd 中宣告，如下所示：<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>64 位元不帶正負號的整數。<br/> 此類型是在 BaseTsd 中宣告，如下所示：<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>浮動</strong></td>
<td>浮點數變數。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td><a href="/windows/desktop/menurc/keyboard-accelerators">快速鍵對應表</a>的控制碼。<br/> 此類型是在 WinDef 中宣告，如下所示：<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>指標的一半大小。 在包含指標和兩個小型欄位的結構中使用。<br/> 此類型是在 BaseTsd 中宣告，如下所示：<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span id="HANDLE"></span><span id="handle"></span><strong>處理</strong></td>
<td><p>物件的控制碼。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p><a href="/windows/desktop/gdi/bitmaps">點陣圖</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p><a href="/windows/desktop/gdi/brushes">筆刷</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p><a href="/previous-versions//dd316799(v=vs.85)">色彩空間</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>動態資料交換 (DDE) 交談的控制碼。</p>
<p>此類型是在 Ddeml 中宣告，如下所示：</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>DDE 交談清單的控制碼。</p>
<p>此類型是在 Ddeml 中宣告，如下所示：</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>資料 <a href="/windows/desktop/menurc/cursors">指標</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></td>
<td><p> (DC) 的 <a href="/windows/desktop/gdi/device-context-types">裝置內容</a> 控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>DDE 資料的控制碼。</p>
<p>此類型是在 Ddeml 中宣告，如下所示：</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p><a href="/windows/desktop/winstation/desktops">桌面</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>內部 drop 結構的控制碼。</p>
<p>此類型是在 ShellApi 中宣告，如下所示：</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>延後視窗位置結構的控制碼。</p>
<p>此類型是在 WinUser 中宣告，如下所示：</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p><a href="/windows/desktop/gdi/metafiles">增強型中繼檔</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p><a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>開啟之檔案的控制碼，而不是<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p><a href="/windows/desktop/gdi/about-fonts">字型</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></td>
<td><p>GDI 物件的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>全域記憶體區塊的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>攔截<a href="/windows/desktop/winmsg/hooks">的控制碼。</a></p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p><a href="/windows/desktop/menurc/icons">圖示</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>實例的控制碼。 這是記憶體中模組的基底位址。</p>
<p><strong>HMODULE</strong>和<strong>HINSTANCE</strong>現在都相同，但在16位 Windows 中代表不同的事物。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>登錄機碼的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>輸入地區設定識別碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>本機記憶體區塊的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p><a href="/windows/desktop/menurc/menus">功能表</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p><a href="/windows/desktop/gdi/metafiles">中繼檔</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>模組的控制碼。 是記憶體中模組的基底位址。</p>
<p><strong>HMODULE</strong>和<strong>HINSTANCE</strong>在 Windows 的最新版本中相同，但在16位 Windows 中表示不同的專案。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></td>
<td><p>顯示監視器的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>調色板的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p><a href="/windows/desktop/gdi/pens">畫筆</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></td>
<td><p>COM 介面所使用的傳回碼。 如需詳細資訊，請參閱 <a href="/windows/desktop/com/structure-of-com-error-codes">COM 錯誤碼的結構</a>。 若要測試 <strong>HRESULT</strong> 值，請使用 <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> 和 <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> 宏。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p><a href="/windows/desktop/gdi/regions">區域</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>資源的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>DDE 字串的控制碼。</p>
<p>此類型是在 Ddeml 中宣告，如下所示：</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p><a href="/windows/desktop/winstation/window-stations">視窗站</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></td>
<td><p><a href="/windows/desktop/winmsg/windows">視窗</a>的控制碼。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>INT</strong></td>
<td><p>32 位元帶正負號的整數。 範圍是-2147483648 到 2147483647 decimal。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>指標有效位數的帶正負號整數類型。 在將指標轉換成整數以執行指標算術時使用。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>8 位元帶正負號的整數。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>16 位元帶正負號的整數。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>時會</strong></td>
<td><p>32 位元帶正負號的整數。 範圍是-2147483648 到 2147483647 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>64 位元帶正負號的整數。 範圍是-9223372036854775808 到 9223372036854775807 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></td>
<td><p>語言識別項。 如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/language-identifiers">語言識別項</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></td>
<td><p>地區設定識別碼。 如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/locale-identifiers">地區設定識別碼</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>地區設定資訊類型。 如需清單，請參閱 <a href="/windows/desktop/Intl/locale-information-constants">地區設定資訊常數</a>。</p>
<p>此類型是在 WinNls 中宣告，如下所示：</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>語言群組識別碼。 如需清單，請參閱 <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>。</p>
<p>此類型是在 WinNls 中宣告，如下所示：</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>長</strong></td>
<td><p>32 位元帶正負號的整數。 範圍是-2147483648 到 2147483647 decimal。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>64 位元帶正負號的整數。 範圍是-9223372036854775808 到 9223372036854775807 decimal。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>指標有效位數的帶正負號的 long 類型。 將指標轉換為 long 以執行指標算術時使用。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>32 位元帶正負號的整數。 範圍是-2147483648 到 2147483647 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>64 位元帶正負號的整數。 範圍是-9223372036854775808 到 9223372036854775807 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>訊息參數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p><a href="#bool"><strong>BOOL</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p><a href="#byte"><strong>位元組</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p><a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a>值的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>8位 Windows 的常數 null 結束字串指標， (ANSI) 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#lpcwstr"><strong>LPCWSTR</strong></a> ，否則為<a href="#lpcstr"><strong>LPCSTR</strong></a> 。 如需詳細資訊，請參閱<a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 字串資料類型</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>任何類型之常數的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>16位 Unicode 字元之以 null 結束的常數位符串指標。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p><a href="#dword"><strong>DWORD</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p><a href="#handle"><strong>控制碼</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p><a href="#int"><strong>整數的指標。</strong></a></p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p><a href="#long"><strong>長整數</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>8位 Windows 之以 null 結束的字串指標， (ANSI) 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#lpwstr"><strong>LPWSTR</strong></a> ，否則為<a href="#lpstr"><strong>LPSTR</strong></a> 。 如需詳細資訊，請參閱<a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 字串資料類型</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>任何類型的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p><a href="#word"><strong>單字</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>16位 Unicode 字元之以 null 結束的字串指標。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>訊息處理的簽署結果。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p><a href="#bool"><strong>BOOL</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p><a href="#boolean"><strong>布林值</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p><a href="#byte"><strong>位元組</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p><a href="#char"><strong>CHAR</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>8位 Windows 的常數 null 結束字串指標， (ANSI) 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#pcwstr"><strong>PCWSTR</strong></a> ，否則為<a href="#pcstr"><strong>PCSTR</strong></a> 。 如需詳細資訊，請參閱<a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 字串資料類型</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>16位 Unicode 字元之以 null 結束的常數位符串指標。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p><a href="#dword"><strong>DWORD</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>指向 <a href="#dwordlong"><strong>DWORDLONG</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p><a href="#dword_ptr"><strong>DWORD_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>指向 <a href="#dword32"><strong>DWORD32</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>指向 <a href="#dword64"><strong>DWORD64</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p><a href="#float"><strong>浮點數</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p><a href="#half_ptr"><strong>HALF_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p><a href="#handle"><strong>控制碼</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p><a href="#hkey"><strong>HKEY</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>品脫</strong></td>
<td><p><a href="#int"><strong>整數的指標。</strong></a></p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p><a href="#int_ptr"><strong>INT_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p><a href="#int8"><strong>INT8</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p><a href="#int16"><strong>INT16</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p><a href="#int32"><strong>INT32</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p><a href="#int64"><strong>INT64</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p><a href="#lcid"><strong>LCID</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p><a href="#long"><strong>長整數</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></td>
<td><p>指向 <a href="#longlong"><strong>LONGLONG</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p><a href="#long_ptr"><strong>LONG_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>指向 <a href="#long32"><strong>LONG32</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>指向 <a href="#long64"><strong>LONG64</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>32位指標。 在32位系統上，這是原生指標。 在64位系統上，這是截斷的64位指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>64位指標。 在64位系統上，這是原生指標。 在32位系統上，這是一個帶正負號的32位指標。</p>
<p>請注意，假設高指標位的狀態並不安全。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>帶正負號的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>不帶正負號的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p><a href="#short"><strong>簡短</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p><a href="#size_t"><strong>SIZE_T</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p><a href="#ssize_t"><strong>SSIZE_T</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></td>
<td><p>8位 Windows 之以 null 結束的字串指標， (ANSI) 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>指向 <a href="#tbyte"><strong>TBYTE</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>指向 <a href="#tchar"><strong>TCHAR</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#pwstr"><strong>PWSTR</strong></a> ，否則為<a href="#pstr"><strong>PSTR</strong></a> 。 如需詳細資訊，請參閱<a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 字串資料類型</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>指向 <a href="#uchar"><strong>UCHAR</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p><a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p><a href="#uint"><strong>UINT</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p><a href="#uint_ptr"><strong>UINT_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>指向 <a href="#uint8"><strong>UINT8</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p><a href="#uint16"><strong>UINT16</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p><a href="#uint32"><strong>UINT32</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p><a href="#uint64"><strong>UINT64</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p><a href="#ulong"><strong>ULONG</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>指向 <a href="#ulonglong"><strong>ULONGLONG</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p><a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>指向 <a href="#ulong32"><strong>ULONG32</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>指向 <a href="#ulong64"><strong>ULONG64</strong></a>的指標。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p><a href="#ushort"><strong>USHORT</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>任何類型的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>指向 <a href="#wchar"><strong>WCHAR</strong></a>的指標。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></td>
<td><p><a href="#word"><strong>單字</strong></a>的指標。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>16位 Unicode 字元之以 null 結束的字串指標。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></td>
<td><p>64 位元不帶正負號的整數。</p>
<p>這種類型的宣告方式如下：</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>服務控制管理員資料庫的控制碼。 如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</p>
<p>此類型是在 WinSvc 中宣告，如下所示：</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>服務控制管理員資料庫的鎖定。 如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</p>
<p>此類型是在 WinSvc 中宣告，如下所示：</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>服務狀態值的控制碼。 如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</p>
<p>此類型是在 WinSvc 中宣告，如下所示：</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>短</strong></td>
<td><p>16位整數。 範圍是-32768 到 32767 decimal。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>指標可以指向的最大位元組數目。 用於必須橫跨指標完整範圍的計數。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p><a href="#size_t"><strong>SIZE_T</strong></a>的帶正負號版本。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#wchar"><strong>WCHAR</strong></a> ，否則為<a href="#char"><strong>字元</strong></a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></td>
<td><p>如果已定義<strong>UNICODE</strong> ，則為<a href="#wchar"><strong>WCHAR</strong></a> ，否則為<a href="#char"><strong>字元</strong></a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p>不帶正負號的 <a href="#char"><strong>字元</strong></a>。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p>不帶正負號的 <a href="#half_ptr"><strong>HALF_PTR</strong></a>。 在包含指標和兩個小型欄位的結構中使用。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p>不帶正負號的 <a href="#int"><strong>整數</strong></a>。 範圍是0到4294967295的十進位數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p>不帶正負號的 <a href="#int_ptr"><strong>INT_PTR</strong></a>。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p>不帶正負號的 <a href="#int8"><strong>INT8</strong></a>。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>不帶正負號的 <a href="#int16"><strong>INT16</strong></a>。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p>不帶正負號的 <a href="#int32"><strong>INT32</strong></a>。 範圍是0到4294967295的十進位數。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>不帶正負號的 <a href="#int64"><strong>INT64</strong></a>。 範圍是0到 18446744073709551615 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></td>
<td><p>不帶正負號的 <a href="#long"><strong>LONG</strong></a>。 範圍是0到4294967295的十進位數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>64 位元不帶正負號的整數。 範圍是0到 18446744073709551615 decimal。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p>不帶正負號的 <a href="#long_ptr"><strong>LONG_PTR</strong></a>。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p>未簽署的 <a href="#long32"><strong>LONG32</strong></a>。 範圍是0到4294967295的十進位數。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p>未簽署的 <a href="#long64"><strong>LONG64</strong></a>。 範圍是0到 18446744073709551615 decimal。</p>
<p>此類型是在 BaseTsd 中宣告，如下所示：</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Unicode 字串。</p>
<p>此類型是在 Winternl 中宣告，如下所示：</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></td>
<td><p>不帶正負號的 <a href="#short"><strong>簡短</strong></a>。 範圍是0到65535的十進位數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>USN</strong></td>
<td><p> (USN) 的更新序號。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>無效</strong></td>
<td><p>任何類型。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>16位的 Unicode 字元。 如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</p>
<p>此類型會在 WinNT 中宣告，如下所示：</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></td>
<td><p>系統函數的呼叫慣例。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>#define WINAPI __stdcall</code></p>
<p><strong>回呼</strong>、 <strong>WINAPI</strong>和 <strong>APIENTRY</strong> 全都用來定義具有 __stdcall 呼叫慣例的函式。 Windows API 中的大部分函式都是使用<strong>WINAPI</strong>來宣告。 您可能會想要針對您所執行的回呼函式使用 <strong>回呼</strong> ，以協助將函式識別為回呼函數。</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>詞</strong></td>
<td><p>16 位元不帶正負號的整數。 範圍是0到65535的十進位數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>訊息參數。</p>
<p>此類型是在 WinDef 中宣告，如下所示：</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>BaseTsd .h;</dt><dt>WinDef .h;</dt><dt>WinNT .h</dt> </dl> |
