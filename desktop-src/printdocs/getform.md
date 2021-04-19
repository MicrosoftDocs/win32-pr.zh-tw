---
description: GetForm 函式會捕獲指定表單的相關資訊。
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: 'GetForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980514"
---
# <a name="getform-function"></a><span data-ttu-id="f8ebc-103">GetForm 函式</span><span class="sxs-lookup"><span data-stu-id="f8ebc-103">GetForm function</span></span>

<span data-ttu-id="f8ebc-104">**GetForm** 函式會捕獲指定表單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ebc-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8ebc-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="f8ebc-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8ebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ebc-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-108">印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-108">A handle to the printer.</span></span> <span data-ttu-id="f8ebc-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f8ebc-110">*pFormName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-111">指定表單名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="f8ebc-112">若要取得印表機支援的表單名稱，請呼叫 [**EnumForms**](enumforms.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f8ebc-113">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-114">*PForm* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="f8ebc-115">此值必須是1或2。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f8ebc-116">*pForm* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-117">位元組陣列的指標，此陣列會接收初始化的 [**表單 \_ 資訊 \_ 1**](form-info-1.md) 或 [**表單 \_ 資訊 \_ 2**](form-info-2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f8ebc-118">*cbBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-119">*PForm* 陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="f8ebc-120">*pcbNeeded* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ebc-121">值的指標，指定函式成功時所複製的位元組數目，或如果 *cbBuf* 太小，則為所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ebc-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ebc-122">Return value</span></span>

<span data-ttu-id="f8ebc-123">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f8ebc-124">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ebc-125">備註</span><span class="sxs-lookup"><span data-stu-id="f8ebc-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8ebc-126">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f8ebc-127">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f8ebc-128">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f8ebc-129">如果呼叫端是遠端的，而且 *層級* 是2，則傳回 [**表單 \_ INFO \_ 2**](form-info-2.md)的 **StringType** 值一律會是字串 \_ LANGPAIR。</span><span class="sxs-lookup"><span data-stu-id="f8ebc-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ebc-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ebc-130">Requirements</span></span>



| <span data-ttu-id="f8ebc-131">需求</span><span class="sxs-lookup"><span data-stu-id="f8ebc-131">Requirement</span></span> | <span data-ttu-id="f8ebc-132">值</span><span class="sxs-lookup"><span data-stu-id="f8ebc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ebc-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8ebc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ebc-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8ebc-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8ebc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ebc-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ebc-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8ebc-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f8ebc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ebc-138"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f8ebc-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8ebc-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8ebc-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8ebc-140"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ebc-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f8ebc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f8ebc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8ebc-142"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="f8ebc-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f8ebc-143">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f8ebc-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8ebc-144">**GetFormW** (Unicode) 和 **GetFormA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f8ebc-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="f8ebc-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8ebc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ebc-146">列印</span><span class="sxs-lookup"><span data-stu-id="f8ebc-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8ebc-147">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="f8ebc-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ebc-148">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="f8ebc-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="f8ebc-149">**DeleteForm**</span><span class="sxs-lookup"><span data-stu-id="f8ebc-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="f8ebc-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f8ebc-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f8ebc-151">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="f8ebc-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




