---
description: EnumForms 函式會列舉指定印表機所支援的表單。
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: 'EnumForms 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319096"
---
# <a name="enumforms-function"></a><span data-ttu-id="ffb8e-103">EnumForms 函式</span><span class="sxs-lookup"><span data-stu-id="ffb8e-103">EnumForms function</span></span>

<span data-ttu-id="ffb8e-104">**EnumForms** 函式會列舉指定印表機所支援的表單。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb8e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffb8e-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="ffb8e-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffb8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb8e-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-108">應列舉表單之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="ffb8e-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ffb8e-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-111">指定 *pForm* 點的結構版本。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="ffb8e-112">此值必須是1或2。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ffb8e-113">*pForm* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-114">一或多個 [**表單 \_ 資訊 \_ 1**](form-info-1.md) 結構的指標，或一個或多個 [**表單 \_ 資訊 \_ 2**](form-info-2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="ffb8e-115">所有結構都有相同的層級。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="ffb8e-116">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-117">指定 *pForm* 點的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="ffb8e-118">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-119">變數的指標，此變數會接收復制到陣列的 PForm 點所複製的位元組數目，如果作業) 成功，則為點 (的位元組數目; 如果失敗，則為 (所需的位元組數目，因為 *cbBuf* 太小) 。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="ffb8e-120">*pcReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8e-121">變數的指標，此變數會接收復制到 *pForm* 點之陣列中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb8e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffb8e-122">Return value</span></span>

<span data-ttu-id="ffb8e-123">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ffb8e-124">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb8e-125">備註</span><span class="sxs-lookup"><span data-stu-id="ffb8e-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ffb8e-126">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ffb8e-127">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ffb8e-128">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ffb8e-129">如果呼叫端是遠端的，而且 *層級* 是2，則傳回 [**表單 \_ INFO \_ 2**](form-info-2.md)結構的 **StringType** 值一律會是 **字串 \_ LANGPAIR**。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="ffb8e-130">在 Windows Vista 中， **EnumForms** 所傳回的表單資料，會在 *hPrinter* 指的是由列印伺服器所裝載的遠端列印伺服器或印表機時，從本機快取中取出，而且至少有一個開啟的連接可連至遠端列印伺服器上的印表機。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="ffb8e-131">在所有其他設定中，會從遠端列印伺服器查詢表單資料。</span><span class="sxs-lookup"><span data-stu-id="ffb8e-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb8e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffb8e-132">Requirements</span></span>



| <span data-ttu-id="ffb8e-133">需求</span><span class="sxs-lookup"><span data-stu-id="ffb8e-133">Requirement</span></span> | <span data-ttu-id="ffb8e-134">值</span><span class="sxs-lookup"><span data-stu-id="ffb8e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb8e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffb8e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb8e-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ffb8e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffb8e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb8e-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffb8e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ffb8e-139">標頭</span><span class="sxs-lookup"><span data-stu-id="ffb8e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb8e-140"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ffb8e-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ffb8e-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="ffb8e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffb8e-142"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8e-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ffb8e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ffb8e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffb8e-144"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8e-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ffb8e-145">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ffb8e-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ffb8e-146">**EnumFormsW** (Unicode) 和 **EnumFormsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ffb8e-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="ffb8e-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffb8e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb8e-148">列印</span><span class="sxs-lookup"><span data-stu-id="ffb8e-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ffb8e-149">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="ffb8e-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ffb8e-150">**Interactivesession.addprinter**</span><span class="sxs-lookup"><span data-stu-id="ffb8e-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="ffb8e-151">**表單 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ffb8e-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="ffb8e-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ffb8e-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




