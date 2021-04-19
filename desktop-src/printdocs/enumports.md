---
description: EnumPorts 函式會列舉可在指定的伺服器上列印的埠。
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: 'EnumPorts 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985244"
---
# <a name="enumports-function"></a><span data-ttu-id="3850d-103">EnumPorts 函式</span><span class="sxs-lookup"><span data-stu-id="3850d-103">EnumPorts function</span></span>

<span data-ttu-id="3850d-104">**EnumPorts** 函式會列舉可在指定的伺服器上列印的埠。</span><span class="sxs-lookup"><span data-stu-id="3850d-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3850d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3850d-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="3850d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3850d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3850d-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3850d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-108">以 null 結束的字串指標，指定您想要列舉其印表機埠的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3850d-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="3850d-109">如果 *pName* 為 **Null**，此函式會列舉本機電腦的印表機埠。</span><span class="sxs-lookup"><span data-stu-id="3850d-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="3850d-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3850d-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-111">*PPorts* 緩衝區中傳回的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="3850d-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="3850d-112">如果 *層級* 為1， *PPorts* 會接收 [**埠 \_ 資訊 \_ 1**](port-info-1.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="3850d-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="3850d-113">如果 *層級* 為2， *PPorts* 會接收 [**埠 \_ 資訊 \_ 2**](port-info-2.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="3850d-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="3850d-114">*pPorts* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3850d-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-115">接收 [**埠 \_ 資訊 \_ 1**](port-info-1.md) 或 [**埠 \_ 資訊 \_ 2**](port-info-2.md) 結構之陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="3850d-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="3850d-116">每個結構都包含描述可用印表機埠的資料。</span><span class="sxs-lookup"><span data-stu-id="3850d-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="3850d-117">緩衝區必須夠大，才能儲存結構成員所指向的字串。</span><span class="sxs-lookup"><span data-stu-id="3850d-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="3850d-118">若要判斷所需的緩衝區大小，請呼叫 **EnumPorts** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="3850d-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="3850d-119">**EnumPorts** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3850d-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="3850d-120">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3850d-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-121">*PPorts* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3850d-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="3850d-122">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3850d-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-123">變數的指標，此變數會接收復制到 *pPorts* 緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3850d-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="3850d-124">如果緩衝區太小，則函式會失敗，而變數會收到所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3850d-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="3850d-125">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3850d-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3850d-126">變數的指標，此變數會接收 *pPorts* 緩衝區中傳回的 [**埠 \_ 資訊 \_ 1**](port-info-1.md)或 [**埠 \_ 資訊 \_ 2**](port-info-2.md)結構的數目。</span><span class="sxs-lookup"><span data-stu-id="3850d-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="3850d-127">這是指定的伺服器上可用的印表機埠數目。</span><span class="sxs-lookup"><span data-stu-id="3850d-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3850d-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="3850d-128">Return value</span></span>

<span data-ttu-id="3850d-129">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="3850d-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3850d-130">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="3850d-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3850d-131">備註</span><span class="sxs-lookup"><span data-stu-id="3850d-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3850d-132">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="3850d-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3850d-133">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="3850d-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3850d-134">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="3850d-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3850d-135">即使 *pName* 指定的伺服器未定義印表機， **EnumPorts** 函式仍會成功。</span><span class="sxs-lookup"><span data-stu-id="3850d-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="3850d-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="3850d-136">Requirements</span></span>



| <span data-ttu-id="3850d-137">需求</span><span class="sxs-lookup"><span data-stu-id="3850d-137">Requirement</span></span> | <span data-ttu-id="3850d-138">值</span><span class="sxs-lookup"><span data-stu-id="3850d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3850d-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3850d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3850d-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3850d-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3850d-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3850d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3850d-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3850d-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3850d-143">標頭</span><span class="sxs-lookup"><span data-stu-id="3850d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3850d-144"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3850d-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3850d-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="3850d-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="3850d-146"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3850d-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3850d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3850d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3850d-148"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="3850d-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3850d-149">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="3850d-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3850d-150">**EnumPortsW** (Unicode) 和 **EnumPortsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="3850d-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="3850d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3850d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3850d-152">列印</span><span class="sxs-lookup"><span data-stu-id="3850d-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3850d-153">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="3850d-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3850d-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="3850d-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="3850d-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="3850d-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="3850d-156">**埠 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3850d-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="3850d-157">**埠 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3850d-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

