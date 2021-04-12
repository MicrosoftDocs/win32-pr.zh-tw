---
description: SetForm 函式會設定指定印表機的表單資訊。
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: 'SetForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319088"
---
# <a name="setform-function"></a><span data-ttu-id="f0ab3-103">SetForm 函式</span><span class="sxs-lookup"><span data-stu-id="f0ab3-103">SetForm function</span></span>

<span data-ttu-id="f0ab3-104">**SetForm** 函式會設定指定印表機的表單資訊。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ab3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0ab3-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="f0ab3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0ab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ab3-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ab3-108">已設定表單資訊之印表機的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="f0ab3-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f0ab3-110">*pFormName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ab3-111">以 null 結束的字串指標，指定設定表單資訊的表單名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="f0ab3-112">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ab3-113">*PForm* 所指向的結構版本。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="f0ab3-114">此值必須是1或2。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f0ab3-115">*pForm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ab3-116">[**表單 \_ 資訊 \_ 1**](form-info-1.md)或 [**表單 \_ 資訊 \_ 2**](form-info-2.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ab3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0ab3-117">Return value</span></span>

<span data-ttu-id="f0ab3-118">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f0ab3-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ab3-120">備註</span><span class="sxs-lookup"><span data-stu-id="f0ab3-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0ab3-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f0ab3-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f0ab3-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f0ab3-124">您可以針對現有的 [**表單 \_ 資訊 \_ 2**](form-info-2.md)多次呼叫 **SetForm** ，每個呼叫都會新增額外的 **pDisplayName** 和 **wLangId** 值配對。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="f0ab3-125">所有語言版本的表單都將在最近的 **SetForm** 呼叫中取得 **表單 \_ INFO \_ 2** 的 **大小** 與 **ImageableArea** 值。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="f0ab3-126">如果呼叫端是遠端的，而且 *層級* 是2，則 [**表單 \_ 資訊 \_ 2**](form-info-2.md)的 **StringType** 值不能是字串 \_ MUIDLL。</span><span class="sxs-lookup"><span data-stu-id="f0ab3-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ab3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0ab3-127">Requirements</span></span>



| <span data-ttu-id="f0ab3-128">需求</span><span class="sxs-lookup"><span data-stu-id="f0ab3-128">Requirement</span></span> | <span data-ttu-id="f0ab3-129">值</span><span class="sxs-lookup"><span data-stu-id="f0ab3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ab3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0ab3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ab3-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f0ab3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0ab3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ab3-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0ab3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f0ab3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f0ab3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ab3-135"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f0ab3-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f0ab3-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0ab3-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0ab3-137"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0ab3-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f0ab3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ab3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0ab3-139"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="f0ab3-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f0ab3-140">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f0ab3-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0ab3-141">**SetFormW** (Unicode) 和 **SetFormA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f0ab3-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="f0ab3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0ab3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ab3-143">列印</span><span class="sxs-lookup"><span data-stu-id="f0ab3-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f0ab3-144">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="f0ab3-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f0ab3-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="f0ab3-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="f0ab3-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f0ab3-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f0ab3-147">**表單 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f0ab3-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="f0ab3-148">**表單 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f0ab3-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




