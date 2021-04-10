---
description: EnumMonitors 函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: 'EnumMonitors 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692908"
---
# <a name="enummonitors-function"></a><span data-ttu-id="7f32c-103">EnumMonitors 函式</span><span class="sxs-lookup"><span data-stu-id="7f32c-103">EnumMonitors function</span></span>

<span data-ttu-id="7f32c-104">**EnumMonitors** 函式會抓取指定的伺服器上所安裝之埠監視器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f32c-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f32c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f32c-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="7f32c-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f32c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f32c-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-108">以 null 結束的字串指標，指定監視器所在伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f32c-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="7f32c-109">如果此參數為 **Null**，則會列舉本機監視器。</span><span class="sxs-lookup"><span data-stu-id="7f32c-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="7f32c-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-111">*PMonitors* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="7f32c-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="7f32c-112">這個值可以是1或2。</span><span class="sxs-lookup"><span data-stu-id="7f32c-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7f32c-113">*pMonitors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-114">接收結構陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="7f32c-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="7f32c-115">緩衝區必須夠大，才能儲存結構成員所參考的字串。</span><span class="sxs-lookup"><span data-stu-id="7f32c-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="7f32c-116">若要判斷所需的緩衝區大小，請呼叫 **EnumMonitors** ，並將 *cbBuf* 設定為零。</span><span class="sxs-lookup"><span data-stu-id="7f32c-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="7f32c-117">**EnumMonitors** 失敗， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤 \_ \_ 的緩衝區，而 *pcbNeeded* 參數會傳回保存結構及其資料陣列所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f32c-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="7f32c-118">如果 *層級* 為1，緩衝區會接收 [**監視 \_ 資訊 \_ 1**](monitor-info-1.md)結構的陣列，如果 *層級* 為2，則會接收 [**監視器 \_ 資訊 \_ 2**](monitor-info-2.md)結構。</span><span class="sxs-lookup"><span data-stu-id="7f32c-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="7f32c-119">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-120">*PMonitors* 所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f32c-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="7f32c-121">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-122">變數的指標，此變數會接收函式成功時所複製的位元組數目，或 *cbBuf* 太小時所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="7f32c-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="7f32c-123">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f32c-124">變數的指標，此變數會接收 *pMonitors* 所指向之緩衝區中傳回的結構數目。</span><span class="sxs-lookup"><span data-stu-id="7f32c-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f32c-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f32c-125">Return value</span></span>

<span data-ttu-id="7f32c-126">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="7f32c-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="7f32c-127">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="7f32c-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f32c-128">備註</span><span class="sxs-lookup"><span data-stu-id="7f32c-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f32c-129">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="7f32c-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="7f32c-130">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="7f32c-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="7f32c-131">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="7f32c-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f32c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f32c-132">Requirements</span></span>



| <span data-ttu-id="7f32c-133">需求</span><span class="sxs-lookup"><span data-stu-id="7f32c-133">Requirement</span></span> | <span data-ttu-id="7f32c-134">值</span><span class="sxs-lookup"><span data-stu-id="7f32c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f32c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f32c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7f32c-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7f32c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f32c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7f32c-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f32c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7f32c-139">標頭</span><span class="sxs-lookup"><span data-stu-id="7f32c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f32c-140"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7f32c-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7f32c-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f32c-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f32c-142"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f32c-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7f32c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7f32c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f32c-144"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="7f32c-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="7f32c-145">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7f32c-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f32c-146">**EnumMonitorsW** (Unicode) 和 **EnumMonitorsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7f32c-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="7f32c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f32c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f32c-148">列印</span><span class="sxs-lookup"><span data-stu-id="7f32c-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7f32c-149">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="7f32c-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="7f32c-150">**監視 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7f32c-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="7f32c-151">**監視 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="7f32c-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

