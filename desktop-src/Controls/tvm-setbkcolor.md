---
title: 'TVM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定控制項的背景色彩。 您可以使用 TreeView SetBkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843783"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="9470e-105">TVM \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="9470e-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="9470e-106">設定控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9470e-106">Sets the background color of the control.</span></span> <span data-ttu-id="9470e-107">您可以使用 [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="9470e-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9470e-108">參數</span><span class="sxs-lookup"><span data-stu-id="9470e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9470e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9470e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9470e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9470e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9470e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9470e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9470e-112">[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9470e-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="9470e-113">如果這個值是-1，控制項將會還原為使用背景色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="9470e-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9470e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9470e-114">Return value</span></span>

<span data-ttu-id="9470e-115">傳回表示先前背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="9470e-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="9470e-116">如果這個值是-1，表示控制項使用的是背景色彩的系統色彩。</span><span class="sxs-lookup"><span data-stu-id="9470e-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="9470e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9470e-117">Requirements</span></span>



| <span data-ttu-id="9470e-118">需求</span><span class="sxs-lookup"><span data-stu-id="9470e-118">Requirement</span></span> | <span data-ttu-id="9470e-119">值</span><span class="sxs-lookup"><span data-stu-id="9470e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9470e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9470e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9470e-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9470e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9470e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9470e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9470e-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9470e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9470e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9470e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9470e-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9470e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9470e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9470e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9470e-127">**TVM \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9470e-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

