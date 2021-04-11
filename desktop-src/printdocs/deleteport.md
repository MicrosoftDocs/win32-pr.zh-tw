---
description: DeletePort 函式會顯示一個對話方塊，可讓使用者刪除埠名稱。
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: 'DeletePort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193617"
---
# <a name="deleteport-function"></a><span data-ttu-id="1cab4-103">DeletePort 函式</span><span class="sxs-lookup"><span data-stu-id="1cab4-103">DeletePort function</span></span>

<span data-ttu-id="1cab4-104">**DeletePort** 函式會顯示一個對話方塊，可讓使用者刪除埠名稱。</span><span class="sxs-lookup"><span data-stu-id="1cab4-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cab4-105">語法</span><span class="sxs-lookup"><span data-stu-id="1cab4-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="1cab4-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cab4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cab4-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cab4-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cab4-108">以零結束的字串指標，指定應刪除其埠之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cab4-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="1cab4-109">如果此參數為 **Null**，則會刪除本機埠。</span><span class="sxs-lookup"><span data-stu-id="1cab4-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="1cab4-110">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cab4-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cab4-111">埠刪除對話方塊之父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cab4-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1cab4-112">*pPortName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cab4-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cab4-113">以零結束的字串指標，指定應該刪除的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="1cab4-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cab4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cab4-114">Return value</span></span>

<span data-ttu-id="1cab4-115">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="1cab4-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1cab4-116">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="1cab4-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cab4-117">備註</span><span class="sxs-lookup"><span data-stu-id="1cab4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cab4-118">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="1cab4-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1cab4-119">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="1cab4-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1cab4-120">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="1cab4-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="1cab4-121">應用程式可以藉由呼叫 [**EnumPorts**](enumports.md) 函式來取得有效埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cab4-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="1cab4-122">如果印表機目前連接到指定的埠， **DeletePort** 函數會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1cab4-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="1cab4-123">**DeletePort** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能存取埠所連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="1cab4-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cab4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cab4-124">Requirements</span></span>



| <span data-ttu-id="1cab4-125">需求</span><span class="sxs-lookup"><span data-stu-id="1cab4-125">Requirement</span></span> | <span data-ttu-id="1cab4-126">值</span><span class="sxs-lookup"><span data-stu-id="1cab4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cab4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cab4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1cab4-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cab4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cab4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cab4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1cab4-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cab4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1cab4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1cab4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cab4-132"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1cab4-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1cab4-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="1cab4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cab4-134"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cab4-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1cab4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1cab4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cab4-136"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="1cab4-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1cab4-137">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="1cab4-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1cab4-138">**DeletePortW** (Unicode) 和 **DeletePortA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="1cab4-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="1cab4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cab4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cab4-140">列印</span><span class="sxs-lookup"><span data-stu-id="1cab4-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1cab4-141">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="1cab4-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1cab4-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="1cab4-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="1cab4-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="1cab4-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




