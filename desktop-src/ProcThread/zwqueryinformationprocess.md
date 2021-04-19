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
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974445"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="f33f9-103">ZwQueryInformationProcess 函式</span><span class="sxs-lookup"><span data-stu-id="f33f9-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="f33f9-104">\[**ZwQueryInformationProcess** 可能會在未來的 Windows 版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f33f9-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="f33f9-105">應用程式應該使用本主題中所列的替代函式。\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="f33f9-106">抓取指定之進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f33f9-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33f9-107">語法</span><span class="sxs-lookup"><span data-stu-id="f33f9-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="f33f9-108">參數</span><span class="sxs-lookup"><span data-stu-id="f33f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33f9-109">*ProcessHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-110">要取得其資訊之進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f33f9-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f33f9-111">*ProcessInformationClass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-112">要抓取之進程資訊的類型。</span><span class="sxs-lookup"><span data-stu-id="f33f9-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="f33f9-113">此參數可以是 **PROCESSINFOCLASS** 列舉中的下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f33f9-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f33f9-114">值</span><span class="sxs-lookup"><span data-stu-id="f33f9-114">Value</span></span></th>
<th><span data-ttu-id="f33f9-115">意義</span><span class="sxs-lookup"><span data-stu-id="f33f9-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="f33f9-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-117">抓取 PEB 結構的指標，此結構可用來判斷指定的進程是否正在進行調試，以及系統用來識別指定進程的唯一值。</span><span class="sxs-lookup"><span data-stu-id="f33f9-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="f33f9-118">最好使用 <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> 和 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> 函數來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="f33f9-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="f33f9-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-120">抓取 <strong>DWORD_PTR</strong> 值，這個值是進程之偵錯工具的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f33f9-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="f33f9-121">非零值表示進程正以環形3偵錯工具的控制執行。</span><span class="sxs-lookup"><span data-stu-id="f33f9-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="f33f9-122">最好使用 <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> 或 <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="f33f9-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="f33f9-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-124">判斷進程是否正在 WOW64 環境中執行 (WOW64 是 x86 模擬器，可讓 Win32 應用程式在64位 Windows) 上執行。</span><span class="sxs-lookup"><span data-stu-id="f33f9-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="f33f9-125">最好使用 <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> 函式來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="f33f9-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="f33f9-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-127">抓取 <strong>UNICODE_STRING</strong> 值，其中包含處理常式的影像檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f33f9-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="f33f9-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-129">抓取 <strong>ULONG</strong> 值，指出進程是否視為嚴重。</span><span class="sxs-lookup"><span data-stu-id="f33f9-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f33f9-130">從 Windows XP SP3 開始，可以使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f33f9-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="f33f9-131">從 Windows 8.1 開始，應該改為使用 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="f33f9-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="f33f9-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="f33f9-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="f33f9-133">抓取位元組值，指出受保護進程的類型以及受保護的進程簽署者。</span><span class="sxs-lookup"><span data-stu-id="f33f9-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f33f9-134">*ProcessInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-135">呼叫應用程式所提供的緩衝區指標，函式會將要求的資訊寫入其中。</span><span class="sxs-lookup"><span data-stu-id="f33f9-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="f33f9-136">寫入的資訊大小會依 *ProcessInformationClass* 參數的值而有所不同：</span><span class="sxs-lookup"><span data-stu-id="f33f9-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="f33f9-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>處理 \_ 基本 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="f33f9-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-138">**ProcessBasicInformation** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **進程 \_ 基本 \_ 資訊** 結構：</span><span class="sxs-lookup"><span data-stu-id="f33f9-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="f33f9-139">**UniqueProcessId** 成員指向此進程的系統唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f33f9-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="f33f9-140">最好使用 [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) 函式來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="f33f9-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="f33f9-141">**PebBaseAddress** 成員指向 [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)結構。</span><span class="sxs-lookup"><span data-stu-id="f33f9-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="f33f9-142">此結構的其他成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="f33f9-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="f33f9-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ PTR</span><span class="sxs-lookup"><span data-stu-id="f33f9-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-144">**ProcessWow64Information** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納 **ULONG 的 \_ PTR**。</span><span class="sxs-lookup"><span data-stu-id="f33f9-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="f33f9-145">如果此值為非零值，則處理常式會在 WOW64 環境中執行;否則，如果值等於零，進程就不會在 WOW64 環境中執行。</span><span class="sxs-lookup"><span data-stu-id="f33f9-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="f33f9-146">最好使用 [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) 函式來判斷處理常式是否正在 WOW64 環境中執行。</span><span class="sxs-lookup"><span data-stu-id="f33f9-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="f33f9-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE \_ 字串</span><span class="sxs-lookup"><span data-stu-id="f33f9-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-148">**ProcessImageFileName** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納 **UNICODE \_ 字串** 結構以及字串本身。</span><span class="sxs-lookup"><span data-stu-id="f33f9-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="f33f9-149">儲存在 **緩衝區** 成員中的字串是影像檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f33f9-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="f33f9-150">如果緩衝區太小，則函式會失敗並出現狀態 \_ 資訊 \_ 長度 \_ 不相符的錯誤碼，而且 *ReturnLength* 參數會設定為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="f33f9-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="f33f9-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="f33f9-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-152">**ProcessProtectionInformation** *ProcessInformationClass* 參數時， *ProcessInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **PS_PROTECTION** 結構：</span><span class="sxs-lookup"><span data-stu-id="f33f9-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

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

<span data-ttu-id="f33f9-153">前3位包含受保護進程的類型：</span><span class="sxs-lookup"><span data-stu-id="f33f9-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="f33f9-154">前4個位包含受保護的進程簽署者：</span><span class="sxs-lookup"><span data-stu-id="f33f9-154">The top 4 bits contain the protected process signer:</span></span>

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

<span data-ttu-id="f33f9-155">*ProcessInformationLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-156">*ProcessInformation* 參數所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f33f9-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f33f9-157">*ReturnLength* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f9-158">變數的指標，此函式會傳回所要求資訊的大小。</span><span class="sxs-lookup"><span data-stu-id="f33f9-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="f33f9-159">如果函式成功，這就是寫入 *ProcessInformation* 參數所指向之緩衝區的資訊大小，但如果緩衝區太小，這就是成功接收資訊所需的最小緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="f33f9-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33f9-160">傳回值</span><span class="sxs-lookup"><span data-stu-id="f33f9-160">Return value</span></span>

<span data-ttu-id="f33f9-161">傳回 NTSTATUS 成功或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f33f9-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="f33f9-162">在 DDK 提供的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的形式和重要性，並在 DDK 檔的 Kernel-Mode 驅動程式架構/設計指南/驅動程式程式設計技術/記錄錯誤中加以說明。</span><span class="sxs-lookup"><span data-stu-id="f33f9-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33f9-163">備註</span><span class="sxs-lookup"><span data-stu-id="f33f9-163">Remarks</span></span>

<span data-ttu-id="f33f9-164">**ZwQueryInformationProcess** 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。</span><span class="sxs-lookup"><span data-stu-id="f33f9-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="f33f9-165">若要維持應用程式的相容性，最好改為使用 *ProcessInformationClass* 參數描述中提及的公用函數。</span><span class="sxs-lookup"><span data-stu-id="f33f9-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="f33f9-166">如果您使用 **ZwQueryInformationProcess**，可透過 [執行時間動態連結](../dlls/using-run-time-dynamic-linking.md)存取函式。</span><span class="sxs-lookup"><span data-stu-id="f33f9-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="f33f9-167">這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。</span><span class="sxs-lookup"><span data-stu-id="f33f9-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="f33f9-168">不過，簽章變更可能無法偵測。</span><span class="sxs-lookup"><span data-stu-id="f33f9-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="f33f9-169">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="f33f9-169">This function has no associated import library.</span></span> <span data-ttu-id="f33f9-170">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="f33f9-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33f9-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="f33f9-171">Requirements</span></span>



| <span data-ttu-id="f33f9-172">需求</span><span class="sxs-lookup"><span data-stu-id="f33f9-172">Requirement</span></span> | <span data-ttu-id="f33f9-173">值</span><span class="sxs-lookup"><span data-stu-id="f33f9-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f33f9-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f33f9-174">Minimum supported client</span></span><br/> | <span data-ttu-id="f33f9-175">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f33f9-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f33f9-176">Minimum supported server</span></span><br/> | <span data-ttu-id="f33f9-177">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f33f9-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f33f9-178">DLL</span><span class="sxs-lookup"><span data-stu-id="f33f9-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33f9-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33f9-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33f9-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f33f9-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33f9-181">**CheckRemoteDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="f33f9-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="f33f9-182">**GetProcessId**</span><span class="sxs-lookup"><span data-stu-id="f33f9-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="f33f9-183">**IsDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="f33f9-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="f33f9-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="f33f9-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
