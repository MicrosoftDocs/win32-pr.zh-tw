---
description: AddMonitor 函式會安裝本機埠監視器，並連結設定、資料和監視檔案。
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: 'AddMonitor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027462"
---
# <a name="addmonitor-function"></a><span data-ttu-id="5a2ce-103">AddMonitor 函式</span><span class="sxs-lookup"><span data-stu-id="5a2ce-103">AddMonitor function</span></span>

<span data-ttu-id="5a2ce-104">**AddMonitor** 函式會安裝本機埠監視器，並連結設定、資料和監視檔案。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a2ce-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="5a2ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a2ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2ce-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a2ce-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ce-108">以 null 結束的字串指標，指定要安裝監視的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="5a2ce-109">針對僅支援本機安裝監視的系統，此字串應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5a2ce-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a2ce-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ce-111">*PMonitors* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="5a2ce-112">此值必須是2。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="5a2ce-113">*pMonitors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a2ce-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2ce-114">[**監視器 \_ 資訊 \_ 2**](monitor-info-2.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="5a2ce-115">如果 *pMonitors* 結構的 **PEnvironment** 成員是 **Null**，則會使用目前的呼叫端環境 (用戶端) ，而不是目的地 (伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="5a2ce-116">請注意，如果環境與伺服器的環境不相符，則呼叫會失敗，也就是說，您只能加入針對伺服器架構所撰寫的監視器。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2ce-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a2ce-117">Return value</span></span>

<span data-ttu-id="5a2ce-118">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="5a2ce-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2ce-120">備註</span><span class="sxs-lookup"><span data-stu-id="5a2ce-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5a2ce-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="5a2ce-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="5a2ce-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="5a2ce-124">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="5a2ce-125">在應用程式呼叫 **AddMonitor** 函式之前，必須將監視器所需的所有檔案複製到 SYSTEM32 目錄。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="5a2ce-126">若要判斷目前已安裝的埠監視器，請呼叫 [**EnumMonitors**](enummonitors.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="5a2ce-127">若要移除 **AddMonitor** 所新增的監視器，請呼叫 [**DeleteMonitor**](deletemonitor.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="5a2ce-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2ce-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a2ce-128">Requirements</span></span>



| <span data-ttu-id="5a2ce-129">需求</span><span class="sxs-lookup"><span data-stu-id="5a2ce-129">Requirement</span></span> | <span data-ttu-id="5a2ce-130">值</span><span class="sxs-lookup"><span data-stu-id="5a2ce-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2ce-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a2ce-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2ce-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a2ce-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5a2ce-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a2ce-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2ce-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a2ce-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5a2ce-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5a2ce-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a2ce-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5a2ce-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5a2ce-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a2ce-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a2ce-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a2ce-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="5a2ce-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5a2ce-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a2ce-140"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="5a2ce-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="5a2ce-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5a2ce-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5a2ce-142">**AddMonitorW** (Unicode) 和 **AddMonitorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5a2ce-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="5a2ce-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a2ce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2ce-144">列印</span><span class="sxs-lookup"><span data-stu-id="5a2ce-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5a2ce-145">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="5a2ce-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5a2ce-146">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="5a2ce-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="5a2ce-147">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="5a2ce-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="5a2ce-148">**監視 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5a2ce-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

