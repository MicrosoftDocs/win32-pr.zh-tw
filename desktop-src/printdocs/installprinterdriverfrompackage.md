---
description: 從列印伺服器驅動程式存放區中的驅動程式套件安裝印表機驅動程式。
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: 'InstallPrinterDriverFromPackage 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194964"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="4e14a-103">InstallPrinterDriverFromPackage 函式</span><span class="sxs-lookup"><span data-stu-id="4e14a-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="4e14a-104">從列印伺服器的驅動程式存放區中的驅動程式套件安裝印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4e14a-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e14a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e14a-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4e14a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e14a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e14a-107">*pszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-108">常數、以 null 結束的字串指標，指定列印伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e14a-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="4e14a-109">**Null** 表示本機電腦。</span><span class="sxs-lookup"><span data-stu-id="4e14a-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="4e14a-110">*pszInfPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-111">常數、以 null 結束的字串指標，指定列印驅動程式 .inf 檔案的驅動程式存放區路徑。</span><span class="sxs-lookup"><span data-stu-id="4e14a-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="4e14a-112">**Null** 表示驅動程式位於隨附于 Windows 的 inf 檔案中。</span><span class="sxs-lookup"><span data-stu-id="4e14a-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4e14a-113">*pszDriverName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-114">常數、以 null 結束的字串指標，指定驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e14a-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="4e14a-115">*pszEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-116">常數、以 null 結束的字串指標，指定處理器架構 (例如 Windows NT x86) 。</span><span class="sxs-lookup"><span data-stu-id="4e14a-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="4e14a-117">這可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e14a-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e14a-118">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-119">這只能是0或 IPDFP \_ 複製 \_ 所有檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4e14a-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="4e14a-120">值為0表示必須在印表機驅動程式目錄中新增印表機驅動程式，而且必須在目前使用中的對應檔案之後，才複製印表機驅動程式目錄中的任何檔案。</span><span class="sxs-lookup"><span data-stu-id="4e14a-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="4e14a-121">IPDFP \_ 複製所有檔案的 \_ 值 \_ 表示必須新增印表機驅動程式和印表機驅動程式目錄中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="4e14a-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="4e14a-122">當 *dwFlags* 的值為 IPDFP 複製所有檔案時，會忽略檔案時間戳記 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4e14a-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e14a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e14a-123">Return value</span></span>

<span data-ttu-id="4e14a-124">如果作業成功，則傳回值為 S \_ OK，否則 **HRESULT** 會包含錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4e14a-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="4e14a-125">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="4e14a-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e14a-126">備註</span><span class="sxs-lookup"><span data-stu-id="4e14a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e14a-127">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4e14a-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4e14a-128">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="4e14a-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4e14a-129">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="4e14a-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4e14a-130">驅動程式存放區通常是% windir% \\ inf 或% windir% \\ System32 \\ DriverStore \\ FileRepository。</span><span class="sxs-lookup"><span data-stu-id="4e14a-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="4e14a-131">**InstallPrinterDriverFromPackage** 也會安裝套件中的其他檔案，例如色彩設定檔和列印處理器。</span><span class="sxs-lookup"><span data-stu-id="4e14a-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="4e14a-132">當使用者使用終端機服務登入時，使用者必須具備印表機管理許可權，才能安裝在遠端電腦或本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="4e14a-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="4e14a-133">只有已簽署的封裝可以安裝在遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="4e14a-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e14a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e14a-134">Requirements</span></span>



| <span data-ttu-id="4e14a-135">需求</span><span class="sxs-lookup"><span data-stu-id="4e14a-135">Requirement</span></span> | <span data-ttu-id="4e14a-136">值</span><span class="sxs-lookup"><span data-stu-id="4e14a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e14a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e14a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4e14a-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4e14a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e14a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4e14a-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e14a-141">標頭</span><span class="sxs-lookup"><span data-stu-id="4e14a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e14a-142"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4e14a-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4e14a-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e14a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e14a-144"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e14a-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4e14a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4e14a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e14a-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e14a-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4e14a-147">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4e14a-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e14a-148">**InstallPrinterDriverFromPackageW** (Unicode) 和 **InstallPrinterDriverFromPackageA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4e14a-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e14a-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e14a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e14a-150">列印</span><span class="sxs-lookup"><span data-stu-id="4e14a-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4e14a-151">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="4e14a-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

