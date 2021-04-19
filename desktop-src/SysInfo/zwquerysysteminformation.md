---
description: 捕獲指定的系統資訊。
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: ZwQuerySystemInformation 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989648"
---
# <a name="zwquerysysteminformation-function"></a>ZwQuerySystemInformation 函式

\[**ZwQuerySystemInformation** 不再提供 Windows 8 使用。 相反地，請使用本主題中所列的替代函數。\]

捕獲指定的系統資訊。

## <a name="syntax"></a>語法


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SystemInformationClass* \[在\]
</dt> <dd>

要取出的系統資訊類型。 這個參數可以是 **系統 \_ 資訊 \_ 類別** 列舉類型中的下列其中一個值。

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

系統 **\_ 基本 \_ 資訊** 結構中的處理器數目。 請改用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

不透明的 **系統 \_ 效能 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。 請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

不透明的 **系統 \_ TIMEOFDAY \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。 請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

**系統 \_ 進程 \_ 資訊** 結構的陣列，在系統中執行的每個進程各一個陣列。

這些結構包含每個進程的資源使用方式的相關資訊，包括進程使用的控制碼數目、尖峰分頁檔案使用方式，以及處理常式已配置的記憶體分頁數目。

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

**系統 \_ 處理器 \_ 效能 \_ 資訊** 結構的陣列，系統中安裝的每個處理器各一個。

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

不透明的 **系統 \_ 中斷 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。 請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

不透明的 **系統 \_ 例外狀況 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。 請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

**系統 \_ 註冊表 \_ 配額 \_ 資訊** 結構。

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

不透明的 **系統 \_ 對應 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。 請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。

</dd> </dl> </dd> <dt>

*SystemInformation* \[in、out\]
</dt> <dd>

接收所要求資訊的緩衝區指標。 這項資訊的大小與結構會根據 *SystemInformationClass* 參數的值而有所不同，如下表所示。

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**系統 \_ 基本 \_ 資訊**


</dt> <dd>

**SystemBasicInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **系統 \_ 基本 \_ 資訊** 結構：

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

**NumberOfProcessors** 成員包含存在於系統中的處理器數目。 請改用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 來取得此資訊。

結構的其他成員是保留供作業系統內部使用。

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**系統 \_ 效能 \_ 資訊**


</dt> <dd>

**SystemPerformanceInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ 效能 \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。 基於這個目的，此結構具有下列版面配置：

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

結構的個別成員是保留供作業系統內部使用。

請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**系統 \_ TIMEOFDAY \_ 資訊**


</dt> <dd>

**SystemTimeOfDayInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ TIMEOFDAY \_ 資訊** 結構，以用於產生亂數產生器不可預測的種子。 基於這個目的，此結構具有下列版面配置：

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

結構的個別成員是保留供作業系統內部使用。

請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**系統 \_ 進程 \_ 資訊**


</dt> <dd>

**SystemProcessInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納包含許多 **系統 \_ 進程 \_ 資訊** 結構的陣列，就像系統中執行的進程一樣。 每個結構都有下列版面配置：

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

**NumberOfThreads** 成員包含進程中目前正在執行的執行緒總數。

**HandleCount** 成員包含有問題的進程所使用的控制碼總數;請改用 [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)來取得此資訊。

**PeakPagefileUsage** 成員包含處理常式所使用之分頁檔儲存體的最大位元組數目，而 **PrivatePageCount** 成員包含配置給此進程使用的記憶體分頁數目。

您也可以使用 [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) 函式或 [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) 類別來取得此資訊。

結構的其他成員是保留供作業系統內部使用。

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**系統 \_ 處理器 \_ 效能 \_ 資訊**


</dt> <dd>

當 *SystemInformationClass* 參數為 **SystemProcessorPerformanceInformation** 時， *SystemInformation* 參數所指向的緩衝區應該夠大到足以容納包含許多 **系統 \_ 進程 \_ 資訊** 結構的陣列，因為系統中已安裝處理器 (的 cpu) 。 每個結構都有下列版面配置：

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

**IdleTime** 成員包含系統閒置的時間量，以 1/100ths 的毫微秒數表示。

**KernelTime** 成員包含系統在核心模式下執行所花費的時間量 (包括所有進程中的所有線程、所有處理器) ，以及 1/100ths 的毫微秒數。

**UserTime** 成員包含系統在使用者模式下執行的時間量 (包括所有進程中的所有線程、所有處理器) ，以及 1/100ths 的毫微秒數。

請改用 [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) 來取得此資訊。

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**系統 \_ 中斷 \_ 資訊**


</dt> <dd>

**SystemInterruptInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大到足以容納包含許多不透明 **系統 \_ 中斷 \_ 資訊** 結構的陣列，因為系統上已安裝處理器 (cpu) 。 每一個結構或整個陣列都可用來產生亂數產生器無法預測的種子。 基於這個目的，此結構具有下列版面配置：

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

結構的個別成員是保留供作業系統內部使用。

請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**系統 \_ 例外狀況 \_ 資訊**


</dt> <dd>

**SystemExceptionInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統例外狀況 \_ \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。 基於這個目的，此結構具有下列版面配置：

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

結構的個別成員是保留供作業系統內部使用。

請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**系統 \_ 註冊表 \_ 配額 \_ 資訊**


</dt> <dd>

**SystemRegistryQuotaInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **系統 \_ 註冊表 \_ 配額 \_ 資訊** 結構：

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

**RegistryQuotaAllowed** 成員包含登錄可在此系統上達到的大小上限（以位元組為單位）。

**RegistryQuotaUsed** 成員包含目前的登錄大小（以位元組為單位）。

請改用 [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) 來取得此資訊。

結構的另一個成員是保留供作業系統內部使用。

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**系統 \_ 對應 \_ 資訊**


</dt> <dd>

**SystemLookasideInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ 對應 \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。 基於這個目的，此結構具有下列版面配置：

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

結構的個別成員是保留供作業系統內部使用。

請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[在\]
</dt> <dd>

*SystemInformation* 參數所指向的緩衝區大小（以位元組為單位）。

</dd> <dt>

*ReturnLength* \[out、optional\]
</dt> <dd>

位置的選擇性指標，函式會寫入所要求資訊的實際大小。 如果該大小小於或等於 *SystemInformationLength* 參數，則函式會將資訊複製到 *SystemInformation* 緩衝區;否則，它會傳回一個 NTSTATUS 錯誤碼，並在 *ReturnLength* 中傳回所需的緩衝區大小，以接收要求的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 NTSTATUS 成功或錯誤碼。

在 DDK 提供的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的形式和重要性，並在 DDK 檔中說明。

## <a name="remarks"></a>備註

**ZwQuerySystemInformation** 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。 為了維持應用程式的相容性，最好改用先前提及的替代函式。

如果您使用 **ZwQuerySystemInformation**，可透過 [執行時間動態連結](/windows/desktop/Dlls/using-run-time-dynamic-linking)存取函式。 這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。 不過，簽章變更可能無法偵測。

此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

