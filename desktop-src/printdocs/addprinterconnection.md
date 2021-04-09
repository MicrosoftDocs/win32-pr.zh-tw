---
description: AddPrinterConnection 函式會將連接加入至指定的印表機，以供目前的使用者使用。
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: 'AddPrinterConnection 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850448"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="360f2-103">AddPrinterConnection 函式</span><span class="sxs-lookup"><span data-stu-id="360f2-103">AddPrinterConnection function</span></span>

<span data-ttu-id="360f2-104">**AddPrinterConnection** 函式會將連接加入至指定的印表機，以供目前的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="360f2-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="360f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="360f2-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="360f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="360f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360f2-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="360f2-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="360f2-108">以 null 結束的字串指標，指定目前使用者想要用來建立連接之印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="360f2-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360f2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="360f2-109">Return value</span></span>

<span data-ttu-id="360f2-110">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="360f2-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="360f2-111">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="360f2-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="360f2-112">備註</span><span class="sxs-lookup"><span data-stu-id="360f2-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="360f2-113">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="360f2-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="360f2-114">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="360f2-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="360f2-115">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="360f2-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="360f2-116">當 Windows 建立印表機的連線時，可能需要將印表機驅動程式檔案複製到印表機所連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="360f2-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="360f2-117">如果使用者沒有許可權可將檔案複製到適當的位置， **AddPrinterConnection** 函式會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="360f2-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="360f2-118">呼叫 **AddPrinterConnection** 所建立的印表機連線將會在呼叫 [**>enumprinters**](enumprinters.md) 時列舉，並將 *dwType* 設定為印表機 \_ 列舉 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="360f2-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="360f2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="360f2-119">Requirements</span></span>



| <span data-ttu-id="360f2-120">需求</span><span class="sxs-lookup"><span data-stu-id="360f2-120">Requirement</span></span> | <span data-ttu-id="360f2-121">值</span><span class="sxs-lookup"><span data-stu-id="360f2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360f2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="360f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="360f2-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="360f2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="360f2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="360f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="360f2-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="360f2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="360f2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="360f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="360f2-127"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="360f2-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="360f2-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="360f2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="360f2-129"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="360f2-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="360f2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="360f2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="360f2-131"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="360f2-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="360f2-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="360f2-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="360f2-133">**AddPrinterConnectionW** (Unicode) 和 **AddPrinterConnectionA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="360f2-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="360f2-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="360f2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360f2-135">列印</span><span class="sxs-lookup"><span data-stu-id="360f2-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="360f2-136">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="360f2-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="360f2-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="360f2-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="360f2-138">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="360f2-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="360f2-139">**>enumprinters**</span><span class="sxs-lookup"><span data-stu-id="360f2-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

