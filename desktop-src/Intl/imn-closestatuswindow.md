---
description: 當 IME 即將關閉狀態視窗時，通知應用程式。 應用程式會透過 \_ 包含參數設定的 WM IME 通知訊息接收此命令， \_ 如下所示。
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: 'IMN_CLOSESTATUSWINDOW 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971825"
---
# <a name="imn_closestatuswindow-notification-code"></a><span data-ttu-id="ebeac-104">IMN \_ CLOSESTATUSWINDOW 通知碼</span><span class="sxs-lookup"><span data-stu-id="ebeac-104">IMN\_CLOSESTATUSWINDOW notification code</span></span>

<span data-ttu-id="ebeac-105">當 IME 即將關閉狀態視窗時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="ebeac-105">Notifies an application when an IME is about to close the status window.</span></span> <span data-ttu-id="ebeac-106">應用程式會透過包含參數設定的 [**WM \_ IME \_ 通知**](wm-ime-notify.md) 訊息接收此命令，如下所示。</span><span class="sxs-lookup"><span data-stu-id="ebeac-106">The application receives this command through the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message with parameter settings as shown below.</span></span>


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="ebeac-107">參數</span><span class="sxs-lookup"><span data-stu-id="ebeac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebeac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebeac-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="ebeac-109">設定為 IMN \_ CLOSESTATUSWINDOW。</span><span class="sxs-lookup"><span data-stu-id="ebeac-109">Set to IMN\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="ebeac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebeac-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ebeac-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="ebeac-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebeac-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebeac-112">Return Value</span></span>

<span data-ttu-id="ebeac-113">此命令沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ebeac-113">This command has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebeac-114">備註</span><span class="sxs-lookup"><span data-stu-id="ebeac-114">Remarks</span></span>

<span data-ttu-id="ebeac-115">如果應用程式顯示 IME 的狀態視窗，則應該處理此命令。</span><span class="sxs-lookup"><span data-stu-id="ebeac-115">An application should process this command if it displays the status window for the IME.</span></span>

<span data-ttu-id="ebeac-116">在處理此命令時，IME 視窗會關閉狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="ebeac-116">The IME window closes the status window when it processes this command.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebeac-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebeac-117">Requirements</span></span>



| <span data-ttu-id="ebeac-118">需求</span><span class="sxs-lookup"><span data-stu-id="ebeac-118">Requirement</span></span> | <span data-ttu-id="ebeac-119">值</span><span class="sxs-lookup"><span data-stu-id="ebeac-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebeac-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebeac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ebeac-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebeac-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebeac-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebeac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ebeac-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebeac-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ebeac-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ebeac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebeac-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ebeac-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebeac-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebeac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebeac-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="ebeac-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="ebeac-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="ebeac-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="ebeac-129">**WM \_ 輸入法 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="ebeac-129">**WM\_IME\_NOTIFY**</span></span>](wm-ime-notify.md)
</dt> </dl>

 

 




