---
title: GetProcessHandleFromHwnd 函式
description: 從視窗控制碼抓取進程控制碼。
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- GetProcessHandleFromHwnd 函式 Windows 協助工具
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103818"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="3a5b7-104">GetProcessHandleFromHwnd 函式</span><span class="sxs-lookup"><span data-stu-id="3a5b7-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="3a5b7-105">從視窗控制碼抓取進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5b7-106">語法</span><span class="sxs-lookup"><span data-stu-id="3a5b7-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="3a5b7-107">參數</span><span class="sxs-lookup"><span data-stu-id="3a5b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5b7-108">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a5b7-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5b7-109">類型： **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a5b7-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a5b7-110">視窗控制代碼 (Window Handle)。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5b7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a5b7-111">Return value</span></span>

<span data-ttu-id="3a5b7-112">類型： **[**控制碼**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a5b7-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a5b7-113">如果成功，會傳回擁有視窗之進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="3a5b7-114">如果不成功，則傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5b7-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a5b7-115">Remarks</span></span>

<span data-ttu-id="3a5b7-116">在舊版作業系統中，進程可以開啟另一個進程 (存取其記憶體，例如) 使用 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="3a5b7-117">如果呼叫端具有適當的許可權，則此函式會成功;呼叫端和目標進程通常必須是相同的使用者。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="3a5b7-118">不過，在 Windows Vista 中， [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) 會在呼叫端具有 UIAccess 的情況下失敗，並提高目標進程的許可權。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="3a5b7-119">在此情況下，目標進程的擁有者是在 Administrators 群組中，但呼叫進程正在以受限制的權杖執行，因此沒有此群組的成員資格，而且會被拒絕存取提升的進程。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="3a5b7-120">但是，如果呼叫端具有 UIAccess，則可以使用 windows 攔截將程式碼插入目標進程，然後從目標進程內，將控制碼傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="3a5b7-121">**GetProcessHandleFromHwnd** 是一個便利的函式，它會使用這項技術來取得擁有指定 HWND 之進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="3a5b7-122">請注意，只有在呼叫端和目標進程以相同使用者的形式執行時，才會成功。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="3a5b7-123">傳回的控制碼具有下列許可權：進程 \_ 重複 \_ 處理 \| 進程 \_ vm \_ 作業 \| 進程 vm \_ 讀取程式 \_ \| \_ vm \_ 寫入 \| 同步處理。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="3a5b7-124">如果需要其他許可權，則可能需要明確地執行攔截技術，而不是使用此函數。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5b7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a5b7-125">Requirements</span></span>



| <span data-ttu-id="3a5b7-126">需求</span><span class="sxs-lookup"><span data-stu-id="3a5b7-126">Requirement</span></span> | <span data-ttu-id="3a5b7-127">值</span><span class="sxs-lookup"><span data-stu-id="3a5b7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5b7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a5b7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5b7-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b7-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a5b7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a5b7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5b7-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b7-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a5b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5b7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5b7-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5b7-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

