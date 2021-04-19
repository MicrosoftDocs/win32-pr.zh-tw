---
description: AddForm 函式會將表單新增至可針對指定印表機選取的可用表單清單。
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: 'AddForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980830"
---
# <a name="addform-function"></a><span data-ttu-id="afb2d-103">AddForm 函式</span><span class="sxs-lookup"><span data-stu-id="afb2d-103">AddForm function</span></span>

<span data-ttu-id="afb2d-104">**AddForm** 函式會將表單新增至可針對指定印表機選取的可用表單清單。</span><span class="sxs-lookup"><span data-stu-id="afb2d-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="afb2d-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="afb2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="afb2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb2d-107">*hPrinter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afb2d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afb2d-108">印表機的控制碼，可支援以指定的表單進行列印。</span><span class="sxs-lookup"><span data-stu-id="afb2d-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="afb2d-109">使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。</span><span class="sxs-lookup"><span data-stu-id="afb2d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="afb2d-110">*層級* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afb2d-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afb2d-111">*PForm* 所指向之結構的層級。</span><span class="sxs-lookup"><span data-stu-id="afb2d-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="afb2d-112">此值必須是1或2。</span><span class="sxs-lookup"><span data-stu-id="afb2d-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="afb2d-113">*pForm* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afb2d-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afb2d-114">[**表單 \_ 資訊 \_ 1**](form-info-1.md)或 [**表單 \_ 資訊 \_ 2**](form-info-2.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="afb2d-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb2d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="afb2d-115">Return value</span></span>

<span data-ttu-id="afb2d-116">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="afb2d-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="afb2d-117">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="afb2d-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="afb2d-118">備註</span><span class="sxs-lookup"><span data-stu-id="afb2d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="afb2d-119">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="afb2d-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="afb2d-120">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="afb2d-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="afb2d-121">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="afb2d-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="afb2d-122">應用程式可以藉由呼叫 [**EnumForms**](enumforms.md) 函式來判斷可供印表機使用的表單。</span><span class="sxs-lookup"><span data-stu-id="afb2d-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="afb2d-123">如果 *pForm* 指向 [**表單 \_ 資訊 \_ 2**](form-info-2.md)，而具有指定名稱的表單已經存在，或結構的 *pKeyword* 值已經存在，則 **AddForm** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="afb2d-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb2d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="afb2d-124">Requirements</span></span>



| <span data-ttu-id="afb2d-125">需求</span><span class="sxs-lookup"><span data-stu-id="afb2d-125">Requirement</span></span> | <span data-ttu-id="afb2d-126">值</span><span class="sxs-lookup"><span data-stu-id="afb2d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afb2d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afb2d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="afb2d-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afb2d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="afb2d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afb2d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="afb2d-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afb2d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="afb2d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="afb2d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="afb2d-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="afb2d-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="afb2d-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="afb2d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="afb2d-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="afb2d-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="afb2d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="afb2d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afb2d-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afb2d-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="afb2d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afb2d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb2d-138">列印</span><span class="sxs-lookup"><span data-stu-id="afb2d-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="afb2d-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="afb2d-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="afb2d-140">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="afb2d-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="afb2d-141">**表單 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="afb2d-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="afb2d-142">**表單 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="afb2d-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="afb2d-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="afb2d-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




