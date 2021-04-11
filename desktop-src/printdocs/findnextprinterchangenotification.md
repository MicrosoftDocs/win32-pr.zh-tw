---
description: FindNextPrinterChangeNotification 函式會針對與印表機或列印伺服器相關聯的變更通知物件，抓取最新變更通知的相關資訊。
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: 'FindNextPrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850064"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="37cb8-103">FindNextPrinterChangeNotification 函式</span><span class="sxs-lookup"><span data-stu-id="37cb8-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="37cb8-104">**FindNextPrinterChangeNotification** 函式會針對與印表機或列印伺服器相關聯的變更通知物件，抓取最新變更通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="37cb8-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="37cb8-105">當滿足變更通知物件的等候作業時，請呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="37cb8-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="37cb8-106">此函數也會將變更通知物件重設為未收到信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="37cb8-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="37cb8-107">然後，您可以在另一個等候作業中使用此物件，以繼續監視印表機或列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="37cb8-108">作業系統會在下一次對印表機或列印伺服器進行一組指定的變更時，將物件設定為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="37cb8-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="37cb8-109">[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)函式會建立變更通知物件，並指定要監視的變更集。</span><span class="sxs-lookup"><span data-stu-id="37cb8-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cb8-110">語法</span><span class="sxs-lookup"><span data-stu-id="37cb8-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="37cb8-111">參數</span><span class="sxs-lookup"><span data-stu-id="37cb8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37cb8-112">*hChange* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37cb8-113">與印表機或列印伺服器相關聯之變更通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="37cb8-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="37cb8-114">您可以藉由呼叫 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 函數來取得這類控制碼。</span><span class="sxs-lookup"><span data-stu-id="37cb8-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="37cb8-115">當偵測到物件的變更通知篩選器中所指定的其中一項變更時，作業系統會將此變更通知物件設定為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="37cb8-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="37cb8-116">*pdwChange* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37cb8-117">變數的指標，其位設定為表示造成最新通知的變更。</span><span class="sxs-lookup"><span data-stu-id="37cb8-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="37cb8-118">可能設定的位旗標，會對應至 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)呼叫的 *fdwFilter* 參數中指定的位旗標。</span><span class="sxs-lookup"><span data-stu-id="37cb8-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="37cb8-119">系統會設定下列一或多個位旗標。</span><span class="sxs-lookup"><span data-stu-id="37cb8-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="37cb8-120">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="37cb8-121">意義</span><span class="sxs-lookup"><span data-stu-id="37cb8-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="37cb8-122"><dt>**印表機 \_ 變更 \_ 新增 \_ 表單**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="37cb8-123">已將表單新增至伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="37cb8-124"><dt>**印表機 \_ 變更 \_ 新增 \_ 作業**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="37cb8-125">列印工作已傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="37cb8-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="37cb8-126"><dt>**印表機 \_ 變更 \_ 新增 \_ 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="37cb8-127">埠或監視器已新增至伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="37cb8-128"><dt>**印表機 \_ 變更 \_ 新增 \_ 列印 \_ 處理器**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="37cb8-129">列印處理器已新增至伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="37cb8-130"><dt>**印表機 \_ 變更 \_ 新增 \_ 印表機**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="37cb8-131">印表機已新增至伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="37cb8-132"><dt>**印表機 \_ 變更 \_ 新增 \_ 印表機 \_ 驅動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="37cb8-133">印表機驅動程式已新增至伺服器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="37cb8-134"><dt>**印表機 \_ 變更 \_ 設定 \_ 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="37cb8-135">已在伺服器上設定埠。</span><span class="sxs-lookup"><span data-stu-id="37cb8-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="37cb8-136"><dt>**印表機 \_ 變更 \_ 刪除 \_ 表單**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="37cb8-137">已從伺服器刪除表單。</span><span class="sxs-lookup"><span data-stu-id="37cb8-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="37cb8-138"><dt>**印表機 \_ 變更 \_ 刪除 \_ 作業**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="37cb8-139">已刪除作業。</span><span class="sxs-lookup"><span data-stu-id="37cb8-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="37cb8-140"><dt>**印表機 \_ 變更 \_ 刪除 \_ 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="37cb8-141">埠或監視器已從伺服器刪除。</span><span class="sxs-lookup"><span data-stu-id="37cb8-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="37cb8-142"><dt>**印表機 \_ 變更 \_ 刪除 \_ 列印 \_ 處理器**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="37cb8-143">已從伺服器刪除列印處理器。</span><span class="sxs-lookup"><span data-stu-id="37cb8-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="37cb8-144"><dt>**印表機 \_ 變更 \_ 刪除 \_ 印表機**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="37cb8-145">已刪除印表機。</span><span class="sxs-lookup"><span data-stu-id="37cb8-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="37cb8-146"><dt>**印表機 \_ 變更 \_ 刪除 \_ 印表機 \_ 驅動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="37cb8-147">已從伺服器刪除印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="37cb8-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="37cb8-148"><dt>**印表機 \_ 變更 \_ \_ 連接 \_ 印表機失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="37cb8-149">印表機連接已失敗。</span><span class="sxs-lookup"><span data-stu-id="37cb8-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="37cb8-150"><dt>**印表機 \_ 變更 \_ 集 \_ 表單**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="37cb8-151">已在伺服器上設定表單。</span><span class="sxs-lookup"><span data-stu-id="37cb8-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="37cb8-152"><dt>**印表機 \_ 變更 \_ 集 \_ 作業**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="37cb8-153">已設定作業。</span><span class="sxs-lookup"><span data-stu-id="37cb8-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="37cb8-154"><dt>**印表機 \_ 變更 \_ 集 \_ 印表機**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="37cb8-155">已設定印表機。</span><span class="sxs-lookup"><span data-stu-id="37cb8-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="37cb8-156"><dt>**印表機 \_ 變更 \_ 集 \_ 印表機 \_ 驅動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="37cb8-157">已設定印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="37cb8-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="37cb8-158"><dt>**印表機 \_ 變更 \_ 寫入 \_ 作業**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="37cb8-159">已寫入工作資料。</span><span class="sxs-lookup"><span data-stu-id="37cb8-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="37cb8-160"><dt>**印表機 \_ 變更 \_ 超時**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="37cb8-161">作業超時。</span><span class="sxs-lookup"><span data-stu-id="37cb8-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="37cb8-162"><dt>**印表機 \_ 變更 \_ 伺服器**</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="37cb8-163">Windows 7：伺服器發生變更。</span><span class="sxs-lookup"><span data-stu-id="37cb8-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="37cb8-164">*pPrinterNotifyOptions* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37cb8-165">[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="37cb8-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="37cb8-166">將此結構的 **旗標** 成員設定為 [ **印表機 \_ 通知 \_ 選項 \_** 重新整理]，讓函式傳回所有受監視印表機資訊欄位的目前資料。</span><span class="sxs-lookup"><span data-stu-id="37cb8-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="37cb8-167">函數會忽略結構的所有其他成員。</span><span class="sxs-lookup"><span data-stu-id="37cb8-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="37cb8-168">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="37cb8-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="37cb8-169">*ppPrinterNotifyInfo* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="37cb8-170">指標變數的指標，此變數會接收系統組態的唯讀緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="37cb8-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="37cb8-171">當您完成時，請呼叫 [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) 函式來釋放緩衝區。</span><span class="sxs-lookup"><span data-stu-id="37cb8-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="37cb8-172">如果不需要任何資訊，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="37cb8-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="37cb8-173">緩衝區包含 [**印表機 \_ 通知 \_ 資訊**](printer-notify-info.md) 結構，其中包含 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="37cb8-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="37cb8-174">陣列的每個元素都包含 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)呼叫的 *pPrinterNotifyOptions* 參數中所指定的其中一個欄位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="37cb8-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="37cb8-175">一般而言，此函數只會針對變更為的欄位提供資料，以導致最近的通知。</span><span class="sxs-lookup"><span data-stu-id="37cb8-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="37cb8-176">但是，如果 *pPrinterNotifyOptions* 參數所指向的結構指定了 **印表機 \_ 通知 \_ 選項 \_** 重新整理，則此函式會為所有受監視的欄位提供資料。</span><span class="sxs-lookup"><span data-stu-id="37cb8-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="37cb8-177">如果 [**印表機通知資訊結構的 \_ \_**](printer-notify-info.md) **旗標** 成員中設定了 [**印表機 \_ 通知資訊已 \_ \_ 捨棄** 位]，就會發生溢位或錯誤，而且通知可能已遺失。</span><span class="sxs-lookup"><span data-stu-id="37cb8-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="37cb8-178">在此情況下，在您進行第二個 **FindNextPrinterChangeNotification** 呼叫以指定 **印表機 \_ 通知 \_ 選項 \_** 重新整理之前，將不會傳送任何其他通知。</span><span class="sxs-lookup"><span data-stu-id="37cb8-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37cb8-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="37cb8-179">Return value</span></span>

<span data-ttu-id="37cb8-180">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="37cb8-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="37cb8-181">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="37cb8-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="37cb8-182">備註</span><span class="sxs-lookup"><span data-stu-id="37cb8-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="37cb8-183">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="37cb8-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="37cb8-184">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="37cb8-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="37cb8-185">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="37cb8-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="37cb8-186">滿足 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)所建立之通知物件的等候作業之後，請呼叫 **FindNextPrinterChangeNotification** 函數。</span><span class="sxs-lookup"><span data-stu-id="37cb8-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="37cb8-187">呼叫 **FindNextPrinterChangeNotification** 可讓您取得滿足等候作業之變更的相關資訊，並重設通知物件，以便在下一次發生變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="37cb8-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="37cb8-188">有一個例外狀況，如果變更通知物件不是處於已發出信號的狀態，請勿呼叫 **FindNextPrinterChangeNotification** 函數。</span><span class="sxs-lookup"><span data-stu-id="37cb8-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="37cb8-189">如果等候函式傳回值 **等候 \_ 超時**，則變更物件不會處於已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="37cb8-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="37cb8-190">只有在等候函式成功時才呼叫 **FindNextPrinterChangeNotification** 函式，而不會超時。當使用 *pPrinterNotifyOptions* 參數中所設定的 **印表機 \_ 通知 \_ 選項 \_** 重新整理位來呼叫 **FindNextPrinterChangeNotification** 時，就會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="37cb8-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="37cb8-191">請注意，即使設定此旗標，仍可能在 *ppPrinterNotifyInfo* 參數中設定 [已 **\_ \_ \_ 捨棄印表機通知資訊**] 旗標。</span><span class="sxs-lookup"><span data-stu-id="37cb8-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="37cb8-192">若要繼續監視印表機或列印伺服器的變更，請重複呼叫其中一個 [wait](/windows/desktop/Sync/wait-functions) 函式的迴圈，然後呼叫 **FindNextPrinterChangeNotification** 函式來檢查變更並重設通知物件。</span><span class="sxs-lookup"><span data-stu-id="37cb8-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="37cb8-193">**FindNextPrinterChangeNotification** 可能會將相同印表機資訊欄位的多個變更合併成單一通知。</span><span class="sxs-lookup"><span data-stu-id="37cb8-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="37cb8-194">發生這種情況時，函式通常會將欄位的所有變更折迭為 *ppPrinterNotifyInfo* 中的 [**印表機 \_ 通知 \_ 資訊 \_ 資料**](printer-notify-info-data.md)結構陣列中的單一專案; 單一專案只報告最新的資訊。</span><span class="sxs-lookup"><span data-stu-id="37cb8-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="37cb8-195">不過，對於某些作業和印表機資訊欄位，此函數可以針對相同的欄位傳回多個陣列專案。</span><span class="sxs-lookup"><span data-stu-id="37cb8-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="37cb8-196">在此情況下，欄位的最後一個陣列專案會報告目前的資料，而較舊的專案則包含中繼階段的資料。</span><span class="sxs-lookup"><span data-stu-id="37cb8-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="37cb8-197">當您不再需要變更通知物件時，請呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) 函式將其關閉。</span><span class="sxs-lookup"><span data-stu-id="37cb8-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="37cb8-198">在 Windows XP Service Pack 2 (SP2) 和更新版本中，網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="37cb8-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="37cb8-199">如果使用者將印表機連線到另一部電腦，但未啟用例外狀況，則使用者將不會收到來自伺服器的印表機變更通知。</span><span class="sxs-lookup"><span data-stu-id="37cb8-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="37cb8-200">電腦系統管理員必須啟用例外狀況。</span><span class="sxs-lookup"><span data-stu-id="37cb8-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="37cb8-201">範例</span><span class="sxs-lookup"><span data-stu-id="37cb8-201">Examples</span></span>

<span data-ttu-id="37cb8-202">下列程式碼範例說明如何使用這些功能來監視印表機狀態。</span><span class="sxs-lookup"><span data-stu-id="37cb8-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="37cb8-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="37cb8-203">Requirements</span></span>



| <span data-ttu-id="37cb8-204">需求</span><span class="sxs-lookup"><span data-stu-id="37cb8-204">Requirement</span></span> | <span data-ttu-id="37cb8-205">值</span><span class="sxs-lookup"><span data-stu-id="37cb8-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cb8-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37cb8-206">Minimum supported client</span></span><br/> | <span data-ttu-id="37cb8-207">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37cb8-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37cb8-208">Minimum supported server</span></span><br/> | <span data-ttu-id="37cb8-209">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37cb8-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37cb8-210">標頭</span><span class="sxs-lookup"><span data-stu-id="37cb8-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="37cb8-211"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="37cb8-212">程式庫</span><span class="sxs-lookup"><span data-stu-id="37cb8-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="37cb8-213"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="37cb8-214">DLL</span><span class="sxs-lookup"><span data-stu-id="37cb8-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37cb8-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37cb8-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="37cb8-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37cb8-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cb8-217">列印</span><span class="sxs-lookup"><span data-stu-id="37cb8-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="37cb8-218">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="37cb8-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="37cb8-219">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="37cb8-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="37cb8-220">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="37cb8-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="37cb8-221">**印表機 \_ 通知 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="37cb8-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="37cb8-222">**印表機 \_ 通知 \_ 資訊 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="37cb8-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="37cb8-223">**印表機 \_ 通知 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="37cb8-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

