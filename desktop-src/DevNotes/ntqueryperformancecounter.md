---
description: 傳回效能計數器的目前值，並選擇性地傳回效能計數器的頻率。
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977461"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="ff9aa-103">NtQueryPerformanceCounter 函式</span><span class="sxs-lookup"><span data-stu-id="ff9aa-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="ff9aa-104">\[這項功能不受支援，因此不應該使用。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="ff9aa-105">請改用 **QueryPerformanceCounter** 和 **QueryPerformanceFrequency** 函數。\]</span><span class="sxs-lookup"><span data-stu-id="ff9aa-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="ff9aa-106">傳回效能計數器的目前值，並選擇性地傳回效能計數器的頻率。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9aa-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff9aa-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="ff9aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff9aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff9aa-109">*PerformanceCounter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ff9aa-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9aa-110">要接收目前效能計數器值的變數位址。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="ff9aa-111">*PerformanceFrequency* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="ff9aa-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9aa-112">要接收效能計數器頻率之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff9aa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff9aa-113">Return value</span></span>

<span data-ttu-id="ff9aa-114">如果函式成功，它會傳回「 **NTSTATUS** 程式碼」 **狀態 \_ 成功**; 否則，它會傳回錯誤代碼，例如 **狀態 \_ 存取 \_ 違規**。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff9aa-115">備註</span><span class="sxs-lookup"><span data-stu-id="ff9aa-115">Remarks</span></span>

<span data-ttu-id="ff9aa-116">沒有適用于 **NtQueryPerformanceCounter** 的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="ff9aa-117">雖然您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至 Ntdll.dll，但您應該使用上述替代函數。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="ff9aa-118">效能頻率是效能計數器的頻率（以赫茲為單位），特別是每秒的計數。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="ff9aa-119">此值與實值相依。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-119">This value is implementation dependent.</span></span> <span data-ttu-id="ff9aa-120">如果實值沒有硬體可支援效能時間，則傳回的值為0。</span><span class="sxs-lookup"><span data-stu-id="ff9aa-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9aa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff9aa-121">Requirements</span></span>



| <span data-ttu-id="ff9aa-122">需求</span><span class="sxs-lookup"><span data-stu-id="ff9aa-122">Requirement</span></span> | <span data-ttu-id="ff9aa-123">值</span><span class="sxs-lookup"><span data-stu-id="ff9aa-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9aa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ff9aa-124">DLL</span></span><br/> | <dl> <span data-ttu-id="ff9aa-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff9aa-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff9aa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff9aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9aa-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="ff9aa-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="ff9aa-128">**QueryPerformanceFrequency**</span><span class="sxs-lookup"><span data-stu-id="ff9aa-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
