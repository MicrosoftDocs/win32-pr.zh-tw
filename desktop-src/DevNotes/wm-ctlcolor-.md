---
description: 在 \_ 16 位版本的 Windows 中，會使用 WM CTLCOLOR 訊息來變更清單方塊的色彩配置、下拉式方塊的清單方塊、訊息方塊、按鈕控制項、編輯控制項、靜態控制項和對話方塊。請注意，如需此訊息和32位版本 Windows 的相關資訊，請參閱備註。
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: 'WM_CTLCOLOR 訊息 (WindowsX .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984100"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="f17e4-103">WM \_ CTLCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="f17e4-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="f17e4-104">在16位版本的 Windows 中，會使用 **WM \_ CTLCOLOR** 訊息來變更清單方塊的色彩配置、下拉式方塊的清單方塊、訊息方塊、按鈕控制項、編輯控制項、靜態控制項和對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f17e4-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="f17e4-105">如需此訊息和32位版本 Windows 的相關資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="f17e4-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="f17e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="f17e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17e4-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="f17e4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f17e4-108">目的地視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f17e4-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="f17e4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f17e4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f17e4-110"> (DC) 的顯示內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="f17e4-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="f17e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f17e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f17e4-112">子視窗的控制碼 (控制項) 。</span><span class="sxs-lookup"><span data-stu-id="f17e4-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f17e4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f17e4-113">Return value</span></span>

<span data-ttu-id="f17e4-114">如果應用程式處理此訊息，則會傳回筆刷的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f17e4-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="f17e4-115">系統會使用筆刷來繪製控制項的背景。</span><span class="sxs-lookup"><span data-stu-id="f17e4-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17e4-116">備註</span><span class="sxs-lookup"><span data-stu-id="f17e4-116">Remarks</span></span>

<span data-ttu-id="f17e4-117">來自16位 Windows 的 **WM \_ CTLCOLOR** 訊息已由更明確的通知取代。</span><span class="sxs-lookup"><span data-stu-id="f17e4-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="f17e4-118">這些取代包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="f17e4-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="f17e4-119">**WM \_ CTLCOLORBTN**</span><span class="sxs-lookup"><span data-stu-id="f17e4-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="f17e4-120">**WM \_ CTLCOLOREDIT**</span><span class="sxs-lookup"><span data-stu-id="f17e4-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="f17e4-121">**WM \_ CTLCOLORDLG**</span><span class="sxs-lookup"><span data-stu-id="f17e4-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="f17e4-122">**WM \_ CTLCOLORLISTBOX**</span><span class="sxs-lookup"><span data-stu-id="f17e4-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="f17e4-123">**WM \_ CTLCOLORSCROLLBAR**</span><span class="sxs-lookup"><span data-stu-id="f17e4-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="f17e4-124">**WM \_ CTLCOLORSTATIC**</span><span class="sxs-lookup"><span data-stu-id="f17e4-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="f17e4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f17e4-125">Requirements</span></span>



| <span data-ttu-id="f17e4-126">需求</span><span class="sxs-lookup"><span data-stu-id="f17e4-126">Requirement</span></span> | <span data-ttu-id="f17e4-127">值</span><span class="sxs-lookup"><span data-stu-id="f17e4-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f17e4-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f17e4-128">Header</span></span><br/> | <dl> <span data-ttu-id="f17e4-129"><dt>WindowsX。h</dt></span><span class="sxs-lookup"><span data-stu-id="f17e4-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 
