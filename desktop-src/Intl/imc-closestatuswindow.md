---
description: 指示 IME 視窗隱藏狀態視窗。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: 'IMC_CLOSESTATUSWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853147"
---
# <a name="imc_closestatuswindow-command"></a><span data-ttu-id="6f59d-104">IMC \_ CLOSESTATUSWINDOW 命令</span><span class="sxs-lookup"><span data-stu-id="6f59d-104">IMC\_CLOSESTATUSWINDOW command</span></span>

<span data-ttu-id="6f59d-105">指示 IME 視窗隱藏狀態視窗。</span><span class="sxs-lookup"><span data-stu-id="6f59d-105">Instructs the IME window to hide the status window.</span></span> <span data-ttu-id="6f59d-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="6f59d-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a><span data-ttu-id="6f59d-107">參數</span><span class="sxs-lookup"><span data-stu-id="6f59d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f59d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f59d-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="6f59d-109">設定為 IMC \_ CLOSESTATUSWINDOW。</span><span class="sxs-lookup"><span data-stu-id="6f59d-109">Set to IMC\_CLOSESTATUSWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="6f59d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f59d-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6f59d-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="6f59d-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f59d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f59d-112">Return Value</span></span>

<span data-ttu-id="6f59d-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6f59d-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f59d-114">備註</span><span class="sxs-lookup"><span data-stu-id="6f59d-114">Remarks</span></span>

<span data-ttu-id="6f59d-115">當輸入法狀態視窗已隱藏時，此命令不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="6f59d-115">When the IME status window is already hidden, this command does nothing.</span></span> <span data-ttu-id="6f59d-116">雖然應用程式可以將此命令傳送至 IME 視窗，但應用程式不會收到對應的 [IMN \_ CLOSESTATUSWINDOW](imn-closestatuswindow.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="6f59d-116">Although an application can send this command to the IME window, the application does not receive the corresponding [IMN\_CLOSESTATUSWINDOW](imn-closestatuswindow.md) command.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f59d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f59d-117">Requirements</span></span>



| <span data-ttu-id="6f59d-118">需求</span><span class="sxs-lookup"><span data-stu-id="6f59d-118">Requirement</span></span> | <span data-ttu-id="6f59d-119">值</span><span class="sxs-lookup"><span data-stu-id="6f59d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f59d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f59d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f59d-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f59d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6f59d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f59d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f59d-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f59d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f59d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6f59d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f59d-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6f59d-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f59d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f59d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f59d-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="6f59d-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6f59d-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="6f59d-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> </dl>

 

 




