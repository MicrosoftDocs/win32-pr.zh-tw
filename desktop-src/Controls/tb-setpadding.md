---
title: 'TB_SETPADDING 訊息 (Commctrl .h) '
description: 設定工具列控制項的邊框距離。
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105750"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="80cdd-104">TB \_ SETPADDING 訊息</span><span class="sxs-lookup"><span data-stu-id="80cdd-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="80cdd-105">設定工具列控制項的邊框距離。</span><span class="sxs-lookup"><span data-stu-id="80cdd-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="80cdd-106">參數</span><span class="sxs-lookup"><span data-stu-id="80cdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80cdd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80cdd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80cdd-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="80cdd-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="80cdd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80cdd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80cdd-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定水準填補（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="80cdd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="80cdd-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定垂直填補（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="80cdd-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80cdd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="80cdd-112">Return value</span></span>

<span data-ttu-id="80cdd-113">傳回 **DWORD** 值，其中包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中先前的水準填補，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中先前的垂直填補（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="80cdd-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="80cdd-114">備註</span><span class="sxs-lookup"><span data-stu-id="80cdd-114">Remarks</span></span>

<span data-ttu-id="80cdd-115">填補值是用來在按鈕的邊緣與按鈕的影像和/或文字之間建立空白區域。</span><span class="sxs-lookup"><span data-stu-id="80cdd-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="80cdd-116">實際套用的填補數量，取決於按鈕的類型，以及是否有影像。</span><span class="sxs-lookup"><span data-stu-id="80cdd-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="80cdd-117">水準填補會套用至按鈕的右邊和左方，而垂直填補會套用至按鈕的頂端和底部。</span><span class="sxs-lookup"><span data-stu-id="80cdd-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="80cdd-118">填補只適用于具有 [**TBSTYLE \_ AUTOSIZE**](toolbar-control-and-button-styles.md) 樣式的按鈕。</span><span class="sxs-lookup"><span data-stu-id="80cdd-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="80cdd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="80cdd-119">Requirements</span></span>



| <span data-ttu-id="80cdd-120">需求</span><span class="sxs-lookup"><span data-stu-id="80cdd-120">Requirement</span></span> | <span data-ttu-id="80cdd-121">值</span><span class="sxs-lookup"><span data-stu-id="80cdd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80cdd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80cdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="80cdd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80cdd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80cdd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80cdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="80cdd-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80cdd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80cdd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="80cdd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="80cdd-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="80cdd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80cdd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80cdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80cdd-129">**TB \_ GETPADDING**</span><span class="sxs-lookup"><span data-stu-id="80cdd-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

