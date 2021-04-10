---
description: 指示 IME 視窗取得撰寫視窗的位置。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: 'IMC_GETCOMPOSITIONWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32b8f4414311d0727f622a1b552428cd31b0716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690848"
---
# <a name="imc_getcompositionwindow-command"></a><span data-ttu-id="77ff5-104">IMC \_ GETCOMPOSITIONWINDOW 命令</span><span class="sxs-lookup"><span data-stu-id="77ff5-104">IMC\_GETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="77ff5-105">指示 IME 視窗取得撰寫視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="77ff5-105">Instructs an IME window to get the position of the composition window.</span></span> <span data-ttu-id="77ff5-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="77ff5-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="77ff5-107">參數</span><span class="sxs-lookup"><span data-stu-id="77ff5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ff5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="77ff5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="77ff5-109">設定為 IMC \_ GETCOMPOSITIONWINDOW。</span><span class="sxs-lookup"><span data-stu-id="77ff5-109">Set to IMC\_GETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="77ff5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="77ff5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="77ff5-111">[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)結構的指標，其中包含組合視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="77ff5-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the position of the composition window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ff5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="77ff5-112">Return Value</span></span>

<span data-ttu-id="77ff5-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="77ff5-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="77ff5-114">備註</span><span class="sxs-lookup"><span data-stu-id="77ff5-114">Remarks</span></span>

<span data-ttu-id="77ff5-115">因為 IME 可能會調整組合視窗的位置，應用程式會使用這個命令來取得實際的位置，以決定是否要重新放置視窗。</span><span class="sxs-lookup"><span data-stu-id="77ff5-115">Because the IME might adjust the position of a composition window, an application uses this command to get the actual position to decide whether to reposition the window.</span></span> <span data-ttu-id="77ff5-116">抓取的位置是在視窗座標中，相對於具有目前輸入焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="77ff5-116">The retrieved position is in window coordinates relative to the window having the current input focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ff5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="77ff5-117">Requirements</span></span>



| <span data-ttu-id="77ff5-118">需求</span><span class="sxs-lookup"><span data-stu-id="77ff5-118">Requirement</span></span> | <span data-ttu-id="77ff5-119">值</span><span class="sxs-lookup"><span data-stu-id="77ff5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ff5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77ff5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77ff5-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77ff5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="77ff5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77ff5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77ff5-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77ff5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="77ff5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="77ff5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ff5-125"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="77ff5-125"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77ff5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77ff5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ff5-127">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="77ff5-127">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="77ff5-128">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="77ff5-128">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="77ff5-129">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="77ff5-129">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




