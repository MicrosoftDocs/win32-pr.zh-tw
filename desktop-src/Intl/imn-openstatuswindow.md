---
description: 當 IME 即將建立狀態視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: 'IMN_OPENSTATUSWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977348"
---
# <a name="imn_openstatuswindow-notification-code"></a><span data-ttu-id="1eadd-104">IMN \_ OPENSTATUSWINDOW 通知碼</span><span class="sxs-lookup"><span data-stu-id="1eadd-104">IMN\_OPENSTATUSWINDOW notification code</span></span>

<span data-ttu-id="1eadd-105">當 IME 即將建立狀態視窗時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="1eadd-105">Notifies an application when an IME is about to create the status window.</span></span> <span data-ttu-id="1eadd-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1eadd-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="1eadd-107">參數</span><span class="sxs-lookup"><span data-stu-id="1eadd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eadd-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="1eadd-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="1eadd-109">設定為 IMN \_ OPENSTATUSWINDOW。</span><span class="sxs-lookup"><span data-stu-id="1eadd-109">Set to IMN\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="1eadd-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="1eadd-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="1eadd-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="1eadd-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eadd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1eadd-112">Return Value</span></span>

<span data-ttu-id="1eadd-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1eadd-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eadd-114">備註</span><span class="sxs-lookup"><span data-stu-id="1eadd-114">Remarks</span></span>

<span data-ttu-id="1eadd-115">應用程式會處理此命令，以顯示 IME 本身的狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="1eadd-115">An application processes this command to display the status window for the IME by itself.</span></span>

<span data-ttu-id="1eadd-116">IME 視窗在處理此命令時，會建立狀態視窗，並將在視窗中顯示的字串設定為輸入內容。</span><span class="sxs-lookup"><span data-stu-id="1eadd-116">The IME window creates a status window when it processes this command and sets the strings to display in the window into the input context.</span></span> <span data-ttu-id="1eadd-117">應用程式可以使用 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 函數來取得狀態視窗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1eadd-117">Applications can get information about the status window by using the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eadd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eadd-118">Requirements</span></span>



| <span data-ttu-id="1eadd-119">需求</span><span class="sxs-lookup"><span data-stu-id="1eadd-119">Requirement</span></span> | <span data-ttu-id="1eadd-120">值</span><span class="sxs-lookup"><span data-stu-id="1eadd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eadd-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eadd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1eadd-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eadd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1eadd-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eadd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1eadd-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eadd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1eadd-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1eadd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eadd-126"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1eadd-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eadd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eadd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eadd-128">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="1eadd-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="1eadd-129">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="1eadd-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="1eadd-130">**ImmGetConversionStatus**</span><span class="sxs-lookup"><span data-stu-id="1eadd-130">**ImmGetConversionStatus**</span></span>](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[<span data-ttu-id="1eadd-131">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="1eadd-131">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




