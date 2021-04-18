---
description: 允許應用程式查詢系統上可用的 CPU 集，以及其目前的狀態。
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: 'GetSystemCpuSetInformation 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192761"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="13a5c-103">GetSystemCpuSetInformation 函式</span><span class="sxs-lookup"><span data-stu-id="13a5c-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="13a5c-104">允許應用程式查詢系統上可用的 CPU 集，以及其目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="13a5c-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a5c-105">語法</span><span class="sxs-lookup"><span data-stu-id="13a5c-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="13a5c-106">參數</span><span class="sxs-lookup"><span data-stu-id="13a5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a5c-107">*資訊* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13a5c-108">[**系統 \_ cpu \_ 集合 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)結構的指標，此結構會接收 cpu 集資料。</span><span class="sxs-lookup"><span data-stu-id="13a5c-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="13a5c-109">以緩衝區長度0傳遞 Null，以決定所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="13a5c-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="13a5c-110">*BufferLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a5c-111">以位元組為單位的輸出緩衝區長度（以位元組為單位），以資訊引數形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="13a5c-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="13a5c-112">*ReturnedLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13a5c-113">輸出緩衝區中有效資料的長度（以位元組為單位），如果緩衝區夠大或需要輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="13a5c-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="13a5c-114">如果沒有任何 CPU 集存在，此值會是0。</span><span class="sxs-lookup"><span data-stu-id="13a5c-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="13a5c-115">*進程* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13a5c-116">進程的選擇性控制碼。</span><span class="sxs-lookup"><span data-stu-id="13a5c-116">An optional handle to a process.</span></span> <span data-ttu-id="13a5c-117">此程式是用來判斷系統 \_ CPU \_ 集資訊結構中 AllocatedToTargetProcess 旗標的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13a5c-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="13a5c-118">如果將 CPU 集合配置給指定的進程，就會設定旗標。</span><span class="sxs-lookup"><span data-stu-id="13a5c-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="13a5c-119">否則，它是明確的。</span><span class="sxs-lookup"><span data-stu-id="13a5c-119">Otherwise, it is clear.</span></span> <span data-ttu-id="13a5c-120">這個控制碼必須有「進程 \_ 查詢 \_ 限制的 \_ 資訊存取權」許可權。</span><span class="sxs-lookup"><span data-stu-id="13a5c-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="13a5c-121">您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="13a5c-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="13a5c-122">*旗標*</span><span class="sxs-lookup"><span data-stu-id="13a5c-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="13a5c-123">保留，必須是0。</span><span class="sxs-lookup"><span data-stu-id="13a5c-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a5c-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a5c-124">Return value</span></span>

<span data-ttu-id="13a5c-125">如果 API 成功，則會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="13a5c-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="13a5c-126">如果失敗，則可透過 **GetLastError** 取得錯誤原因。</span><span class="sxs-lookup"><span data-stu-id="13a5c-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="13a5c-127">如果資訊緩衝區為 Null 或不夠大，則會傳回錯誤碼錯誤的 \_ \_ 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13a5c-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="13a5c-128">當傳遞有效的參數和足以容納所有傳回資料的緩衝區時，此 API 無法失敗。</span><span class="sxs-lookup"><span data-stu-id="13a5c-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a5c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a5c-129">Requirements</span></span>



| <span data-ttu-id="13a5c-130">需求</span><span class="sxs-lookup"><span data-stu-id="13a5c-130">Requirement</span></span> | <span data-ttu-id="13a5c-131">值</span><span class="sxs-lookup"><span data-stu-id="13a5c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a5c-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13a5c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="13a5c-133">Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="13a5c-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13a5c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="13a5c-135">Windows Server 2016 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a5c-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="13a5c-136">標頭</span><span class="sxs-lookup"><span data-stu-id="13a5c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a5c-137"><dt>Processthreadsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="13a5c-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="13a5c-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="13a5c-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="13a5c-139"><dt>Windows。h</dt></span><span class="sxs-lookup"><span data-stu-id="13a5c-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="13a5c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="13a5c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a5c-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a5c-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

