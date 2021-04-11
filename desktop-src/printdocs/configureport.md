---
description: ConfigurePort 函式會顯示指定伺服器上端口的 [埠-設定] 對話方塊。
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: 'ConfigurePort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944199"
---
# <a name="configureport-function"></a><span data-ttu-id="b8621-103">ConfigurePort 函式</span><span class="sxs-lookup"><span data-stu-id="b8621-103">ConfigurePort function</span></span>

<span data-ttu-id="b8621-104">**ConfigurePort** 函式會顯示指定伺服器上端口的 [埠-設定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b8621-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8621-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8621-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="b8621-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8621-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8621-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8621-108">指標，指向以 null 終止的字串，這個字串會指定指定的埠所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8621-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="b8621-109">如果此參數為 **Null**，則埠為本機。</span><span class="sxs-lookup"><span data-stu-id="b8621-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="b8621-110">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8621-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8621-111">埠設定對話方塊的父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8621-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b8621-112">*pPortName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8621-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8621-113">以 null 結束的字串指標，指定要設定的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="b8621-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8621-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8621-114">Return value</span></span>

<span data-ttu-id="b8621-115">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="b8621-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b8621-116">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="b8621-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8621-117">備註</span><span class="sxs-lookup"><span data-stu-id="b8621-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8621-118">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="b8621-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b8621-119">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="b8621-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b8621-120">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="b8621-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b8621-121">在呼叫 **ConfigurePort** 函式之前，應用程式應該呼叫 [**EnumPorts**](enumports.md) 函數來判斷有效的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="b8621-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8621-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8621-122">Requirements</span></span>



| <span data-ttu-id="b8621-123">需求</span><span class="sxs-lookup"><span data-stu-id="b8621-123">Requirement</span></span> | <span data-ttu-id="b8621-124">值</span><span class="sxs-lookup"><span data-stu-id="b8621-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8621-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8621-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8621-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8621-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8621-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8621-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8621-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8621-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8621-129">標頭</span><span class="sxs-lookup"><span data-stu-id="b8621-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8621-130"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b8621-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b8621-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8621-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8621-132"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8621-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b8621-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b8621-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8621-134"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="b8621-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b8621-135">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b8621-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8621-136">**ConfigurePortW** (Unicode) 和 **ConfigurePortA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b8621-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="b8621-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8621-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8621-138">列印</span><span class="sxs-lookup"><span data-stu-id="b8621-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b8621-139">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="b8621-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b8621-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="b8621-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




