---
description: 為指定的執行緒設定選取的 CPU 集合指派。 此指派會覆寫進程預設指派（如果有設定）。
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: 'SetThreadSelectedCpuSets 函式 (Processthreadapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849261"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="eee80-104">SetThreadSelectedCpuSets 函式</span><span class="sxs-lookup"><span data-stu-id="eee80-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="eee80-105">為指定的執行緒設定選取的 CPU 集合指派。</span><span class="sxs-lookup"><span data-stu-id="eee80-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="eee80-106">此指派會覆寫進程預設指派（如果有設定）。</span><span class="sxs-lookup"><span data-stu-id="eee80-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee80-107">語法</span><span class="sxs-lookup"><span data-stu-id="eee80-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="eee80-108">參數</span><span class="sxs-lookup"><span data-stu-id="eee80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee80-109">*執行緒* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eee80-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee80-110">指定要設定 CPU 集合指派的執行緒。</span><span class="sxs-lookup"><span data-stu-id="eee80-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="eee80-111">這個控制碼必須設定執行緒 \_ 的 \_ 有限 \_ 資訊存取權限。</span><span class="sxs-lookup"><span data-stu-id="eee80-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="eee80-112">也可以使用 [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) 傳回的值。</span><span class="sxs-lookup"><span data-stu-id="eee80-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="eee80-113">*CpuSetIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eee80-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee80-114">指定要設定為執行緒所選 CPU 集的 CPU 集識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="eee80-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="eee80-115">如果這是 Null，則 API 會清除任何指派，如果有設定，則會還原為處理預設指派。</span><span class="sxs-lookup"><span data-stu-id="eee80-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="eee80-116">*CpuSetIdCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eee80-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee80-117">指定在 **CpuSetIds** 引數中傳遞之清單中的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="eee80-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="eee80-118">如果該值為 Null，則應為0。</span><span class="sxs-lookup"><span data-stu-id="eee80-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee80-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="eee80-119">Return value</span></span>

<span data-ttu-id="eee80-120">傳遞的有效參數時，此函式不能失敗。</span><span class="sxs-lookup"><span data-stu-id="eee80-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee80-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eee80-121">Requirements</span></span>



| <span data-ttu-id="eee80-122">需求</span><span class="sxs-lookup"><span data-stu-id="eee80-122">Requirement</span></span> | <span data-ttu-id="eee80-123">值</span><span class="sxs-lookup"><span data-stu-id="eee80-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee80-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eee80-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eee80-125">Windows 10 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eee80-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="eee80-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eee80-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eee80-127">Windows Server 2016 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eee80-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="eee80-128">標頭</span><span class="sxs-lookup"><span data-stu-id="eee80-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee80-129"><dt>Processthreadsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee80-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="eee80-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="eee80-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eee80-131"><dt>Windows。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee80-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="eee80-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eee80-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee80-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eee80-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 
