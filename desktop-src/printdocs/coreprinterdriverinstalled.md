---
description: CorePrinterDriverInstalled 函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: 'CorePrinterDriverInstalled 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027122"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="67035-103">CorePrinterDriverInstalled 函式</span><span class="sxs-lookup"><span data-stu-id="67035-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="67035-104">**CorePrinterDriverInstalled** 函式會報告是否已安裝具有指定 GUID、日期和版本的核心印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="67035-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="67035-105">語法</span><span class="sxs-lookup"><span data-stu-id="67035-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="67035-106">參數</span><span class="sxs-lookup"><span data-stu-id="67035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67035-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67035-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-108">常數、以 null 結束的字串指標，指定列印伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="67035-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="67035-109">針對本機電腦使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="67035-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="67035-110">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67035-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-111">常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="67035-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="67035-112">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="67035-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67035-113">*CoreDriverGUID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67035-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-114">核心印表機驅動程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="67035-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="67035-115">*ftDriverDate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67035-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-116">核心印表機驅動程式的日期。</span><span class="sxs-lookup"><span data-stu-id="67035-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="67035-117">*dwlDriverVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67035-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-118">核心印表機驅動程式的版本。</span><span class="sxs-lookup"><span data-stu-id="67035-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="67035-119">*pbDriverInstalled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67035-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67035-120">如果已安裝驅動程式或較新的版本， **則為 TRUE** 的指標，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="67035-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67035-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="67035-121">Return value</span></span>

<span data-ttu-id="67035-122">如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67035-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="67035-123">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="67035-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="67035-124">備註</span><span class="sxs-lookup"><span data-stu-id="67035-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67035-125">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="67035-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="67035-126">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="67035-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="67035-127">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="67035-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67035-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="67035-128">Requirements</span></span>



| <span data-ttu-id="67035-129">需求</span><span class="sxs-lookup"><span data-stu-id="67035-129">Requirement</span></span> | <span data-ttu-id="67035-130">值</span><span class="sxs-lookup"><span data-stu-id="67035-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67035-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67035-131">Minimum supported client</span></span><br/> | <span data-ttu-id="67035-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67035-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="67035-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67035-133">Minimum supported server</span></span><br/> | <span data-ttu-id="67035-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67035-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="67035-135">標頭</span><span class="sxs-lookup"><span data-stu-id="67035-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="67035-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="67035-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="67035-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="67035-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="67035-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="67035-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="67035-139">DLL</span><span class="sxs-lookup"><span data-stu-id="67035-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67035-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67035-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="67035-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="67035-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="67035-142">**CorePrinterDriverInstalledW** (Unicode) 和 **CorePrinterDriverInstalledA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="67035-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="67035-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67035-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67035-144">列印</span><span class="sxs-lookup"><span data-stu-id="67035-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="67035-145">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="67035-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

