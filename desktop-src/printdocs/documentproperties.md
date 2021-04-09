---
description: DocumentProperties 函式會抓取或修改印表機初始化資訊，或顯示指定印表機的印表機設定屬性工作表。
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: 'DocumentProperties 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115793"
---
# <a name="documentproperties-function"></a><span data-ttu-id="07cc7-103">DocumentProperties 函式</span><span class="sxs-lookup"><span data-stu-id="07cc7-103">DocumentProperties function</span></span>

<span data-ttu-id="07cc7-104">**DocumentProperties** 函式會抓取或修改印表機初始化資訊，或顯示指定印表機的印表機設定屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="07cc7-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cc7-105">語法</span><span class="sxs-lookup"><span data-stu-id="07cc7-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="07cc7-106">參數</span><span class="sxs-lookup"><span data-stu-id="07cc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07cc7-107">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-108">印表機設定屬性工作表的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="07cc7-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="07cc7-109">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-110">印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="07cc7-110">A handle to a printer object.</span></span> <span data-ttu-id="07cc7-111">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="07cc7-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="07cc7-112">*pDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-113">以 null 結束的字串指標，指定顯示印表機設定屬性工作表之裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="07cc7-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="07cc7-114">*pDevModeOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-115">[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，此結構會接收使用者指定的印表機設定資料。</span><span class="sxs-lookup"><span data-stu-id="07cc7-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="07cc7-116">*pDevModeInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-117">由作業系統用來初始化屬性工作表控制項的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="07cc7-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="07cc7-118">只有在 *fMode* 參數中設定了 [ **DM \_ in \_ BUFFER** ] 旗標時，才會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="07cc7-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="07cc7-119">如果未設定 [ **\_ 在 \_ 緩衝區中的 DM** ]，則作業系統會使用印表機的預設 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)。</span><span class="sxs-lookup"><span data-stu-id="07cc7-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="07cc7-120">*fMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07cc7-121">函數所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="07cc7-121">The operations the function performs.</span></span> <span data-ttu-id="07cc7-122">如果此參數為零，則 **DocumentProperties** 函數會傳回印表機驅動程式的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 資料結構所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="07cc7-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="07cc7-123">否則，請使用下列一或多個常數來建立這個參數的值。不過請注意，為了變更列印設定，應用程式必須指定至少一個輸入值和一個輸出值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="07cc7-124">值</span><span class="sxs-lookup"><span data-stu-id="07cc7-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="07cc7-125">意義</span><span class="sxs-lookup"><span data-stu-id="07cc7-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="07cc7-126"><dt>**\_緩衝區中的 DM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="07cc7-127">輸入值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-127">Input value.</span></span> <span data-ttu-id="07cc7-128">在提示、複製或更新之前，函式會將印表機驅動程式的目前列印設定與 *pDevModeInput* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構中的設定合併。</span><span class="sxs-lookup"><span data-stu-id="07cc7-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="07cc7-129">函數只會針對由 **DEVMODE** 結構的 **dmFields** 成員所指定的成員，更新結構。</span><span class="sxs-lookup"><span data-stu-id="07cc7-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="07cc7-130">此值也會定義為 **DM \_ MODIFY**。</span><span class="sxs-lookup"><span data-stu-id="07cc7-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="07cc7-131">在合併期間發生衝突的情況下， *pDevModeInput* 所指定的 **DEVMODE** 結構中的設定會覆寫印表機驅動程式目前的列印設定。</span><span class="sxs-lookup"><span data-stu-id="07cc7-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="07cc7-132"><dt>**DM \_ IN \_ PROMPT**</dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="07cc7-133">輸入值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-133">Input value.</span></span> <span data-ttu-id="07cc7-134">此函式會顯示印表機驅動程式的列印設置屬性工作表，然後將印表機的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 資料結構中的設定變更為使用者指定的值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="07cc7-135">此值也會定義為 **DM \_ 提示**。</span><span class="sxs-lookup"><span data-stu-id="07cc7-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="07cc7-136"><dt>**DM \_ OUT \_ 緩衝區**</dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="07cc7-137">輸出值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-137">Output value.</span></span> <span data-ttu-id="07cc7-138">函數會將印表機驅動程式的目前列印設定（包括私用資料）寫入 *pDevModeOutput* 參數所指定的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)資料結構中。</span><span class="sxs-lookup"><span data-stu-id="07cc7-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="07cc7-139">呼叫端必須配置夠大的緩衝區以包含資訊。</span><span class="sxs-lookup"><span data-stu-id="07cc7-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="07cc7-140">如果位 **DM 的 \_ 輸出 \_ 緩衝區** 集很清楚， *pDevModeOutput* 參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="07cc7-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="07cc7-141">此值也會定義為 **DM \_ 複製**。</span><span class="sxs-lookup"><span data-stu-id="07cc7-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07cc7-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="07cc7-142">Return value</span></span>

<span data-ttu-id="07cc7-143">如果 *fMode* 參數為零，則傳回值是包含印表機驅動程式初始化資料所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="07cc7-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="07cc7-144">請注意，如果印表機驅動程式將私用資料附加至結構，此緩衝區可能會大於 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。</span><span class="sxs-lookup"><span data-stu-id="07cc7-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="07cc7-145">如果函數顯示內容表，則傳回值會是 **IDOK** 或 **IDCANCEL**，視使用者選取的按鈕而定。</span><span class="sxs-lookup"><span data-stu-id="07cc7-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="07cc7-146">如果函式未顯示內容表且成功，則傳回值為 **IDOK**。</span><span class="sxs-lookup"><span data-stu-id="07cc7-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="07cc7-147">如果函式失敗，則傳回值小於零。</span><span class="sxs-lookup"><span data-stu-id="07cc7-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07cc7-148">備註</span><span class="sxs-lookup"><span data-stu-id="07cc7-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07cc7-149">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="07cc7-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="07cc7-150">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="07cc7-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="07cc7-151">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="07cc7-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="07cc7-152">*PDeviceName* 參數所指向的字串可以藉由呼叫 [**GetPrinter**](getprinter.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="07cc7-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="07cc7-153">印表機驅動程式實際使用的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構包含與裝置無關的部分 (如上面所定義) 接著會有每個驅動程式和驅動程式版本的大小和內容各異的驅動程式特定元件。</span><span class="sxs-lookup"><span data-stu-id="07cc7-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="07cc7-154">因為此驅動程式相依性，所以在為它配置緩衝區之前，應用程式必須查詢驅動程式的正確大小，才是很重要的。</span><span class="sxs-lookup"><span data-stu-id="07cc7-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="07cc7-155">**若要對應用程式的本機列印設定進行變更，應用程式應該遵循下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="07cc7-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="07cc7-156">藉由呼叫 **DocumentProperties** ，並在 *fMode* 參數中指定零，取得完整 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="07cc7-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="07cc7-157">為完整的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="07cc7-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="07cc7-158">藉由呼叫 **DocumentProperties** 來取得目前的印表機設定。</span><span class="sxs-lookup"><span data-stu-id="07cc7-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="07cc7-159">將步驟2中配置的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構指標傳遞為 *pDevModeOutput* 參數，並指定 **DM \_ OUT \_ 緩衝區** 值。</span><span class="sxs-lookup"><span data-stu-id="07cc7-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="07cc7-160">修改所傳回之 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的適當成員，並藉由在 **DEVMODE** 的 **dmFields** 成員中設定對應的位，來指出哪些成員已變更。</span><span class="sxs-lookup"><span data-stu-id="07cc7-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="07cc7-161">呼叫 **DocumentProperties** ，並將修改過的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構傳回做 *為 pDevModeInput* 和 *pDevModeOutput* 參數，並同時指定在緩衝區和 **dm \_ 輸出 \_ 緩衝區** 值 **\_ 中 \_ 的 dm** ， (使用 OR 運算子) 來合併。第三次呼叫 **DocumentProperties** 所傳回的 **DEVMODE** 結構，可以當做 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)函式呼叫中的引數使用。</span><span class="sxs-lookup"><span data-stu-id="07cc7-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="07cc7-162">若要使用目前的印表機設定來建立印表機裝置內容的控制碼，您只需要呼叫 **DocumentProperties** 兩次，如上所述。</span><span class="sxs-lookup"><span data-stu-id="07cc7-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="07cc7-163">第一個呼叫會取得完整 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 的大小，而第二個呼叫則會使用目前的印表機設定來初始化 **DEVMODE** 。</span><span class="sxs-lookup"><span data-stu-id="07cc7-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="07cc7-164">將初始化的 **DEVMODE** 傳遞給 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ，以取得印表機裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="07cc7-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cc7-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="07cc7-165">Requirements</span></span>



| <span data-ttu-id="07cc7-166">需求</span><span class="sxs-lookup"><span data-stu-id="07cc7-166">Requirement</span></span> | <span data-ttu-id="07cc7-167">值</span><span class="sxs-lookup"><span data-stu-id="07cc7-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07cc7-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07cc7-168">Minimum supported client</span></span><br/> | <span data-ttu-id="07cc7-169">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="07cc7-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07cc7-170">Minimum supported server</span></span><br/> | <span data-ttu-id="07cc7-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07cc7-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="07cc7-172">標頭</span><span class="sxs-lookup"><span data-stu-id="07cc7-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="07cc7-173"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="07cc7-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="07cc7-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="07cc7-175"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="07cc7-176">DLL</span><span class="sxs-lookup"><span data-stu-id="07cc7-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07cc7-177"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="07cc7-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="07cc7-178">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="07cc7-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="07cc7-179">**DocumentPropertiesW** (Unicode) 和 **DocumentPropertiesA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="07cc7-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="07cc7-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07cc7-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cc7-181">列印</span><span class="sxs-lookup"><span data-stu-id="07cc7-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="07cc7-182">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="07cc7-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="07cc7-183">**AdvancedDocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="07cc7-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="07cc7-184">**CreateDC**</span><span class="sxs-lookup"><span data-stu-id="07cc7-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="07cc7-185">**版**</span><span class="sxs-lookup"><span data-stu-id="07cc7-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="07cc7-186">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="07cc7-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="07cc7-187">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="07cc7-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

