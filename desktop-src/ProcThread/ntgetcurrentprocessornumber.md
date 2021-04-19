---
description: 在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987927"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="27b28-103">NtGetCurrentProcessorNumber 函式</span><span class="sxs-lookup"><span data-stu-id="27b28-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="27b28-104">\[**NtGetCurrentProcessorNumber** 可能會在未來的 Windows 版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="27b28-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="27b28-105">應用程式應該改用 [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) 函數。\]</span><span class="sxs-lookup"><span data-stu-id="27b28-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="27b28-106">在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="27b28-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="27b28-107">語法</span><span class="sxs-lookup"><span data-stu-id="27b28-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="27b28-108">參數</span><span class="sxs-lookup"><span data-stu-id="27b28-108">Parameters</span></span>

<span data-ttu-id="27b28-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="27b28-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27b28-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="27b28-110">Return value</span></span>

<span data-ttu-id="27b28-111">函數會傳回目前的處理器號碼。</span><span class="sxs-lookup"><span data-stu-id="27b28-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="27b28-112">備註</span><span class="sxs-lookup"><span data-stu-id="27b28-112">Remarks</span></span>

<span data-ttu-id="27b28-113">此函數是用來提供用來評估進程效能的資訊。</span><span class="sxs-lookup"><span data-stu-id="27b28-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="27b28-114">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="27b28-114">This function has no associated import library.</span></span> <span data-ttu-id="27b28-115">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Ntdll.dll。</span><span class="sxs-lookup"><span data-stu-id="27b28-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="27b28-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="27b28-116">Requirements</span></span>



| <span data-ttu-id="27b28-117">需求</span><span class="sxs-lookup"><span data-stu-id="27b28-117">Requirement</span></span> | <span data-ttu-id="27b28-118">值</span><span class="sxs-lookup"><span data-stu-id="27b28-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="27b28-119">DLL</span><span class="sxs-lookup"><span data-stu-id="27b28-119">DLL</span></span><br/> | <dl> <span data-ttu-id="27b28-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27b28-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27b28-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27b28-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27b28-122">多個處理器</span><span class="sxs-lookup"><span data-stu-id="27b28-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="27b28-123">處理序和執行緒函式</span><span class="sxs-lookup"><span data-stu-id="27b28-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="27b28-124">處理序</span><span class="sxs-lookup"><span data-stu-id="27b28-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
