---
description: DeletePrintProvidor 函式會移除 AddPrintProvidor 函數所新增的列印提供者。
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: 'DeletePrintProvidor 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193616"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="87d8f-103">DeletePrintProvidor 函式</span><span class="sxs-lookup"><span data-stu-id="87d8f-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="87d8f-104">**DeletePrintProvidor** 函式會移除 [**AddPrintProvidor**](addprintprovidor.md)函數所新增的列印提供者。</span><span class="sxs-lookup"><span data-stu-id="87d8f-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d8f-105">語法</span><span class="sxs-lookup"><span data-stu-id="87d8f-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="87d8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="87d8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87d8f-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87d8f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87d8f-108">保護必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="87d8f-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87d8f-109">*pEnvironment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87d8f-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87d8f-110">以 null 結束的字串指標，指定要從中移除提供者的環境 (例如 Windows NT x86、Windows IA64 或 Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="87d8f-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="87d8f-111">如果這個參數是 **Null**，就會從目前的呼叫應用程式和用戶端電腦的環境中移除提供者， (不是目的地應用程式和列印伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="87d8f-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="87d8f-112">**Null** 是建議的值，因為它提供最大的可攜性。</span><span class="sxs-lookup"><span data-stu-id="87d8f-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="87d8f-113">*pPrintProviderName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="87d8f-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87d8f-114">以 null 結束的字串指標，指定要移除之提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="87d8f-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87d8f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="87d8f-115">Return value</span></span>

<span data-ttu-id="87d8f-116">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="87d8f-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="87d8f-117">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="87d8f-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d8f-118">備註</span><span class="sxs-lookup"><span data-stu-id="87d8f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87d8f-119">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="87d8f-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="87d8f-120">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="87d8f-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="87d8f-121">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="87d8f-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87d8f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="87d8f-122">Requirements</span></span>



| <span data-ttu-id="87d8f-123">需求</span><span class="sxs-lookup"><span data-stu-id="87d8f-123">Requirement</span></span> | <span data-ttu-id="87d8f-124">值</span><span class="sxs-lookup"><span data-stu-id="87d8f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d8f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87d8f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="87d8f-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87d8f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="87d8f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87d8f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="87d8f-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87d8f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="87d8f-129">標頭</span><span class="sxs-lookup"><span data-stu-id="87d8f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="87d8f-130"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="87d8f-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="87d8f-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="87d8f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="87d8f-132"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87d8f-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="87d8f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="87d8f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87d8f-134"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="87d8f-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="87d8f-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="87d8f-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87d8f-136">**DeletePrintProvidorW** (Unicode) 和 **DeletePrintProvidorA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="87d8f-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="87d8f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87d8f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d8f-138">列印</span><span class="sxs-lookup"><span data-stu-id="87d8f-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="87d8f-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="87d8f-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="87d8f-140">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="87d8f-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




