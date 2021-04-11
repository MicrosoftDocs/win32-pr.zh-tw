---
description: AdvancedDocumentProperties 函式會顯示指定印表機的 [印表機設定] 對話方塊，讓使用者可以設定該印表機。
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: 'AdvancedDocumentProperties 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695015"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="a39df-103">AdvancedDocumentProperties 函式</span><span class="sxs-lookup"><span data-stu-id="a39df-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="a39df-104">**AdvancedDocumentProperties** 函式會顯示指定印表機的 [印表機設定] 對話方塊，讓使用者可以設定該印表機。</span><span class="sxs-lookup"><span data-stu-id="a39df-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="a39df-105">此函數是 [**DocumentProperties**](documentproperties.md) 函數的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="a39df-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="a39df-106">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="a39df-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="a39df-107">語法</span><span class="sxs-lookup"><span data-stu-id="a39df-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="a39df-108">參數</span><span class="sxs-lookup"><span data-stu-id="a39df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a39df-109">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a39df-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a39df-110">印表機設定對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="a39df-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="a39df-111">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a39df-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a39df-112">印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a39df-112">A handle to a printer object.</span></span> <span data-ttu-id="a39df-113">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="a39df-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="a39df-114">*pDeviceName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a39df-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a39df-115">以 null 結束的字串指標，指定應顯示印表機設定對話方塊的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="a39df-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a39df-116">*pDevModeOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a39df-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a39df-117">[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，此結構會包含使用者所指定的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a39df-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="a39df-118">*pDevModeInput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a39df-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a39df-119">[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，其中包含用來初始化 [印表機設定] 對話方塊之控制項的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a39df-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a39df-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a39df-120">Return value</span></span>

<span data-ttu-id="a39df-121">如果具有這些參數的 [**DocumentProperties**](documentproperties.md) 函數成功，則 **AdvancedDocumentProperties** 的傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="a39df-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="a39df-122">否則，傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a39df-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a39df-123">備註</span><span class="sxs-lookup"><span data-stu-id="a39df-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a39df-124">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a39df-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a39df-125">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a39df-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a39df-126">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a39df-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a39df-127">此功能只會顯示 [印表機設定] 對話方塊，讓使用者可以進行設定。</span><span class="sxs-lookup"><span data-stu-id="a39df-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="a39df-128">如需更多控制，請使用 [**DocumentProperties**](documentproperties.md)。</span><span class="sxs-lookup"><span data-stu-id="a39df-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="a39df-129">此函式的輸入參數會直接傳遞至 **DocumentProperties** ，而 *fMode* 值會在 \_ \_ \| \_ \_ 提示 \| dm \_ 輸出 \_ 緩衝區的緩衝區 DM 中設定為 DM。</span><span class="sxs-lookup"><span data-stu-id="a39df-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="a39df-130">與 **DocumentProperties** 不同，此函數只會傳回1或0。</span><span class="sxs-lookup"><span data-stu-id="a39df-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="a39df-131">因此，您無法藉由將 *pDevMode* 設定為零，判斷所需的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小。</span><span class="sxs-lookup"><span data-stu-id="a39df-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="a39df-132">應用程式可以透過呼叫 [**GetPrinter**](getprinter.md)函式，然後檢查 [**印表機 \_ INFO \_ 2**](printer-info-2.md)結構的 **pPrinterName** 成員，來取得 *pDeviceName* 參數所指向的名稱。</span><span class="sxs-lookup"><span data-stu-id="a39df-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a39df-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a39df-133">Requirements</span></span>



| <span data-ttu-id="a39df-134">需求</span><span class="sxs-lookup"><span data-stu-id="a39df-134">Requirement</span></span> | <span data-ttu-id="a39df-135">值</span><span class="sxs-lookup"><span data-stu-id="a39df-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39df-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a39df-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a39df-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a39df-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a39df-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a39df-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a39df-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a39df-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a39df-140">標頭</span><span class="sxs-lookup"><span data-stu-id="a39df-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a39df-141"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a39df-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a39df-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="a39df-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="a39df-143"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a39df-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a39df-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a39df-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a39df-145"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a39df-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a39df-146">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a39df-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a39df-147">**AdvancedDocumentPropertiesW** (Unicode) 和 **AdvancedDocumentPropertiesA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a39df-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a39df-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a39df-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39df-149">列印</span><span class="sxs-lookup"><span data-stu-id="a39df-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a39df-150">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a39df-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a39df-151">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="a39df-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="a39df-152">**版**</span><span class="sxs-lookup"><span data-stu-id="a39df-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="a39df-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="a39df-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="a39df-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="a39df-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="a39df-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a39df-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a39df-156">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a39df-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




