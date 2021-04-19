---
description: ConnectToPrinterDlg 函式會顯示一個對話方塊，讓使用者流覽並聯機到網路上的印表機。
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: 'ConnectToPrinterDlg 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980507"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="963a0-103">ConnectToPrinterDlg 函式</span><span class="sxs-lookup"><span data-stu-id="963a0-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="963a0-104">**ConnectToPrinterDlg** 函式會顯示一個對話方塊，讓使用者流覽並聯機到網路上的印表機。</span><span class="sxs-lookup"><span data-stu-id="963a0-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="963a0-105">如果使用者選取印表機，此函式會嘗試建立與它的連接;如果伺服器上未安裝適當的驅動程式，則會提供使用者在本機建立印表機的選項。</span><span class="sxs-lookup"><span data-stu-id="963a0-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="963a0-106">語法</span><span class="sxs-lookup"><span data-stu-id="963a0-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="963a0-107">參數</span><span class="sxs-lookup"><span data-stu-id="963a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963a0-108">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="963a0-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963a0-109">指定對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="963a0-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="963a0-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="963a0-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963a0-111">此參數是保留的，而且必須為零。</span><span class="sxs-lookup"><span data-stu-id="963a0-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963a0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="963a0-112">Return value</span></span>

<span data-ttu-id="963a0-113">如果函式成功且使用者選取印表機，則傳回值會是所選印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="963a0-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="963a0-114">如果函式失敗，或使用者取消對話方塊，而不選取印表機，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="963a0-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="963a0-115">備註</span><span class="sxs-lookup"><span data-stu-id="963a0-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="963a0-116">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="963a0-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="963a0-117">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="963a0-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="963a0-118">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="963a0-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="963a0-119">**ConnectToPrinterDlg** 函式會嘗試建立與所選印表機的連接。</span><span class="sxs-lookup"><span data-stu-id="963a0-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="963a0-120">但是，如果印表機所在的伺服器沒有安裝適合的驅動程式，則此函式會提供使用者在本機建立印表機的選項。</span><span class="sxs-lookup"><span data-stu-id="963a0-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="963a0-121">呼叫應用程式可以藉由呼叫 [**GetPrinter**](getprinter.md) 與 [**印表機 \_ 資訊 \_ 2**](printer-info-2.md) 結構，然後檢查該結構的 **屬性** 成員，來判斷函式是否已在本機建立印表機。</span><span class="sxs-lookup"><span data-stu-id="963a0-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="963a0-122">應用程式應該呼叫 [**DeletePrinter**](deleteprinter.md) 來刪除本機印表機。</span><span class="sxs-lookup"><span data-stu-id="963a0-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="963a0-123">應用程式應該呼叫 [**DeletePrinterConnection**](deleteprinterconnection.md) 來刪除印表機的連接。</span><span class="sxs-lookup"><span data-stu-id="963a0-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="963a0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="963a0-124">Requirements</span></span>



| <span data-ttu-id="963a0-125">需求</span><span class="sxs-lookup"><span data-stu-id="963a0-125">Requirement</span></span> | <span data-ttu-id="963a0-126">值</span><span class="sxs-lookup"><span data-stu-id="963a0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="963a0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="963a0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="963a0-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="963a0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="963a0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="963a0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="963a0-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="963a0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="963a0-131">標頭</span><span class="sxs-lookup"><span data-stu-id="963a0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="963a0-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="963a0-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="963a0-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="963a0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="963a0-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="963a0-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="963a0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="963a0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963a0-136"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="963a0-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="963a0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="963a0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="963a0-138">列印</span><span class="sxs-lookup"><span data-stu-id="963a0-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="963a0-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="963a0-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="963a0-140">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="963a0-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="963a0-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="963a0-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="963a0-142">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="963a0-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="963a0-143">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="963a0-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="963a0-144">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="963a0-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="963a0-145">**印表機 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="963a0-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




