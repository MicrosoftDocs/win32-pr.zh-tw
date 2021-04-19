---
description: 將連接新增至目前使用者的指定印表機，並指定連接詳細資料。
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: 'AddPrinterConnection2 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998495"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="205cc-103">AddPrinterConnection2 函式</span><span class="sxs-lookup"><span data-stu-id="205cc-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="205cc-104">將連接新增至目前使用者的指定印表機，並指定連接詳細資料。</span><span class="sxs-lookup"><span data-stu-id="205cc-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="205cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="205cc-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="205cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="205cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205cc-107">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205cc-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205cc-108">父視窗的控制碼，如果列印系統必須從列印伺服器下載此連接的印表機驅動程式，則會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="205cc-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="205cc-109">*pszName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205cc-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205cc-110">常數以 null 終止的字串指標，指定目前使用者希望連接的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="205cc-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="205cc-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="205cc-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="205cc-112">*PConnectionInfo* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="205cc-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="205cc-113">目前只會定義層級1，因此 *dwLevel* 的值必須是1。</span><span class="sxs-lookup"><span data-stu-id="205cc-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="205cc-114">*pConnectionInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205cc-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205cc-115">[**印表機 \_ 連接 \_ 資訊 \_ 1**](printer-connection-info-1.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="205cc-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="205cc-116">如需此參數的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="205cc-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205cc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="205cc-117">Return value</span></span>

<span data-ttu-id="205cc-118">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="205cc-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="205cc-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="205cc-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="205cc-120">如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="205cc-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="205cc-121">備註</span><span class="sxs-lookup"><span data-stu-id="205cc-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="205cc-122">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="205cc-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="205cc-123">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="205cc-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="205cc-124">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="205cc-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="205cc-125">當 Windows Vista 連接至印表機時，可能需要從印表機所連接的伺服器複製印表機驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="205cc-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="205cc-126">如果使用者沒有許可權可將檔案複製到適當的位置， **AddPrinterConnection2** 函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="205cc-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="205cc-127">如果印表機驅動程式檔案必須從列印伺服器複製，但因為有作用中的群組原則，而且無法以無訊息方式複製， \_ \_ \_ *pConnectionInfo->dwFlags* 中不會設定任何對話方塊，而且呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="205cc-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="205cc-128">如果本機印表機驅動程式可用來轉譯此印表機的列印工作，而且本機驅動程式的版本必須與伺服器上的印表機驅動程式版本不相符，請 \_ \_ 在 *PConnectionInfo->DWFLAGS* 中設定印表機連線不相符，然後將指標指派給包含本機印表機驅動程式路徑的字串變數，以 *pConnectionInfo >pszDriverName*。</span><span class="sxs-lookup"><span data-stu-id="205cc-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="205cc-129">呼叫 **AddPrinterConnection2** 時所建立的印表機連線將會在呼叫 [**>enumprinters**](enumprinters.md) 時列舉，並將 *dwType* 設定為印表機 \_ 列舉 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="205cc-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="205cc-130">此函式 **AddPrinterConnection2A** 的 ANSI 版本不受支援，而且會傳回 **\_ 不 \_ 支援的錯誤**。</span><span class="sxs-lookup"><span data-stu-id="205cc-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="205cc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="205cc-131">Requirements</span></span>



| <span data-ttu-id="205cc-132">需求</span><span class="sxs-lookup"><span data-stu-id="205cc-132">Requirement</span></span> | <span data-ttu-id="205cc-133">值</span><span class="sxs-lookup"><span data-stu-id="205cc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="205cc-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="205cc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="205cc-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="205cc-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="205cc-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="205cc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="205cc-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="205cc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="205cc-138">標頭</span><span class="sxs-lookup"><span data-stu-id="205cc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="205cc-139"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="205cc-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="205cc-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="205cc-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="205cc-141"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="205cc-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="205cc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="205cc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="205cc-143"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="205cc-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="205cc-144">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="205cc-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="205cc-145">**AddPrinterConnection2W** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="205cc-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="205cc-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="205cc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205cc-147">列印</span><span class="sxs-lookup"><span data-stu-id="205cc-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="205cc-148">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="205cc-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="205cc-149">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="205cc-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="205cc-150">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="205cc-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="205cc-151">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="205cc-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

