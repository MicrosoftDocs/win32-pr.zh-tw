---
description: 抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: 'GetCorePrinterDrivers 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319091"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="e90a8-103">GetCorePrinterDrivers 函式</span><span class="sxs-lookup"><span data-stu-id="e90a8-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="e90a8-104">抓取指定的核心印表機驅動程式的 GUID、版本和日期，以及其套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="e90a8-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="e90a8-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="e90a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="e90a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90a8-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90a8-108">常數、以 null 結束的字串指標，指定列印伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e90a8-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="e90a8-109">針對本機電腦使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e90a8-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e90a8-110">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90a8-111">常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="e90a8-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="e90a8-112">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e90a8-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e90a8-113">*pszzCoreDriverDependencies* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90a8-114">以 null 終止的多字串指標，指定核心印表機驅動程式的 Guid。</span><span class="sxs-lookup"><span data-stu-id="e90a8-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="e90a8-115">*cCorePrinterDrivers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90a8-116">*PszzCoreDriverDependencies* 中的字串數目。</span><span class="sxs-lookup"><span data-stu-id="e90a8-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="e90a8-117">*pCorePrinterDrivers* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e90a8-118">一或多個 [**核心 \_ 印表機 \_ 驅動程式**](core-printer-driver.md) 結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="e90a8-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90a8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e90a8-119">Return value</span></span>

<span data-ttu-id="e90a8-120">如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e90a8-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="e90a8-121">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="e90a8-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e90a8-122">備註</span><span class="sxs-lookup"><span data-stu-id="e90a8-122">Remarks</span></span>

<span data-ttu-id="e90a8-123">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e90a8-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e90a8-124">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e90a8-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e90a8-125">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e90a8-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90a8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e90a8-126">Requirements</span></span>



| <span data-ttu-id="e90a8-127">需求</span><span class="sxs-lookup"><span data-stu-id="e90a8-127">Requirement</span></span> | <span data-ttu-id="e90a8-128">值</span><span class="sxs-lookup"><span data-stu-id="e90a8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90a8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e90a8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e90a8-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e90a8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e90a8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e90a8-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e90a8-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e90a8-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e90a8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90a8-134"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e90a8-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e90a8-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="e90a8-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e90a8-136"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90a8-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e90a8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e90a8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90a8-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90a8-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="e90a8-139">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e90a8-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e90a8-140">**GetCorePrinterDriversW** (Unicode) 和 **GetCorePrinterDriversA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e90a8-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="e90a8-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e90a8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90a8-142">列印</span><span class="sxs-lookup"><span data-stu-id="e90a8-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e90a8-143">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e90a8-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

