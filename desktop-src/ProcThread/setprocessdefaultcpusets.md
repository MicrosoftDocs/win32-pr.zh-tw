---
description: 針對指定進程中的執行緒，設定預設的 CPU 集合指派。 建立的執行緒如果沒有使用 SetThreadSelectedCpuSets 明確設定的 CPU 集，將會自動繼承 SetProcessDefaultCpuSets 所指定的集合。
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: 'SetProcessDefaultCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993127"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="37708-104">SetProcessDefaultCpuSets 函式</span><span class="sxs-lookup"><span data-stu-id="37708-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="37708-105">針對指定進程中的執行緒，設定預設的 CPU 集合指派。</span><span class="sxs-lookup"><span data-stu-id="37708-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="37708-106">建立的執行緒如果沒有使用 [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)明確設定的 CPU 集，將會自動繼承 **SetProcessDefaultCpuSets** 所指定的集合。</span><span class="sxs-lookup"><span data-stu-id="37708-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="37708-107">語法</span><span class="sxs-lookup"><span data-stu-id="37708-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="37708-108">參數</span><span class="sxs-lookup"><span data-stu-id="37708-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37708-109">*進程* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37708-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37708-110">指定要設定預設 CPU 集的進程。</span><span class="sxs-lookup"><span data-stu-id="37708-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="37708-111">這個控制碼必須有進程 \_ 集的 \_ 有限 \_ 資訊存取權限。</span><span class="sxs-lookup"><span data-stu-id="37708-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="37708-112">您也可以在這裡指定 [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="37708-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="37708-113">*CpuSetIds* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="37708-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37708-114">指定要設定為進程預設 CPU 集的 CPU 集識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="37708-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="37708-115">如果這是 Null，則 **SetProcessDefaultCpuSets** 會清除任何指派。</span><span class="sxs-lookup"><span data-stu-id="37708-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="37708-116">*CpuSetIdCound* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37708-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37708-117">指定在 **CpuSetIds** 引數中傳遞之清單中的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="37708-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="37708-118">如果該值為 Null，則應為0。</span><span class="sxs-lookup"><span data-stu-id="37708-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37708-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="37708-119">Return value</span></span>

<span data-ttu-id="37708-120">傳遞的有效參數時，此函式不能失敗。</span><span class="sxs-lookup"><span data-stu-id="37708-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="37708-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="37708-121">Requirements</span></span>



| <span data-ttu-id="37708-122">需求</span><span class="sxs-lookup"><span data-stu-id="37708-122">Requirement</span></span> | <span data-ttu-id="37708-123">值</span><span class="sxs-lookup"><span data-stu-id="37708-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37708-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37708-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37708-125">Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37708-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="37708-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37708-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37708-127">Windows Server 2016 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37708-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="37708-128">標頭</span><span class="sxs-lookup"><span data-stu-id="37708-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="37708-129"><dt>Processthreadsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="37708-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="37708-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="37708-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="37708-131"><dt>Windows。h</dt></span><span class="sxs-lookup"><span data-stu-id="37708-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="37708-132">DLL</span><span class="sxs-lookup"><span data-stu-id="37708-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37708-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37708-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
