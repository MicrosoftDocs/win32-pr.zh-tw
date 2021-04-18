---
description: ReadPrinter 函數會從指定的印表機抓取資料。
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: 'ReadPrinter 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978207"
---
# <a name="readprinter-function"></a><span data-ttu-id="40fbe-103">ReadPrinter 函式</span><span class="sxs-lookup"><span data-stu-id="40fbe-103">ReadPrinter function</span></span>

<span data-ttu-id="40fbe-104">**ReadPrinter** 函數會從指定的印表機抓取資料。</span><span class="sxs-lookup"><span data-stu-id="40fbe-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fbe-105">語法</span><span class="sxs-lookup"><span data-stu-id="40fbe-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="40fbe-106">參數</span><span class="sxs-lookup"><span data-stu-id="40fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40fbe-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fbe-108">要取得其資料之印表機物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="40fbe-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="40fbe-109">使用 [**OpenPrinter**](openprinter.md) 函式來取出印表機物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="40fbe-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="40fbe-110">使用格式： Printername，Job xxxx。</span><span class="sxs-lookup"><span data-stu-id="40fbe-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="40fbe-111">*pBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fbe-112">接收印表機資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="40fbe-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="40fbe-113">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40fbe-114">*PBuf* 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="40fbe-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="40fbe-115">*pNoBytesRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fbe-116">變數的指標，此變數會接收復制到 *pBuf* 點之陣列中的資料位元組數。</span><span class="sxs-lookup"><span data-stu-id="40fbe-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40fbe-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="40fbe-117">Return value</span></span>

<span data-ttu-id="40fbe-118">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="40fbe-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="40fbe-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="40fbe-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="40fbe-120">備註</span><span class="sxs-lookup"><span data-stu-id="40fbe-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="40fbe-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="40fbe-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="40fbe-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="40fbe-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="40fbe-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="40fbe-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="40fbe-124">如果裝置或印表機不是雙向， **ReadPrinter** 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="40fbe-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="40fbe-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="40fbe-125">Requirements</span></span>



| <span data-ttu-id="40fbe-126">需求</span><span class="sxs-lookup"><span data-stu-id="40fbe-126">Requirement</span></span> | <span data-ttu-id="40fbe-127">值</span><span class="sxs-lookup"><span data-stu-id="40fbe-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fbe-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40fbe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="40fbe-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40fbe-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40fbe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="40fbe-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40fbe-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="40fbe-132">標頭</span><span class="sxs-lookup"><span data-stu-id="40fbe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="40fbe-133"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="40fbe-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="40fbe-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="40fbe-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="40fbe-135"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="40fbe-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="40fbe-136">DLL</span><span class="sxs-lookup"><span data-stu-id="40fbe-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40fbe-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40fbe-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="40fbe-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40fbe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fbe-139">列印</span><span class="sxs-lookup"><span data-stu-id="40fbe-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="40fbe-140">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="40fbe-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="40fbe-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="40fbe-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




