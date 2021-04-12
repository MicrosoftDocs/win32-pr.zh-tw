---
description: FindFirstPrinterChangeNotification 函式會建立變更通知物件，並將控制碼傳回物件。 然後，您可以在呼叫其中一個等候函式時，使用這個控制碼來監視印表機或列印伺服器的變更。
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: 'FindFirstPrinterChangeNotification 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192721"
---
# <a name="findfirstprinterchangenotification-function"></a><span data-ttu-id="a7155-104">FindFirstPrinterChangeNotification 函式</span><span class="sxs-lookup"><span data-stu-id="a7155-104">FindFirstPrinterChangeNotification function</span></span>

<span data-ttu-id="a7155-105">**FindFirstPrinterChangeNotification** 函式會建立變更通知物件，並將控制碼傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a7155-105">The **FindFirstPrinterChangeNotification** function creates a change notification object and returns a handle to the object.</span></span> <span data-ttu-id="a7155-106">然後，您可以在呼叫其中一個等候函式時，使用這個控制碼來監視印表機或列印伺服器的變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-106">You can then use this handle in a call to one of the wait functions to monitor changes to the printer or print server.</span></span>

<span data-ttu-id="a7155-107">**FindFirstPrinterChangeNotification** 呼叫會指定要監視的變更類型。</span><span class="sxs-lookup"><span data-stu-id="a7155-107">The **FindFirstPrinterChangeNotification** call specifies the type of changes to be monitored.</span></span> <span data-ttu-id="a7155-108">您可以指定一組條件來監視變更、一組要監視的印表機資訊欄位，或兩者。</span><span class="sxs-lookup"><span data-stu-id="a7155-108">You can specify a set of conditions to monitor for changes, a set of printer information fields to monitor, or both.</span></span>

<span data-ttu-id="a7155-109">當指定的印表機或列印伺服器發生其中一個指定的變更時，變更通知控制碼上的等候作業就會成功。</span><span class="sxs-lookup"><span data-stu-id="a7155-109">A wait operation on the change notification handle succeeds when one of the specified changes occurs in the specified printer or print server.</span></span> <span data-ttu-id="a7155-110">然後，您可以呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式來取得變更的相關資訊，以及重設變更通知物件，以便在下一次等候操作中使用。</span><span class="sxs-lookup"><span data-stu-id="a7155-110">You then call the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to retrieve information about the change, and to reset the change notification object for use in the next wait operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7155-111">語法</span><span class="sxs-lookup"><span data-stu-id="a7155-111">Syntax</span></span>


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a><span data-ttu-id="a7155-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7155-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7155-113">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7155-113">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7155-114">您要監視的印表機或列印伺服器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7155-114">A handle to the printer or print server that you want to monitor.</span></span> <span data-ttu-id="a7155-115">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7155-115">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a7155-116">*fdwFilter*</span><span class="sxs-lookup"><span data-stu-id="a7155-116">*fdwFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="a7155-117">會導致變更通知物件進入信號狀態的條件。</span><span class="sxs-lookup"><span data-stu-id="a7155-117">The conditions that will cause the change notification object to enter a signaled state.</span></span> <span data-ttu-id="a7155-118">當符合一或多個指定的條件時，就會發生變更通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-118">A change notification occurs when one or more of the specified conditions are met.</span></span> <span data-ttu-id="a7155-119">如果 *pPrinterNotifyOptions* 為非 **Null**，則 *fdwFilter* 參數可以為零。</span><span class="sxs-lookup"><span data-stu-id="a7155-119">The *fdwFilter* parameter can be zero if *pPrinterNotifyOptions* is non-**NULL**.</span></span>

<span data-ttu-id="a7155-120">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a7155-120">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a7155-121">值</span><span class="sxs-lookup"><span data-stu-id="a7155-121">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="a7155-122">意義</span><span class="sxs-lookup"><span data-stu-id="a7155-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <span data-ttu-id="a7155-123"><dt>**印表機 \_ 變更 \_ 表單**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-123"><dt>**PRINTER\_CHANGE\_FORM**</dt></span></span> </dl>                                   | <span data-ttu-id="a7155-124">通知表單的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-124">Notify of any changes to a form.</span></span> <span data-ttu-id="a7155-125">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-125">You can set this general flag or one or more of the following specific flags:</span></span><br/> <dl> <dd><span data-ttu-id="a7155-126">印表機 \_ 變更 \_ 新增 \_ 表單</span><span class="sxs-lookup"><span data-stu-id="a7155-126">PRINTER\_CHANGE\_ADD\_FORM</span></span></dd> <dd><span data-ttu-id="a7155-127">印表機 \_ 變更 \_ 集 \_ 表單</span><span class="sxs-lookup"><span data-stu-id="a7155-127">PRINTER\_CHANGE\_SET\_FORM</span></span></dd> <dd><span data-ttu-id="a7155-128">印表機 \_ 變更 \_ 刪除 \_ 表單</span><span class="sxs-lookup"><span data-stu-id="a7155-128">PRINTER\_CHANGE\_DELETE\_FORM</span></span></dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <span data-ttu-id="a7155-129"><dt>**印表機 \_ 變更 \_ 作業**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-129"><dt>**PRINTER\_CHANGE\_JOB**</dt></span></span> </dl>                                      | <span data-ttu-id="a7155-130">通知作業的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-130">Notify of any changes to a job.</span></span> <span data-ttu-id="a7155-131">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-131">You can set this general flag or one or more of the following specific flags:</span></span><br/> <dl> <dd><span data-ttu-id="a7155-132">印表機 \_ 變更 \_ 新增 \_ 作業</span><span class="sxs-lookup"><span data-stu-id="a7155-132">PRINTER\_CHANGE\_ADD\_JOB</span></span></dd> <dd><span data-ttu-id="a7155-133">印表機 \_ 變更 \_ 集 \_ 作業</span><span class="sxs-lookup"><span data-stu-id="a7155-133">PRINTER\_CHANGE\_SET\_JOB</span></span></dd> <dd><span data-ttu-id="a7155-134">印表機 \_ 變更 \_ 刪除 \_ 作業</span><span class="sxs-lookup"><span data-stu-id="a7155-134">PRINTER\_CHANGE\_DELETE\_JOB</span></span></dd> <dd><span data-ttu-id="a7155-135">印表機 \_ 變更 \_ 寫入 \_ 作業</span><span class="sxs-lookup"><span data-stu-id="a7155-135">PRINTER\_CHANGE\_WRITE\_JOB</span></span></dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <span data-ttu-id="a7155-136"><dt>**印表機 \_ 變更 \_ 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-136"><dt>**PRINTER\_CHANGE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="a7155-137">通知埠的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-137">Notify of any changes to a port.</span></span> <span data-ttu-id="a7155-138">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-138">You can set this general flag or one or more of the following specific flags:</span></span><br/> <dl> <dd><span data-ttu-id="a7155-139">印表機 \_ 變更 \_ 新增 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="a7155-139">PRINTER\_CHANGE\_ADD\_PORT</span></span></dd> <dd><span data-ttu-id="a7155-140">印表機 \_ 變更 \_ 設定 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="a7155-140">PRINTER\_CHANGE\_CONFIGURE\_PORT</span></span> </dd> <dd><span data-ttu-id="a7155-141">印表機 \_ 變更 \_ 刪除 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="a7155-141">PRINTER\_CHANGE\_DELETE\_PORT</span></span></dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <span data-ttu-id="a7155-142"><dt>**印表機 \_ 變更 \_ 列印 \_ 處理器**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-142"><dt>**PRINTER\_CHANGE\_PRINT\_PROCESSOR**</dt></span></span> </dl> | <span data-ttu-id="a7155-143">對列印處理器進行任何變更的通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-143">Notify of any changes to a print processor.</span></span> <span data-ttu-id="a7155-144">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-144">You can set this general flag or one or more of the following specific flags:</span></span> <br/> <dl> <dd><span data-ttu-id="a7155-145">印表機 \_ 變更 \_ 新增 \_ 列印 \_ 處理器</span><span class="sxs-lookup"><span data-stu-id="a7155-145">PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR</span></span> </dd> <dd><span data-ttu-id="a7155-146">印表機 \_ 變更 \_ 刪除 \_ 列印 \_ 處理器</span><span class="sxs-lookup"><span data-stu-id="a7155-146">PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR</span></span></dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <span data-ttu-id="a7155-147"><dt>**印表機 \_ 變更 \_ 印表機**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-147"><dt>**PRINTER\_CHANGE\_PRINTER**</dt></span></span> </dl>                          | <span data-ttu-id="a7155-148">通知印表機的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-148">Notify of any changes to a printer.</span></span> <span data-ttu-id="a7155-149">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-149">You can set this general flag or one or more of the following specific flags:</span></span><br/> <dl> <dd><span data-ttu-id="a7155-150">印表機 \_ 變更 \_ 新增 \_ 印表機</span><span class="sxs-lookup"><span data-stu-id="a7155-150">PRINTER\_CHANGE\_ADD\_PRINTER</span></span></dd> <dd><span data-ttu-id="a7155-151">印表機 \_ 變更 \_ 集 \_ 印表機</span><span class="sxs-lookup"><span data-stu-id="a7155-151">PRINTER\_CHANGE\_SET\_PRINTER</span></span></dd> <dd><span data-ttu-id="a7155-152">印表機 \_ 變更 \_ 刪除 \_ 印表機</span><span class="sxs-lookup"><span data-stu-id="a7155-152">PRINTER\_CHANGE\_DELETE\_PRINTER</span></span></dd> <dd><span data-ttu-id="a7155-153">印表機 \_ 變更 \_ \_ 連接 \_ 印表機失敗</span><span class="sxs-lookup"><span data-stu-id="a7155-153">PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER</span></span></dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <span data-ttu-id="a7155-154"><dt>**印表機 \_ 變更 \_ 印表機 \_ 驅動程式**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-154"><dt>**PRINTER\_CHANGE\_PRINTER\_DRIVER**</dt></span></span> </dl>    | <span data-ttu-id="a7155-155">通知印表機驅動程式的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-155">Notify of any changes to a printer driver.</span></span> <span data-ttu-id="a7155-156">您可以設定這個一般旗標或下列一或多個特定旗標：</span><span class="sxs-lookup"><span data-stu-id="a7155-156">You can set this general flag or one or more of the following specific flags:</span></span><br/> <dl> <dd><span data-ttu-id="a7155-157">印表機 \_ 變更 \_ 新增 \_ 印表機 \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="a7155-157">PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER</span></span></dd> <dd><span data-ttu-id="a7155-158">印表機 \_ 變更 \_ 集 \_ 印表機 \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="a7155-158">PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER</span></span></dd> <dd><span data-ttu-id="a7155-159">印表機 \_ 變更 \_ 刪除 \_ 印表機 \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="a7155-159">PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER</span></span></dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <span data-ttu-id="a7155-160"><dt>**印表機 \_ \_ 全部變更**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-160"><dt>**PRINTER\_CHANGE\_ALL**</dt></span></span> </dl>                                      | <span data-ttu-id="a7155-161">如果發生上述任何變更，請通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-161">Notify if any of the preceding changes occur.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="a7155-162"><dt>**印表機 \_ 變更 \_ 伺服器**</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                             | <span data-ttu-id="a7155-163">Windows 7：通知伺服器的任何變更。</span><span class="sxs-lookup"><span data-stu-id="a7155-163">Windows 7: Notify of any changes to the server.</span></span><br/> <span data-ttu-id="a7155-164">此旗標不包含在藉由設定 **印表機 \_ \_ 全部變更** 值所監視的變更中。</span><span class="sxs-lookup"><span data-stu-id="a7155-164">This flag is not included in the changes monitored by setting the **PRINTER\_CHANGE\_ALL** value.</span></span><br/>                                                                                                                                                                                                      |



 

<span data-ttu-id="a7155-165">如需上表中更明確旗標的說明，請參閱 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="a7155-165">For descriptions of the more specific flags in the preceding table, see the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a7155-166">*fdwOptions*</span><span class="sxs-lookup"><span data-stu-id="a7155-166">*fdwOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="a7155-167">此旗標會決定可用於通知的印表機分類。</span><span class="sxs-lookup"><span data-stu-id="a7155-167">The flag that determines the category of printers for which notifications will work.</span></span>



| <span data-ttu-id="a7155-168">值</span><span class="sxs-lookup"><span data-stu-id="a7155-168">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="a7155-169">意義</span><span class="sxs-lookup"><span data-stu-id="a7155-169">Meaning</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <span data-ttu-id="a7155-170"><dt>**印表機 \_通知 \_ 類別 \_ 所有**</dt> <dt>0x001000</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-170"><dt>**PRINTER\_NOTIFY\_CATEGORY\_ALL**</dt> <dt>0x001000</dt></span></span> </dl> | <span data-ttu-id="a7155-171">[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 會傳回2D 和3d 印表機的通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-171">[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) returns notifications for both 2D and 3D printers.</span></span><br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <span data-ttu-id="a7155-172"><dt>**印表機 \_通知 \_ 類別 \_ 3d**</dt> <dt>0x002000</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-172"><dt>**PRINTER\_NOTIFY\_CATEGORY\_3D**</dt> <dt>0x002000</dt></span></span> </dl>    | <span data-ttu-id="a7155-173">[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 只會傳回3d 印表機的通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-173">[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) returns notifications only for 3D printers.</span></span><br/>        |



 

<span data-ttu-id="a7155-174">當此旗標設定為零 (0) 時， **FindFirstPrinterChangeNotification** 將只適用于2d 印表機。</span><span class="sxs-lookup"><span data-stu-id="a7155-174">When this flag is set to zero (0), **FindFirstPrinterChangeNotification** will only work for 2D printers.</span></span> <span data-ttu-id="a7155-175">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="a7155-175">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="a7155-176">*pPrinterNotifyOptions* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a7155-176">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7155-177">[**印表機 \_ 通知 \_ 選項**](printer-notify-options.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a7155-177">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="a7155-178">此結構的 **pTypes** 成員是一或多個 [**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md) 結構的陣列，每個都指定要監視的印表機資訊欄位。</span><span class="sxs-lookup"><span data-stu-id="a7155-178">The **pTypes** member of this structure is an array of one or more [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures, each of which specifies a printer information field to monitor.</span></span> <span data-ttu-id="a7155-179">當一或多個指定的欄位變更時，就會發生變更通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-179">A change notification occurs when one or more of the specified fields changes.</span></span> <span data-ttu-id="a7155-180">發生變更時， [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式可以取得新的印表機資訊。</span><span class="sxs-lookup"><span data-stu-id="a7155-180">When a change occurs, the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function can retrieve the new printer information.</span></span> <span data-ttu-id="a7155-181">如果 *fdwFilter* 為非零值，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a7155-181">This parameter can be **NULL** if *fdwFilter* is nonzero.</span></span>

<span data-ttu-id="a7155-182">如需可監視的欄位清單，請參閱 [**印表機 \_ 通知 \_ 選項 \_ 類型**](printer-notify-options-type.md)。</span><span class="sxs-lookup"><span data-stu-id="a7155-182">For a list of fields that can be monitored, see [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7155-183">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7155-183">Return value</span></span>

<span data-ttu-id="a7155-184">如果函式成功，則傳回值是與指定的印表機或列印伺服器相關聯之變更通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7155-184">If the function succeeds, the return value is a handle to a change notification object associated with the specified printer or print server.</span></span>

<span data-ttu-id="a7155-185">如果函式失敗，則傳回值是不正確 \_ 控制碼 \_ 值。</span><span class="sxs-lookup"><span data-stu-id="a7155-185">If the function fails, the return value is INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7155-186">備註</span><span class="sxs-lookup"><span data-stu-id="a7155-186">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a7155-187">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a7155-187">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a7155-188">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a7155-188">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a7155-189">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a7155-189">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a7155-190">若要監視印表機或列印伺服器，請呼叫 **FindFirstPrinterChangeNotification** 函式，然後在呼叫其中一個 [等候](/windows/desktop/Sync/wait-functions)函式時，使用傳回的變更通知物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7155-190">To monitor a printer or print server, call the **FindFirstPrinterChangeNotification** function, then use the returned change notification object handle in a call to one of the [wait functions](/windows/desktop/Sync/wait-functions).</span></span> <span data-ttu-id="a7155-191">變更通知物件進入已發出信號的狀態時，會滿足變更通知物件的等候作業。</span><span class="sxs-lookup"><span data-stu-id="a7155-191">A wait operation on a change notification object is satisfied when the change notification object enters the signaled state.</span></span> <span data-ttu-id="a7155-192">當受監視的印表機或列印伺服器發生 *fdwFilter* 或 *pPrinterNotifyOptions* 所指定的一或多項變更時，系統會通知物件。</span><span class="sxs-lookup"><span data-stu-id="a7155-192">The system signals the object when one or more of the changes specified by *fdwFilter* or *pPrinterNotifyOptions* occurs in the monitored printer or print server.</span></span>

<span data-ttu-id="a7155-193">當您呼叫 **FindFirstPrinterChangeNotification** 時， *fdwFilter* 必須為非零值，否則 *pPrinterNotifyOptions* 必須是非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7155-193">When you call **FindFirstPrinterChangeNotification**, either *fdwFilter* must be nonzero or *pPrinterNotifyOptions* must be non-**NULL**.</span></span> <span data-ttu-id="a7155-194">如果同時指定這兩者，則會對兩者進行通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-194">If both are specified, notifications will occur for both.</span></span>

<span data-ttu-id="a7155-195">當滿足印表機變更通知物件的等候操作時，請呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函式來判斷通知的原因。</span><span class="sxs-lookup"><span data-stu-id="a7155-195">When a wait operation on a printer change notification object is satisfied, call the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to determine the cause of the notification.</span></span> <span data-ttu-id="a7155-196">針對 *fdwFilter* 所指定的條件， **FindNextPrinterChangeNotification** 會報告已變更的條件或條件。</span><span class="sxs-lookup"><span data-stu-id="a7155-196">For a condition specified by *fdwFilter*, **FindNextPrinterChangeNotification** reports the condition or conditions that changed.</span></span> <span data-ttu-id="a7155-197">針對 *pPrinterNotifyOptions* 所指定的印表機資訊欄位， **FindNextPrinterChangeNotification** 會報告已變更的欄位，以及這些欄位的新資訊。</span><span class="sxs-lookup"><span data-stu-id="a7155-197">For a printer information field specified by *pPrinterNotifyOptions*, **FindNextPrinterChangeNotification** reports the field or fields that changed as well as the new information for these fields.</span></span> <span data-ttu-id="a7155-198">**FindNextPrinterChangeNotification** 也會將變更通知物件重設為未收到信號狀態，因此您可以在另一個等候作業中使用它來繼續監視印表機或列印伺服器。</span><span class="sxs-lookup"><span data-stu-id="a7155-198">**FindNextPrinterChangeNotification** also resets the change notification object to the nonsignaled state so you can use it in another wait operation to continue monitoring the printer or print server.</span></span>

<span data-ttu-id="a7155-199">有一個例外狀況，如果變更通知物件不是處於已發出信號的狀態，請勿呼叫 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="a7155-199">With one exception, do not call the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="a7155-200">如果 wait 函式傳回值等候 \_ 超時，則變更物件不會處於已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7155-200">If the wait function returns the value WAIT\_TIMEOUT, the change object is not in the signaled state.</span></span> <span data-ttu-id="a7155-201">只有在等候函式成功時才呼叫 **FindNextPrinterChangeNotification** 函式，而不會超時。當使用 \_ \_ \_ *PPRINTERNOTIFYOPTIONS* 參數中所設定的印表機通知選項重新整理位來呼叫 FindNextPrinterChangeNotification 時，就會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a7155-201">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the PRINTER\_NOTIFY\_OPTIONS\_REFRESH bit set in the *pPrinterNotifyOptions* parameter.</span></span>

<span data-ttu-id="a7155-202">當您不再需要變更通知物件時，請呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) 函式將其關閉。</span><span class="sxs-lookup"><span data-stu-id="a7155-202">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

<span data-ttu-id="a7155-203">**FindFirstPrinterChangeNotification** 的呼叫端必須確保傳入 **FindFirstPrinterChangeNotification** 的印表機控制碼會維持有效，直到呼叫 [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)為止。</span><span class="sxs-lookup"><span data-stu-id="a7155-203">Callers of **FindFirstPrinterChangeNotification** must ensure that the printer handle passed into **FindFirstPrinterChangeNotification** remains valid until [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) is called.</span></span> <span data-ttu-id="a7155-204">如果印表機控制碼在印表機變更通知控制碼之前關閉，將無法傳遞進一步的通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-204">If the printer handle is closed before the printer change notification handle, further notifications will fail to be delivered.</span></span>

<span data-ttu-id="a7155-205">**FindFirstPrinterChangeNotification** 不會將3d 印表機的變更通知傳送到伺服器控制碼。</span><span class="sxs-lookup"><span data-stu-id="a7155-205">**FindFirstPrinterChangeNotification** will not send change notifications for 3D printers to server handles.</span></span>

> [!Note]  
> <span data-ttu-id="a7155-206">在 Windows XP Service Pack 2 (SP2) 和更新版本中，網際網路連線防火牆 (ICF) 預設會封鎖印表機埠，但是可以啟用檔案和列印共用的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a7155-206">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="a7155-207">如果使用者將印表機連線到另一部電腦，但未啟用例外狀況，則使用者將不會收到來自伺服器的印表機變更通知。</span><span class="sxs-lookup"><span data-stu-id="a7155-207">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="a7155-208">電腦系統管理員必須啟用例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a7155-208">A machine admin will have to enable exception.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7155-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7155-209">Requirements</span></span>



| <span data-ttu-id="a7155-210">需求</span><span class="sxs-lookup"><span data-stu-id="a7155-210">Requirement</span></span> | <span data-ttu-id="a7155-211">值</span><span class="sxs-lookup"><span data-stu-id="a7155-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7155-212">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7155-212">Minimum supported client</span></span><br/> | <span data-ttu-id="a7155-213">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7155-213">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7155-214">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7155-214">Minimum supported server</span></span><br/> | <span data-ttu-id="a7155-215">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7155-215">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7155-216">標頭</span><span class="sxs-lookup"><span data-stu-id="a7155-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7155-217"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a7155-217"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a7155-218">程式庫</span><span class="sxs-lookup"><span data-stu-id="a7155-218">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7155-219"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-219"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a7155-220">DLL</span><span class="sxs-lookup"><span data-stu-id="a7155-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7155-221"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7155-221"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a7155-222">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7155-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7155-223">列印</span><span class="sxs-lookup"><span data-stu-id="a7155-223">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a7155-224">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a7155-224">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a7155-225">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="a7155-225">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="a7155-226">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="a7155-226">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="a7155-227">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a7155-227">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a7155-228">**印表機 \_ 通知 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="a7155-228">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> <dt>

[<span data-ttu-id="a7155-229">**印表機 \_ 通知 \_ 選項 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="a7155-229">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

