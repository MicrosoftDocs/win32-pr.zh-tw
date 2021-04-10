---
description: 指示 IME 視窗設定狀態視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配參數設定，如下所示。
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: 'IMC_SETSTATUSWINDOWPOS 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026293"
---
# <a name="imc_setstatuswindowpos-command"></a><span data-ttu-id="714e2-104">IMC \_ SETSTATUSWINDOWPOS 命令</span><span class="sxs-lookup"><span data-stu-id="714e2-104">IMC\_SETSTATUSWINDOWPOS command</span></span>

<span data-ttu-id="714e2-105">指示 IME 視窗設定狀態視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="714e2-105">Instructs an IME window to set the position of the status window.</span></span> <span data-ttu-id="714e2-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配參數設定，如下所示。</span><span class="sxs-lookup"><span data-stu-id="714e2-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with parameter settings as shown below.</span></span>


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a><span data-ttu-id="714e2-107">參數</span><span class="sxs-lookup"><span data-stu-id="714e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="714e2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="714e2-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="714e2-109">設定為 IMC \_ SETSTATUSWINDOWPOS。</span><span class="sxs-lookup"><span data-stu-id="714e2-109">Set to IMC\_SETSTATUSWINDOWPOS.</span></span>

</dd> <dt>

<span data-ttu-id="714e2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="714e2-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="714e2-111">[**點**](/previous-versions//dd162808(v=vs.85))結構的指標，其中包含狀態視窗位置的 x 座標和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="714e2-111">Pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x coordinate and y coordinate of the position of the status window.</span></span> <span data-ttu-id="714e2-112">座標是在螢幕座標中，相對於顯示的左上角。</span><span class="sxs-lookup"><span data-stu-id="714e2-112">The coordinates are in screen coordinates, relative to the upper left corner of the display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="714e2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="714e2-113">Return Value</span></span>

<span data-ttu-id="714e2-114">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="714e2-114">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="714e2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="714e2-115">Requirements</span></span>



| <span data-ttu-id="714e2-116">需求</span><span class="sxs-lookup"><span data-stu-id="714e2-116">Requirement</span></span> | <span data-ttu-id="714e2-117">值</span><span class="sxs-lookup"><span data-stu-id="714e2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="714e2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="714e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="714e2-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="714e2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="714e2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="714e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="714e2-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="714e2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="714e2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="714e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="714e2-123"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="714e2-123"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="714e2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="714e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="714e2-125">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="714e2-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="714e2-126">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="714e2-126">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="714e2-127">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="714e2-127">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 
