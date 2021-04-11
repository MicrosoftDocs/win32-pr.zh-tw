---
description: 指示 IME 視窗顯示狀態視窗。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: 'IMC_OPENSTATUSWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd0b5e19ef6a026459eedb050e9ac9587b5ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848194"
---
# <a name="imc_openstatuswindow-command"></a><span data-ttu-id="9b281-104">IMC \_ OPENSTATUSWINDOW 命令</span><span class="sxs-lookup"><span data-stu-id="9b281-104">IMC\_OPENSTATUSWINDOW command</span></span>

<span data-ttu-id="9b281-105">指示 IME 視窗顯示狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="9b281-105">Instructs the IME window to show the status window.</span></span> <span data-ttu-id="9b281-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="9b281-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="9b281-107">參數</span><span class="sxs-lookup"><span data-stu-id="9b281-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b281-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b281-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9b281-109">設定為 IMC \_ OPENSTATUSWINDOW。</span><span class="sxs-lookup"><span data-stu-id="9b281-109">Set to IMC\_OPENSTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="9b281-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b281-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9b281-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="9b281-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b281-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b281-112">Return Value</span></span>

<span data-ttu-id="9b281-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="9b281-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b281-114">備註</span><span class="sxs-lookup"><span data-stu-id="9b281-114">Remarks</span></span>

<span data-ttu-id="9b281-115">如果作業系統不是顯示輸入法狀態模式，則會忽略這個命令。</span><span class="sxs-lookup"><span data-stu-id="9b281-115">This command is ignored if the operating system is not in the show IME status mode.</span></span> <span data-ttu-id="9b281-116">使用者可以從工作列設定或清除 [顯示輸入法狀態模式]。</span><span class="sxs-lookup"><span data-stu-id="9b281-116">The user can set or clear the show IME status mode from the task bar.</span></span>

<span data-ttu-id="9b281-117">如果已顯示 [狀態] 視窗，此命令不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="9b281-117">If the status window is already shown, this command does nothing.</span></span> <span data-ttu-id="9b281-118">雖然應用程式可以將此命令傳送至 IME 視窗，但應用程式不會收到對應的 [**IMN \_ OPENSTATUSWINDOW**](imn-openstatuswindow.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="9b281-118">Although the application can send this command to the IME window, the application does not receive the corresponding [**IMN\_OPENSTATUSWINDOW**](imn-openstatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b281-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b281-119">Requirements</span></span>



| <span data-ttu-id="9b281-120">需求</span><span class="sxs-lookup"><span data-stu-id="9b281-120">Requirement</span></span> | <span data-ttu-id="9b281-121">值</span><span class="sxs-lookup"><span data-stu-id="9b281-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b281-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b281-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9b281-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b281-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9b281-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b281-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9b281-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b281-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9b281-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9b281-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b281-127"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9b281-127"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b281-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b281-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b281-129">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="9b281-129">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="9b281-130">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="9b281-130">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="9b281-131">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="9b281-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




