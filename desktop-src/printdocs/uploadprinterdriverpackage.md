---
description: 將印表機驅動程式上傳至列印伺服器驅動程式存放區，以便藉由呼叫 InstallPrinterDriverFromPackage 來進行安裝。
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: 'UploadPrinterDriverPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194581"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="9035c-103">UploadPrinterDriverPackage 函式</span><span class="sxs-lookup"><span data-stu-id="9035c-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="9035c-104">將印表機驅動程式上傳至列印伺服器的驅動程式存放區，以便藉由呼叫 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md)來進行安裝。</span><span class="sxs-lookup"><span data-stu-id="9035c-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9035c-105">語法</span><span class="sxs-lookup"><span data-stu-id="9035c-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="9035c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9035c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9035c-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9035c-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-108">常數、以 null 結束的字串指標，指定列印伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9035c-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="9035c-109">如果伺服器是本機電腦，請使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9035c-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9035c-110">*pszInfPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9035c-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-111">常數、以 null 結束的字串指標，指定驅動程式 .inf 檔案的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="9035c-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="9035c-112">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9035c-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-113">常數、以 null 結束的字串指標，指定伺服器的處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="9035c-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="9035c-114">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9035c-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9035c-115">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9035c-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-116">這可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9035c-116">This can be any of the following values:</span></span>



| <span data-ttu-id="9035c-117">值</span><span class="sxs-lookup"><span data-stu-id="9035c-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="9035c-118">意義</span><span class="sxs-lookup"><span data-stu-id="9035c-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="9035c-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="9035c-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="9035c-120">上傳期間將不會顯示 UI。</span><span class="sxs-lookup"><span data-stu-id="9035c-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="9035c-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="9035c-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="9035c-122">即使封裝已在伺服器的驅動程式存放區中，也會上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="9035c-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="9035c-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="9035c-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="9035c-124">將會先檢查伺服器的驅動程式存放區，然後再上傳，以查看套件是否已存在。</span><span class="sxs-lookup"><span data-stu-id="9035c-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="9035c-125">如果已設定 UPDP_UPLOAD_ALWAYS，則會忽略此設定。</span><span class="sxs-lookup"><span data-stu-id="9035c-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9035c-126">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9035c-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-127">複製使用者介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9035c-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="9035c-128">*pszDestInfPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9035c-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-129">驅動程式存放區中複製驅動程式 .inf 檔案的目的地路徑指標。</span><span class="sxs-lookup"><span data-stu-id="9035c-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="9035c-130">*pcchDestInfPath* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9035c-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9035c-131">在 [輸入] 上，指定 *pszDestInfPath* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="9035c-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="9035c-132">在輸出時，會接收路徑字串的大小（以字元為單位），包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="9035c-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9035c-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="9035c-133">Return value</span></span>

<span data-ttu-id="9035c-134">如果作業成功，則傳回值為 S_OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9035c-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="9035c-135">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="9035c-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9035c-136">備註</span><span class="sxs-lookup"><span data-stu-id="9035c-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9035c-137">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="9035c-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9035c-138">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="9035c-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9035c-139">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="9035c-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9035c-140">驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。</span><span class="sxs-lookup"><span data-stu-id="9035c-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="9035c-141">可以上傳一次只能上傳一個封裝。</span><span class="sxs-lookup"><span data-stu-id="9035c-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="9035c-142">如果封裝相依于其他套件，則必須分別上傳。</span><span class="sxs-lookup"><span data-stu-id="9035c-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="9035c-143">只可上傳已簽署的驅動程式套件。</span><span class="sxs-lookup"><span data-stu-id="9035c-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="9035c-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="9035c-144">Requirements</span></span>



| <span data-ttu-id="9035c-145">需求</span><span class="sxs-lookup"><span data-stu-id="9035c-145">Requirement</span></span> | <span data-ttu-id="9035c-146">值</span><span class="sxs-lookup"><span data-stu-id="9035c-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9035c-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9035c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9035c-148">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9035c-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9035c-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9035c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9035c-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9035c-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9035c-151">標頭</span><span class="sxs-lookup"><span data-stu-id="9035c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9035c-152"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9035c-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9035c-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="9035c-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="9035c-154"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9035c-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9035c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9035c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9035c-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9035c-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="9035c-157">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="9035c-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9035c-158">**UploadPrinterDriverPackageW** (Unicode) 和 **UploadPrinterDriverPackageA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="9035c-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9035c-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9035c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9035c-160">列印</span><span class="sxs-lookup"><span data-stu-id="9035c-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9035c-161">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="9035c-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

