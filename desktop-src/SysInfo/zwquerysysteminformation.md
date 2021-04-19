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
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="808d0-103">ZwQuerySystemInformation 函式</span><span class="sxs-lookup"><span data-stu-id="808d0-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="808d0-104">\[**ZwQuerySystemInformation** 不再提供 Windows 8 使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="808d0-105">相反地，請使用本主題中所列的替代函數。\]</span><span class="sxs-lookup"><span data-stu-id="808d0-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="808d0-106">捕獲指定的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="808d0-107">語法</span><span class="sxs-lookup"><span data-stu-id="808d0-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="808d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="808d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="808d0-109">*SystemInformationClass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="808d0-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808d0-110">要取出的系統資訊類型。</span><span class="sxs-lookup"><span data-stu-id="808d0-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="808d0-111">這個參數可以是 **系統 \_ 資訊 \_ 類別** 列舉類型中的下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="808d0-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="808d0-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-113">系統 **\_ 基本 \_ 資訊** 結構中的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="808d0-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="808d0-114">請改用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="808d0-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-116">不透明的 **系統 \_ 效能 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-117">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="808d0-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-119">不透明的 **系統 \_ TIMEOFDAY \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-120">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="808d0-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-122">**系統 \_ 進程 \_ 資訊** 結構的陣列，在系統中執行的每個進程各一個陣列。</span><span class="sxs-lookup"><span data-stu-id="808d0-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="808d0-123">這些結構包含每個進程的資源使用方式的相關資訊，包括進程使用的控制碼數目、尖峰分頁檔案使用方式，以及處理常式已配置的記憶體分頁數目。</span><span class="sxs-lookup"><span data-stu-id="808d0-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="808d0-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-125">**系統 \_ 處理器 \_ 效能 \_ 資訊** 結構的陣列，系統中安裝的每個處理器各一個。</span><span class="sxs-lookup"><span data-stu-id="808d0-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="808d0-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-127">不透明的 **系統 \_ 中斷 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-128">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="808d0-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-130">不透明的 **系統 \_ 例外狀況 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-131">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="808d0-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-133">**系統 \_ 註冊表 \_ 配額 \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="808d0-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="808d0-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span><span class="sxs-lookup"><span data-stu-id="808d0-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-135">不透明的 **系統 \_ 對應 \_ 資訊** 結構，可用來針對亂數產生器產生無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-136">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數。</span><span class="sxs-lookup"><span data-stu-id="808d0-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="808d0-137">*SystemInformation* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="808d0-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="808d0-138">接收所要求資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="808d0-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="808d0-139">這項資訊的大小與結構會根據 *SystemInformationClass* 參數的值而有所不同，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="808d0-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="808d0-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**系統 \_ 基本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-141">**SystemBasicInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **系統 \_ 基本 \_ 資訊** 結構：</span><span class="sxs-lookup"><span data-stu-id="808d0-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="808d0-142">**NumberOfProcessors** 成員包含存在於系統中的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="808d0-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="808d0-143">請改用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="808d0-144">結構的其他成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="808d0-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**系統 \_ 效能 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-146">**SystemPerformanceInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ 效能 \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-147">基於這個目的，此結構具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="808d0-148">結構的個別成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="808d0-149">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。</span><span class="sxs-lookup"><span data-stu-id="808d0-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="808d0-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**系統 \_ TIMEOFDAY \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-151">**SystemTimeOfDayInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ TIMEOFDAY \_ 資訊** 結構，以用於產生亂數產生器不可預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-152">基於這個目的，此結構具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="808d0-153">結構的個別成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="808d0-154">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。</span><span class="sxs-lookup"><span data-stu-id="808d0-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="808d0-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**系統 \_ 進程 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-156">**SystemProcessInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納包含許多 **系統 \_ 進程 \_ 資訊** 結構的陣列，就像系統中執行的進程一樣。</span><span class="sxs-lookup"><span data-stu-id="808d0-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="808d0-157">每個結構都有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-157">Each structure has the following layout:</span></span>

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

<span data-ttu-id="808d0-158">**NumberOfThreads** 成員包含進程中目前正在執行的執行緒總數。</span><span class="sxs-lookup"><span data-stu-id="808d0-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="808d0-159">**HandleCount** 成員包含有問題的進程所使用的控制碼總數;請改用 [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="808d0-160">**PeakPagefileUsage** 成員包含處理常式所使用之分頁檔儲存體的最大位元組數目，而 **PrivatePageCount** 成員包含配置給此進程使用的記憶體分頁數目。</span><span class="sxs-lookup"><span data-stu-id="808d0-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="808d0-161">您也可以使用 [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) 函式或 [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) 類別來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="808d0-162">結構的其他成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="808d0-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**系統 \_ 處理器 \_ 效能 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-164">當 *SystemInformationClass* 參數為 **SystemProcessorPerformanceInformation** 時， *SystemInformation* 參數所指向的緩衝區應該夠大到足以容納包含許多 **系統 \_ 進程 \_ 資訊** 結構的陣列，因為系統中已安裝處理器 (的 cpu) 。</span><span class="sxs-lookup"><span data-stu-id="808d0-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="808d0-165">每個結構都有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-165">Each structure has the following layout:</span></span>

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

<span data-ttu-id="808d0-166">**IdleTime** 成員包含系統閒置的時間量，以 1/100ths 的毫微秒數表示。</span><span class="sxs-lookup"><span data-stu-id="808d0-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="808d0-167">**KernelTime** 成員包含系統在核心模式下執行所花費的時間量 (包括所有進程中的所有線程、所有處理器) ，以及 1/100ths 的毫微秒數。</span><span class="sxs-lookup"><span data-stu-id="808d0-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="808d0-168">**UserTime** 成員包含系統在使用者模式下執行的時間量 (包括所有進程中的所有線程、所有處理器) ，以及 1/100ths 的毫微秒數。</span><span class="sxs-lookup"><span data-stu-id="808d0-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="808d0-169">請改用 [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) 來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="808d0-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**系統 \_ 中斷 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-171">**SystemInterruptInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大到足以容納包含許多不透明 **系統 \_ 中斷 \_ 資訊** 結構的陣列，因為系統上已安裝處理器 (cpu) 。</span><span class="sxs-lookup"><span data-stu-id="808d0-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="808d0-172">每一個結構或整個陣列都可用來產生亂數產生器無法預測的種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-173">基於這個目的，此結構具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="808d0-174">結構的個別成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="808d0-175">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。</span><span class="sxs-lookup"><span data-stu-id="808d0-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="808d0-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**系統 \_ 例外狀況 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-177">**SystemExceptionInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統例外狀況 \_ \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-178">基於這個目的，此結構具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="808d0-179">結構的個別成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="808d0-180">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。</span><span class="sxs-lookup"><span data-stu-id="808d0-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="808d0-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**系統 \_ 註冊表 \_ 配額 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-182">**SystemRegistryQuotaInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大，足以容納具有下列配置的單一 **系統 \_ 註冊表 \_ 配額 \_ 資訊** 結構：</span><span class="sxs-lookup"><span data-stu-id="808d0-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="808d0-183">**RegistryQuotaAllowed** 成員包含登錄可在此系統上達到的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="808d0-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="808d0-184">**RegistryQuotaUsed** 成員包含目前的登錄大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="808d0-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="808d0-185">請改用 [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) 來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="808d0-186">結構的另一個成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="808d0-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**系統 \_ 對應 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="808d0-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="808d0-188">**SystemLookasideInformation** *SystemInformationClass* 參數時， *SystemInformation* 參數所指向的緩衝區應該夠大以容納不透明的 **系統 \_ 對應 \_ 資訊** 結構，以用於產生亂數產生器的無法預測種子。</span><span class="sxs-lookup"><span data-stu-id="808d0-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="808d0-189">基於這個目的，此結構具有下列版面配置：</span><span class="sxs-lookup"><span data-stu-id="808d0-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="808d0-190">結構的個別成員是保留供作業系統內部使用。</span><span class="sxs-lookup"><span data-stu-id="808d0-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="808d0-191">請改用 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 函數來產生密碼編譯亂數據。</span><span class="sxs-lookup"><span data-stu-id="808d0-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="808d0-192">*SystemInformationLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="808d0-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808d0-193">*SystemInformation* 參數所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="808d0-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="808d0-194">*ReturnLength* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="808d0-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="808d0-195">位置的選擇性指標，函式會寫入所要求資訊的實際大小。</span><span class="sxs-lookup"><span data-stu-id="808d0-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="808d0-196">如果該大小小於或等於 *SystemInformationLength* 參數，則函式會將資訊複製到 *SystemInformation* 緩衝區;否則，它會傳回一個 NTSTATUS 錯誤碼，並在 *ReturnLength* 中傳回所需的緩衝區大小，以接收要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="808d0-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="808d0-197">傳回值</span><span class="sxs-lookup"><span data-stu-id="808d0-197">Return value</span></span>

<span data-ttu-id="808d0-198">傳回 NTSTATUS 成功或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="808d0-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="808d0-199">在 DDK 提供的 Ntstatus 標頭檔中，會列出 NTSTATUS 錯誤碼的形式和重要性，並在 DDK 檔中說明。</span><span class="sxs-lookup"><span data-stu-id="808d0-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="808d0-200">備註</span><span class="sxs-lookup"><span data-stu-id="808d0-200">Remarks</span></span>

<span data-ttu-id="808d0-201">**ZwQuerySystemInformation** 函式和它所傳回的結構是作業系統的內部，而且可能會從某個 Windows 版本變更為另一個。</span><span class="sxs-lookup"><span data-stu-id="808d0-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="808d0-202">為了維持應用程式的相容性，最好改用先前提及的替代函式。</span><span class="sxs-lookup"><span data-stu-id="808d0-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="808d0-203">如果您使用 **ZwQuerySystemInformation**，可透過 [執行時間動態連結](/windows/desktop/Dlls/using-run-time-dynamic-linking)存取函式。</span><span class="sxs-lookup"><span data-stu-id="808d0-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="808d0-204">這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。</span><span class="sxs-lookup"><span data-stu-id="808d0-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="808d0-205">不過，簽章變更可能無法偵測。</span><span class="sxs-lookup"><span data-stu-id="808d0-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="808d0-206">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="808d0-206">This function has no associated import library.</span></span> <span data-ttu-id="808d0-207">您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="808d0-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="808d0-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="808d0-208">Requirements</span></span>



| <span data-ttu-id="808d0-209">需求</span><span class="sxs-lookup"><span data-stu-id="808d0-209">Requirement</span></span> | <span data-ttu-id="808d0-210">值</span><span class="sxs-lookup"><span data-stu-id="808d0-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="808d0-211">DLL</span><span class="sxs-lookup"><span data-stu-id="808d0-211">DLL</span></span><br/> | <dl> <span data-ttu-id="808d0-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="808d0-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="808d0-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="808d0-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808d0-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="808d0-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="808d0-215">**GetProcessHandleCount**</span><span class="sxs-lookup"><span data-stu-id="808d0-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="808d0-216">**GetProcessMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="808d0-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="808d0-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="808d0-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="808d0-218">**GetSystemRegistryQuota**</span><span class="sxs-lookup"><span data-stu-id="808d0-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

