---
description: 指示 IME 視窗設定組合視窗的樣式。 若要傳送此命令，應用程式會使用「WM \_ IME」 \_ 控制項訊息搭配如下所示的參數設定。
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: 'IMC_SETCOMPOSITIONWINDOW 命令 (Imm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971254"
---
# <a name="imc_setcompositionwindow-command"></a><span data-ttu-id="55b36-104">IMC \_ SETCOMPOSITIONWINDOW 命令</span><span class="sxs-lookup"><span data-stu-id="55b36-104">IMC\_SETCOMPOSITIONWINDOW command</span></span>

<span data-ttu-id="55b36-105">指示 IME 視窗設定組合視窗的樣式。</span><span class="sxs-lookup"><span data-stu-id="55b36-105">Instructs an IME window to set the style of the composition window.</span></span> <span data-ttu-id="55b36-106">若要傳送此命令，應用程式會使用「 [**WM \_ IME」 \_ 控制項**](wm-ime-control.md) 訊息搭配如下所示的參數設定。</span><span class="sxs-lookup"><span data-stu-id="55b36-106">To send this command, the application uses the [**WM\_IME\_CONTROL**](wm-ime-control.md) message with the parameter settings shown below.</span></span>


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a><span data-ttu-id="55b36-107">參數</span><span class="sxs-lookup"><span data-stu-id="55b36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b36-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="55b36-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="55b36-109">設定為 IMC \_ SETCOMPOSITIONWINDOW。</span><span class="sxs-lookup"><span data-stu-id="55b36-109">Set to IMC\_SETCOMPOSITIONWINDOW.</span></span>

</dd> <dt>

<span data-ttu-id="55b36-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="55b36-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="55b36-111">[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)結構的指標，其中包含樣式資訊。</span><span class="sxs-lookup"><span data-stu-id="55b36-111">Pointer to a [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) structure that contains the style information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b36-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="55b36-112">Return Value</span></span>

<span data-ttu-id="55b36-113">如果成功，則傳回0，否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="55b36-113">Returns 0 if successful, or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b36-114">備註</span><span class="sxs-lookup"><span data-stu-id="55b36-114">Remarks</span></span>

<span data-ttu-id="55b36-115">此命令會在目前的輸入內容中設定樣式，並接著將樣式套用到每個接收該輸入內容的輸入法視窗。</span><span class="sxs-lookup"><span data-stu-id="55b36-115">This command sets the style in the current input context, and the style is subsequently applied to each IME window that receives that input context.</span></span>

<span data-ttu-id="55b36-116">根據預設，IME 視窗具有 CFS \_ 點樣式。</span><span class="sxs-lookup"><span data-stu-id="55b36-116">By default, the IME window has the CFS\_POINT style.</span></span> <span data-ttu-id="55b36-117">使用此樣式時，IME 視窗會在開啟任何撰寫視窗時使用目前的插入號位置和視窗工作區。</span><span class="sxs-lookup"><span data-stu-id="55b36-117">With this style, the IME window uses the current caret position and window client area when it opens any composition window.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b36-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="55b36-118">Requirements</span></span>



| <span data-ttu-id="55b36-119">需求</span><span class="sxs-lookup"><span data-stu-id="55b36-119">Requirement</span></span> | <span data-ttu-id="55b36-120">值</span><span class="sxs-lookup"><span data-stu-id="55b36-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b36-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55b36-121">Minimum supported client</span></span><br/> | <span data-ttu-id="55b36-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b36-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="55b36-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55b36-123">Minimum supported server</span></span><br/> | <span data-ttu-id="55b36-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b36-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55b36-125">標頭</span><span class="sxs-lookup"><span data-stu-id="55b36-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b36-126"><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="55b36-126"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b36-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55b36-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b36-128">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="55b36-128">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="55b36-129">輸入方法管理員命令</span><span class="sxs-lookup"><span data-stu-id="55b36-129">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="55b36-130">**COMPOSITIONFORM**</span><span class="sxs-lookup"><span data-stu-id="55b36-130">**COMPOSITIONFORM**</span></span>](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[<span data-ttu-id="55b36-131">**WM \_ IME \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="55b36-131">**WM\_IME\_CONTROL**</span></span>](wm-ime-control.md)
</dt> </dl>

 

 




