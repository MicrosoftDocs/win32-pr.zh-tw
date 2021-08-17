---
description: 抓取指定之進程的相關資訊。
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: ZwQueryInformationProcess 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 7972d3d2e6b98f56829680dd77c4c0a97b51679ffb2d9cfef928d4a279f6b7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792912"
---
# <a name="zwqueryinformationprocess-function"></a>ZwQueryInformationProcess 函式

\[**ZwQueryInformationProcess** 可能會在未來的 Windows 版本中變更或無法使用。 應用程式應該使用本主題中所列的替代函式。\]

抓取指定之進程的相關資訊。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProcessHandle* \[在\]
</dt> <dd>

要取得其資訊之進程的控制碼。

</dd> <dt>

*ProcessInformationClass* \[在\]
</dt> <dd>

要抓取之進程資訊的類型。 此參數可以是 **PROCESSINFOCLASS** 列舉中的下列其中一個值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </dl></td>
<td>抓取 PEB 結構的指標，此結構可用來判斷指定的進程是否正在進行調試，以及系統用來識別指定進程的唯一值。 <br/> 最好使用 <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> 和 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> 函數來取得此資訊。<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>抓取 <strong>DWORD_PTR</strong> 值，這個值是進程之偵錯工具的埠號碼。 非零值表示進程正以環形3偵錯工具的控制執行。<br/> 最好使用 <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> 或 <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> 函數。<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>判斷進程是否正在 wow64 環境中執行 (wow64 是 x86 模擬器，可讓 Win32 應用程式在 64 Windows) 上執行。<br/> 最好使用 <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> 函式來取得此資訊。<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>抓取 <strong>UNICODE_STRING</strong> 值，其中包含處理常式的影像檔名稱。<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>抓取 <strong>ULONG</strong> 值，指出進程是否視為嚴重。<br/>
<blockquote>
[!Note]<br />
從 Windows XP SP3 開始，可以使用這個值。 從 Windows 8.1 開始，應該改為使用<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> 。
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>抓取位元組值，指出受保護進程的類型以及受保護的進程簽署者。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*ProcessInformation* \[擴展\]
</dt> <dd>

呼叫應用程式所提供的緩衝區指標，函式會將要求的資訊寫入其中。 寫入的資訊大小會依 *ProcessInformationClass* 參數的值而有所不同：

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>處理 \_ 基本 \_ 資訊
</dt> <dd>

**ProcessBasicInformation** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **進程 \_ 基本 \_ 資訊** 結構：

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

**UniqueProcessId** 成員指向此進程的系統唯一識別碼。 最好使用 [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) 函式來取得此資訊。

**PebBaseAddress** 成員指向 [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)結構。

此結構的其他成員是保留供作業系統內部使用。

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ PTR
</dt> <dd>

**ProcessWow64Information** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納 **ULONG 的 \_ PTR**。 如果此值為非零值，則處理常式會在 WOW64 環境中執行;否則，如果值等於零，進程就不會在 WOW64 環境中執行。

最好使用 [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) 函式來判斷處理常式是否正在 WOW64 環境中執行。

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE \_ 字串
</dt> <dd>

**ProcessImageFileName** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納 **UNICODE \_ 字串** 結構以及字串本身。 儲存在 **緩衝區** 成員中的字串是影像檔案的名稱。

如果緩衝區太小，則函式會失敗並出現狀態 \_ 資訊 \_ 長度 \_ 不相符的錯誤碼，而且 *ReturnLength* 參數會設定為所需的緩衝區大小。

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

**ProcessProtectionInformation** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **PS_PROTECTION** 結構：

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

前3位包含受保護進程的類型：

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

前4個位包含受保護的進程簽署者：

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

*ProcessInformationLength* \[在\]
</dt> <dd>

*ProcessInformation* 參數所指向的緩衝區大小（以位元組為單位）。

</dd> <dt>

*ReturnLength* \[out、optional\]
</dt> <dd>

變數的指標，此函式會傳回所要求資訊的大小。 如果函式成功，這就是寫入 *ProcessInformation* 參數所指向之緩衝區的資訊大小，但如果緩衝區太小，這就是成功接收資訊所需的最小緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 NTSTATUS 成功或錯誤碼。

在 DDK 提供的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的形式和重要性，並在 DDK 檔的 Kernel-Mode 驅動程式架構/設計指南/驅動程式程式設計技術/記錄錯誤中加以說明。

## <a name="remarks"></a>備註

**ZwQueryInformationProcess** 函式及其傳回的結構都是作業系統的內部，而且可能會從一個 Windows 版本變更為另一個版本。 若要維持應用程式的相容性，最好改為使用 *ProcessInformationClass* 參數描述中提及的公用函數。

如果您使用 **ZwQueryInformationProcess**，可透過 [執行時間動態連結](../dlls/using-run-time-dynamic-linking.md)存取函式。 這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。 不過，簽章變更可能無法偵測。

此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
