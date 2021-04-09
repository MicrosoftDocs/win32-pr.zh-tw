---
title: 'LVM_REDRAWITEMS 訊息 (Commctrl .h) '
description: 強制清單視圖控制項重新繪製某個範圍的專案。 您可以明確地傳送此訊息，或使用 ListView \_ RedrawItems 宏來傳送。
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025077"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="e84f4-105">LVM \_ REDRAWITEMS 訊息</span><span class="sxs-lookup"><span data-stu-id="e84f4-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="e84f4-106">強制清單視圖控制項重新繪製某個範圍的專案。</span><span class="sxs-lookup"><span data-stu-id="e84f4-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="e84f4-107">您可以明確地傳送此訊息，或使用 [**ListView \_ RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="e84f4-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e84f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="e84f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e84f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84f4-110">要重繪之第一個專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e84f4-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="e84f4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e84f4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e84f4-112">要重繪之最後一個專案的索引。</span><span class="sxs-lookup"><span data-stu-id="e84f4-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84f4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e84f4-113">Return value</span></span>

<span data-ttu-id="e84f4-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e84f4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84f4-115">備註</span><span class="sxs-lookup"><span data-stu-id="e84f4-115">Remarks</span></span>

<span data-ttu-id="e84f4-116">在清單視圖視窗收到要重新繪製的 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息之前，不會實際重新繪製指定的專案。</span><span class="sxs-lookup"><span data-stu-id="e84f4-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="e84f4-117">若要立即重新繪製，請在使用這個宏之後呼叫 [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) 函式。</span><span class="sxs-lookup"><span data-stu-id="e84f4-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84f4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e84f4-118">Requirements</span></span>



| <span data-ttu-id="e84f4-119">需求</span><span class="sxs-lookup"><span data-stu-id="e84f4-119">Requirement</span></span> | <span data-ttu-id="e84f4-120">值</span><span class="sxs-lookup"><span data-stu-id="e84f4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e84f4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e84f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e84f4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84f4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e84f4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e84f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e84f4-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e84f4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e84f4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e84f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84f4-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e84f4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

