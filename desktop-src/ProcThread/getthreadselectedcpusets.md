---
description: 如果已使用 SetThreadSelectedCpuSets API 設定任何指派，則會傳回指定執行緒的明確 CPU 集指派。 如果未設定明確指派，RequiredIdCount 會設為0，且函數會傳回 TRUE。
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: 'GetThreadSelectedCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026748"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="cd937-104">GetThreadSelectedCpuSets 函式</span><span class="sxs-lookup"><span data-stu-id="cd937-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="cd937-105">如果已使用 [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API 設定任何指派，則會傳回指定執行緒的明確 CPU 集指派。</span><span class="sxs-lookup"><span data-stu-id="cd937-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="cd937-106">如果未設定明確指派， **RequiredIdCount** 會設為0，且函數會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="cd937-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd937-107">語法</span><span class="sxs-lookup"><span data-stu-id="cd937-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="cd937-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd937-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd937-109">*執行緒* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd937-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd937-110">指定要查詢所選 CPU 集的執行緒。</span><span class="sxs-lookup"><span data-stu-id="cd937-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="cd937-111">這個控制碼的 \_ 存取權必須限制為執行緒查詢的 \_ 有限 \_ 資訊。</span><span class="sxs-lookup"><span data-stu-id="cd937-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="cd937-112">您也可以在這裡指定 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="cd937-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="cd937-113">*CpuSetIds* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="cd937-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd937-114">指定一個選擇性的緩衝區，以抓取 CPU 組識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="cd937-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cd937-115">*CpuSetIdCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd937-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd937-116">指定 **CpuSetIds** 中指定之緩衝區的容量。</span><span class="sxs-lookup"><span data-stu-id="cd937-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="cd937-117">如果緩衝區為 Null，則必須是0。</span><span class="sxs-lookup"><span data-stu-id="cd937-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="cd937-118">*RequiredIdCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd937-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd937-119">指定緩衝區的必要容量，以保存完整的執行緒選取的 CPU 集合清單。</span><span class="sxs-lookup"><span data-stu-id="cd937-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="cd937-120">在成功傳回時，這會指定填入緩衝區的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="cd937-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd937-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd937-121">Return value</span></span>

<span data-ttu-id="cd937-122">此 API 會在成功時傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="cd937-122">This API returns TRUE on success.</span></span> <span data-ttu-id="cd937-123">如果緩衝區不夠大，則 **GetLastError** 值是緩衝區不足的錯誤 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="cd937-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="cd937-124">傳遞有效的參數且傳回緩衝區夠大時，此 API 無法失敗。</span><span class="sxs-lookup"><span data-stu-id="cd937-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd937-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd937-125">Requirements</span></span>



| <span data-ttu-id="cd937-126">需求</span><span class="sxs-lookup"><span data-stu-id="cd937-126">Requirement</span></span> | <span data-ttu-id="cd937-127">值</span><span class="sxs-lookup"><span data-stu-id="cd937-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd937-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd937-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd937-129">Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd937-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="cd937-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd937-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd937-131">Windows Server 2016 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd937-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="cd937-132">標頭</span><span class="sxs-lookup"><span data-stu-id="cd937-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd937-133"><dt>Processthreadsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd937-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="cd937-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd937-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd937-135"><dt>Windows。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd937-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="cd937-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd937-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd937-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd937-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

