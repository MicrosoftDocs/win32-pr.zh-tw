---
description: Session 物件的 Message 方法會執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。 您可以選擇性地為各種訊息類型啟用記錄。 請參閱 EnableLog 方法。
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995077"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="d86af-105">Session 方法</span><span class="sxs-lookup"><span data-stu-id="d86af-105">Session.Message method</span></span>

<span data-ttu-id="d86af-106">[**Session**](session-object.md)物件的 **Message** 方法會執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="d86af-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="d86af-107">您可以選擇性地為各種訊息類型啟用記錄。</span><span class="sxs-lookup"><span data-stu-id="d86af-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="d86af-108">請參閱 [**EnableLog**](installer-enablelog.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d86af-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="d86af-109">如果記錄欄位0包含格式化字串，則會使用它來格式化其他欄位中的資料。</span><span class="sxs-lookup"><span data-stu-id="d86af-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="d86af-110">否則，如果訊息是錯誤、警告或使用者訊息，則會嘗試使用訊息類型和傳回值記錄之欄位1中找到的錯誤號碼，在目前資料庫的錯誤資料表中尋找訊息範本。</span><span class="sxs-lookup"><span data-stu-id="d86af-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86af-111">語法</span><span class="sxs-lookup"><span data-stu-id="d86af-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="d86af-112">參數</span><span class="sxs-lookup"><span data-stu-id="d86af-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86af-113">*類別*</span><span class="sxs-lookup"><span data-stu-id="d86af-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="d86af-114">*Kind* 參數必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="d86af-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="d86af-115">若要顯示含有推播按鈕和圖示的訊息方塊，請將 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)和 [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa)所使用的標準訊息方塊樣式新增至 **msiMessageTypeError**、 **msiMessageTypeWarning** 或 **msiMessageTypeUser**，以計算 *類型* 的值。</span><span class="sxs-lookup"><span data-stu-id="d86af-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="d86af-116">如需詳細資訊，請參閱下面的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d86af-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="d86af-117">常數</span><span class="sxs-lookup"><span data-stu-id="d86af-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="d86af-118">意義</span><span class="sxs-lookup"><span data-stu-id="d86af-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="d86af-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="d86af-120">提前終止，可能是記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d86af-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="d86af-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="d86af-122">格式化的錯誤訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="d86af-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="d86af-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="d86af-124">格式化的警告訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="d86af-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="d86af-125"><dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="d86af-126">使用者要求訊息， \[ 1 \] 是 [錯誤資料表](error-table.md)中的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="d86af-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="d86af-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="d86af-128">記錄檔的資訊性訊息，不會顯示。</span><span class="sxs-lookup"><span data-stu-id="d86af-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="d86af-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="d86af-130">使用中需要取代的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="d86af-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="d86af-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="d86af-132">要求判斷有效的來源位置。</span><span class="sxs-lookup"><span data-stu-id="d86af-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="d86af-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="d86af-134">磁碟空間不足的訊息。</span><span class="sxs-lookup"><span data-stu-id="d86af-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="d86af-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="d86af-136">動作的開頭， \[ 1 個 \] 動作名稱、 \[ 2 個 \] 描述、 \[ 3 \] 個 ACTIONDATA 訊息的範本。</span><span class="sxs-lookup"><span data-stu-id="d86af-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="d86af-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="d86af-138">動作資料。</span><span class="sxs-lookup"><span data-stu-id="d86af-138">Action data.</span></span> <span data-ttu-id="d86af-139">記錄欄位會對應至 ACTIONSTART 訊息的範本。</span><span class="sxs-lookup"><span data-stu-id="d86af-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="d86af-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="d86af-141">進度列資訊。</span><span class="sxs-lookup"><span data-stu-id="d86af-141">Progress bar information.</span></span> <span data-ttu-id="d86af-142">請參閱下方的記錄欄位描述。</span><span class="sxs-lookup"><span data-stu-id="d86af-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="d86af-143"><dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="d86af-144">若要啟用 [取消] 按鈕，請將 \[ 1 設定 \] 為2，並將 \[ 2 設定 \] 為1。</span><span class="sxs-lookup"><span data-stu-id="d86af-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="d86af-145">若要停用 [取消] 按鈕，請將 \[ 1 設定 \] 為2， \[ 2 \] 為0</span><span class="sxs-lookup"><span data-stu-id="d86af-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d86af-146">*記錄*</span><span class="sxs-lookup"><span data-stu-id="d86af-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="d86af-147">包含訊息特定欄位的必要 [**記錄**](record-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d86af-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86af-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="d86af-148">Return value</span></span>



| <span data-ttu-id="d86af-149">常數</span><span class="sxs-lookup"><span data-stu-id="d86af-149">Constant</span></span>                                                                                              | <span data-ttu-id="d86af-150">值</span><span class="sxs-lookup"><span data-stu-id="d86af-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="d86af-151"><dt>**msiMessageStatusError**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="d86af-152">-1</span><span class="sxs-lookup"><span data-stu-id="d86af-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="d86af-153"><dt>**msiMessageStatusNone**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="d86af-154">0</span><span class="sxs-lookup"><span data-stu-id="d86af-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-155"><dt>**msiMessageStatusOk**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="d86af-156">1</span><span class="sxs-lookup"><span data-stu-id="d86af-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-157"><dt>**msiMessageStatusCancel**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="d86af-158">2</span><span class="sxs-lookup"><span data-stu-id="d86af-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-159"><dt>**msiMessageStatusAbort**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="d86af-160">3</span><span class="sxs-lookup"><span data-stu-id="d86af-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-161"><dt>**msiMessageStatusRetry**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="d86af-162">4</span><span class="sxs-lookup"><span data-stu-id="d86af-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-163"><dt>**msiMessageStatusIgnore**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="d86af-164">5</span><span class="sxs-lookup"><span data-stu-id="d86af-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-165"><dt>**msiMessageStatusYes**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="d86af-166">6</span><span class="sxs-lookup"><span data-stu-id="d86af-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="d86af-167"><dt>**msiMessageStatusNo**</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="d86af-168">7</span><span class="sxs-lookup"><span data-stu-id="d86af-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d86af-169">備註</span><span class="sxs-lookup"><span data-stu-id="d86af-169">Remarks</span></span>

<span data-ttu-id="d86af-170">**訊息記錄欄位**</span><span class="sxs-lookup"><span data-stu-id="d86af-170">**Message Record Fields**</span></span>

<span data-ttu-id="d86af-171">以下描述當 msiMessageTypeProgress 傳遞為訊息類型時的記錄欄位定義。</span><span class="sxs-lookup"><span data-stu-id="d86af-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="d86af-172">欄位1指定進度訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="d86af-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="d86af-173">其他欄位的意義會根據此欄位中的值而定。</span><span class="sxs-lookup"><span data-stu-id="d86af-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="d86af-174">可以設定為欄位1的可能值如下所示。</span><span class="sxs-lookup"><span data-stu-id="d86af-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="d86af-175">訊息名稱</span><span class="sxs-lookup"><span data-stu-id="d86af-175">Message name</span></span>     | <span data-ttu-id="d86af-176">值</span><span class="sxs-lookup"><span data-stu-id="d86af-176">Value</span></span> | <span data-ttu-id="d86af-177">欄位1描述</span><span class="sxs-lookup"><span data-stu-id="d86af-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86af-178">MasterReset</span><span class="sxs-lookup"><span data-stu-id="d86af-178">MasterReset</span></span>      | <span data-ttu-id="d86af-179">0</span><span class="sxs-lookup"><span data-stu-id="d86af-179">0</span></span>     | <span data-ttu-id="d86af-180">重設進度列，並在橫條圖中設定預期的總刻度數。</span><span class="sxs-lookup"><span data-stu-id="d86af-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="d86af-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="d86af-181">ActionInfo</span></span>       | <span data-ttu-id="d86af-182">1</span><span class="sxs-lookup"><span data-stu-id="d86af-182">1</span></span>     | <span data-ttu-id="d86af-183">提供目前動作要傳送的進度訊息相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d86af-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="d86af-184">ProgressReport</span><span class="sxs-lookup"><span data-stu-id="d86af-184">ProgressReport</span></span>   | <span data-ttu-id="d86af-185">2</span><span class="sxs-lookup"><span data-stu-id="d86af-185">2</span></span>     | <span data-ttu-id="d86af-186">遞增進度列。</span><span class="sxs-lookup"><span data-stu-id="d86af-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="d86af-187">ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="d86af-187">ProgressAddition</span></span> | <span data-ttu-id="d86af-188">3</span><span class="sxs-lookup"><span data-stu-id="d86af-188">3</span></span>     | <span data-ttu-id="d86af-189">啟用動作 (例如 CustomAction) ，將刻度加入進度列的預期進度總數。</span><span class="sxs-lookup"><span data-stu-id="d86af-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="d86af-190">欄位2的意義取決於 [欄位 1] 中的值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d86af-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d86af-191">欄位1值</span><span class="sxs-lookup"><span data-stu-id="d86af-191">Field 1 value</span></span> | <span data-ttu-id="d86af-192">欄位2描述</span><span class="sxs-lookup"><span data-stu-id="d86af-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86af-193">0</span><span class="sxs-lookup"><span data-stu-id="d86af-193">0</span></span>             | <span data-ttu-id="d86af-194">進度列中預期的總刻度數。</span><span class="sxs-lookup"><span data-stu-id="d86af-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="d86af-195">1</span><span class="sxs-lookup"><span data-stu-id="d86af-195">1</span></span>             | <span data-ttu-id="d86af-196">進度列針對每個 ActionData 訊息移動的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="d86af-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="d86af-197">如果欄位3為0，則會忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="d86af-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="d86af-198">2</span><span class="sxs-lookup"><span data-stu-id="d86af-198">2</span></span>             | <span data-ttu-id="d86af-199">進度列移動的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="d86af-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="d86af-200">3</span><span class="sxs-lookup"><span data-stu-id="d86af-200">3</span></span>             | <span data-ttu-id="d86af-201">要加入至總預期進度的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="d86af-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="d86af-202">欄位3的意義取決於 [欄位 1] 中的值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d86af-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d86af-203">欄位1值</span><span class="sxs-lookup"><span data-stu-id="d86af-203">Field 1 value</span></span> | <span data-ttu-id="d86af-204">欄位3值</span><span class="sxs-lookup"><span data-stu-id="d86af-204">Field 3 value</span></span> | <span data-ttu-id="d86af-205">欄位3描述</span><span class="sxs-lookup"><span data-stu-id="d86af-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86af-206">0</span><span class="sxs-lookup"><span data-stu-id="d86af-206">0</span></span>             | <span data-ttu-id="d86af-207">0</span><span class="sxs-lookup"><span data-stu-id="d86af-207">0</span></span>             | <span data-ttu-id="d86af-208">轉寄進度列 (從左至右) </span><span class="sxs-lookup"><span data-stu-id="d86af-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="d86af-209">1</span><span class="sxs-lookup"><span data-stu-id="d86af-209">1</span></span>             | <span data-ttu-id="d86af-210">回溯進度列 (向左) </span><span class="sxs-lookup"><span data-stu-id="d86af-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="d86af-211">1</span><span class="sxs-lookup"><span data-stu-id="d86af-211">1</span></span>             | <span data-ttu-id="d86af-212">0</span><span class="sxs-lookup"><span data-stu-id="d86af-212">0</span></span>             | <span data-ttu-id="d86af-213">目前的動作將會傳送明確的 ProgressReport 訊息。</span><span class="sxs-lookup"><span data-stu-id="d86af-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="d86af-214">1</span><span class="sxs-lookup"><span data-stu-id="d86af-214">1</span></span>             | <span data-ttu-id="d86af-215">每次傳送 ActionData 訊息時，依欄位2中指定的刻度數目遞增進度列。</span><span class="sxs-lookup"><span data-stu-id="d86af-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="d86af-216">2</span><span class="sxs-lookup"><span data-stu-id="d86af-216">2</span></span>             | <span data-ttu-id="d86af-217">未使用</span><span class="sxs-lookup"><span data-stu-id="d86af-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="d86af-218">3</span><span class="sxs-lookup"><span data-stu-id="d86af-218">3</span></span>             | <span data-ttu-id="d86af-219">未使用</span><span class="sxs-lookup"><span data-stu-id="d86af-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="d86af-220">欄位4的意義取決於 [欄位 1] 中的值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d86af-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d86af-221">欄位1值</span><span class="sxs-lookup"><span data-stu-id="d86af-221">Field 1 value</span></span> | <span data-ttu-id="d86af-222">欄位4值</span><span class="sxs-lookup"><span data-stu-id="d86af-222">Field 4 value</span></span> | <span data-ttu-id="d86af-223">欄位4描述</span><span class="sxs-lookup"><span data-stu-id="d86af-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86af-224">0</span><span class="sxs-lookup"><span data-stu-id="d86af-224">0</span></span>             | <span data-ttu-id="d86af-225">0</span><span class="sxs-lookup"><span data-stu-id="d86af-225">0</span></span>             | <span data-ttu-id="d86af-226">執行正在進行中。</span><span class="sxs-lookup"><span data-stu-id="d86af-226">Execution is in progress.</span></span> <span data-ttu-id="d86af-227">在此情況下，UI 可以計算並顯示剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="d86af-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="d86af-228">1</span><span class="sxs-lookup"><span data-stu-id="d86af-228">1</span></span>             | <span data-ttu-id="d86af-229">建立執行腳本。</span><span class="sxs-lookup"><span data-stu-id="d86af-229">Creating the execution script.</span></span> <span data-ttu-id="d86af-230">在此情況下，UI 可能會顯示一則訊息，等候安裝程式完成準備安裝時請稍候。</span><span class="sxs-lookup"><span data-stu-id="d86af-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="d86af-231">1</span><span class="sxs-lookup"><span data-stu-id="d86af-231">1</span></span>             | <span data-ttu-id="d86af-232">未使用</span><span class="sxs-lookup"><span data-stu-id="d86af-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="d86af-233">2</span><span class="sxs-lookup"><span data-stu-id="d86af-233">2</span></span>             | <span data-ttu-id="d86af-234">未使用</span><span class="sxs-lookup"><span data-stu-id="d86af-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="d86af-235">3</span><span class="sxs-lookup"><span data-stu-id="d86af-235">3</span></span>             | <span data-ttu-id="d86af-236">未使用</span><span class="sxs-lookup"><span data-stu-id="d86af-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="d86af-237">**顯示訊息方塊**</span><span class="sxs-lookup"><span data-stu-id="d86af-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="d86af-238">若要顯示含有推播按鈕和圖示的訊息方塊，請將 **MessageBox** 和 **MessageBoxEx** 所使用的標準訊息方塊樣式新增至 **msiMessageTypeError**、 **msiMessageTypeWarning** 或 **msiTypeUser**，以計算 *類型* 的值。</span><span class="sxs-lookup"><span data-stu-id="d86af-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="d86af-239">VBScript 的可用推播按鈕選項有 vbOKOnly (MB \_ OK) 、vbOKCancel (MB \_ OKCANCEL) 、VBABORTRETRYIGNORE (MB \_ ABORTRETRYIGNORE) 、vbYesNoCancel (MB \_ YESNOCANCEL) 、vbYesNo (Mb \_ YESNO) 和 vbRetryCancel (mb \_ RETRYCANCEL) 。</span><span class="sxs-lookup"><span data-stu-id="d86af-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="d86af-240">VBScript 的可用圖示選項有 vbCritical (MB \_ ICONERROR) 、vbQuestion (MB \_ ICONQUESTION) 、VBEXCLAMATION (mb \_ ICONWARNING) 和 vbInformation (mb \_ ICONINFORMATION) 。</span><span class="sxs-lookup"><span data-stu-id="d86af-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="d86af-241">例如，下列呼叫會傳送具有 vbExclamation 圖示和 vbYesNo 按鈕的 **msiMessageTypeError** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d86af-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="d86af-242">如果自訂動作呼叫 **訊息** 方法，自訂動作應該能夠處理使用者的取消作業，而且應該會傳回 **msiDoActionStatusUserExit**。</span><span class="sxs-lookup"><span data-stu-id="d86af-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d86af-243">規格需求</span><span class="sxs-lookup"><span data-stu-id="d86af-243">Requirements</span></span>



| <span data-ttu-id="d86af-244">需求</span><span class="sxs-lookup"><span data-stu-id="d86af-244">Requirement</span></span> | <span data-ttu-id="d86af-245">值</span><span class="sxs-lookup"><span data-stu-id="d86af-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86af-246">版本</span><span class="sxs-lookup"><span data-stu-id="d86af-246">Version</span></span><br/> | <span data-ttu-id="d86af-247">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d86af-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d86af-248">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d86af-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d86af-249">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d86af-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d86af-250">DLL</span><span class="sxs-lookup"><span data-stu-id="d86af-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="d86af-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d86af-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d86af-252">IID</span><span class="sxs-lookup"><span data-stu-id="d86af-252">IID</span></span><br/>     | <span data-ttu-id="d86af-253">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d86af-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
