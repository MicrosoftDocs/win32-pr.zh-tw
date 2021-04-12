---
title: Windows 資料類型 (BaseTsd.h)
description: Windows 所支援的資料類型是用來定義函數傳回值、函數和訊息參數，以及結構成員。
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- 資料類型
- 資料類型，Windows
- Windows 應用程式開發介面
- Windows API，資料類型
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
- Usn
- 無效
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384525"
---
# <a name="windows-data-types"></a><span data-ttu-id="8b1c5-280">Windows 資料類型</span><span class="sxs-lookup"><span data-stu-id="8b1c5-280">Windows Data Types</span></span>

<span data-ttu-id="8b1c5-281">Windows 所支援的資料類型是用來定義函數傳回值、函數和訊息參數，以及結構成員。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="8b1c5-282">它們會定義這些元素的大小和意義。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="8b1c5-283">如需基礎 C/c + + 資料類型的詳細資訊，請參閱 [資料類型範圍](/cpp/cpp/data-type-ranges?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="8b1c5-284">下表包含下列類型：字元、整數、布林值、指標和控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="8b1c5-285">字元、整數和布林值類型通用於大部分的 C 編譯器。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="8b1c5-286">大部分的指標類型名稱都是以 P 或 LP 的前置詞開頭。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="8b1c5-287">控制碼指的是已載入記憶體的資源。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="8b1c5-288">如需有關處理64位整數的詳細資訊，請參閱 [大型整數](large-integers.md)。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-289">資料類型</span><span class="sxs-lookup"><span data-stu-id="8b1c5-289">Data type</span></span></th>
<th><span data-ttu-id="8b1c5-290">描述</span><span class="sxs-lookup"><span data-stu-id="8b1c5-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b1c5-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="8b1c5-292">系統函數的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="8b1c5-293">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-294"><span id="ATOM"></span><span id="atom"></span><strong>原子</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="8b1c5-295">Atom。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-295">An atom.</span></span> <span data-ttu-id="8b1c5-296">如需詳細資訊，請參閱 <a href="/windows/desktop/dataxchg/about-atom-tables">關於 Atom 資料表</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="8b1c5-297">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-298"><span id="BOOL"></span><span id="bool"></span><strong>Bool</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="8b1c5-299">布林值變數 (應該是 <strong>TRUE</strong> 或 <strong>FALSE</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="8b1c5-300">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>布林</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="8b1c5-302">布林值變數 (應該是 <strong>TRUE</strong> 或 <strong>FALSE</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="8b1c5-303">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-304"><span id="BYTE"></span><span id="byte"></span><strong>位元組</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="8b1c5-305">)  (8 個位的位元組。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="8b1c5-306">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-307"><span id="CALLBACK"></span><span id="callback"></span><strong>回檔</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="8b1c5-308">回呼函數的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="8b1c5-309">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="8b1c5-310"><strong>回呼</strong>、 <strong>WINAPI</strong>和 <strong>APIENTRY</strong> 全都用來定義具有 __stdcall 呼叫慣例的函式。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="8b1c5-311">Windows API 中的大部分函式都是使用 <strong>WINAPI</strong>來宣告。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="8b1c5-312">您可能會想要針對您所執行的回呼函式使用 <strong>回呼</strong> ，以協助將函式識別為回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="8b1c5-314">8位 Windows (ANSI) 字元。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="8b1c5-315">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-316"><span id="CHAR"></span><span id="char"></span><strong>字元</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="8b1c5-317">8位 Windows (ANSI) 字元。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="8b1c5-318">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="8b1c5-319">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="8b1c5-321">紅色、綠色、藍色 (RGB) 色彩值 (32 個位) 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="8b1c5-322">如需此類型的詳細資訊，請參閱 <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="8b1c5-323">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-324"><span id="CONST"></span><span id="const"></span><strong>常量</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="8b1c5-325">值在執行期間保持不變的變數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="8b1c5-326">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-327"><span id="DWORD"></span><span id="dword"></span><strong>Dword</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="8b1c5-328">32 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="8b1c5-329">範圍是0到4294967295的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="8b1c5-330">此類型是在 IntSafe 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="8b1c5-332">64 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="8b1c5-333">範圍是0到 18446744073709551615 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="8b1c5-334">此類型是在 IntSafe 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="8b1c5-336">指標有效位數不帶正負號的 long 類型。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="8b1c5-337">在將指標轉換為 long 類型以執行指標算術時使用。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="8b1c5-338"> (也常用於已在64位 Windows 中延伸至64位的一般32位參數。 ) </span><span class="sxs-lookup"><span data-stu-id="8b1c5-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="8b1c5-339">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="8b1c5-341">32 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="8b1c5-342">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="8b1c5-344">64 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="8b1c5-345">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-346"><span id="FLOAT"></span><span id="float"></span><strong>浮動</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="8b1c5-347">浮點數變數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-347">A floating-point variable.</span></span><br/> <span data-ttu-id="8b1c5-348">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="8b1c5-350"><a href="/windows/desktop/menurc/keyboard-accelerators">快速鍵對應表</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="8b1c5-351">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="8b1c5-353">指標的一半大小。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-353">Half the size of a pointer.</span></span> <span data-ttu-id="8b1c5-354">在包含指標和兩個小型欄位的結構中使用。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="8b1c5-355">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-356">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-356">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-357"><span id="HANDLE"></span><span id="handle"></span><strong>處理</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-358">物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="8b1c5-359">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-361"><a href="/windows/desktop/gdi/bitmaps">點陣圖</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-362">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-364"><a href="/windows/desktop/gdi/brushes">筆刷</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-365">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-367"><a href="/previous-versions//dd316799(v=vs.85)">色彩空間</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-368">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-370">動態資料交換 (DDE) 交談的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="8b1c5-371">此類型是在 Ddeml 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-373">DDE 交談清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="8b1c5-374">此類型是在 Ddeml 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-376">資料 <a href="/windows/desktop/menurc/cursors">指標</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-377">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-379"> (DC) 的 <a href="/windows/desktop/gdi/device-context-types">裝置內容</a> 控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="8b1c5-380">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-382">DDE 資料的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="8b1c5-383">此類型是在 Ddeml 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-385"><a href="/windows/desktop/winstation/desktops">桌面</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-386">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-388">內部 drop 結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="8b1c5-389">此類型是在 ShellApi 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-391">延後視窗位置結構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="8b1c5-392">此類型是在 WinUser 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-394"><a href="/windows/desktop/gdi/metafiles">增強型中繼檔</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-395">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-397"><a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>開啟之檔案的控制碼，而不是<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-398">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-400"><a href="/windows/desktop/gdi/about-fonts">字型</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-401">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-403">GDI 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="8b1c5-404">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-406">全域記憶體區塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="8b1c5-407">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-409">攔截<a href="/windows/desktop/winmsg/hooks">的控制碼。</a></span><span class="sxs-lookup"><span data-stu-id="8b1c5-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-410">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-412"><a href="/windows/desktop/menurc/icons">圖示</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-413">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-415">實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-415">A handle to an instance.</span></span> <span data-ttu-id="8b1c5-416">這是記憶體中模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="8b1c5-417"><strong>HMODULE</strong> 和 <strong>HINSTANCE</strong> 現在是一樣的，但在16位 Windows 中表示不同的事物。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="8b1c5-418">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-420">登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="8b1c5-421">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-423">輸入地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="8b1c5-424">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-426">本機記憶體區塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="8b1c5-427">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-429"><a href="/windows/desktop/menurc/menus">功能表</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-430">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-432"><a href="/windows/desktop/gdi/metafiles">中繼檔</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-433">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-435">模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-435">A handle to a module.</span></span> <span data-ttu-id="8b1c5-436">是記憶體中模組的基底位址。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="8b1c5-437"><strong>HMODULE</strong> 和 <strong>HINSTANCE</strong> 在目前的 windows 版本中是相同的，但在16位 Windows 中表示不同的專案。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="8b1c5-438">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-440">顯示監視器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="8b1c5-441">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-443">調色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="8b1c5-444">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-446"><a href="/windows/desktop/gdi/pens">畫筆</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-447">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-449">COM 介面所使用的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="8b1c5-450">如需詳細資訊，請參閱 <a href="/windows/desktop/com/structure-of-com-error-codes">COM 錯誤碼的結構</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="8b1c5-451">若要測試 <strong>HRESULT</strong> 值，請使用 <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> 和 <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> 宏。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="8b1c5-452">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-454"><a href="/windows/desktop/gdi/regions">區域</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-455">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-457">資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="8b1c5-458">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-460">DDE 字串的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="8b1c5-461">此類型是在 Ddeml 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-463"><a href="/windows/desktop/winstation/window-stations">視窗站</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-464">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-466"><a href="/windows/desktop/winmsg/windows">視窗</a>的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-467">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-468"><span id="INT"></span><span id="int"></span><strong>Int</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-469">32 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-469">A 32-bit signed integer.</span></span> <span data-ttu-id="8b1c5-470">範圍是-2147483648 到 2147483647 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-471">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-473">指標有效位數的帶正負號整數類型。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="8b1c5-474">在將指標轉換成整數以執行指標算術時使用。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="8b1c5-475">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-476">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-476">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-478">8 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="8b1c5-479">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-481">16 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="8b1c5-482">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-483"><span id="INT32"></span><span id="int32"></span><strong>時會</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-484">32 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-484">A 32-bit signed integer.</span></span> <span data-ttu-id="8b1c5-485">範圍是-2147483648 到 2147483647 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-486">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-488">64 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-488">A 64-bit signed integer.</span></span> <span data-ttu-id="8b1c5-489">範圍是-9223372036854775808 到 9223372036854775807 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-490">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-492">語言識別項。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-492">A language identifier.</span></span> <span data-ttu-id="8b1c5-493">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/language-identifiers">語言識別項</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-494">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-495"><span id="LCID"></span><span id="lcid"></span><strong>Lcid</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-496">地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-496">A locale identifier.</span></span> <span data-ttu-id="8b1c5-497">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/locale-identifiers">地區設定識別碼</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-498">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-500">地區設定資訊類型。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-500">A locale information type.</span></span> <span data-ttu-id="8b1c5-501">如需清單，請參閱 <a href="/windows/desktop/Intl/locale-information-constants">地區設定資訊常數</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-502">此類型是在 WinNls 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-504">語言群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-504">A language group identifier.</span></span> <span data-ttu-id="8b1c5-505">如需清單，請參閱 <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-506">此類型是在 WinNls 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-507"><span id="LONG"></span><span id="long"></span><strong>長</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-508">32 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-508">A 32-bit signed integer.</span></span> <span data-ttu-id="8b1c5-509">範圍是-2147483648 到 2147483647 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-510">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-512">64 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-512">A 64-bit signed integer.</span></span> <span data-ttu-id="8b1c5-513">範圍是-9223372036854775808 到 9223372036854775807 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-514">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-515">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-515">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-517">指標有效位數的帶正負號的 long 類型。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="8b1c5-518">將指標轉換為 long 以執行指標算術時使用。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="8b1c5-519">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-520">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-520">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-522">32 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-522">A 32-bit signed integer.</span></span> <span data-ttu-id="8b1c5-523">範圍是-2147483648 到 2147483647 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-524">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-526">64 位元帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-526">A 64-bit signed integer.</span></span> <span data-ttu-id="8b1c5-527">範圍是-9223372036854775808 到 9223372036854775807 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-528">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-530">訊息參數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-530">A message parameter.</span></span></p>
<p><span data-ttu-id="8b1c5-531">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-533"><a href="#bool"><strong>BOOL</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-534">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-536"><a href="#byte"><strong>位元組</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-537">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-539"><a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a>值的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="8b1c5-540">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-542">以零結束的8位 Windows (ANSI) 字元之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8b1c5-543">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-544">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-546">如果已定義<strong>UNICODE</strong> ，則為<a href="#lpcwstr"><strong>LPCWSTR</strong></a> ，否則為<a href="#lpcstr"><strong>LPCSTR</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8b1c5-547">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 資料類型的字串</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-548">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-549">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-549">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-551">任何類型之常數的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="8b1c5-552">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-554">16位 Unicode 字元之以 null 結束的常數位符串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8b1c5-555">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-556">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-558"><a href="#dword"><strong>DWORD</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-559">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-561"><a href="#handle"><strong>控制碼</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-562">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-564"><a href="#int"><strong>整數的指標。</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b1c5-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-565">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-567"><a href="#long"><strong>長整數</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-568">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-570">8位 Windows (ANSI) 字元之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8b1c5-571">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-572">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-574">如果已定義<strong>UNICODE</strong> ，則為<a href="#lpwstr"><strong>LPWSTR</strong></a> ，否則為<a href="#lpstr"><strong>LPSTR</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8b1c5-575">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 資料類型的字串</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-576">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-577">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-577">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-579">任何類型的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="8b1c5-580">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-582"><a href="#word"><strong>單字</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-583">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-585">16位 Unicode 字元之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8b1c5-586">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-587">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-589">訊息處理的簽署結果。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="8b1c5-590">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-592"><a href="#bool"><strong>BOOL</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-593">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-595"><a href="#boolean"><strong>布林值</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-596">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-598"><a href="#byte"><strong>位元組</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-599">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-601"><a href="#char"><strong>CHAR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-602">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-604">以零結束的8位 Windows (ANSI) 字元之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8b1c5-605">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-606">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-608">如果已定義<strong>UNICODE</strong> ，則為<a href="#pcwstr"><strong>PCWSTR</strong></a> ，否則為<a href="#pcstr"><strong>PCSTR</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8b1c5-609">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 資料類型的字串</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-610">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-611">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-611">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-613">16位 Unicode 字元之以 null 結束的常數位符串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8b1c5-614">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-615">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-617"><a href="#dword"><strong>DWORD</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-618">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-620">指向 <a href="#dwordlong"><strong>DWORDLONG</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-621">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-623"><a href="#dword_ptr"><strong>DWORD_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-624">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-626">指向 <a href="#dword32"><strong>DWORD32</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-627">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-629">指向 <a href="#dword64"><strong>DWORD64</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-630">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-632"><a href="#float"><strong>浮點數</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-633">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-635"><a href="#half_ptr"><strong>HALF_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-636">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-637">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-637">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-639"><a href="#handle"><strong>控制碼</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-640">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-642"><a href="#hkey"><strong>HKEY</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-643">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-644"><span id="PINT"></span><span id="pint"></span><strong>品脫</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-645"><a href="#int"><strong>整數的指標。</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b1c5-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-646">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-648"><a href="#int_ptr"><strong>INT_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-649">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-651"><a href="#int8"><strong>INT8</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-652">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-654"><a href="#int16"><strong>INT16</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-655">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-657"><a href="#int32"><strong>INT32</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-658">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-660"><a href="#int64"><strong>INT64</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-661">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-663"><a href="#lcid"><strong>LCID</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-664">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-666"><a href="#long"><strong>長整數</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-667">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-669">指向 <a href="#longlong"><strong>LONGLONG</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-670">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-672"><a href="#long_ptr"><strong>LONG_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-673">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-675">指向 <a href="#long32"><strong>LONG32</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-676">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-678">指向 <a href="#long64"><strong>LONG64</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-679">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-681">32位指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-681">A 32-bit pointer.</span></span> <span data-ttu-id="8b1c5-682">在32位系統上，這是原生指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="8b1c5-683">在64位系統上，這是截斷的64位指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="8b1c5-684">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-685">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-685">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-687">64位指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-687">A 64-bit pointer.</span></span> <span data-ttu-id="8b1c5-688">在64位系統上，這是原生指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="8b1c5-689">在32位系統上，這是一個帶正負號的32位指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="8b1c5-690">請注意，假設高指標位的狀態並不安全。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="8b1c5-691">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-692">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-692">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-694">帶正負號的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="8b1c5-695">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-697">不帶正負號的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="8b1c5-698">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-700"><a href="#short"><strong>簡短</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-701">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-703"><a href="#size_t"><strong>SIZE_T</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-704">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-706"><a href="#ssize_t"><strong>SSIZE_T</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-707">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-709">8位 Windows (ANSI) 字元之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8b1c5-710">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-711">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-713">指向 <a href="#tbyte"><strong>TBYTE</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-714">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-716">指向 <a href="#tchar"><strong>TCHAR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-717">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-719">如果已定義<strong>UNICODE</strong> ，則為<a href="#pwstr"><strong>PWSTR</strong></a> ，否則為<a href="#pstr"><strong>PSTR</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8b1c5-720">如需詳細資訊，請參閱 <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows 資料類型的字串</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-721">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-722">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-722">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-724">指向 <a href="#uchar"><strong>UCHAR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-725">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-727"><a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-728">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-729">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-729">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-731"><a href="#uint"><strong>UINT</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-732">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-734"><a href="#uint_ptr"><strong>UINT_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-735">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-737">指向 <a href="#uint8"><strong>UINT8</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-738">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-740"><a href="#uint16"><strong>UINT16</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-741">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-743"><a href="#uint32"><strong>UINT32</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-744">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-746"><a href="#uint64"><strong>UINT64</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-747">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-749"><a href="#ulong"><strong>ULONG</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-750">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-752">指向 <a href="#ulonglong"><strong>ULONGLONG</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-753">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-755"><a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-756">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-758">指向 <a href="#ulong32"><strong>ULONG32</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-759">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-761">指向 <a href="#ulong64"><strong>ULONG64</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-762">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-764"><a href="#ushort"><strong>USHORT</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-765">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-767">任何類型的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="8b1c5-768">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-770">指向 <a href="#wchar"><strong>WCHAR</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-771">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-773"><a href="#word"><strong>單字</strong></a>的指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-774">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-776">16位 Unicode 字元之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8b1c5-777">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-778">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-780">64 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="8b1c5-781">這種類型的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-783">服務控制管理員資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-783">A handle to a service control manager database.</span></span> <span data-ttu-id="8b1c5-784">如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-785">此類型是在 WinSvc 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-787">服務控制管理員資料庫的鎖定。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-787">A lock to a service control manager database.</span></span> <span data-ttu-id="8b1c5-788">如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-789">此類型是在 WinSvc 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-791">服務狀態值的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-791">A handle to a service status value.</span></span> <span data-ttu-id="8b1c5-792">如需詳細資訊，請參閱 <a href="/windows/desktop/Services/scm-handles">SCM 控制碼</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-793">此類型是在 WinSvc 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-794"><span id="SHORT"></span><span id="short"></span><strong>短</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-795">16位整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-795">A 16-bit integer.</span></span> <span data-ttu-id="8b1c5-796">範圍是-32768 到 32767 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-797">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-799">指標可以指向的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="8b1c5-800">用於必須橫跨指標完整範圍的計數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="8b1c5-801">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-803"><a href="#size_t"><strong>SIZE_T</strong></a>的帶正負號版本。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-804">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-806">如果已定義<strong>UNICODE</strong> ，則為<a href="#wchar"><strong>WCHAR</strong></a> ，否則為<a href="#char"><strong>字元</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="8b1c5-807">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-808">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-808">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-810">如果已定義<strong>UNICODE</strong> ，則為<a href="#wchar"><strong>WCHAR</strong></a> ，否則為<a href="#char"><strong>字元</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="8b1c5-811">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-812">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-812">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-814">不帶正負號的 <a href="#char"><strong>字元</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-815">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-817">不帶正負號的 <a href="#half_ptr"><strong>HALF_PTR</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="8b1c5-818">在包含指標和兩個小型欄位的結構中使用。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="8b1c5-819">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-820">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-820">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-822">不帶正負號的 <a href="#int"><strong>整數</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="8b1c5-823">範圍是0到4294967295的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-824">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-826">不帶正負號的 <a href="#int_ptr"><strong>INT_PTR</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-827">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-828">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-828">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-830">不帶正負號的 <a href="#int8"><strong>INT8</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-831">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-833">不帶正負號的 <a href="#int16"><strong>INT16</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-834">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-836">不帶正負號的 <a href="#int32"><strong>INT32</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="8b1c5-837">範圍是0到4294967295的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-838">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-840">不帶正負號的 <a href="#int64"><strong>INT64</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="8b1c5-841">範圍是0到 18446744073709551615 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-842">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-844">不帶正負號的 <a href="#long"><strong>LONG</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="8b1c5-845">範圍是0到4294967295的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-846">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-848">64 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="8b1c5-849">範圍是0到 18446744073709551615 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-850">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-851">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-851">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-853">不帶正負號的 <a href="#long_ptr"><strong>LONG_PTR</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8b1c5-854">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-855">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-855">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-857">未簽署的 <a href="#long32"><strong>LONG32</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="8b1c5-858">範圍是0到4294967295的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-859">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-861">未簽署的 <a href="#long64"><strong>LONG64</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="8b1c5-862">範圍是0到 18446744073709551615 decimal。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-863">此類型是在 BaseTsd 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-865">Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="8b1c5-866">此類型是在 Winternl 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1c5-867">C++</span><span class="sxs-lookup"><span data-stu-id="8b1c5-867">C++</span></span></th>
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
<td><span data-ttu-id="8b1c5-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-869">不帶正負號的 <a href="#short"><strong>簡短</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="8b1c5-870">範圍是0到65535的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-871">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-872"><span id="USN"></span><span id="usn"></span><strong>Usn</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-873"> (USN) 的更新序號。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="8b1c5-874">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-875"><span id="VOID"></span><span id="void"></span><strong>無效</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-876">任何類型。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-876">Any type.</span></span></p>
<p><span data-ttu-id="8b1c5-877">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-879">16位的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="8b1c5-880">如需詳細資訊，請參閱 <a href="/windows/desktop/gdi/character-sets-used-by-fonts">字體所使用的字元集</a>。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8b1c5-881">此類型會在 WinNT 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-883">系統函數的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="8b1c5-884">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="8b1c5-885"><strong>回呼</strong>、 <strong>WINAPI</strong>和 <strong>APIENTRY</strong> 全都用來定義具有 __stdcall 呼叫慣例的函式。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="8b1c5-886">Windows API 中的大部分函式都是使用 <strong>WINAPI</strong>來宣告。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="8b1c5-887">您可能會想要針對您所執行的回呼函式使用 <strong>回呼</strong> ，以協助將函式識別為回呼函數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b1c5-888"><span id="WORD"></span><span id="word"></span><strong>詞</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-889">16 位元不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="8b1c5-890">範圍是0到65535的十進位數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="8b1c5-891">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b1c5-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="8b1c5-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="8b1c5-893">訊息參數。</span><span class="sxs-lookup"><span data-stu-id="8b1c5-893">A message parameter.</span></span></p>
<p><span data-ttu-id="8b1c5-894">此類型是在 WinDef 中宣告，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b1c5-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8b1c5-895">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b1c5-895">Requirements</span></span>



| <span data-ttu-id="8b1c5-896">需求</span><span class="sxs-lookup"><span data-stu-id="8b1c5-896">Requirement</span></span> | <span data-ttu-id="8b1c5-897">值</span><span class="sxs-lookup"><span data-stu-id="8b1c5-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1c5-898">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b1c5-898">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1c5-899">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b1c5-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="8b1c5-900">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b1c5-900">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1c5-901">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b1c5-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="8b1c5-902">標頭</span><span class="sxs-lookup"><span data-stu-id="8b1c5-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b1c5-903"><dt>BaseTsd .h;</dt><dt>WinDef .h;</dt><dt>WinNT .h</dt></span><span class="sxs-lookup"><span data-stu-id="8b1c5-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
