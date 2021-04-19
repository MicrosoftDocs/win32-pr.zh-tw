---
description: DeletePrinterDriverEx 函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。 此函數也可以刪除驅動程式的特定版本。
ms.assetid: 1a3d7c7f-1d45-4877-a8f7-a77f40e3c319
title: 'DeletePrinterDriverEx 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverEx
- DeletePrinterDriverExA
- DeletePrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b88ef38236961286875a1885dad9dde936887d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993176"
---
# <a name="deleteprinterdriverex-function"></a><span data-ttu-id="25f4b-104">DeletePrinterDriverEx 函式</span><span class="sxs-lookup"><span data-stu-id="25f4b-104">DeletePrinterDriverEx function</span></span>

<span data-ttu-id="25f4b-105">**DeletePrinterDriverEx** 函式會從伺服器上支援的驅動程式名稱清單中移除指定的印表機驅動程式名稱，並刪除與驅動程式相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="25f4b-105">The **DeletePrinterDriverEx** function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="25f4b-106">此函數也可以刪除驅動程式的特定版本。</span><span class="sxs-lookup"><span data-stu-id="25f4b-106">This function can also delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f4b-107">語法</span><span class="sxs-lookup"><span data-stu-id="25f4b-107">Syntax</span></span>


```C++
BOOL DeletePrinterDriverEx(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName,
  _In_ DWORD  dwDeleteFlag,
  _In_ DWORD  dwVersionFlag
);
```



## <a name="parameters"></a><span data-ttu-id="25f4b-108">參數</span><span class="sxs-lookup"><span data-stu-id="25f4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f4b-109">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f4b-110">以 null 結束的字串指標，指定要從中刪除驅動程式之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="25f4b-110">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="25f4b-111">如果此參數為 **Null**，此函式會從本機電腦刪除印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25f4b-111">If this parameter is **NULL**, the function deletes the printer-driver from the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="25f4b-112">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f4b-113">以 null 結束的字串指標，指定要從中刪除驅動程式的環境 (例如 Windows NT x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="25f4b-113">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="25f4b-114">如果此參數為 **Null**，則會從目前的呼叫應用程式和用戶端電腦的環境中刪除驅動程式名稱， (不是目的地應用程式和列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="25f4b-114">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client computer (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="25f4b-115">*pDriverName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-115">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f4b-116">以 null 結束的字串指標，指定要刪除之驅動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="25f4b-116">A pointer to a null-terminated string specifying the name of the driver to delete.</span></span>

</dd> <dt>

<span data-ttu-id="25f4b-117">*dwDeleteFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-117">*dwDeleteFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f4b-118">用來刪除驅動程式檔案和版本的選項。</span><span class="sxs-lookup"><span data-stu-id="25f4b-118">The options for deleting files and versions of the driver.</span></span> <span data-ttu-id="25f4b-119">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="25f4b-119">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="25f4b-120">值</span><span class="sxs-lookup"><span data-stu-id="25f4b-120">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="25f4b-121">意義</span><span class="sxs-lookup"><span data-stu-id="25f4b-121">Meaning</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DPD_DELETE_SPECIFIC_VERSION"></span><span id="dpd_delete_specific_version"></span><dl> <span data-ttu-id="25f4b-122"><dt>**DPD \_ 刪除 \_ 特定 \_ 版本**</dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-122"><dt>**DPD\_DELETE\_SPECIFIC\_VERSION**</dt></span></span> </dl> | <span data-ttu-id="25f4b-123">刪除在 *dwVersionFlag* 中指定的版本。</span><span class="sxs-lookup"><span data-stu-id="25f4b-123">Deletes the version specified in *dwVersionFlag*.</span></span> <span data-ttu-id="25f4b-124">這並不確定會從伺服器支援的驅動程式清單中移除驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25f4b-124">This does not ensure that the driver will be removed from the list of supported drivers for the server.</span></span><br/>                  |
| <span id="DPD_DELETE_UNUSED_FILES"></span><span id="dpd_delete_unused_files"></span><dl> <span data-ttu-id="25f4b-125"><dt>**DPD \_ 刪除 \_ 未使用的檔案 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-125"><dt>**DPD\_DELETE\_UNUSED\_FILES**</dt></span></span> </dl>             | <span data-ttu-id="25f4b-126">移除任何未使用的驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="25f4b-126">Removes any unused driver files.</span></span><br/>                                                                                                                                           |
| <span id="DPD_DELETE_ALL_FILES"></span><span id="dpd_delete_all_files"></span><dl> <span data-ttu-id="25f4b-127"><dt>**DPD \_ 刪除 \_ 所有 \_ 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-127"><dt>**DPD\_DELETE\_ALL\_FILES**</dt></span></span> </dl>                      | <span data-ttu-id="25f4b-128">只有在所有相關聯的檔案都可以移除時，才會刪除驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25f4b-128">Deletes the driver only if all its associated files can be removed.</span></span> <span data-ttu-id="25f4b-129">如果有其他安裝的驅動程式正在使用任何驅動程式的檔案，刪除作業將會失敗。</span><span class="sxs-lookup"><span data-stu-id="25f4b-129">The delete operation fails if any of the driver's files are being used by some other installed driver.</span></span><br/> |



 

<span data-ttu-id="25f4b-130">如果 \_ \_ 未指定 DPD 刪除特定 \_ 版本，則函式會刪除所有版本的驅動程式（如果沒有使用的話）。</span><span class="sxs-lookup"><span data-stu-id="25f4b-130">If DPD\_DELETE\_SPECIFIC\_VERSION is not specified, the function deletes all versions of the driver if none of them is in use.</span></span> <span data-ttu-id="25f4b-131">如果 DPD \_ 刪除 \_ 未使用的檔案 \_ ，或未 \_ 指定 DPD 刪除所有檔案 \_ ，則該函式不 \_ 會刪除驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="25f4b-131">If neither DPD\_DELETE\_UNUSED\_FILES nor DPD\_DELETE\_ALL\_FILES is specified, the function does not delete driver files.</span></span>

</dd> <dt>

<span data-ttu-id="25f4b-132">*dwVersionFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-132">*dwVersionFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f4b-133">要刪除的驅動程式版本。</span><span class="sxs-lookup"><span data-stu-id="25f4b-133">The version of the driver to be deleted.</span></span> <span data-ttu-id="25f4b-134">此參數可以是0、1、2或3。</span><span class="sxs-lookup"><span data-stu-id="25f4b-134">This parameter can be 0, 1, 2 or 3.</span></span> <span data-ttu-id="25f4b-135">只有在 *dwDeleteFlag* 包含 DPD \_ DELETE \_ 特定版本旗標時，才會使用此參數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="25f4b-135">This parameter is used only if *dwDeleteFlag* includes the DPD\_DELETE\_SPECIFIC\_VERSION flag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f4b-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="25f4b-136">Return value</span></span>

<span data-ttu-id="25f4b-137">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="25f4b-137">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="25f4b-138">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="25f4b-138">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f4b-139">備註</span><span class="sxs-lookup"><span data-stu-id="25f4b-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25f4b-140">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="25f4b-140">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="25f4b-141">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="25f4b-141">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="25f4b-142">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="25f4b-142">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="25f4b-143">在函數刪除驅動程式檔案之前，它會呼叫驅動程式的 **DrvDriverEvent** 函式，讓驅動程式能夠移除任何未使用的私用檔案。</span><span class="sxs-lookup"><span data-stu-id="25f4b-143">Before the function deletes the driver files, it calls the driver's **DrvDriverEvent** function, allowing the driver to remove any private files that are not used.</span></span> <span data-ttu-id="25f4b-144">如需有關 **DrvDriverEvent** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="25f4b-144">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="25f4b-145">如果目前已載入驅動程式檔案，則函式會將它們移至臨時目錄，並在重新開機時將它們標示為刪除。</span><span class="sxs-lookup"><span data-stu-id="25f4b-145">If the driver files are currently loaded, the function moves them to a temp directory and marks them for deletion on restart.</span></span>

<span data-ttu-id="25f4b-146">在呼叫 **DeletePrinterDriverEx** 之前，您必須刪除所有使用印表機驅動程式的印表機物件。</span><span class="sxs-lookup"><span data-stu-id="25f4b-146">Before calling **DeletePrinterDriverEx**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f4b-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="25f4b-147">Requirements</span></span>



| <span data-ttu-id="25f4b-148">需求</span><span class="sxs-lookup"><span data-stu-id="25f4b-148">Requirement</span></span> | <span data-ttu-id="25f4b-149">值</span><span class="sxs-lookup"><span data-stu-id="25f4b-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f4b-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25f4b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="25f4b-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="25f4b-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25f4b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="25f4b-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25f4b-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="25f4b-154">標頭</span><span class="sxs-lookup"><span data-stu-id="25f4b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f4b-155"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-155"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="25f4b-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="25f4b-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="25f4b-157"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-157"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="25f4b-158">DLL</span><span class="sxs-lookup"><span data-stu-id="25f4b-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f4b-159"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="25f4b-159"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="25f4b-160">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="25f4b-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="25f4b-161">**DeletePrinterDriverExW** (Unicode) 和 **DeletePrinterDriverExA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="25f4b-161">**DeletePrinterDriverExW** (Unicode) and **DeletePrinterDriverExA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="25f4b-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25f4b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f4b-163">列印</span><span class="sxs-lookup"><span data-stu-id="25f4b-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="25f4b-164">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="25f4b-164">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="25f4b-165">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="25f4b-165">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

 




