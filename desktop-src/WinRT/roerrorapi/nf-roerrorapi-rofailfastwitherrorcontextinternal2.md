---
title: RoFailFastWithErrorCoNtextInternal2 函式
description: 在目前的進程中引發不可持續性例外狀況，也可讓您包含作業系統尚未捕捉的其他錯誤內容。
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969735"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="b69b2-103">RoFailFastWithErrorCoNtextInternal2 函式</span><span class="sxs-lookup"><span data-stu-id="b69b2-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="b69b2-104">在目前的進程中引發不可持續性例外狀況，也可讓您包含作業系統 (OS) 尚未捕捉的其他錯誤內容。</span><span class="sxs-lookup"><span data-stu-id="b69b2-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="b69b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="b69b2-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="b69b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="b69b2-106">Parameters</span></span>

`hrError`

<span data-ttu-id="b69b2-107">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="b69b2-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="b69b2-108">與目前錯誤相關聯的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="b69b2-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="b69b2-109">*HrError* 的任何值都會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b69b2-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="b69b2-110">類型： **[ULONG](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b69b2-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b69b2-111">*AStowedExceptionPointers* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b69b2-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="b69b2-112">類型： **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="b69b2-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="b69b2-113">[**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md)結構的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="b69b2-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="b69b2-114">每個結構都包含描述 stowed 例外狀況的資訊。</span><span class="sxs-lookup"><span data-stu-id="b69b2-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="b69b2-115">然後，這些結構中的資訊會提交給 Windows 錯誤報告 (WER) 以及平臺所捕捉的 stowed 例外狀況資訊。</span><span class="sxs-lookup"><span data-stu-id="b69b2-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="b69b2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b69b2-116">Return value</span></span>

<span data-ttu-id="b69b2-117">此函數不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b69b2-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b69b2-118">備註</span><span class="sxs-lookup"><span data-stu-id="b69b2-118">Remarks</span></span>

<span data-ttu-id="b69b2-119">**RoFailFastWithErrorCoNtextInternal2** 不會與匯入程式庫和標頭檔相關聯。</span><span class="sxs-lookup"><span data-stu-id="b69b2-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="b69b2-120">您可以先使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) 函式 (載入 `ComBase.dll`) ，然後呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來取出 **RoFailFastWithErrorCoNtextInternal2** 的位址，藉此呼叫該函數。</span><span class="sxs-lookup"><span data-stu-id="b69b2-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="b69b2-121">如需詳細資訊，請參閱 [RoFailFastWithErrorCoNtext 函數](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)。</span><span class="sxs-lookup"><span data-stu-id="b69b2-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="b69b2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b69b2-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b69b2-123">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="b69b2-123">**Target Platform**</span></span> | <span data-ttu-id="b69b2-124">Windows</span><span class="sxs-lookup"><span data-stu-id="b69b2-124">Windows</span></span> |
| <span data-ttu-id="b69b2-125">**標頭**</span><span class="sxs-lookup"><span data-stu-id="b69b2-125">**Header**</span></span> | <span data-ttu-id="b69b2-126">N/A</span><span class="sxs-lookup"><span data-stu-id="b69b2-126">N/A</span></span> |
| <span data-ttu-id="b69b2-127">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="b69b2-127">**Library**</span></span> | <span data-ttu-id="b69b2-128">N/A</span><span class="sxs-lookup"><span data-stu-id="b69b2-128">N/A</span></span> |
| <span data-ttu-id="b69b2-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="b69b2-129">**DLL**</span></span> | <span data-ttu-id="b69b2-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="b69b2-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="b69b2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b69b2-131">See also</span></span>

* [<span data-ttu-id="b69b2-132">RoFailFastWithErrorCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="b69b2-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)