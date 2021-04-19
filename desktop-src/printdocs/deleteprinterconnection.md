---
description: DeletePrinterConnection 函式會刪除 AddPrinterConnection 或 ConnectToPrinterDlg 的呼叫所建立之印表機的連接。
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: 'DeletePrinterConnection 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998531"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="a4c8b-103">DeletePrinterConnection 函式</span><span class="sxs-lookup"><span data-stu-id="a4c8b-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="a4c8b-104">**DeletePrinterConnection** 函式會刪除 [**AddPrinterConnection**](addprinterconnection.md)或 [**ConnectToPrinterDlg**](connecttoprinterdlg.md)的呼叫所建立之印表機的連接。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4c8b-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="a4c8b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4c8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c8b-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4c8b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c8b-108">指標，指向以 null 終止的字串，指定要刪除之印表機連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c8b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4c8b-109">Return value</span></span>

<span data-ttu-id="a4c8b-110">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a4c8b-111">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c8b-112">備註</span><span class="sxs-lookup"><span data-stu-id="a4c8b-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4c8b-113">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a4c8b-114">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a4c8b-115">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a4c8b-116">**DeletePrinterConnection** 函式不會刪除任何已複製到印表機所連接之伺服器的印表機驅動程式檔案。</span><span class="sxs-lookup"><span data-stu-id="a4c8b-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c8b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4c8b-117">Requirements</span></span>



| <span data-ttu-id="a4c8b-118">需求</span><span class="sxs-lookup"><span data-stu-id="a4c8b-118">Requirement</span></span> | <span data-ttu-id="a4c8b-119">值</span><span class="sxs-lookup"><span data-stu-id="a4c8b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4c8b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c8b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4c8b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a4c8b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4c8b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c8b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4c8b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a4c8b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a4c8b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c8b-125"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a4c8b-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a4c8b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a4c8b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4c8b-127"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4c8b-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a4c8b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c8b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4c8b-129"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="a4c8b-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a4c8b-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a4c8b-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a4c8b-131">**DeletePrinterConnectionW** (Unicode) 和 **DeletePrinterConnectionA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a4c8b-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a4c8b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4c8b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c8b-133">列印</span><span class="sxs-lookup"><span data-stu-id="a4c8b-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a4c8b-134">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="a4c8b-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a4c8b-135">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="a4c8b-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="a4c8b-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="a4c8b-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="a4c8b-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="a4c8b-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




