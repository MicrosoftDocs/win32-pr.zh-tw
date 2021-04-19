---
description: AddPrinterDriverEx 函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: 'AddPrinterDriverEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996716"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="93a6f-103">AddPrinterDriverEx 函式</span><span class="sxs-lookup"><span data-stu-id="93a6f-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="93a6f-104">**AddPrinterDriverEx** 函式會安裝本機或遠端印表機驅動程式，並連結設定、資料和驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="93a6f-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="93a6f-105">除了擁有 [**AddPrinterDriver**](addprinterdriver.md)的功能之外，它也有一些選項可允許嚴格升級、嚴格降級、只複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="93a6f-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="93a6f-106">不再建議您安裝不含驅動程式套件的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="93a6f-107">請改用 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) 。</span><span class="sxs-lookup"><span data-stu-id="93a6f-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="93a6f-108">語法</span><span class="sxs-lookup"><span data-stu-id="93a6f-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="93a6f-109">參數</span><span class="sxs-lookup"><span data-stu-id="93a6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a6f-110">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a6f-111">以 null 結束的字串指標，指定應該安裝驅動程式之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="93a6f-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="93a6f-112">如果此參數為 **Null**，則函式會在本機電腦上安裝驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="93a6f-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a6f-114">*PDriverInfo* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="93a6f-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="93a6f-115">此值可以是2、3、4、6或8。</span><span class="sxs-lookup"><span data-stu-id="93a6f-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="93a6f-116">*pDriverInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93a6f-117">包含印表機驅動程式資訊之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="93a6f-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="93a6f-118">它可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="93a6f-118">It can be one of the following.</span></span>



| <span data-ttu-id="93a6f-119">層級的值</span><span class="sxs-lookup"><span data-stu-id="93a6f-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="93a6f-120">驅動程式 \_ 資訊 \_ \* 結構</span><span class="sxs-lookup"><span data-stu-id="93a6f-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="93a6f-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="93a6f-122">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="93a6f-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="93a6f-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="93a6f-124">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="93a6f-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="93a6f-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="93a6f-126">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="93a6f-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="93a6f-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="93a6f-128">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="93a6f-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="93a6f-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="93a6f-130">**驅動程式 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="93a6f-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="93a6f-131">如果 *pDriverInfo* 所指向之結構的 **PEnvironment** 成員為 **Null**，則此函式會使用目前的呼叫端/用戶端環境，而不是目的地/伺服器的環境。</span><span class="sxs-lookup"><span data-stu-id="93a6f-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="93a6f-132">*dwFileCopyFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a6f-133">複製驅動程式檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="93a6f-133">The options for copying the driver files.</span></span> <span data-ttu-id="93a6f-134">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="93a6f-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="93a6f-135">值</span><span class="sxs-lookup"><span data-stu-id="93a6f-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="93a6f-136">意義</span><span class="sxs-lookup"><span data-stu-id="93a6f-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="93a6f-137"><dt>**APD \_ 複製 \_ 所有 \_ 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="93a6f-138">新增印表機驅動程式，並複製印表機驅動程式目錄中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="93a6f-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="93a6f-139">此選項會忽略檔案時間戳記。</span><span class="sxs-lookup"><span data-stu-id="93a6f-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="93a6f-140"><dt>**APD \_ \_ 從 \_ 目錄複寫**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="93a6f-141">使用 [**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md) 結構中指定的完整檔案名來新增印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="93a6f-142">此旗標會與其中一個其他複製旗標一起 Or 運算。</span><span class="sxs-lookup"><span data-stu-id="93a6f-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="93a6f-143">如果設定此旗標，則如果檔案不存在，且 **驅動程式 \_ 資訊 \_ 6** 結構指定這些檔案，則 **AddPrinterDriverEx** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="93a6f-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="93a6f-144">這些檔案不需要複製到系統的印表機驅動程式目錄。</span><span class="sxs-lookup"><span data-stu-id="93a6f-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="93a6f-145">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="93a6f-145">See the Remarks.</span></span><br/> <span data-ttu-id="93a6f-146">**Windows 2000：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="93a6f-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="93a6f-147"><dt>**APD \_ 複製 \_ 新 \_ 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="93a6f-148">新增印表機驅動程式，並將印表機驅動程式目錄中的檔案，複製到目前使用中的任何對應檔案。</span><span class="sxs-lookup"><span data-stu-id="93a6f-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="93a6f-149">此旗標會模擬 [**AddPrinterDriver**](addprinterdriver.md)的行為。</span><span class="sxs-lookup"><span data-stu-id="93a6f-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="93a6f-150"><dt>**APD \_ STRICT \_ 降級**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="93a6f-151">只有當印表機驅動程式目錄中的所有檔案都早于目前使用中的任何對應檔案時，才新增印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="93a6f-152"><dt>**APD \_ STRICT \_ 升級**</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="93a6f-153">只有在印表機驅動程式目錄中的所有檔案都比目前使用中的任何對應檔案更新時，才新增印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a6f-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="93a6f-154">Return value</span></span>

<span data-ttu-id="93a6f-155">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="93a6f-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="93a6f-156">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="93a6f-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="93a6f-157">如果已知的印表機驅動程式在使用作業系統時發生問題， **AddPrinterDriverEx** 將會失敗，並出現下列其中一個錯誤代碼：</span><span class="sxs-lookup"><span data-stu-id="93a6f-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="93a6f-158">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="93a6f-158">Error Code</span></span>                      | <span data-ttu-id="93a6f-159">意義</span><span class="sxs-lookup"><span data-stu-id="93a6f-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a6f-160">\_印表機 \_ 驅動程式 \_ 封鎖錯誤</span><span class="sxs-lookup"><span data-stu-id="93a6f-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="93a6f-161">驅動程式無法在作業系統上運作。</span><span class="sxs-lookup"><span data-stu-id="93a6f-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="93a6f-162">錯誤 \_ 印表機 \_ 驅動程式 \_ 警告</span><span class="sxs-lookup"><span data-stu-id="93a6f-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="93a6f-163">作業系統上的驅動程式不可靠。</span><span class="sxs-lookup"><span data-stu-id="93a6f-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="93a6f-164">但是，如果指定了 APD \_ 安裝 \_ 警告 \_ 驅動程式，則會安裝驅動程式，且不會提供任何警告。</span><span class="sxs-lookup"><span data-stu-id="93a6f-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="93a6f-165">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="93a6f-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a6f-166">備註</span><span class="sxs-lookup"><span data-stu-id="93a6f-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="93a6f-167">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="93a6f-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="93a6f-168">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="93a6f-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="93a6f-169">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="93a6f-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="93a6f-170">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="93a6f-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="93a6f-171">在呼叫 **AddPrinterDriverEx** 函式之前，驅動程式所需的所有檔案都必須複製到系統的印表機驅動程式目錄。</span><span class="sxs-lookup"><span data-stu-id="93a6f-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="93a6f-172">若要取出這個目錄的名稱，請呼叫 [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="93a6f-173">若要判斷目前已安裝的印表機驅動程式，請呼叫 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="93a6f-174">如果已成功新增印表機驅動程式，此函式會呼叫 DrvDriverEvent (驅動程式 \_ 事件 \_ 初始化、層級、驅動程式 \_ 資訊 \_ \* 、lparam ) 函式，以允許驅動程式在安裝印表機驅動程式期間執行任何必要的初始化工作。</span><span class="sxs-lookup"><span data-stu-id="93a6f-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="93a6f-175">如需有關 **DrvDriverEvent** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) </span><span class="sxs-lookup"><span data-stu-id="93a6f-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="93a6f-176">在呼叫 **DrvDriverEvent** 期間，驅動程式不應使用 UI 呼叫。</span><span class="sxs-lookup"><span data-stu-id="93a6f-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="93a6f-177">若要執行 UI 相關的工作，安裝程式應該使用印表機的 .inf 檔案中的 VendorSetup 專案，或針對隨插即用的裝置，安裝程式可以使用裝置特定的共同安裝程式。</span><span class="sxs-lookup"><span data-stu-id="93a6f-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="93a6f-178">如需 VendorSetup 的詳細資訊，請參閱 DDK。</span><span class="sxs-lookup"><span data-stu-id="93a6f-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="93a6f-179">[**驅動程式 \_ 資訊 \_ 6**](driver-info-6.md)結構中所參考的檔案，必須是進行呼叫之來源電腦的本機。</span><span class="sxs-lookup"><span data-stu-id="93a6f-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="93a6f-180">檔案名可以是 UNC 名稱，前提是 UNC 名稱是本機電腦。</span><span class="sxs-lookup"><span data-stu-id="93a6f-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a6f-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a6f-181">Requirements</span></span>



| <span data-ttu-id="93a6f-182">需求</span><span class="sxs-lookup"><span data-stu-id="93a6f-182">Requirement</span></span> | <span data-ttu-id="93a6f-183">值</span><span class="sxs-lookup"><span data-stu-id="93a6f-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a6f-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a6f-184">Minimum supported client</span></span><br/> | <span data-ttu-id="93a6f-185">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93a6f-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a6f-186">Minimum supported server</span></span><br/> | <span data-ttu-id="93a6f-187">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a6f-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93a6f-188">標頭</span><span class="sxs-lookup"><span data-stu-id="93a6f-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="93a6f-189"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="93a6f-190">程式庫</span><span class="sxs-lookup"><span data-stu-id="93a6f-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="93a6f-191"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="93a6f-192">DLL</span><span class="sxs-lookup"><span data-stu-id="93a6f-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a6f-193"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="93a6f-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="93a6f-194">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="93a6f-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="93a6f-195">**AddPrinterDriverExW** (Unicode) 和 **AddPrinterDriverExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="93a6f-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="93a6f-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93a6f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a6f-197">列印</span><span class="sxs-lookup"><span data-stu-id="93a6f-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="93a6f-198">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="93a6f-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="93a6f-199">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="93a6f-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="93a6f-200">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="93a6f-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="93a6f-201">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="93a6f-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="93a6f-202">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="93a6f-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="93a6f-203">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="93a6f-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="93a6f-204">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="93a6f-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="93a6f-205">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="93a6f-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="93a6f-206">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="93a6f-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

