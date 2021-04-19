---
description: 抓取 SetProcessDefaultCpuSets 所設定之進程預設集中的 CPU 集合清單。 如果未針對指定的進程設定預設的 CPU 集，則 RequiredIdCount 會設定為0，且函式會成功。
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: 'GetProcessDefaultCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001711"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="c1e7c-104">GetProcessDefaultCpuSets 函式</span><span class="sxs-lookup"><span data-stu-id="c1e7c-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="c1e7c-105">抓取 [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)所設定之進程預設集中的 CPU 集合清單。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="c1e7c-106">如果未針對指定的進程設定預設的 CPU 集，則 **RequiredIdCount** 會設定為0，且函式會成功。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e7c-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1e7c-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="c1e7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1e7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e7c-109">*進程* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e7c-110">指定要查詢之進程的進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="c1e7c-111">這個控制碼必須有「進程 \_ 查詢 \_ 限制的 \_ 資訊存取權」許可權。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="c1e7c-112">您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="c1e7c-113">*CpuSetIds* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e7c-114">指定一個選擇性的緩衝區，以抓取 CPU 組識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="c1e7c-115">*CpuSetIdCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e7c-116">指定 **CpuSetIds** 中指定之緩衝區的容量。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="c1e7c-117">如果緩衝區為 Null，則必須是0。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="c1e7c-118">*RequiredIdCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e7c-119">指定保留整個進程預設 CPU 集清單的緩衝區所需的容量。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="c1e7c-120">在成功傳回時，這會指定填入緩衝區的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e7c-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1e7c-121">Return value</span></span>

<span data-ttu-id="c1e7c-122">此 API 會在成功時傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-122">This API returns TRUE on success.</span></span> <span data-ttu-id="c1e7c-123">如果緩衝區不夠大，則 API 會傳回 FALSE，而 **GetLastError** 值是 \_ 緩衝區不足的錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="c1e7c-124">傳遞有效的參數且傳回緩衝區夠大時，此 API 無法失敗。</span><span class="sxs-lookup"><span data-stu-id="c1e7c-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e7c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1e7c-125">Requirements</span></span>



| <span data-ttu-id="c1e7c-126">需求</span><span class="sxs-lookup"><span data-stu-id="c1e7c-126">Requirement</span></span> | <span data-ttu-id="c1e7c-127">值</span><span class="sxs-lookup"><span data-stu-id="c1e7c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e7c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1e7c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e7c-129">Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="c1e7c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1e7c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e7c-131">Windows Server 2016 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e7c-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="c1e7c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c1e7c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e7c-133"><dt>Processthreadsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e7c-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c1e7c-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1e7c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1e7c-135"><dt>Windows。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e7c-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="c1e7c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c1e7c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1e7c-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1e7c-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

