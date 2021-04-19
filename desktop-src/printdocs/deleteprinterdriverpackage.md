---
description: 從驅動程式存放區刪除印表機驅動程式套件。
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: 'DeletePrinterDriverPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991858"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="8092a-103">DeletePrinterDriverPackage 函式</span><span class="sxs-lookup"><span data-stu-id="8092a-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="8092a-104">從驅動程式存放區刪除印表機驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="8092a-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8092a-105">語法</span><span class="sxs-lookup"><span data-stu-id="8092a-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="8092a-106">參數</span><span class="sxs-lookup"><span data-stu-id="8092a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8092a-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8092a-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8092a-108">常數、以 null 結束的字串指標，指定要從中刪除驅動程式套件的列印伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8092a-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="8092a-109">**Null** 指標值表示本機電腦。</span><span class="sxs-lookup"><span data-stu-id="8092a-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8092a-110">*pszInfPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8092a-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8092a-111">常數、以 null 結束的字串指標，指定驅動程式 .inf 檔案的路徑 \* 。</span><span class="sxs-lookup"><span data-stu-id="8092a-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="8092a-112">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8092a-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8092a-113">常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="8092a-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="8092a-114">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8092a-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8092a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8092a-115">Return value</span></span>

<span data-ttu-id="8092a-116">\_如果作業成功，則為 [確定]。</span><span class="sxs-lookup"><span data-stu-id="8092a-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="8092a-117">E \_ ACCESSDENIED，如果封裝隨附于 Windows。</span><span class="sxs-lookup"><span data-stu-id="8092a-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="8092a-118">HRESULT \_ 程式碼 (錯誤 \_ 列印 \_ 驅動程式 \_ 封裝 \_ 在 \_ 使用中) （如果正在使用套件）。</span><span class="sxs-lookup"><span data-stu-id="8092a-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="8092a-119">否則， **HRESULT** 將會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8092a-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="8092a-120">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="8092a-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8092a-121">備註</span><span class="sxs-lookup"><span data-stu-id="8092a-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8092a-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="8092a-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8092a-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="8092a-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8092a-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="8092a-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8092a-125">驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。</span><span class="sxs-lookup"><span data-stu-id="8092a-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="8092a-126">使用此功能時，無法移除隨附于 Windows 的驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="8092a-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="8092a-127">使用者必須具備印表機管理許可權。</span><span class="sxs-lookup"><span data-stu-id="8092a-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="8092a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="8092a-128">Requirements</span></span>



| <span data-ttu-id="8092a-129">需求</span><span class="sxs-lookup"><span data-stu-id="8092a-129">Requirement</span></span> | <span data-ttu-id="8092a-130">值</span><span class="sxs-lookup"><span data-stu-id="8092a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8092a-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8092a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8092a-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8092a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8092a-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8092a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8092a-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8092a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8092a-135">標頭</span><span class="sxs-lookup"><span data-stu-id="8092a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8092a-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8092a-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8092a-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="8092a-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="8092a-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8092a-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8092a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8092a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8092a-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8092a-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="8092a-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8092a-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8092a-142">**DeletePrinterDriverPackageW** (Unicode) 和 **DeletePrinterDriverPackageA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8092a-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8092a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8092a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8092a-144">列印</span><span class="sxs-lookup"><span data-stu-id="8092a-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8092a-145">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="8092a-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

