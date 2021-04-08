---
description: AddPrinterDriver 函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: 'AddPrinterDriver 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693880"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="e31e2-103">AddPrinterDriver 函式</span><span class="sxs-lookup"><span data-stu-id="e31e2-103">AddPrinterDriver function</span></span>

<span data-ttu-id="e31e2-104">**AddPrinterDriver** 函式會安裝本機或遠端印表機驅動程式，並產生設定、資料和驅動程式檔案的關聯。</span><span class="sxs-lookup"><span data-stu-id="e31e2-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="e31e2-105">若要在安裝或升級印表機驅動程式時有更大的彈性，請使用 [**AddPrinterDriverEx**](addprinterdriverex.md) 函式，因為它允許嚴格升級、嚴格降級、複製較新的檔案，以及複製所有檔案 (無論檔案時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="e31e2-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="e31e2-106">不再建議您安裝不含驅動程式套件的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e31e2-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="e31e2-107">請改用 [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) 。</span><span class="sxs-lookup"><span data-stu-id="e31e2-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e31e2-108">語法</span><span class="sxs-lookup"><span data-stu-id="e31e2-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e31e2-109">參數</span><span class="sxs-lookup"><span data-stu-id="e31e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31e2-110">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e31e2-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31e2-111">以 null 結束的字串指標，指定應該安裝驅動程式之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="e31e2-112">如果 *pName* 為 **Null**，驅動程式將會安裝在本機。</span><span class="sxs-lookup"><span data-stu-id="e31e2-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="e31e2-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e31e2-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31e2-114">*PDriverInfo* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="e31e2-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="e31e2-115">此值可以是2、3、4、6或8。</span><span class="sxs-lookup"><span data-stu-id="e31e2-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="e31e2-116">*pDriverInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e31e2-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31e2-117">包含印表機驅動程式資訊之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e31e2-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="e31e2-118">這取決於 *層級* 的值。</span><span class="sxs-lookup"><span data-stu-id="e31e2-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="e31e2-119">值</span><span class="sxs-lookup"><span data-stu-id="e31e2-119">Value</span></span> | <span data-ttu-id="e31e2-120">印表機磁片磁碟機結構</span><span class="sxs-lookup"><span data-stu-id="e31e2-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="e31e2-121">2</span><span class="sxs-lookup"><span data-stu-id="e31e2-121">2</span></span>     | [<span data-ttu-id="e31e2-122">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e31e2-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="e31e2-123">3</span><span class="sxs-lookup"><span data-stu-id="e31e2-123">3</span></span>     | [<span data-ttu-id="e31e2-124">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e31e2-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="e31e2-125">4</span><span class="sxs-lookup"><span data-stu-id="e31e2-125">4</span></span>     | [<span data-ttu-id="e31e2-126">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="e31e2-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="e31e2-127">6</span><span class="sxs-lookup"><span data-stu-id="e31e2-127">6</span></span>     | [<span data-ttu-id="e31e2-128">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="e31e2-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="e31e2-129">8</span><span class="sxs-lookup"><span data-stu-id="e31e2-129">8</span></span>     | [<span data-ttu-id="e31e2-130">**驅動程式 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="e31e2-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="e31e2-131">如果 *pDriverInfo* 所指向之結構的 **PEnvironment** 成員為 **Null**，則會使用目前的呼叫端/用戶端環境 (不是目的地/伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="e31e2-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31e2-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="e31e2-132">Return value</span></span>

<span data-ttu-id="e31e2-133">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="e31e2-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e31e2-134">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e31e2-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31e2-135">備註</span><span class="sxs-lookup"><span data-stu-id="e31e2-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e31e2-136">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e31e2-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e31e2-137">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="e31e2-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e31e2-138">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="e31e2-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e31e2-139">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="e31e2-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="e31e2-140">在應用程式呼叫 **AddPrinterDriver** 函式之前，驅動程式所需的所有檔案都必須複製到系統的印表機驅動程式目錄。</span><span class="sxs-lookup"><span data-stu-id="e31e2-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="e31e2-141">應用程式可以藉由呼叫 [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) 函式來取得此目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31e2-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="e31e2-142">應用程式可以藉由呼叫 [**EnumPrinterDrivers**](enumprinterdrivers.md) 函式來判斷目前安裝的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e31e2-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31e2-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e31e2-143">Requirements</span></span>



| <span data-ttu-id="e31e2-144">需求</span><span class="sxs-lookup"><span data-stu-id="e31e2-144">Requirement</span></span> | <span data-ttu-id="e31e2-145">值</span><span class="sxs-lookup"><span data-stu-id="e31e2-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31e2-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e31e2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e31e2-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e31e2-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e31e2-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e31e2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e31e2-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e31e2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e31e2-150">標頭</span><span class="sxs-lookup"><span data-stu-id="e31e2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31e2-151"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e31e2-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e31e2-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="e31e2-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="e31e2-153"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e31e2-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e31e2-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e31e2-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31e2-155"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="e31e2-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e31e2-156">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e31e2-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e31e2-157">**AddPrinterDriverW** (Unicode) 和 **AddPrinterDriverA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e31e2-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="e31e2-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e31e2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31e2-159">列印</span><span class="sxs-lookup"><span data-stu-id="e31e2-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e31e2-160">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="e31e2-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e31e2-161">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="e31e2-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="e31e2-162">**驅動程式 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e31e2-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="e31e2-163">**驅動程式 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e31e2-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="e31e2-164">**驅動程式 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="e31e2-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="e31e2-165">**驅動程式 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="e31e2-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="e31e2-166">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="e31e2-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="e31e2-167">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="e31e2-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

