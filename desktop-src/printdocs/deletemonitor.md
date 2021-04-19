---
description: DeleteMonitor 函式會移除 AddMonitor 函數所新增的埠監視器。
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: 'DeleteMonitor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996715"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="4bc7c-103">DeleteMonitor 函式</span><span class="sxs-lookup"><span data-stu-id="4bc7c-103">DeleteMonitor function</span></span>

<span data-ttu-id="4bc7c-104">**DeleteMonitor** 函式會移除 [**AddMonitor**](addmonitor.md)函數所新增的埠監視器。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bc7c-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="4bc7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bc7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc7c-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc7c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc7c-108">以 null 結束的字串指標，指定要移除監視的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="4bc7c-109">如果此參數為 **Null**，則會在本機移除埠監視器。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="4bc7c-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc7c-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc7c-111">以 null 結束的字串指標，指定要移除監視的環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="4bc7c-112">如果此參數為 **Null**，則會從目前的呼叫應用程式和用戶端電腦的環境中移除監視， (不是目的地應用程式和列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="4bc7c-113">*pMonitorName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bc7c-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc7c-114">以 null 結束的字串指標，指定要移除之監視的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc7c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bc7c-115">Return value</span></span>

<span data-ttu-id="4bc7c-116">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4bc7c-117">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bc7c-118">備註</span><span class="sxs-lookup"><span data-stu-id="4bc7c-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4bc7c-119">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4bc7c-120">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4bc7c-121">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4bc7c-122">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="4bc7c-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc7c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bc7c-123">Requirements</span></span>



| <span data-ttu-id="4bc7c-124">需求</span><span class="sxs-lookup"><span data-stu-id="4bc7c-124">Requirement</span></span> | <span data-ttu-id="4bc7c-125">值</span><span class="sxs-lookup"><span data-stu-id="4bc7c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc7c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bc7c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc7c-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bc7c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4bc7c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bc7c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc7c-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bc7c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4bc7c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="4bc7c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bc7c-131"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4bc7c-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4bc7c-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bc7c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bc7c-133"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bc7c-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4bc7c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc7c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc7c-135"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="4bc7c-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4bc7c-136">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4bc7c-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4bc7c-137">**DeleteMonitorW** (Unicode) 和 **DeleteMonitorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4bc7c-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="4bc7c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bc7c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc7c-139">列印</span><span class="sxs-lookup"><span data-stu-id="4bc7c-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4bc7c-140">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="4bc7c-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4bc7c-141">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="4bc7c-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

