---
description: SetPrinter 函式會設定指定印表機的資料，或藉由暫停列印、繼續列印或清除所有列印工作來設定指定印表機的狀態。
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: 'SetPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979812"
---
# <a name="setprinter-function"></a><span data-ttu-id="7e32f-103">SetPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="7e32f-103">SetPrinter function</span></span>

<span data-ttu-id="7e32f-104">**SetPrinter** 函式會設定指定印表機的資料，或藉由暫停列印、繼續列印或清除所有列印工作來設定指定印表機的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e32f-104">The **SetPrinter** function sets the data for a specified printer or sets the state of the specified printer by pausing printing, resuming printing, or clearing all print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e32f-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e32f-105">Syntax</span></span>


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a><span data-ttu-id="7e32f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e32f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e32f-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e32f-108">印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7e32f-108">A handle to the printer.</span></span> <span data-ttu-id="7e32f-109">使用 [**OpenPrinter**](openprinter.md)、 [**OpenPrinter2**](openprinter2.md)或 [**interactivesession.addprinter**](addprinter.md) 函數來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="7e32f-109">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="7e32f-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e32f-111">函數儲存在 *pPrinter* 所指向之緩衝區中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7e32f-111">The type of data that the function stores into the buffer pointed to by *pPrinter*.</span></span> <span data-ttu-id="7e32f-112">如果 *命令* 參數不等於零，則 *Level* 參數必須為零。</span><span class="sxs-lookup"><span data-stu-id="7e32f-112">If the *Command* parameter is not equal to zero, the *Level* parameter must be zero.</span></span>

<span data-ttu-id="7e32f-113">這個值可以是0、2、3、4、5、6、7、8或9。</span><span class="sxs-lookup"><span data-stu-id="7e32f-113">This value can be 0, 2, 3, 4, 5, 6, 7, 8, or 9.</span></span>

</dd> <dt>

<span data-ttu-id="7e32f-114">*pPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-114">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e32f-115">緩衝區的指標，其中包含要針對印表機設定的資料，或包含 *命令* 參數所指定之命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="7e32f-115">A pointer to a buffer containing data to set for the printer, or containing information for the command specified by the *Command* parameter.</span></span> <span data-ttu-id="7e32f-116">緩衝區中的資料類型取決於 *層級* 的值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-116">The type of data in the buffer is determined by the value of *Level*.</span></span>



| <span data-ttu-id="7e32f-117">層級</span><span class="sxs-lookup"><span data-stu-id="7e32f-117">Level</span></span>                                                                                                | <span data-ttu-id="7e32f-118">結構</span><span class="sxs-lookup"><span data-stu-id="7e32f-118">Structure</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="7e32f-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-119"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="7e32f-120">如果 *命令* 參數是 **印表機 \_ 控制 \_ 集 \_ 狀態**， *pPrinter* 必須包含 **DWORD** 值，以指定要設定的新印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="7e32f-120">If the *Command* parameter is **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must contain a **DWORD** value that specifies the new printer status to set.</span></span> <span data-ttu-id="7e32f-121">如需可能狀態值的清單，請參閱 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **狀態** 成員。</span><span class="sxs-lookup"><span data-stu-id="7e32f-121">For a list of the possible status values, see the **Status** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span> <span data-ttu-id="7e32f-122">請注意，[ **印表機 \_ 狀態 \_ 暫停** ] 和 [ **印表機 \_ 狀態 \_ 擱置 \_ 刪除** ] 不是要設定的有效狀態值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-122">Note that **PRINTER\_STATUS\_PAUSED** and **PRINTER\_STATUS\_PENDING\_DELETION** are not valid status values to set.</span></span><br/> <span data-ttu-id="7e32f-123">如果 *層級* 為0，但 *命令* 參數不是 **印表機 \_ 控制 \_ 集 \_ 狀態**，則 *pPrinter* 必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7e32f-123">If *Level* is 0, but the *Command* parameter is not **PRINTER\_CONTROL\_SET\_STATUS**, *pPrinter* must be **NULL**.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="7e32f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="7e32f-125">[**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構，內含印表機的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7e32f-125">A [**PRINTER\_INFO\_2**](printer-info-2.md) structure containing detailed information about the printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <span data-ttu-id="7e32f-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="7e32f-127">[**印表機 \_ 資訊 \_ 3**](printer-info-3.md)結構，內含印表機的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="7e32f-127">A [**PRINTER\_INFO\_3**](printer-info-3.md) structure containing the printer's security information.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <span data-ttu-id="7e32f-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="7e32f-129">[**印表機 \_ 資訊 \_ 4**](printer-info-4.md)結構，其中包含最少量的印表機資訊，包括印表機的名稱、伺服器的名稱，以及印表機是否為遠端或本機。</span><span class="sxs-lookup"><span data-stu-id="7e32f-129">A [**PRINTER\_INFO\_4**](printer-info-4.md) structure containing minimal printer information, including the name of the printer, the name of the server, and whether the printer is remote or local.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <span data-ttu-id="7e32f-130"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-130"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="7e32f-131">[**印表機 \_ 資訊 \_ 5**](printer-info-5.md)結構，包含印表機屬性和超時設定等印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="7e32f-131">A [**PRINTER\_INFO\_5**](printer-info-5.md) structure containing printer information such as printer attributes and time-out settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <span data-ttu-id="7e32f-132"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-132"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="7e32f-133">[**印表機 \_ 資訊 \_ 6**](printer-info-6.md)結構，指定印表機的狀態值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-133">A [**PRINTER\_INFO\_6**](printer-info-6.md) structure specifying the status value of a printer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <span data-ttu-id="7e32f-134"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-134"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="7e32f-135">[**印表機 \_ 資訊 \_ 7**](printer-info-7.md)結構。</span><span class="sxs-lookup"><span data-stu-id="7e32f-135">A [**PRINTER\_INFO\_7**](printer-info-7.md) structure.</span></span> <span data-ttu-id="7e32f-136">此結構的 *dwAction* 成員指出 **SetPrinter** 是否應該在目錄服務中發佈、取消發行、重新發行或更新印表機的資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-136">The *dwAction* member of this structure indicates whether **SetPrinter** should publish, unpublish, re-publish, or update the printer's data in the directory service.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <span data-ttu-id="7e32f-137"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-137"><dt>**8**</dt></span></span> </dl> | <span data-ttu-id="7e32f-138">[**印表機 \_ 資訊 \_ 8**](printer-info-8.md)結構，指定全域預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="7e32f-138">A [**PRINTER\_INFO\_8**](printer-info-8.md) structure specifying the global default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <span data-ttu-id="7e32f-139"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-139"><dt>**9**</dt></span></span> </dl> | <span data-ttu-id="7e32f-140">[**印表機 \_ 資訊 \_ 9**](printer-info-9.md)結構，指定每個使用者的預設印表機設定。</span><span class="sxs-lookup"><span data-stu-id="7e32f-140">A [**PRINTER\_INFO\_9**](printer-info-9.md) structure specifying the per-user default printer settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="7e32f-141">*命令* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-141">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e32f-142">要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="7e32f-142">The action to perform.</span></span>

<span data-ttu-id="7e32f-143">如果 *Level* 參數為非零值，請將此參數的值設定為零。</span><span class="sxs-lookup"><span data-stu-id="7e32f-143">If the *Level* parameter is nonzero, set the value of this parameter to zero.</span></span> <span data-ttu-id="7e32f-144">在此情況下，印表機會保留其目前的狀態，而函式會根據 *Level* 和 *pPrinter* 參數所指定的方式重新配置印表機資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-144">In this case, the printer retains its current state and the function reconfigures the printer data as specified by the *Level* and *pPrinter* parameters.</span></span>

<span data-ttu-id="7e32f-145">如果 *Level* 參數為零，請將此參數的值設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-145">If the *Level* parameter is zero, set the value of this parameter to one of the following values.</span></span>



| <span data-ttu-id="7e32f-146">值</span><span class="sxs-lookup"><span data-stu-id="7e32f-146">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="7e32f-147">意義</span><span class="sxs-lookup"><span data-stu-id="7e32f-147">Meaning</span></span>                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <span data-ttu-id="7e32f-148"><dt>**印表機 \_ 控制項 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-148"><dt>**PRINTER\_CONTROL\_PAUSE**</dt></span></span> </dl>                 | <span data-ttu-id="7e32f-149">暫停印表機。</span><span class="sxs-lookup"><span data-stu-id="7e32f-149">Pause the printer.</span></span><br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <span data-ttu-id="7e32f-150"><dt>**印表機 \_ 控制項 \_ 清除**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-150"><dt>**PRINTER\_CONTROL\_PURGE**</dt></span></span> </dl>                 | <span data-ttu-id="7e32f-151">刪除印表機中的所有列印工作。</span><span class="sxs-lookup"><span data-stu-id="7e32f-151">Delete all print jobs in the printer.</span></span><br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <span data-ttu-id="7e32f-152"><dt>**印表機 \_ 控制項 \_ 繼續**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-152"><dt>**PRINTER\_CONTROL\_RESUME**</dt></span></span> </dl>              | <span data-ttu-id="7e32f-153">繼續暫停的印表機。</span><span class="sxs-lookup"><span data-stu-id="7e32f-153">Resume a paused printer.</span></span><br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <span data-ttu-id="7e32f-154"><dt>**印表機 \_ 控制 \_ 集 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-154"><dt>**PRINTER\_CONTROL\_SET\_STATUS**</dt></span></span> </dl> | <span data-ttu-id="7e32f-155">設定印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="7e32f-155">Set the printer status.</span></span><br/> <span data-ttu-id="7e32f-156">將 *pPrinter* 參數設定為 **DWORD** 值的指標，以指定新的印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="7e32f-156">Set the *pPrinter* parameter to a pointer to a **DWORD** value that specifies the new printer status.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e32f-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e32f-157">Return value</span></span>

<span data-ttu-id="7e32f-158">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-158">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7e32f-159">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="7e32f-159">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="7e32f-160">如果 *層級* 為7且發行動作失敗， **SetPrinter** 會傳回 **錯誤 \_ IO \_ 暫** 止，並嘗試在背景中完成動作。</span><span class="sxs-lookup"><span data-stu-id="7e32f-160">If *Level* is 7 and the publish action failed, **SetPrinter** returns **ERROR\_IO\_PENDING** and attempts to complete the action in the background.</span></span> <span data-ttu-id="7e32f-161">如果 *層級* 為7且更新動作失敗，則 **SetPrinter** 會傳回錯誤檔案，但 **\_ \_ \_ 找不到**。</span><span class="sxs-lookup"><span data-stu-id="7e32f-161">If *Level* is 7 and the update action failed, **SetPrinter** returns **ERROR\_FILE\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e32f-162">備註</span><span class="sxs-lookup"><span data-stu-id="7e32f-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7e32f-163">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="7e32f-163">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7e32f-164">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="7e32f-164">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7e32f-165">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="7e32f-165">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="7e32f-166">您無法使用 **SetPrinter** 來變更預設印表機。</span><span class="sxs-lookup"><span data-stu-id="7e32f-166">You cannot use **SetPrinter** to change the default printer.</span></span>

<span data-ttu-id="7e32f-167">若要修改目前的印表機設定，請呼叫 [**GetPrinter**](getprinter.md) 函式，將目前的設定取出至 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構，視需要修改該結構的成員，然後再呼叫 **SetPrinter**。</span><span class="sxs-lookup"><span data-stu-id="7e32f-167">To modify the current printer settings, call the [**GetPrinter**](getprinter.md) function to retrieve the current settings into a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, modify the members of that structure as necessary, and then call **SetPrinter**.</span></span>

<span data-ttu-id="7e32f-168">**SetPrinter** 函式會忽略 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構的 **pServerName**、 **AveragePPM**、 **Status** 和 **cJobs** 成員。</span><span class="sxs-lookup"><span data-stu-id="7e32f-168">The **SetPrinter** function ignores the **pServerName**, **AveragePPM**, **Status**, and **cJobs** members of a [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

<span data-ttu-id="7e32f-169">暫停印表機會暫停該印表機所有列印工作的排程，但可能正在列印的列印工作除外。</span><span class="sxs-lookup"><span data-stu-id="7e32f-169">Pausing a printer suspends scheduling of all print jobs for that printer, except for the one print job that may be currently printing.</span></span> <span data-ttu-id="7e32f-170">列印工作可以提交到暫停的印表機，但在繼續列印之前，將不會排定在該印表機上列印工作。</span><span class="sxs-lookup"><span data-stu-id="7e32f-170">Print jobs can be submitted to a paused printer, but no jobs will be scheduled to print on that printer until printing is resumed.</span></span> <span data-ttu-id="7e32f-171">如果清除印表機，則會刪除該印表機的所有列印工作，但目前的列印工作除外。</span><span class="sxs-lookup"><span data-stu-id="7e32f-171">If a printer is cleared, all print jobs for that printer are deleted, except for the current print job.</span></span>

<span data-ttu-id="7e32f-172">如果您使用 **SetPrinter** 來修改印表機的預設 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構 (全域設定印表機預設值) ，您必須先呼叫 [**DocumentProperties**](documentproperties.md) 函數來驗證 **DEVMODE** 結構。</span><span class="sxs-lookup"><span data-stu-id="7e32f-172">If you use **SetPrinter** to modify the default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure for a printer (globally setting the printer defaults), you must first call the [**DocumentProperties**](documentproperties.md) function to validate the **DEVMODE** structure.</span></span>

<span data-ttu-id="7e32f-173">針對包含安全描述項指標的 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 和 [**印表機 \_ 資訊 \_ 3**](printer-info-3.md) 結構，此函式只能設定呼叫者有權修改之安全描述項的元件。</span><span class="sxs-lookup"><span data-stu-id="7e32f-173">For the [**PRINTER\_INFO\_2**](printer-info-2.md) and [**PRINTER\_INFO\_3**](printer-info-3.md) structures that contain a pointer to a security descriptor, the function can set only those components of the security descriptor that the caller has permission to modify.</span></span> <span data-ttu-id="7e32f-174">若要設定特定的安全描述項元件，您必須在呼叫 [**OpenPrinter**](openprinter.md) 或 [**OpenPrinter2**](openprinter2.md) 函式來取得印表機的控制碼時，指定必要的存取權限。</span><span class="sxs-lookup"><span data-stu-id="7e32f-174">To set particular security descriptor components, you must specify the necessary access rights when you call the [**OpenPrinter**](openprinter.md) or [**OpenPrinter2**](openprinter2.md) function to retrieve a handle to the printer.</span></span> <span data-ttu-id="7e32f-175">下表顯示修改各種安全描述項元件所需的存取權限。</span><span class="sxs-lookup"><span data-stu-id="7e32f-175">The following table shows the access rights required to modify the various security descriptor components.</span></span>



| <span data-ttu-id="7e32f-176">存取權限</span><span class="sxs-lookup"><span data-stu-id="7e32f-176">Access permission</span></span>            | <span data-ttu-id="7e32f-177">安全描述項元件</span><span class="sxs-lookup"><span data-stu-id="7e32f-177">Security descriptor component</span></span>             |
|------------------------------|-------------------------------------------|
| <span data-ttu-id="7e32f-178">**寫入 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="7e32f-178">**WRITE\_OWNER**</span></span>             | <span data-ttu-id="7e32f-179">擁有者</span><span class="sxs-lookup"><span data-stu-id="7e32f-179">Owner</span></span><br/> <span data-ttu-id="7e32f-180">主要群組</span><span class="sxs-lookup"><span data-stu-id="7e32f-180">Primary group</span></span><br/> |
| <span data-ttu-id="7e32f-181">**寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="7e32f-181">**WRITE\_DAC**</span></span>               | <span data-ttu-id="7e32f-182">任意存取控制清單 (DACL) </span><span class="sxs-lookup"><span data-stu-id="7e32f-182">Discretionary access-control list (DACL)</span></span>  |
| <span data-ttu-id="7e32f-183">**存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="7e32f-183">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="7e32f-184">系統存取控制清單 (SACL) </span><span class="sxs-lookup"><span data-stu-id="7e32f-184">System access-control list (SACL)</span></span>         |



 

<span data-ttu-id="7e32f-185">如果安全描述項包含呼叫端沒有修改許可權的元件， **SetPrinter** 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="7e32f-185">If the security descriptor contains a component that the caller does not have the access right to modify, **SetPrinter** fails.</span></span> <span data-ttu-id="7e32f-186">您不想要修改之安全描述項的元件應該是 **Null** 或不存在。</span><span class="sxs-lookup"><span data-stu-id="7e32f-186">Those components of a security descriptor that you don't want to modify should be **NULL** or not be present, as appropriate.</span></span> <span data-ttu-id="7e32f-187">如果您不想要修改安全描述項，並且使用 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md)結構來呼叫 **SetPrinter** ，請將該結構的 **pSecurityDescriptor** 成員設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7e32f-187">If you do not want to modify the security descriptor, and are calling **SetPrinter** with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, set the **pSecurityDescriptor** member of that structure to **NULL**.</span></span>

<span data-ttu-id="7e32f-188">網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7e32f-188">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="7e32f-189">如果電腦系統管理員呼叫 **SetPrinter** ，則會啟用例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7e32f-189">If **SetPrinter** is called by a machine admin, it enables the exception.</span></span> <span data-ttu-id="7e32f-190">如果非系統管理員呼叫它，而且尚未啟用例外狀況，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="7e32f-190">If it is called by a non-admin and the exception has not already been enabled, the call fails.</span></span>

<span data-ttu-id="7e32f-191">您可以使用層級7搭配 [**印表機 \_ 資訊 \_ 7**](printer-info-7.md) 結構，來發佈、取消發行或更新印表機的目錄服務資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-191">You can use level 7 with the [**PRINTER\_INFO\_7**](printer-info-7.md) structure to publish, unpublish, or update directory service data for the printer.</span></span> <span data-ttu-id="7e32f-192">印表機的目錄服務資料會藉 \_ \* 由呼叫印表機的 [**SetPrinterDataEx**](setprinterdataex.md)函式，包含儲存在 SPLDS 機碼下的所有資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-192">The directory service data for a printer includes all the data stored under the SPLDS\_\* keys by calls to the [**SetPrinterDataEx**](setprinterdataex.md) function for the printer.</span></span> <span data-ttu-id="7e32f-193">在呼叫 **SetPrinter** 之前，請將 **印表機 \_ 資訊 \_ 7** 的 **pszObjectGUID** 成員設為 **Null** ，並將 *dwAction* 成員設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-193">Before calling **SetPrinter**, set the **pszObjectGUID** member of **PRINTER\_INFO\_7** to **NULL** and set the *dwAction* member to one of the following values.</span></span>



| <span data-ttu-id="7e32f-194">值</span><span class="sxs-lookup"><span data-stu-id="7e32f-194">Value</span></span>                             | <span data-ttu-id="7e32f-195">描述</span><span class="sxs-lookup"><span data-stu-id="7e32f-195">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e32f-196">**DSPRINT \_ 發行**</span><span class="sxs-lookup"><span data-stu-id="7e32f-196">**DSPRINT\_PUBLISH**</span></span><br/>   | <span data-ttu-id="7e32f-197">發佈目錄服務資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-197">Publishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7e32f-198">**DSPRINT 重新 \_ 發佈**</span><span class="sxs-lookup"><span data-stu-id="7e32f-198">**DSPRINT\_REPUBLISH**</span></span><br/> | <span data-ttu-id="7e32f-199">印表機的目錄服務資料會解除發佈，然後再重新發佈，以重新整理已發佈印表機中的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="7e32f-199">The directory service data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="7e32f-200">重新發佈也會變更已發行之印表機的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7e32f-200">Re-publishing also changes the GUID of the published printer.</span></span> <span data-ttu-id="7e32f-201">如果您懷疑印表機已發佈的資料已損毀，請使用此值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-201">Use this value if you suspect the printer's published data has been corrupted.</span></span><br/>                                                                                         |
| <span data-ttu-id="7e32f-202">**DSPRINT \_ 取消發佈**</span><span class="sxs-lookup"><span data-stu-id="7e32f-202">**DSPRINT\_UNPUBLISH**</span></span><br/> | <span data-ttu-id="7e32f-203">Unpublishes 目錄服務資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-203">Unpublishes the directory service data.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7e32f-204">**DSPRINT \_ 更新**</span><span class="sxs-lookup"><span data-stu-id="7e32f-204">**DSPRINT\_UPDATE**</span></span><br/>    | <span data-ttu-id="7e32f-205">更新目錄服務資料。</span><span class="sxs-lookup"><span data-stu-id="7e32f-205">Updates the directory service data.</span></span> <span data-ttu-id="7e32f-206">這與 **DSPRINT \_ PUBLISH** 相同，不同之處在于如果印表機尚未發佈，則 **SetPrinter** 會失敗，而且 **\_ \_ \_ 找不到錯誤** 檔案。</span><span class="sxs-lookup"><span data-stu-id="7e32f-206">This is the same as **DSPRINT\_PUBLISH**, except that **SetPrinter** fails with **ERROR\_FILE\_NOT\_FOUND** if the printer is not already published.</span></span><br/> <span data-ttu-id="7e32f-207">使用 **DSPRINT \_ update** 來更新已發行的屬性，但不強制發行。</span><span class="sxs-lookup"><span data-stu-id="7e32f-207">Use **DSPRINT\_UPDATE** to update published properties but not force publishing.</span></span> <span data-ttu-id="7e32f-208">印表機驅動程式應該一律使用 **DSPRINT \_ UPDATE** ，而不是 **DSPRINT \_ PUBLISH**。</span><span class="sxs-lookup"><span data-stu-id="7e32f-208">Printer drivers should always use **DSPRINT\_UPDATE** rather than **DSPRINT\_PUBLISH**.</span></span><br/> |



 

<span data-ttu-id="7e32f-209">**DSPRINT \_暫** 止不是 **SetPrinter** 的有效 *dwAction* 值。</span><span class="sxs-lookup"><span data-stu-id="7e32f-209">**DSPRINT\_PENDING** is not a valid *dwAction* value for **SetPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e32f-210">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e32f-210">Requirements</span></span>



| <span data-ttu-id="7e32f-211">需求</span><span class="sxs-lookup"><span data-stu-id="7e32f-211">Requirement</span></span> | <span data-ttu-id="7e32f-212">值</span><span class="sxs-lookup"><span data-stu-id="7e32f-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e32f-213">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e32f-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7e32f-214">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-214">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7e32f-215">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e32f-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7e32f-216">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e32f-216">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7e32f-217">標頭</span><span class="sxs-lookup"><span data-stu-id="7e32f-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e32f-218"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-218"><dt>WinSpool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7e32f-219">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e32f-219">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e32f-220"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-220"><dt>WinSpool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7e32f-221">DLL</span><span class="sxs-lookup"><span data-stu-id="7e32f-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e32f-222"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="7e32f-222"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7e32f-223">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7e32f-223">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7e32f-224">**SetPrinterW** (Unicode) 和 **SetPrinterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7e32f-224">**SetPrinterW** (Unicode) and **SetPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="7e32f-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e32f-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e32f-226">列印</span><span class="sxs-lookup"><span data-stu-id="7e32f-226">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7e32f-227">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="7e32f-227">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7e32f-228">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="7e32f-228">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="7e32f-229">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="7e32f-229">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="7e32f-230">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="7e32f-230">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="7e32f-231">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="7e32f-231">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="7e32f-232">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7e32f-232">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="7e32f-233">**印表機 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="7e32f-233">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="7e32f-234">**印表機 \_ 資訊 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="7e32f-234">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="7e32f-235">**印表機 \_ 資訊 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="7e32f-235">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="7e32f-236">**印表機 \_ 資訊 \_ 6**</span><span class="sxs-lookup"><span data-stu-id="7e32f-236">**PRINTER\_INFO\_6**</span></span>](printer-info-6.md)
</dt> <dt>

[<span data-ttu-id="7e32f-237">**印表機 \_ 資訊 \_ 7**</span><span class="sxs-lookup"><span data-stu-id="7e32f-237">**PRINTER\_INFO\_7**</span></span>](printer-info-7.md)
</dt> <dt>

[<span data-ttu-id="7e32f-238">**印表機 \_ 資訊 \_ 8**</span><span class="sxs-lookup"><span data-stu-id="7e32f-238">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> <dt>

[<span data-ttu-id="7e32f-239">**印表機 \_ 資訊 \_ 9**</span><span class="sxs-lookup"><span data-stu-id="7e32f-239">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> <dt>

[<span data-ttu-id="7e32f-240">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="7e32f-240">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




