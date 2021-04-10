---
description: DeletePrintProcessor 函式會移除 AddPrintProcessor 函數所新增的列印處理器。
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: 'DeletePrintProcessor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192605"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="b8429-103">DeletePrintProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="b8429-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="b8429-104">**DeletePrintProcessor** 函式會移除 [**AddPrintProcessor**](addprintprocessor.md)函數所新增的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="b8429-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8429-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8429-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="b8429-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8429-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8429-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8429-108">以 null 結束的字串指標，指定要移除處理器的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8429-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="b8429-109">如果此參數為 **Null**，則會在本機移除印表機處理器。</span><span class="sxs-lookup"><span data-stu-id="b8429-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="b8429-110">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8429-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8429-111">以 null 結束的字串指標，指定要移除處理器的環境 (例如 Windows NT x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="b8429-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="b8429-112">如果這個參數是 **Null**，就會從目前的呼叫應用程式和用戶端電腦的環境中移除處理器 (不是目的地應用程式和列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="b8429-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="b8429-113">**Null** 是建議的值，因為它提供最大的可攜性。</span><span class="sxs-lookup"><span data-stu-id="b8429-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="b8429-114">*pPrintProcessorName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8429-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8429-115">以 null 結束的字串指標，指定要移除的處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8429-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8429-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8429-116">Return value</span></span>

<span data-ttu-id="b8429-117">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="b8429-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b8429-118">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b8429-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8429-119">備註</span><span class="sxs-lookup"><span data-stu-id="b8429-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8429-120">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="b8429-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b8429-121">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="b8429-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b8429-122">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="b8429-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b8429-123">呼叫端必須有 [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="b8429-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8429-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8429-124">Requirements</span></span>



| <span data-ttu-id="b8429-125">需求</span><span class="sxs-lookup"><span data-stu-id="b8429-125">Requirement</span></span> | <span data-ttu-id="b8429-126">值</span><span class="sxs-lookup"><span data-stu-id="b8429-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8429-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8429-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b8429-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8429-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8429-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8429-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b8429-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8429-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8429-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b8429-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8429-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b8429-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b8429-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8429-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8429-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8429-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b8429-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b8429-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8429-136"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="b8429-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b8429-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b8429-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8429-138">**DeletePrintProcessorW** (Unicode) 和 **DeletePrintProcessorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b8429-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b8429-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8429-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8429-140">列印</span><span class="sxs-lookup"><span data-stu-id="b8429-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b8429-141">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="b8429-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b8429-142">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="b8429-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

